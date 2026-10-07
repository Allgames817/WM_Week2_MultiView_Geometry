# 原始数据与只读约定

## 数据来源

沿用 Day5 的 Open3D SampleRedwoodRGBDImages。
官方路径、固定版本 descriptor 与 MD5 见 [SOURCES.md](SOURCES.md) 的 D1。
本包不重分发样例图像、现成点云或第三方论文全文。

Day5 的 prepare_data.py 保留了五对原始图像、camera_primesense.json 和可用的 odometry.log 等元数据。
Day6 对同一份输入重新计算 SHA256，并与 Day5 manifest 比较。
本日只使用 odometry.log 作为给定 camera-to-world 轨迹；不会替换为 trajectory.log、COLMAP 位姿或自己猜的 pose。

## 已有 Day5 数据缺少轨迹时

先确认 configs/day6.json 的 day5_root / data_root 没有指错目录。
如确实缺失，使用 Day5 留下的同一份原始 ZIP，在你本机准备一个**新目录**。
例如 Day5 使用过 --download 时，默认缓存为 data/_downloads/SampleRedwoodRGBDImages.zip：

```powershell
cd D:\WM_W02_Day5
python prepare_data.py --archive data/_downloads/SampleRedwoodRGBDImages.zip --out data/SampleRedwoodRGBDImages_day6
```

如用浏览器下载的 ZIP，则把 --archive 换成它的实际路径。
然后在 Day6 的 configs/day6.json 中将 data_root 设为：

```text
../WM_W02_Day5/data/SampleRedwoodRGBDImages_day6
```

这个恢复步骤由你显式运行 Day5 的原始数据准备脚本，不覆盖旧目录。
不建议简单删除 manifest 或手填哈希绕过验证。

## 轨迹来源不是验收结论

样例轨迹用于今天的给定位姿实验。没有外部设备真值验证，也没有在本日重新估计位姿。
Camera-to-world 的方向由固定版本官方教程与 LOG loader 源码确定，不靠哪个方向“看起来更好”来选择。
相机/深度的实际误差、动态物体、遮挡和离散投影会影响跨帧残差。
