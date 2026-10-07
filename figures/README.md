# 精选实验图

所有图直接取自本地实际运行或已有报告截图，没有重新绘制实验值。逐图原路径和 SHA-256 见 [source_manifest](../results/source_manifest.json)。

| 文件 | 含义 |
|---|---|
| [day1_baseline_3d.png](day1_baseline_3d.png) | 基线 / 像素噪声与三维误差 |
| [day1_baseline_reprojection.png](day1_baseline_reprojection.png) | 同组条件的重投影误差 |
| [day2_matches_inliers.png](day2_matches_inliers.png) | 真实图像 F 内点可视化 |
| [day3_sfm_4096.png](day3_sfm_4096.png)、[day3_sfm_2048.png](day3_sfm_2048.png) | 两个 COLMAP 运行的已有截图 |
| [day4_camera_layout.png](day4_camera_layout.png) | 读取模型后的相机布局 |
| [day4_reprojection_histogram.png](day4_reprojection_histogram.png)、[day4_overlay_1.png](day4_overlay_1.png) | 全 Track 误差分布与代表图像叠加 |
| [day5_rgbd_cloud.png](day5_rgbd_cloud.png)、[day5_api_difference.png](day5_api_difference.png) | 相机点云与同像素 API 差异 |
| [day6_fused_rgb.png](day6_fused_rgb.png) | 五帧给定位姿融合点云 |
| [day6_depth_residual.png](day6_depth_residual.png) | 4→0 重叠深度残差直方图 |
| [day6_control_residual.png](day6_control_residual.png) | 历史 target_coverage 图：展示各诊断条件的目标覆盖率 |
| [day6_tsdf_preview.png](day6_tsdf_preview.png) | 已有 TSDF 可视化截图 |
| [day7_ray_range.png](day7_ray_range.png)、[day7_controls.png](day7_controls.png) | Z 与 range 的关系及错误射线诊断 |

覆盖率图不代表残差统计。Day6 五条件的共同目标集合为空，原 common_target_residual 图未选取；专题笔记使用各条件与基准的成对公共集合。
