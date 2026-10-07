# WM-W02 Day7：阅读资料与来源

核对日期：2026-10-07。今天以回顾和接口衔接为主，不新增模型安装。
本包未附论文全文、图片数据、完成版 TODO 或预跑结果。

## R1 — COLMAP 模型与坐标约定（复习）

- 固定到你前几天使用的 4.2.1 格式说明：
  https://raw.githubusercontent.com/colmap/colmap/4.2.1/doc/format.rst
- 可读网页（可能随新版变化，版本差异以固定来源为准）：
  https://colmap.github.io/format.html
- 只复习 `images.txt` 和 `points3D.txt`：wxyz、world-to-camera、相机中心、ID 与 index、Track 和存储 ERROR。
- 今天不重新执行 COLMAP，也不将 South Building 的任意 SfM 世界与 Redwood 的给定轨迹世界拼接。

## R2 — RGB-D 与给定位姿（复习）

- Open3D 0.19.0 反投影公式：
  https://www.open3d.org/docs/0.19.0/python_api/open3d.geometry.PointCloud.html
- RGB-D 基本条件：
  https://www.open3d.org/docs/0.19.0/tutorial/geometry/rgbd_image.html
- 配套轨迹与融合教程：
  https://www.open3d.org/docs/0.19.0/tutorial/pipelines/rgbd_integration.html
- LOG loader 的矩阵求逆：
  https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/io/file_format/FileLOG.cpp
- 阅读目标：区分原始 LOG 的 camera-to-world、API 返回的 extrinsic、camera Z 深度、点到相机的距离。
- 教程中的显示轴翻转不是输入点云的全局坐标定义。不要借显示操作改变保存的几何。

## R3 — NeRF 项目页（新阅读，只建立接口直觉）

https://www.matthewtancik.com/nerf

只读 **Abstract & Method**。回答：输入图像和相机怎样变成射线？网络查询位置和方向后输出什么？像素颜色怎样由采样得到？

本日不要求通读论文、不下载训练集、不运行仓库。完整 NeRF 学习放在 WM-W03。

## R4 — 原作者 NeRF 源码（选读，不能直接照搬坐标）

- `run_nerf_helpers.py` 中 `get_rays` / `get_rays_np`：
  https://github.com/bmild/nerf/blob/master/run_nerf_helpers.py
  https://raw.githubusercontent.com/bmild/nerf/master/run_nerf_helpers.py
- `run_nerf.py` 中 `raw2outputs` 的方向范数处理：
  https://github.com/bmild/nerf/blob/master/run_nerf.py
  https://raw.githubusercontent.com/bmild/nerf/master/run_nerf.py

上述 master 链接为核对时的阅读来源，不是本日安装依赖或固定训练环境。
该实现的相机局部射线包含 Y、Z 负号，且 `get_rays_np` 不把射线方向归一化。
它在体渲染中用方向范数换算采样间距。这些是该仓库的选择，不代表所有 NeRF 工程都相同。
本日保留右/下/前相机约定，输出单位世界方向，并显式记录轴向深度到射线距离的比例。

## R5 — 独立数值检查

https://docs.opencv.org/4.13.0/d9/d0c/group__calib3d.html

检查脚本使用 `Rodrigues` 构造测试旋转，使用 `projectPoints` 独立生成无畸变像素观测。
输入真值在测试器中使用，不作为未知量泄露给待测函数。只是教学数值测试，不是外部三维测量。

## 归属与边界

公式说明、24 项检查设计、证据索引和三个诊断条件是本包的教学安排。
它们不是某篇论文的评测结论。依赖官方 API 的一致性也不是物理精度证书。
