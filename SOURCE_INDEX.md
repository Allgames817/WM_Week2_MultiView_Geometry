# 来源与证据索引

整理输入为 `D:\WM_Study\Week2_Day1`–`Week2_Day7`。编号笔记根据已有报告、实际源码和结果重写；表格数字优先核对原始 JSON / CSV，没有从参考输出补写个人实验。

| 专题 | 核心证据 |
|---|---|
| Day1 | [代码检查](results/Week2_Day1/outputs/check_student.json)、[基线/噪声汇总](results/Week2_Day1/outputs/sweep_student/summary.json)、[运行配置](results/Week2_Day1/outputs/sweep_student/run_config.json) |
| Day2 | [代码检查](results/Week2_Day2/outputs/check_student.json)、[匹配扫参](results/Week2_Day2/outputs/real_sweep_student/summary.json)、[合成位姿](results/Week2_Day2/outputs/pose_demo_student/metrics.json) |
| Day3 | [base4096 摘要](results/Week2_Day3/outputs/base4096/summary.json)、[features2048 摘要](results/Week2_Day3/outputs/features2048/summary.json)、[比较表](results/Week2_Day3/outputs/comparison.csv) |
| Day4 | [全 Track 重投影](results/Week2_Day4/outputs/reproject/metrics.json)、[错误对照](results/Week2_Day4/outputs/controls/comparison.json)、[相机中心](results/Week2_Day4/outputs/poses/camera_centers.csv) |
| Day5 | [同像素 API 对照](results/Week2_Day5/outputs/compare/implementation_comparison.json)、[深度参数对照](results/Week2_Day5/outputs/controls/comparison.json)、[像素追踪样本](results/Week2_Day5/outputs/compare/pixel_trace_sample.csv) |
| Day6 | [融合](results/Week2_Day6/outputs/fuse/metrics.json)、[双向深度检查](results/Week2_Day6/outputs/pair_check/pair_summary.json)、[错误对照](results/Week2_Day6/outputs/controls/comparison.json)、[TSDF](results/Week2_Day6/outputs/tsdf/tsdf_summary.json) |
| Day7 | [射线指标](results/Week2_Day7/outputs/rays/metrics.json)、[相机契约](results/Week2_Day7/outputs/rays/camera_contract.json)、[诊断对照](results/Week2_Day7/outputs/controls/comparison.json)、[射线数组](results/Week2_Day7/outputs/rays/ray_interface.npz) |

[source_manifest.json](results/source_manifest.json) 记录本精简版保留的历史原文件、整理后路径及 SHA-256。完整运行源码、配置和工具没有收录；正文提及的 Python 文件名用于解释本地实现职责。历史 JSON / CSV / 日志中的本地路径和源码哈希仍保留原值。

原始资料出处与数据声明保留于 `results/source_notes/`，见 [SOURCES](SOURCES.md)。

修正后读取归档的结果为 **17/17 found**，见 [新索引](results/archive_index/evidence_index.md)。该索引没有重新执行旧实验。旧 Day7 归档中 12 found、2 not_found、3 metadata_missing 的记录仍保留，用于追溯原配置状态。

七天代码重新检查结果与整理校验见 [PACKAGE_CHECKS](results/PACKAGE_CHECKS.md)。历史源码哈希只记录文件身份，不认证实验准确性。原结果内部的绝对路径和时间戳是历史记录，不是移动后直接运行所需的配置。

本精简版未附完整运行脚本、源码快照、配置、工具、原始图片、下载 ZIP、数据库、完整模型、大型点云及教学指南。最初整理的历史排除清单见 [excluded_files.json](results/excluded_files.json)。
