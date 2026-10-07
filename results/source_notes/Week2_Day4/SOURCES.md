# Day4 阅读与源码

本日查证日期：2026-10-07。以 Day3 选择的 COLMAP 4.2.1 模型约定为主；在线文档可能显示开发版。无需升级本机 COLMAP。
本日不要求下载论文或通读仓库。先读 S1 的三个文件，再按 TODO 查 S2–S4；S5/S6 用于解释统计。

## S1 — COLMAP Output Format（必读）

https://colmap.github.io/format.html

固定版本文档源码：https://github.com/colmap/colmap/blob/4.2.1/doc/format.rst

阅读：Indices and Identifiers；cameras.txt；images.txt；points3D.txt。
关注：Hamilton qvec 的 wxyz 顺序；world-to-camera；C=-Rᵀt；相机 x右/y下/z前；非连续 ID；POINT2D_IDX 从0开始；POINT3D_ID=-1 没有三维关联。
新版本可能有 rigs/frames。images.txt 中的位姿是图像的 world-to-camera，不能再额外乘一次 rig 位姿。本包保留这些文件，只在本日投影计算中使用已导出的图像位姿。

## S2 — COLMAP Camera Models / Projection（必读）

https://colmap.github.io/cameras.html

阅读 SIMPLE_RADIAL 参数与三阶段投影：除深度 → 归一化坐标上的径向畸变 → 内参。
本日不学习鱼眼模型。遇到非 SIMPLE_RADIAL 模型，inventory/poses 可以读取；重投影主动报错，不能偷偷当成针孔相机。

## S3 — COLMAP 4.2.1 camera model 源码（查阅）

https://github.com/colmap/colmap/blob/4.2.1/src/colmap/sensor/models.h

搜索 SimpleRadialCameraModel::InitializeParamsInfo、ImgFromCam、Distortion。
源码定义了 f,cx,cy,k 顺序和像素约定：左上角为(0,0)，左上像素中心为(0.5,0.5)。本包观察值和预测值处于同一坐标系；不对其中一方单独加减0.5。绘图通过 extent=(0,W,H,0) 对齐显示。

## S4 — OpenCV projectPoints 与 Rodrigues（查阅）

https://docs.opencv.org/4.x/d9/d0c/group__calib3d.html

阅读 projectPoints、Rodrigues。
本地检查用 Rodrigues 验证轴角构造的旋转，用 projectPoints 验证投影。
SIMPLE_RADIAL 在此映射为 fx=fy=f；OpenCV 畸变参数为[k,0,0,0,0]。
调用 API 的数值对照不提供真实标定，也不证明输入的世界模型正确。

## S5 — COLMAP 重投影 ERROR 的计算（选读，统计时查）

https://github.com/colmap/colmap/blob/4.2.1/src/colmap/scene/reconstruction.cc

搜索 UpdatePoint3DErrors 和 ComputeMeanReprojectionError。
前者对一个三维点的 Track 取欧氏像素误差的算术平均；后者对有效 stored point ERROR 取点等权平均。
这与将所有观测混在一起取平均一般不是同一个数。

## S6 — Stored ERROR 的更新时间（与 S1 同源）

Output Format 的 points3D.txt 段落指出 ERROR 只在 global bundle adjustment 后更新。
因此本日逐点重算并报告差异，不设一个盲目的实际数据误差阈值要求二者完全相等。

## 本包范围与材料状态

所有实验都使用你本地的 Day3 数据。本包不内置重建模型、预跑图表、参考指标或完成版 TODO。
单元检查中的小型格式夹具在你执行检查时临时创建，只用于检查解析约定，不是预跑真实实验。
仅做静态源码语法与压缩包结构检查；尚未在你的 Windows 环境执行，也未运行单元检查或实验。
