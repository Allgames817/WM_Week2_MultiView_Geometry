# Day3 阅读与代码来源

查阅日期：2026-10-07。只使用 COLMAP 官方文档、官方源码和原论文。
网页文档目前显示 4.3.0.dev0，官方已发布版本中本日选用 4.2.1。
本地执行以安装版本各子命令 `-h` 的输出为准；脚本会保存这些帮助信息。

## 必读

### [PAPER] Structure-from-Motion Revisited — Schönberger & Frahm, CVPR 2016

https://demuc.de/papers/schoenberger2016sfm.pdf

先看 PDF 第 2 页 Figure 2；读 Section 2.2 的 Initialization、Image Registration、Triangulation、Bundle Adjustment。
BA 段落延续到第 3 页左栏。今天掌握输入、优化变量和重投影目标，不要求推导稀疏求解器。
论文描述的是当年的系统；今天安装的版本已经演进，不能把源码逐项等同于 2016 实现。

### [TUTORIAL] COLMAP Tutorial

https://colmap.github.io/tutorial.html

读 Feature Detection and Extraction、Feature Matching and Geometric Verification、Sparse Reconstruction、Importing and Exporting。
跳过 Dense Reconstruction。认识 Exhaustive Matching 与 Incremental Mapper 的职责。

### [CLI] Command-line Interface

https://colmap.github.io/cli.html

查 feature_extractor、exhaustive_matcher、mapper、model_converter、model_analyzer。
不直接复制网页的 Linux `$` 提示符、`mkdir -p` 或反斜杠续行到 PowerShell。
本包用 Python 的参数列表调用 COLMAP，避免续行和路径引号混淆。

### [FORMAT] Output Format

https://colmap.github.io/format.html

今天只需理解 cameras/images/points3D 的分工、ID 不连续、TRACK、ERROR。
保留 rigs/frames 文件。明天再详细处理四元数、相机中心、畸变模型和重投影。

## 安装与数据

### [INSTALL] 官方 Windows 安装说明

https://colmap.github.io/install.html

### [RELEASE] 本日选择的版本：4.2.1

https://github.com/colmap/colmap/releases/tag/4.2.1

Windows + NVIDIA 显卡主线：
https://github.com/colmap/colmap/releases/download/4.2.1/colmap-x64-windows-cuda.zip

官方资源页公布此包 SHA-256：
`e9c5cbd84c2ea986d2e970a2473fc2d2e6b34a2cdcf5d3df2765c319a63af881`

无 CUDA 包（仅在 GPU/驱动路线不适用时考虑）：
https://github.com/colmap/colmap/releases/download/4.2.1/colmap-x64-windows-nocuda.zip

官方资源页：
https://github.com/colmap/colmap/releases/expanded_assets/4.2.1

完整解压后保留 bin/、plugins/ 和 COLMAP.bat，不单独移动 exe，不下载来源不明的 DLL。
本日不安装 CUDA Toolkit、不编译源码；预编译程序的 GPU 是否可用以本机实际执行为准。

### [DATA] South Building

描述：https://colmap.github.io/datasets.html
下载入口：https://demuc.de/colmap/datasets/

点 South Building 下载 ZIP。官方说明为同一相机拍摄的 128 张图，由 Christopher Zach 提供。
同一物理相机不自动证明所有图像内参严格相同，因此本包默认不强制 single_camera。
本包不重新分发数据；使用数据时保留下载页及原包中相关许可/说明。

## 按需查阅与源码走读

### [CAMERA] Camera Models
https://colmap.github.io/cameras.html

### [DB] Database Format
https://colmap.github.io/database.html

认识 images 表的条目数和已注册图像数的差别，以及 cameras 与 images 的 1:N 关系。

### [BATCH] 官方 Windows 启动器，4.2.1
https://github.com/colmap/colmap/blob/4.2.1/scripts/shell/colmap.bat

本包运行器通过设置进程内 bin/plugins 路径并直接调用 exe，避免 shell 解析问题。
仅复制启动思路；未打包第三方源码。

### [OPTIONS] 参数登记，4.2.1
https://github.com/colmap/colmap/blob/4.2.1/src/colmap/controllers/option_manager.cc

搜索 AddFeatureExtractionOptions、AddFeatureMatchingOptions。

### [TYPES] 特征/匹配器类型枚举，4.2.1
https://github.com/colmap/colmap/blob/4.2.1/src/colmap/feature/types.h

今天固定 SIFT / SIFT_BRUTEFORCE，不启用学习型匹配器或下载模型权重。

### [ANALYZER] 模型分析与格式转换，4.2.1
https://github.com/colmap/colmap/blob/4.2.1/src/colmap/exe/model.cc

搜索 RunModelAnalyzer。核对 Registered images、Points、Mean track length 等指标来自哪里。
