# WM-W02 Day1 — 阅读资料与代码来源

核对日期：2026-10-06。以下均为官方文档、官方源码或作者论文。
本包代码是教学实现，不是完整 COLMAP 复现；不附第三方论文全文或源码副本。

## R1. OpenCV — Epipolar Geometry（必读 15–20 分钟）
https://docs.opencv.org/4.13.0/da/de9/tutorial_py_epipolar_geometry.html

只读 **Basic Concepts**，看两台相机与投影射线的示意。今天先不运行 Code 中的 SIFT/FLANN/F 估计。
回答：一张图像中的一个点为什么只确定一条射线？另一张图像如何补充约束？极线约束为什么不等于已经找到了对应点？
F/E 的估计放在 Day2；今天只知道 F 把一幅图中的点映射为另一幅图中的极线即可。

## R2. Schönberger & Frahm — Structure-from-Motion Revisited（必读 10–15 分钟）
https://demuc.de/papers/schoenberger2016sfm.pdf

看 **PDF 第 2 页的 Figure 2**，读 **Section 2.2 中的 Triangulation 段落**。
今天只定位三角化在完整 SfM 管线中的角色。不要求读完整 Section 4 或实现 Bundle Adjustment。
选读：Section 4.3 的式 (2)–(5)，位于 PDF 第 5 页，用于理解三角化角度、正深度和重投影检查。
注意：论文局部的 R/t 参数化不一定与本包同名符号具有同义。以 world-to-camera 映射的实际定义为准，不能直接照搬符号。

## R3. OpenCV — Camera Calibration and 3D Reconstruction（实现时查阅）
https://docs.opencv.org/4.13.0/d9/d0c/group__calib3d.html

查 `triangulatePoints`。两个 P 是 3×4，两组输入点为 2×N，输出为 4×N 齐次坐标。
本包对外存点为 N×2，调用 cv2 时转置。所有输入使用 float64。
本包像素坐标与 K[R|t] 配对。归一化图像坐标与 [R|t] 配对。畸变不在今天的合成模型中。

## R4. OpenCV 4.13.0 — triangulate.cpp（选读）
https://github.com/opencv/opencv/blob/4.13.0/modules/calib3d/src/triangulate.cpp

搜 `icvTriangulatePoints`，看为每个点构造 4×4 方程矩阵、做 SVD、输出齐次点的部分。
不要把后面的 `icvCorrectMatches`（匹配校正）误当成本日的 DLT 三角化。
本日 DLT 的目标是代数残差最小，不等于直接求解非线性重投影误差最小值。

## R5. NumPy — numpy.linalg.svd（实现时查阅）
https://numpy.org/doc/2.3/reference/generated/numpy.linalg.svd.html

核对返回值 `U, s, Vh`。奇异值降序排列。对于本日的实数矩阵，Vh 就是 V 的转置。
今天需要最小奇异值对应的右奇异向量。

## 本包与资料的关系

`geometry_core.py` 是沿用 WM-W01 坐标约定的新写自包含辅助代码；它不是从用户本地 Week1 文件中导入的实现。
`solutions/geometry_reference.py` 是线性 DLT 的参考实现。
`geometry_exercise.py` 是留给用户独立完成的两个 TODO。
论文只是提供流程和质量检查的背景；本包没有实现论文的完整增量重建、鲁棒三角化或 BA。
