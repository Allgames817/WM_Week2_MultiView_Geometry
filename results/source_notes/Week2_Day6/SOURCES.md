# WM-W02 Day6 — 阅读资料与来源

核对日期：2026-10-07。沿用 Day5 的 Open3D 0.19.0 接口，不声称它是最新版本。
本包没有第三方论文全文、原始图像副本、现成点云或预跑结果。

## R1（必读）：RGBD integration

https://www.open3d.org/docs/0.19.0/tutorial/pipelines/rgbd_integration.html

今天先读 `Read trajectory from .log file`。
随后对照 `TSDF volume integration` 中读取 `odometry_log_path` 和传入 `np.linalg.inv(camera_poses[i].pose)` 的位置。
暂时不要求推导 TSDF；最后一部分作为选读。

需要回答：原始 `.log` 矩阵把哪个坐标系映射到哪个坐标系？为什么 API 调用前要取逆？
这是本包采用 `odometry.log` 作为 camera-to-world 输入的直接来源。
注意：本包不会照抄教程中的深度阈值或 PrimeSenseDefault 常数；深度配置沿用 Day5，K 读取原始内参 JSON。

## R2（必读）：Transformation — General transformation

https://www.open3d.org/docs/0.19.0/tutorial/geometry/transformation.html#general-transformation

阅读 4×4 齐次变换的使用方式。留意 `transform` 修改几何对象本身。
本包的 NumPy TODO 要求不修改输入；Open3D 对照会新建点云后再调用 `transform`。

## R3（必查）：原始 LOG 与 Open3D `extrinsic` 的差别

固定版本源码：
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/io/file_format/FileLOG.cpp

定位 `ReadPinholeCameraTrajectoryFromLOG`。
这里读入原矩阵 `trans` 后，把它的逆放入 `param.extrinsic_`。
因此：**手写解析得到的原矩阵**与**Open3D trajectory.parameters[i].extrinsic**方向相反。
不要把已经求逆的 `.extrinsic` 再当成原始 camera-to-world。

本包 `fusion_io.parse_log_text` 只解析原始矩阵，不求逆。
`fuse` 模式在你运行时，才把你的 `invert_se3` 与 Open3D 的 LOG 加载结果比较。

## R4（必读短节）：Point cloud — Voxel downsampling

https://www.open3d.org/docs/0.19.0/tutorial/geometry/pointcloud.html#voxel-downsampling

了解按体素聚合点的作用。下采样改变表示的密度和点位置，不等于纠正位姿。
本包保留原始逐帧点及其 frame_id、pixel_id，再另外保存体素化显示结果。

## R5（选读）：ScalableTSDFVolume

https://www.open3d.org/docs/0.19.0/python_api/open3d.pipelines.integration.ScalableTSDFVolume.html

查 `voxel_length`、`sdf_trunc`、`integrate`、`extract_triangle_mesh`。
区分深度输入的 `depth_trunc` 与体素 SDF 的 `sdf_trunc`。
TSDF 维护体积中的截断符号距离信息，不是把多帧点列表拼接起来。

## R6（查阅）：RGBDImage 与点云创建

https://www.open3d.org/docs/0.19.0/python_api/open3d.geometry.RGBDImage.html
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/geometry/PointCloudFactory.cpp

本包选做 TSDF 使用已经由你 Day5 函数转换成米的 float32 深度构造 RGBDImage，不再次除以 1000。
点云工厂源码内部对 extrinsic 求逆，可辅助确认外参方向。

## D1：本日沿用的原始样例

官方 descriptor：
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/data/dataset/SampleRedwoodRGBDImages.cpp

官方原始归档：
https://github.com/isl-org/open3d_downloads/releases/download/20220301-data/SampleRedwoodRGBDImages.zip

官方 descriptor 中的 MD5：`43971c5f690c9cfc52dda8c96a0140ee`。
索引 0..4 的五对原始图像、相机内参、odometry.log 来自同一份归档。
本包读取 Day5 创建的 SHA256 清单并重新核对文件。不会重新下载数据或调用预制点云。

## 本包自行设计、不是官方 benchmark 的部分

三项 TODO、22 项检查、干预条件、最近目标像素 + 前向 Z-buffer 的深度检查、公共目标像素统计、报告模板均为教学设计。
跨帧残差没有真实对应点标签，不等同于论文 benchmark 或物理精度评估。
没有执行位姿估计、ICP、SLAM、BA、神经网络训练或外部真值对齐。
