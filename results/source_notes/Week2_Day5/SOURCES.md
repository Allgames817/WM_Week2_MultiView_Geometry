# Day5 阅读资料、官方下载与实现依据

核对日期：2026-10-07。代码接口固定使用 Open3D **0.19.0**，不声称这是最新版本。
网页的 `latest` / `release` 链接会变化；本包优先使用版本化文档与 tag。

## 必读 R1：RGBD images — Redwood dataset

https://www.open3d.org/docs/0.19.0/tutorial/geometry/rgbd_image.html#redwood-dataset

读 Redwood 小节即可。今天不用通读 SUN、NYU、TUM。
重点：RGB 与 Depth 已注册到同一相机/同一分辨率；原始深度为 16-bit、毫米；RGBD 对象中的深度已变为米。
注意教程的 `pcd.transform(...)` 用于显示，不是反投影公式的步骤。

## 必读 R2：RGBDImage.create_from_color_and_depth

https://www.open3d.org/docs/0.19.0/python_api/open3d.geometry.RGBDImage.html#open3d.geometry.RGBDImage.create_from_color_and_depth

读 `depth_scale`、`depth_trunc`、`convert_rgb_to_intensity`。
本包明确设 `convert_rgb_to_intensity=False`，保留输入 RGB。

精确截断边界的实现依据：
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/geometry/Image.cpp

找 `Image::ConvertDepthToFloatImage`：先除以 float32 scale，`depth >= depth_trunc` 置零。
API 摘要只写 “larger than”，本包按照 v0.19.0 源码及本地边界检查定义行为。
对于教学中额外出现的负值和非有限值，本包也明确置零；真实样例是非负 uint16。

## 必读 R3：PointCloud.create_from_rgbd_image

https://www.open3d.org/docs/0.19.0/python_api/open3d.geometry.PointCloud.html#open3d.geometry.PointCloud.create_from_rgbd_image

看轴向深度反投影、内参、extrinsic 与 `project_valid_depth_only`。
`RGBDImage` 已经包含转换后的米制深度；进入 `create_from_rgbd_image` 后不要再除一次 1000。

源码核对：
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/geometry/PointCloudFactory.cpp

找 `CreatePointCloudFromRGBDImageT`：逐行逐列、整数像素坐标、从 RGB 取色、反向外参。
本日显式传 identity extrinsic，输出当前相机坐标；组织形式比较使用 `project_valid_depth_only=False` 保留像素身份。

## 查阅 R4：样例文件清单与内参

https://www.open3d.org/docs/0.19.0/python_api/open3d.data.SampleRedwoodRGBDImages.html

https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/data/dataset/SampleRedwoodRGBDImages.cpp

样例提供索引 0..4 的五对 RGB-D、`camera_primesense.json` 和其他元数据。
本日从 JSON 读取内参，不把教程的 PrimeSenseDefault 常数当作自己测得的精确标定。

内参序列化依据：
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/camera/PinholeCameraIntrinsic.cpp
https://raw.githubusercontent.com/isl-org/Open3D/v0.19.0/cpp/open3d/utility/IJsonConvertible.cpp

JSON 中的 9 个元素按 Eigen 的列主序存储。本包独立读取，再与 Open3D 读取同一文件的结果对照。

## 数据下载（官方原始归档）

https://github.com/isl-org/open3d_downloads/releases/download/20220301-data/SampleRedwoodRGBDImages.zip

官方 v0.19.0 descriptor 给出的 MD5：`43971c5f690c9cfc52dda8c96a0140ee`。
脚本校验此 MD5，然后为本地输入逐文件记录 SHA256。
本包没有重分发图片，原始数据在用户本机获取。
官方 ZIP 可能含现成 `example_tsdf_pcd.ply`；准备脚本不会将它提取为实验数据或成果。

## 环境与版本

https://www.open3d.org/docs/0.19.0/getting_started.html
https://github.com/isl-org/Open3D/releases/tag/v0.19.0

v0.19.0 release 说明增加 NumPy 2 支持。使用已有 Windows / Python 3.11 的 `wm_geometry`，不安装 WSL、不要求 CUDA Toolkit。
官方 `open3d-cpu` 小包不是本包给 Windows 的安装方式；这里安装 `open3d==0.19.0`。
不引入 PyTorch/JAX/TensorFlow 训练步骤。

## 本包没有做出的断言

没有证明样例内参达到某个物理精度；没有测量 RGB/Depth 标定误差；没有把原始深度当作无噪声的世界真值。
Open3D 与 NumPy 对照共享数据及标定前提，不是两种独立传感器的交叉验证。
没有执行用户 TODO、单元检查、点云实验或任何学习曲线/预跑结果生成。
