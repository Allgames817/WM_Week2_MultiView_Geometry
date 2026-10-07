# Day2 阅读与代码来源

核对日期：2026-10-06。以下均为官方文档或原始项目；课程实验脚本是教学实现，不是官方完整项目复现。

## [MATCH] OpenCV Feature Matching — 必读，约 15–20 分钟

https://docs.opencv.org/4.13.0/dc/dc3/tutorial_py_matcher.html

读 `What is this Matcher Object?`、`Brute-Force Matching with SIFT Descriptors and Ratio Test`。
重点：`queryIdx`/`trainIdx`、`distance`、`knnMatch(k=2)`、严格 ratio test。
本包用 SIFT + L2 + BFMatcher，不使用 FLANN，暂不读 ORB 和 FLANN 细节。

## [EPI] OpenCV Epipolar Geometry — 必读，约 15–20 分钟

https://docs.opencv.org/4.13.0/da/de9/tutorial_py_epipolar_geometry.html

复习 Basic Concepts，再看 F 的估计和极线绘制。
本包与教程示例不同：保留亚像素 float64，不把关键点先转为 int32；显式用 FM_RANSAC，不用教程片段里的 FM_LMEDS。
不要原样复制示例并声称运行了同一套 RANSAC 实验。

## [CALIB] OpenCV Camera Calibration and 3D Reconstruction — 按函数查阅

https://docs.opencv.org/4.13.0/d9/d0c/group__calib3d.html

查 `findFundamentalMat`、`findEssentialMat`、`recoverPose`、`sampsonDistance`、`triangulatePoints`。
注意 F 的像素坐标、E 的归一化坐标、recoverPose 的单位长度 t、输入/输出 mask 和 distanceThresh。
本包明确传 `distanceThresh=1e6`，单位是“基线规范化为 1 的坐标”，不是米。
`recoverPose` 返回的 mask 会进一步筛选输入 mask，所以保存两份，不能覆盖后忘掉原始 E-RANSAC 数量。

## [COLMAP] COLMAP Tutorial — 选读，5–10 分钟

https://colmap.github.io/tutorial.html

只读 `Feature Matching and Geometric Verification`，建立今天和 Day3 的联系。不要求今天安装。

## [DATA] scikit-image stereo_motorcycle — 数据与来源

https://scikit-image.org/docs/0.26.x/api/skimage.data.html#skimage.data.stereo_motorcycle
https://scikit-image.org/docs/0.26.x/auto_examples/transform/plot_fundamental_matrix.html

两张图像来自本运行环境 scikit-image 0.26.0 已内置的样例；已复制原始 PNG 字节，没有重新截图或从网络缩略图取样。
该样例源于 Middlebury 2014，经四倍降采样；官方文档说明两图已作立体校正。其公开标定/视差存在，但本包真实分支不使用。
原始采集作者包括 Nera Nesic、Porter Westling、Xi Wang、York Kitajima、Greg Krathwohl、Daniel Scharstein。

原始来源：https://vision.middlebury.edu/stereo/data/scenes2014/

`data/manifest.json` 记录文件 SHA-256；`data/SCIKIT_IMAGE_LICENSE.txt` 保留上游发行包许可和来源说明。
图像并非本课程原创，不把这些样例重新声称为本课程独占授权的数据。
本包不依赖 scikit-image，使用 OpenCV 读取内置 PNG。
