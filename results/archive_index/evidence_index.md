# 第二周本地证据索引

这是文件与原始字段的索引，不自动给第二周评分。没有重新执行旧实验。
路径缺失不等于实验没做；文件存在不等于几何正确。私有绝对路径公开前请检查。

| 标识 | 日次 | 用途 | 文件状态 |
|---|---|---|---|
| d1_check | Day1 | 本地代码检查 | found |
| d2_check | Day2 | 本地代码检查 | found |
| d3_check | Day3 | 本地代码检查 | found |
| d4_check | Day4 | 本地代码检查 | found |
| d5_check | Day5 | 本地代码检查 | found |
| d6_check | Day6 | 本地代码检查 | found |
| d1_sweep | Day1 | 基线/噪声对照 | found |
| d2_matches | Day2 | 真实外观筛选对照 | found |
| d2_pose | Day2 | 合成相对位姿 | found |
| d3_model | Day3 | COLMAP稀疏模型 | found |
| d4_reprojection | Day4 | 完整Track重投影 | found |
| d4_controls | Day4 | 位姿/畸变诊断 | found |
| d5_api | Day5 | 同像素实现对照 | found |
| d5_controls | Day5 | 深度尺度与截断 | found |
| d6_fuse | Day6 | 给定位姿的多帧合并 | found |
| d6_pairs | Day6 | 双向跨帧检查 | found |
| d6_controls | Day6 | 跨帧错误对照 | found |

## d1_check

文件：[check_student.json](../../results/Week2_Day1/outputs/check_student.json)

解释任务：这是全组还是局部检查？与使用的源码和实验设置是否对应？

SHA256：`ec39c22cc8adf584c90af2248644aeefbb826aea5c902f3bbc2e922d56d33209`

```json
[
  {
    "json_pointer": "/implementation",
    "value": "student"
  },
  {
    "json_pointer": "/solver_sha256",
    "value": "96333113c8e64a05de4252d644bf5aaf332f927d2a9a0d6bda3feddf423a4db6"
  },
  {
    "json_pointer": "/passed",
    "value": 14
  },
  {
    "json_pointer": "/total",
    "value": 14
  },
  {
    "json_pointer": "/scope",
    "value": "Day1 numerical checks only; not Week1 acceptance or concept mastery"
  },
  {
    "json_pointer": "/versions/python",
    "value": "3.11.17"
  },
  {
    "json_pointer": "/versions/numpy",
    "value": "2.3.5"
  },
  {
    "json_pointer": "/versions/opencv",
    "value": "4.13.0"
  }
]
```

你的解释：待填写。

## d2_check

文件：[check_student.json](../../results/Week2_Day2/outputs/check_student.json)

解释任务：这是全组还是局部检查？与使用的源码和实验设置是否对应？

SHA256：`8733b50f688d8ff0fb1c7fe58203b69faa6f246d496c38f3db4dc3fe71c23204`

```json
[
  {
    "json_pointer": "/implementation",
    "value": "student"
  },
  {
    "json_pointer": "/versions/python",
    "value": "3.11.17"
  },
  {
    "json_pointer": "/versions/platform",
    "value": "Windows-10-10.0.26200-SP0"
  },
  {
    "json_pointer": "/versions/numpy",
    "value": "2.3.5"
  },
  {
    "json_pointer": "/versions/opencv",
    "value": "4.13.0"
  },
  {
    "json_pointer": "/passed",
    "value": 18
  },
  {
    "json_pointer": "/total",
    "value": 18
  },
  {
    "json_pointer": "/exercise_passed",
    "value": 14
  },
  {
    "json_pointer": "/exercise_total",
    "value": 14
  },
  {
    "json_pointer": "/completion_status",
    "value": "numerical checks only; experiment/report required"
  }
]
```

你的解释：待填写。

## d3_check

文件：[check_all.json](../../results/Week2_Day3/outputs/check_all.json)

解释任务：这是全组还是局部检查？与使用的源码和实验设置是否对应？

SHA256：`61dac700f609af486d62b96bbda4aec6c4262770c608b57bd177ba97c3400a3d`

```json
[
  {
    "json_pointer": "/part",
    "value": "all"
  },
  {
    "json_pointer": "/tests_run",
    "value": 15
  },
  {
    "json_pointer": "/success",
    "value": true
  },
  {
    "json_pointer": "/scope",
    "value": "Unit tests of user code, not a reconstruction/geometry quality certificate."
  }
]
```

你的解释：待填写。

## d4_check

文件：[all_latest.json](../../results/Week2_Day4/outputs/checks/all_latest.json)

解释任务：这是全组还是局部检查？与使用的源码和实验设置是否对应？

SHA256：`f5febbf7220bdc310d78395e72442b8d82efd7a2f50f9c2b97ac4181a8dd2201`

```json
[
  {
    "json_pointer": "/part",
    "value": "all"
  },
  {
    "json_pointer": "/passed",
    "value": 20
  },
  {
    "json_pointer": "/total",
    "value": 20
  },
  {
    "json_pointer": "/student_source_sha256",
    "value": "09cc77e6932e92d8b7450b3159c770cdc6c6d3352792d57e948ef7b391221918"
  },
  {
    "json_pointer": "/note",
    "value": "单元检查含已提供的输入验证和3项格式检查；不能代替本地真实实验分析。"
  }
]
```

你的解释：待填写。

## d5_check

文件：[check_report.json](../../results/Week2_Day5/outputs/check_all_todo/check_report.json)

解释任务：这是全组还是局部检查？与使用的源码和实验设置是否对应？

SHA256：`d4460dcd1bfb9b0674818ef3c64b3635667030c2ba151b592ca7bcbaa52a025e`

```json
[
  {
    "json_pointer": "/part",
    "value": "all"
  },
  {
    "json_pointer": "/passed",
    "value": 20
  },
  {
    "json_pointer": "/total",
    "value": 20
  },
  {
    "json_pointer": "/real_dataset_experiment_completed",
    "value": false
  }
]
```

你的解释：待填写。

## d6_check

文件：[check_results.json](../../results/Week2_Day6/outputs/check_all/check_results.json)

解释任务：这是全组还是局部检查？与使用的源码和实验设置是否对应？

SHA256：`99a4358dde103ac0519fd58201fa470459761522fae2b71abd246b95e4e1e8bd`

```json
[
  {
    "json_pointer": "/part",
    "value": "all"
  },
  {
    "json_pointer": "/passed",
    "value": 22
  },
  {
    "json_pointer": "/total",
    "value": 22
  },
  {
    "json_pointer": "/student_file_sha256",
    "value": "00c8525cd18cad55467f4c1b6c030baf7e962206b99fadd00984568c3236aae1"
  },
  {
    "json_pointer": "/note",
    "value": "Synthetic implementation checks, not real-world reconstruction accuracy."
  }
]
```

你的解释：待填写。

## d1_sweep

文件：[summary.json](../../results/Week2_Day1/outputs/sweep_student/summary.json)

解释任务：选固定噪声条件比较基线；同时解释三维误差、重投影误差与统计聚合。

SHA256：`ef209e7abe315767ddd5782433a97934b0d6607ae30b725cc1d0ea0ad1ef6b9e`

```json
[
  {
    "json_pointer": "/aggregation",
    "value": "mean and sample SD across trial-level metrics; fixed scene; paired noise across baselines"
  },
  {
    "json_pointer": "/errors",
    "value": "3D metrics on all finite points, including negative-depth points; invalid fractions reported separately"
  },
  {
    "json_pointer": "/rows/0/baseline_m",
    "value": 0.5
  },
  {
    "json_pointer": "/rows/0/noise_px",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/0/repeats",
    "value": 1
  },
  {
    "json_pointer": "/rows/0/mean_median_3d_m",
    "value": 3.566841437502201e-15
  },
  {
    "json_pointer": "/rows/0/std_median_3d_m",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/0/mean_median_reprojection_px",
    "value": 6.355287432313019e-14
  },
  {
    "json_pointer": "/rows/0/std_median_reprojection_px",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/0/mean_rmse_3d_m",
    "value": 6.107296996197642e-15
  },
  {
    "json_pointer": "/rows/0/std_rmse_3d_m",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/0/mean_finite_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/0/std_finite_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/0/mean_positive_depth_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/0/std_positive_depth_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/0/mean_opencv_max_difference_m",
    "value": 2.2360522891433096e-14
  },
  {
    "json_pointer": "/rows/0/std_opencv_max_difference_m",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/1/baseline_m",
    "value": 0.5
  },
  {
    "json_pointer": "/rows/1/noise_px",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/1/repeats",
    "value": 10
  },
  {
    "json_pointer": "/rows/1/mean_median_3d_m",
    "value": 0.07930184971050111
  },
  {
    "json_pointer": "/rows/1/std_median_3d_m",
    "value": 0.0038565082203450723
  },
  {
    "json_pointer": "/rows/1/mean_median_reprojection_px",
    "value": 0.4854393562330199
  },
  {
    "json_pointer": "/rows/1/std_median_reprojection_px",
    "value": 0.04296791371085144
  },
  {
    "json_pointer": "/rows/1/mean_rmse_3d_m",
    "value": 0.13809944744270897
  },
  {
    "json_pointer": "/rows/1/std_rmse_3d_m",
    "value": 0.00650470350810361
  },
  {
    "json_pointer": "/rows/1/mean_finite_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/1/std_finite_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/1/mean_positive_depth_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/1/std_positive_depth_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/1/mean_opencv_max_difference_m",
    "value": 4.940658960015369e-13
  },
  {
    "json_pointer": "/rows/1/std_opencv_max_difference_m",
    "value": 7.58400435593336e-14
  },
  {
    "json_pointer": "/rows/2/baseline_m",
    "value": 0.05
  },
  {
    "json_pointer": "/rows/2/noise_px",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/2/repeats",
    "value": 1
  },
  {
    "json_pointer": "/rows/2/mean_median_3d_m",
    "value": 2.1413475271204137e-14
  },
  {
    "json_pointer": "/rows/2/std_median_3d_m",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/2/mean_median_reprojection_px",
    "value": 5.684341886080802e-14
  },
  {
    "json_pointer": "/rows/2/std_median_reprojection_px",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/2/mean_rmse_3d_m",
    "value": 5.46329499723658e-14
  },
  {
    "json_pointer": "/rows/2/std_rmse_3d_m",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/2/mean_finite_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/2/std_finite_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/2/mean_positive_depth_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/2/std_positive_depth_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/2/mean_opencv_max_difference_m",
    "value": 3.658033502462342e-13
  },
  {
    "json_pointer": "/rows/2/std_opencv_max_difference_m",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/3/baseline_m",
    "value": 0.05
  },
  {
    "json_pointer": "/rows/3/noise_px",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/3/repeats",
    "value": 10
  },
  {
    "json_pointer": "/rows/3/mean_median_3d_m",
    "value": 0.7933700397614957
  },
  {
    "json_pointer": "/rows/3/std_median_3d_m",
    "value": 0.047507515986751625
  },
  {
    "json_pointer": "/rows/3/mean_median_reprojection_px",
    "value": 0.48544408081710877
  },
  {
    "json_pointer": "/rows/3/std_median_reprojection_px",
    "value": 0.042969128968712994
  },
  {
    "json_pointer": "/rows/3/mean_rmse_3d_m",
    "value": 2.2505717249790815
  },
  {
    "json_pointer": "/rows/3/std_rmse_3d_m",
    "value": 1.210165388531968
  },
  {
    "json_pointer": "/rows/3/mean_finite_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/3/std_finite_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/3/mean_positive_depth_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/rows/3/std_positive_depth_fraction",
    "value": 0.0
  },
  {
    "json_pointer": "/rows/3/mean_opencv_max_difference_m",
    "value": 3.835972334569162e-12
  },
  {
    "json_pointer": "/rows/3/std_opencv_max_difference_m",
    "value": 7.375443006689792e-12
  }
]
```

你的解释：待填写。

## d2_matches

文件：[summary.json](../../results/Week2_Day2/outputs/real_sweep_student/summary.json)

解释任务：区分候选数、几何内点率与未知的真实匹配准确率。

SHA256：`f00717064798c69f219770bb5dd3d65b5a9e46739fb97e8d80f915f2a32c5001`

```json
[
  {
    "json_pointer": "/0/ratio",
    "value": 0.6
  },
  {
    "json_pointer": "/0/ratio_pass",
    "value": 775
  },
  {
    "json_pointer": "/0/unique_tentative",
    "value": 764
  },
  {
    "json_pointer": "/0/F_inliers",
    "value": 605
  },
  {
    "json_pointer": "/0/F_inlier_fraction",
    "value": 0.7918848167539267
  },
  {
    "json_pointer": "/0/median_sqrt_sampson_inliers_px",
    "value": 0.15220246056078202
  },
  {
    "json_pointer": "/1/ratio",
    "value": 0.75
  },
  {
    "json_pointer": "/1/ratio_pass",
    "value": 985
  },
  {
    "json_pointer": "/1/unique_tentative",
    "value": 953
  },
  {
    "json_pointer": "/1/F_inliers",
    "value": 872
  },
  {
    "json_pointer": "/1/F_inlier_fraction",
    "value": 0.9150052465897167
  },
  {
    "json_pointer": "/1/median_sqrt_sampson_inliers_px",
    "value": 0.11876842390721314
  },
  {
    "json_pointer": "/2/ratio",
    "value": 0.9
  },
  {
    "json_pointer": "/2/ratio_pass",
    "value": 1327
  },
  {
    "json_pointer": "/2/unique_tentative",
    "value": 1165
  },
  {
    "json_pointer": "/2/F_inliers",
    "value": 959
  },
  {
    "json_pointer": "/2/F_inlier_fraction",
    "value": 0.8231759656652361
  },
  {
    "json_pointer": "/2/median_sqrt_sampson_inliers_px",
    "value": 0.12320143258177665
  }
]
```

你的解释：待填写。

## d2_pose

文件：[metrics.json](../../results/Week2_Day2/outputs/pose_demo_student/metrics.json)

解释任务：哪些输入已知？平移方向是否有米尺度？错配标签只用于哪里？

SHA256：`65434a4f76280babd36354dd6d9f5ba607b49d2bf91cf16ace685aac408fc398`

```json
[
  {
    "json_pointer": "/method",
    "value": "essential_ransac"
  },
  {
    "json_pointer": "/n_matches",
    "value": 300
  },
  {
    "json_pointer": "/n_true_matches",
    "value": 210
  },
  {
    "json_pointer": "/n_model_selected",
    "value": 177
  },
  {
    "json_pointer": "/selected_precision_vs_gt",
    "value": 0.9887005649717514
  },
  {
    "json_pointer": "/selected_recall_vs_gt",
    "value": 0.8333333333333334
  },
  {
    "json_pointer": "/rotation_error_deg",
    "value": 0.39841612524012965
  },
  {
    "json_pointer": "/translation_direction_error_deg",
    "value": 0.36201089206766524
  },
  {
    "json_pointer": "/translation_norm",
    "value": 1.0
  },
  {
    "json_pointer": "/n_finite_all",
    "value": 300
  },
  {
    "json_pointer": "/n_positive_all",
    "value": 270
  },
  {
    "json_pointer": "/positive_fraction_of_model_selected",
    "value": 0.9943502824858758
  },
  {
    "json_pointer": "/n_recover_pose_retained",
    "value": 176
  },
  {
    "json_pointer": "/reprojection_px_model_selected/n",
    "value": 177
  },
  {
    "json_pointer": "/reprojection_px_model_selected/n_finite",
    "value": 177
  },
  {
    "json_pointer": "/reprojection_px_model_selected/median",
    "value": 0.28865817885863054
  },
  {
    "json_pointer": "/reprojection_px_model_selected/p90",
    "value": 0.5839415003139233
  },
  {
    "json_pointer": "/sqrt_sampson_px_model_selected/n",
    "value": 177
  },
  {
    "json_pointer": "/sqrt_sampson_px_model_selected/n_finite",
    "value": 177
  },
  {
    "json_pointer": "/sqrt_sampson_px_model_selected/median",
    "value": 0.4082222531008391
  },
  {
    "json_pointer": "/sqrt_sampson_px_model_selected/p90",
    "value": 0.8257134373090381
  },
  {
    "json_pointer": "/gt_baseline_m_used_ONLY_for_evaluation",
    "value": 0.6517092910186258
  },
  {
    "json_pointer": "/scale_aligned_3d_m_all_true_finite/n",
    "value": 210
  },
  {
    "json_pointer": "/scale_aligned_3d_m_all_true_finite/n_finite",
    "value": 210
  },
  {
    "json_pointer": "/scale_aligned_3d_m_all_true_finite/median",
    "value": 0.29128714206445433
  },
  {
    "json_pointer": "/scale_aligned_3d_m_all_true_finite/p90",
    "value": 0.47841422345265866
  },
  {
    "json_pointer": "/scale_aligned_3d_m_model_selected_true_finite/n",
    "value": 175
  },
  {
    "json_pointer": "/scale_aligned_3d_m_model_selected_true_finite/n_finite",
    "value": 175
  },
  {
    "json_pointer": "/scale_aligned_3d_m_model_selected_true_finite/median",
    "value": 0.2939449799064006
  },
  {
    "json_pointer": "/scale_aligned_3d_m_model_selected_true_finite/p90",
    "value": 0.47532154533135157
  },
  {
    "json_pointer": "/n_true_nonfinite",
    "value": 0
  },
  {
    "json_pointer": "/note",
    "value": "Raw translation and raw 3D are in unit-baseline coordinates, NOT metres. Pose-selected positive-depth fraction is not independent proof."
  }
]
```

你的解释：待填写。

## d3_model

文件：[summary.json](../../results/Week2_Day3/outputs/base4096/summary.json)

解释任务：记录实际子模型、注册分母、点数及误差聚合；不能把最多注册称为最准确。

SHA256：`f0a4e796781a3cca784211a82bcbd862d97ed59101500ec0b928f33eb723c1f4`

```json
[
  {
    "json_pointer": "/run_name",
    "value": "base4096"
  },
  {
    "json_pointer": "/n_input_images",
    "value": 128
  },
  {
    "json_pointer": "/n_models",
    "value": 1
  },
  {
    "json_pointer": "/selected_by_coverage",
    "value": "0"
  },
  {
    "json_pointer": "/union_registered_images",
    "value": 128
  },
  {
    "json_pointer": "/union_registration_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/models/0/model_id",
    "value": "0"
  },
  {
    "json_pointer": "/models/0/n_input_images",
    "value": 128
  },
  {
    "json_pointer": "/models/0/n_registered_images",
    "value": 128
  },
  {
    "json_pointer": "/models/0/registration_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/models/0/n_points3D",
    "value": 40692
  },
  {
    "json_pointer": "/models/0/mean_point_error_px",
    "value": 0.7634736755019236
  },
  {
    "json_pointer": "/models/0/median_point_error_px",
    "value": 0.6256041549626155
  },
  {
    "json_pointer": "/models/0/mean_track_length",
    "value": 5.925144991644549
  },
  {
    "json_pointer": "/models/0/n_observations",
    "value": 241106
  },
  {
    "json_pointer": "/models/0/cross_checked_counts/n_registered_images",
    "value": 128
  },
  {
    "json_pointer": "/models/0/cross_checked_counts/n_points3D",
    "value": 40692
  },
  {
    "json_pointer": "/metric_definition",
    "value": "ERROR in points3D.txt, unweighted across 3D points; not recomputed, not GT."
  },
  {
    "json_pointer": "/union_warning",
    "value": "Coverage union across disconnected models is NOT one common reconstructed world."
  },
  {
    "json_pointer": "/scale_warning",
    "value": "No metric scale or gravity alignment was supplied."
  },
  {
    "json_pointer": "/summary_source_sha256",
    "value": "775520ef64a81ef5f99eb2fe475660a88356cf5febecfca011af0076493392e2"
  },
  {
    "json_pointer": "/generated_utc",
    "value": "2026-10-06T19:27:20.859919+00:00"
  }
]
```

你的解释：待填写。

## d4_reprojection

文件：[metrics.json](../../results/Week2_Day4/outputs/reproject/metrics.json)

解释任务：这是全部关联观测还是可视化子样本？存储ERROR与重算值如何对应？

SHA256：`bda845687c6e7047a61cf4caff36088cc006b42e91bbad21422e9d803bec6766`

```json
[
  {
    "json_pointer": "/condition",
    "value": "baseline"
  },
  {
    "json_pointer": "/n_associated_observations",
    "value": 241106
  },
  {
    "json_pointer": "/n_valid",
    "value": 241106
  },
  {
    "json_pointer": "/valid_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/n_invalid",
    "value": 0
  },
  {
    "json_pointer": "/n_unassociated_keypoints",
    "value": 448131
  },
  {
    "json_pointer": "/n_valid_projected_outside_image",
    "value": 1
  },
  {
    "json_pointer": "/observation_error_px/n_finite",
    "value": 241106
  },
  {
    "json_pointer": "/observation_error_px/mean",
    "value": 0.8001413645390376
  },
  {
    "json_pointer": "/observation_error_px/median",
    "value": 0.614935827579603
  },
  {
    "json_pointer": "/observation_error_px/p95",
    "value": 2.1623764007859494
  },
  {
    "json_pointer": "/observation_error_px/max",
    "value": 3.9856550575834433
  },
  {
    "json_pointer": "/observation_error_px/rms",
    "value": 1.024330229836544
  },
  {
    "json_pointer": "/opencv_projection_difference_px/n_finite",
    "value": 241106
  },
  {
    "json_pointer": "/opencv_projection_difference_px/mean",
    "value": 3.959102341079869e-14
  },
  {
    "json_pointer": "/opencv_projection_difference_px/median",
    "value": 0.0
  },
  {
    "json_pointer": "/opencv_projection_difference_px/p95",
    "value": 2.2737367544323206e-13
  },
  {
    "json_pointer": "/opencv_projection_difference_px/max",
    "value": 9.374856803373542e-13
  },
  {
    "json_pointer": "/opencv_projection_difference_px/rms",
    "value": 1.0660968026627915e-13
  },
  {
    "json_pointer": "/note",
    "value": "原有 Track 观测的拟合一致性；不是新视角测试、真实三维误差或绝对尺度精度。"
  },
  {
    "json_pointer": "/stored_point_error_comparison/n_model_points",
    "value": 40692
  },
  {
    "json_pointer": "/stored_point_error_comparison/n_comparable_complete_tracks",
    "value": 40692
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_recomputed_error_px/n_finite",
    "value": 40692
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_recomputed_error_px/mean",
    "value": 0.7634736755019217
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_recomputed_error_px/median",
    "value": 0.6256041549624289
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_recomputed_error_px/p95",
    "value": 1.7811439719724638
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_recomputed_error_px/max",
    "value": 3.7536754629001052
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_recomputed_error_px/rms",
    "value": 0.9112397038076572
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_stored_error_px_same_points/n_finite",
    "value": 40692
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_stored_error_px_same_points/mean",
    "value": 0.7634736755019236
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_stored_error_px_same_points/median",
    "value": 0.6256041549626155
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_stored_error_px_same_points/p95",
    "value": 1.7811439719724764
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_stored_error_px_same_points/max",
    "value": 3.753675462899994
  },
  {
    "json_pointer": "/stored_point_error_comparison/point_equal_weight_stored_error_px_same_points/rms",
    "value": 0.9112397038076578
  },
  {
    "json_pointer": "/stored_point_error_comparison/absolute_difference_px/n_finite",
    "value": 40692
  },
  {
    "json_pointer": "/stored_point_error_comparison/absolute_difference_px/mean",
    "value": 1.0977910830413348e-13
  },
  {
    "json_pointer": "/stored_point_error_comparison/absolute_difference_px/median",
    "value": 7.016609515630989e-14
  },
  {
    "json_pointer": "/stored_point_error_comparison/absolute_difference_px/p95",
    "value": 3.5679514898134796e-13
  },
  {
    "json_pointer": "/stored_point_error_comparison/absolute_difference_px/max",
    "value": 2.022382261657185e-12
  },
  {
    "json_pointer": "/stored_point_error_comparison/absolute_difference_px/rms",
    "value": 1.6810962017443943e-13
  },
  {
    "json_pointer": "/stored_point_error_comparison/note",
    "value": "不能与全观测等权均值直接比较。stored ERROR 更新时机可能不同；差异不能单独判定几何真伪。"
  }
]
```

你的解释：待填写。

## d4_controls

文件：[comparison.json](../../results/Week2_Day4/outputs/controls/comparison.json)

解释任务：比较共同有效集合及有效率，区分参数诊断与物理精度。

SHA256：`35672f54580652b3d74851f1bf939911961b207f6f659aba5fd5c89029ec321d`

```json
[
  {
    "json_pointer": "/conditions/0/condition",
    "value": "baseline"
  },
  {
    "json_pointer": "/conditions/0/n_original",
    "value": 241106
  },
  {
    "json_pointer": "/conditions/0/valid_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/conditions/0/median_all_valid_px",
    "value": 0.614935827579603
  },
  {
    "json_pointer": "/conditions/0/n_common_valid",
    "value": 241106
  },
  {
    "json_pointer": "/conditions/0/baseline_median_common_px",
    "value": 0.614935827579603
  },
  {
    "json_pointer": "/conditions/0/condition_median_common_px",
    "value": 0.614935827579603
  },
  {
    "json_pointer": "/conditions/0/mean_paired_delta_px",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/1/condition",
    "value": "ignore_distortion"
  },
  {
    "json_pointer": "/conditions/1/n_original",
    "value": 241106
  },
  {
    "json_pointer": "/conditions/1/valid_fraction",
    "value": 1.0
  },
  {
    "json_pointer": "/conditions/1/median_all_valid_px",
    "value": 2.0548730400923585
  },
  {
    "json_pointer": "/conditions/1/n_common_valid",
    "value": 241106
  },
  {
    "json_pointer": "/conditions/1/baseline_median_common_px",
    "value": 0.614935827579603
  },
  {
    "json_pointer": "/conditions/1/condition_median_common_px",
    "value": 2.0548730400923585
  },
  {
    "json_pointer": "/conditions/1/mean_paired_delta_px",
    "value": 2.2948329534352507
  },
  {
    "json_pointer": "/conditions/2/condition",
    "value": "inverse_as_forward"
  },
  {
    "json_pointer": "/conditions/2/n_original",
    "value": 241106
  },
  {
    "json_pointer": "/conditions/2/valid_fraction",
    "value": 0.5245784012011314
  },
  {
    "json_pointer": "/conditions/2/median_all_valid_px",
    "value": 1385.3715030062576
  },
  {
    "json_pointer": "/conditions/2/n_common_valid",
    "value": 126479
  },
  {
    "json_pointer": "/conditions/2/baseline_median_common_px",
    "value": 0.5832358507236789
  },
  {
    "json_pointer": "/conditions/2/condition_median_common_px",
    "value": 1385.3715030062576
  },
  {
    "json_pointer": "/conditions/2/mean_paired_delta_px",
    "value": 22544385807.35284
  },
  {
    "json_pointer": "/changes/baseline",
    "value": "model as stored"
  },
  {
    "json_pointer": "/changes/ignore_distortion",
    "value": "only k set to zero during projection"
  },
  {
    "json_pointer": "/changes/inverse_as_forward",
    "value": "use entire T_camera_to_world where T_world_to_camera is needed"
  },
  {
    "json_pointer": "/fixed",
    "value": "same text model, original observations, image IDs, overlay sampling, no optimization"
  },
  {
    "json_pointer": "/interpretation",
    "value": "implementation sensitivity diagnostic; not a trained-model ablation or physical ground truth"
  }
]
```

你的解释：待填写。

## d5_api

文件：[implementation_comparison.json](../../results/Week2_Day5/outputs/compare/implementation_comparison.json)

解释任务：有效掩码是否一致？API差异是不是外部深度真值误差？

SHA256：`bbaa3aff7c92e9b9f044109dbdbc759a8ea113597220e46d756f76913a4329ed`

```json
[
  {
    "json_pointer": "/common_pixel_count",
    "value": 267129
  },
  {
    "json_pointer": "/only_a_pixel_count",
    "value": 0
  },
  {
    "json_pointer": "/only_b_pixel_count",
    "value": 0
  },
  {
    "json_pointer": "/same_pixel_xyz_difference_m/n",
    "value": 267129
  },
  {
    "json_pointer": "/same_pixel_xyz_difference_m/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_xyz_difference_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_xyz_difference_m/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_xyz_difference_m/max",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_xyz_difference_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/open3d_version",
    "value": "0.19.0"
  },
  {
    "json_pointer": "/intrinsic_readers_agree",
    "value": true
  },
  {
    "json_pointer": "/numpy_valid_count",
    "value": 267129
  },
  {
    "json_pointer": "/open3d_valid_count",
    "value": 267129
  },
  {
    "json_pointer": "/input_pixel_count",
    "value": 307200
  },
  {
    "json_pointer": "/mask_disagreement_count",
    "value": 0
  },
  {
    "json_pointer": "/depth_image_absolute_difference_m/n",
    "value": 307200
  },
  {
    "json_pointer": "/depth_image_absolute_difference_m/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/depth_image_absolute_difference_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/depth_image_absolute_difference_m/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/depth_image_absolute_difference_m/max",
    "value": 0.0
  },
  {
    "json_pointer": "/depth_image_absolute_difference_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_color_max_channel_difference/n",
    "value": 267129
  },
  {
    "json_pointer": "/same_pixel_color_max_channel_difference/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_color_max_channel_difference/median",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_color_max_channel_difference/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_color_max_channel_difference/max",
    "value": 0.0
  },
  {
    "json_pointer": "/same_pixel_color_max_channel_difference/min",
    "value": 0.0
  },
  {
    "json_pointer": "/alignment_method",
    "value": "original pixel_id=v*W+u, not nearest-neighbor registration"
  },
  {
    "json_pointer": "/ground_truth_accuracy_measured",
    "value": false
  },
  {
    "json_pointer": "/tolerances/xyz_m",
    "value": 1e-06
  },
  {
    "json_pointer": "/tolerances/depth_m",
    "value": 1e-07
  },
  {
    "json_pointer": "/tolerances/rgb",
    "value": 1e-12
  },
  {
    "json_pointer": "/notes/0",
    "value": "Depth conversion compared from raw uint16 in both branches."
  },
  {
    "json_pointer": "/notes/1",
    "value": "Both branches use identical raw RGB, raw depth, K, scale, truncation and identity extrinsic."
  },
  {
    "json_pointer": "/notes/2",
    "value": "Agreement validates implementation under these assumptions, not sensor accuracy."
  },
  {
    "json_pointer": "/numeric_agreement_checks/nonempty_common_subset",
    "value": true
  },
  {
    "json_pointer": "/numeric_agreement_checks/same_valid_pixel_set",
    "value": true
  },
  {
    "json_pointer": "/numeric_agreement_checks/depth_difference_within_tolerance",
    "value": true
  },
  {
    "json_pointer": "/numeric_agreement_checks/xyz_difference_within_tolerance",
    "value": true
  },
  {
    "json_pointer": "/numeric_agreement_checks/rgb_difference_within_tolerance",
    "value": true
  },
  {
    "json_pointer": "/numeric_agreement",
    "value": true
  }
]
```

你的解释：待填写。

## d5_controls

文件：[comparison.json](../../results/Week2_Day5/outputs/controls/comparison.json)

解释任务：哪些量改变，哪些像素仍然可比？同相机回投能否验单位？

SHA256：`252680fb37261e3377c4d3d97454323c8393f91a3b82b7a492e4172880d36f57`

```json
[
  {
    "json_pointer": "/conditions/baseline/full_valid_population/frame_index",
    "value": 0
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/raw_dtype",
    "value": "uint16"
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/input_pixel_count",
    "value": 307200
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/valid_pixel_count",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/valid_fraction",
    "value": 0.869560546875
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/depth_scale",
    "value": 1000.0
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/depth_trunc_m",
    "value": 3.0
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/axial_depth_m/n",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/axial_depth_m/mean",
    "value": 1.793887336424306
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/axial_depth_m/median",
    "value": 1.8609999418258667
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/axial_depth_m/p95",
    "value": 2.578000068664551
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/axial_depth_m/max",
    "value": 2.7019999027252197
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/axial_depth_m/min",
    "value": 0.9549999833106995
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/ray_distance_m/n",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/ray_distance_m/mean",
    "value": 1.9305308025683485
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/ray_distance_m/median",
    "value": 1.956610577345635
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/ray_distance_m/p95",
    "value": 2.7729524432945483
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/ray_distance_m/max",
    "value": 3.2463657011940725
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/ray_distance_m/min",
    "value": 1.0510457482637963
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/cycle_consistency_px/n",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/cycle_consistency_px/mean",
    "value": 3.293124605587575e-16
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/cycle_consistency_px/median",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/cycle_consistency_px/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/cycle_consistency_px/max",
    "value": 6.572520305780927e-14
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/cycle_consistency_px/min",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/extent_xyz_m/0",
    "value": 2.409436142331078
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/extent_xyz_m/1",
    "value": 1.5965809102285475
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/extent_xyz_m/2",
    "value": 1.7469999194145203
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/coordinate_frame",
    "value": "camera_00000"
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/global_pose_estimated",
    "value": false
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/geometric_ground_truth_available",
    "value": false
  },
  {
    "json_pointer": "/conditions/baseline/full_valid_population/interpretation",
    "value": "Units follow configured depth_scale; no independent metric calibration. Cycle consistency is not a depth-accuracy measurement."
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/common_pixel_count",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/only_a_pixel_count",
    "value": 0
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/only_b_pixel_count",
    "value": 0
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/same_pixel_xyz_difference_m/n",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/same_pixel_xyz_difference_m/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/same_pixel_xyz_difference_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/same_pixel_xyz_difference_m/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/same_pixel_xyz_difference_m/max",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/pairwise_baseline_comparison/same_pixel_xyz_difference_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/all_conditions_common_pixel_count",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/baseline/common_axial_depth_m/n",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/baseline/common_axial_depth_m/mean",
    "value": 1.2443223111333679
  },
  {
    "json_pointer": "/conditions/baseline/common_axial_depth_m/median",
    "value": 1.253999948501587
  },
  {
    "json_pointer": "/conditions/baseline/common_axial_depth_m/p95",
    "value": 1.440999984741211
  },
  {
    "json_pointer": "/conditions/baseline/common_axial_depth_m/max",
    "value": 1.49399995803833
  },
  {
    "json_pointer": "/conditions/baseline/common_axial_depth_m/min",
    "value": 0.9549999833106995
  },
  {
    "json_pointer": "/conditions/baseline/common_xyz_delta_from_baseline_m/n",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/baseline/common_xyz_delta_from_baseline_m/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_xyz_delta_from_baseline_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_xyz_delta_from_baseline_m/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_xyz_delta_from_baseline_m/max",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_xyz_delta_from_baseline_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_cycle_consistency_px/n",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/baseline/common_cycle_consistency_px/mean",
    "value": 2.720239513750241e-16
  },
  {
    "json_pointer": "/conditions/baseline/common_cycle_consistency_px/median",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_cycle_consistency_px/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/common_cycle_consistency_px/max",
    "value": 5.904883742358415e-14
  },
  {
    "json_pointer": "/conditions/baseline/common_cycle_consistency_px/min",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/frame_index",
    "value": 0
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/raw_dtype",
    "value": "uint16"
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/input_pixel_count",
    "value": 307200
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/valid_pixel_count",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/valid_fraction",
    "value": 0.2735188802083333
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/depth_scale",
    "value": 500.0
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/depth_trunc_m",
    "value": 3.0
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/axial_depth_m/n",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/axial_depth_m/mean",
    "value": 2.4886446222667358
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/axial_depth_m/median",
    "value": 2.507999897003174
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/axial_depth_m/p95",
    "value": 2.881999969482422
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/axial_depth_m/max",
    "value": 2.98799991607666
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/axial_depth_m/min",
    "value": 1.909999966621399
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/ray_distance_m/n",
    "value": 84025
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/ray_distance_m/mean",
    "value": 2.7371715159281065
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/ray_distance_m/median",
    "value": 2.7251517321111725
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/ray_distance_m/p95",
    "value": 3.175636019073273
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/ray_distance_m/max",
    "value": 3.549960937294248
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/ray_distance_m/min",
    "value": 2.1020914965275925
  },
  {
    "json_pointer": "/conditions/scale_500/full_valid_population/cycle_consistency_px/n",
    "value": 84025
  }
]
```

你的解释：待填写。

## d6_fuse

文件：[metrics.json](../../results/Week2_Day6/outputs/fuse/metrics.json)

解释任务：位姿从哪里来？拼点、体素降采样、TSDF是否同一操作？

SHA256：`eb9083266a259dfe41308f1724385ddc1b5a8b2243f55f49e99d518d4d0b83d4`

```json
[
  {
    "json_pointer": "/counts/unpooled_point_count",
    "value": 1340711
  },
  {
    "json_pointer": "/counts/voxel_point_count",
    "value": 28218
  },
  {
    "json_pointer": "/counts/voxel_size_m",
    "value": 0.02
  },
  {
    "json_pointer": "/counts/note",
    "value": "Voxel downsampling is a derived representation; raw frame/pixel identities are not retained in its vertices."
  },
  {
    "json_pointer": "/per_frame/0/frame_id",
    "value": 0
  },
  {
    "json_pointer": "/per_frame/0/point_count",
    "value": 267129
  },
  {
    "json_pointer": "/per_frame/0/world_transform_difference_vs_Open3D_m/n",
    "value": 267129
  },
  {
    "json_pointer": "/per_frame/0/world_transform_difference_vs_Open3D_m/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/0/world_transform_difference_vs_Open3D_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/0/world_transform_difference_vs_Open3D_m/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/0/world_transform_difference_vs_Open3D_m/max",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/0/world_transform_difference_vs_Open3D_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/0/inverse_matrix_difference_vs_LOG_API_max_abs",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/0/own_camera_roundtrip_xyz_m/n",
    "value": 267129
  },
  {
    "json_pointer": "/per_frame/0/own_camera_roundtrip_xyz_m/mean",
    "value": 1.3037330064102853e-16
  },
  {
    "json_pointer": "/per_frame/0/own_camera_roundtrip_xyz_m/median",
    "value": 1.2412670766236366e-16
  },
  {
    "json_pointer": "/per_frame/0/own_camera_roundtrip_xyz_m/p95",
    "value": 2.482534153247273e-16
  },
  {
    "json_pointer": "/per_frame/0/own_camera_roundtrip_xyz_m/max",
    "value": 3.1401849173675503e-16
  },
  {
    "json_pointer": "/per_frame/0/own_camera_roundtrip_xyz_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/1/frame_id",
    "value": 1
  },
  {
    "json_pointer": "/per_frame/1/point_count",
    "value": 267728
  },
  {
    "json_pointer": "/per_frame/1/world_transform_difference_vs_Open3D_m/n",
    "value": 267728
  },
  {
    "json_pointer": "/per_frame/1/world_transform_difference_vs_Open3D_m/mean",
    "value": 8.20495260767974e-17
  },
  {
    "json_pointer": "/per_frame/1/world_transform_difference_vs_Open3D_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/1/world_transform_difference_vs_Open3D_m/p95",
    "value": 4.440892098500626e-16
  },
  {
    "json_pointer": "/per_frame/1/world_transform_difference_vs_Open3D_m/max",
    "value": 6.661338147750939e-16
  },
  {
    "json_pointer": "/per_frame/1/world_transform_difference_vs_Open3D_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/1/inverse_matrix_difference_vs_LOG_API_max_abs",
    "value": 1.8559498566883548e-06
  },
  {
    "json_pointer": "/per_frame/1/own_camera_roundtrip_xyz_m/n",
    "value": 267728
  },
  {
    "json_pointer": "/per_frame/1/own_camera_roundtrip_xyz_m/mean",
    "value": 1.6199003117810674e-06
  },
  {
    "json_pointer": "/per_frame/1/own_camera_roundtrip_xyz_m/median",
    "value": 1.652851694261703e-06
  },
  {
    "json_pointer": "/per_frame/1/own_camera_roundtrip_xyz_m/p95",
    "value": 2.2766103932252843e-06
  },
  {
    "json_pointer": "/per_frame/1/own_camera_roundtrip_xyz_m/max",
    "value": 2.6017485254467766e-06
  },
  {
    "json_pointer": "/per_frame/1/own_camera_roundtrip_xyz_m/min",
    "value": 9.535605578127265e-07
  },
  {
    "json_pointer": "/per_frame/2/frame_id",
    "value": 2
  },
  {
    "json_pointer": "/per_frame/2/point_count",
    "value": 268183
  },
  {
    "json_pointer": "/per_frame/2/world_transform_difference_vs_Open3D_m/n",
    "value": 268183
  },
  {
    "json_pointer": "/per_frame/2/world_transform_difference_vs_Open3D_m/mean",
    "value": 9.490078428388947e-17
  },
  {
    "json_pointer": "/per_frame/2/world_transform_difference_vs_Open3D_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/2/world_transform_difference_vs_Open3D_m/p95",
    "value": 4.440892098500626e-16
  },
  {
    "json_pointer": "/per_frame/2/world_transform_difference_vs_Open3D_m/max",
    "value": 6.661338147750939e-16
  },
  {
    "json_pointer": "/per_frame/2/world_transform_difference_vs_Open3D_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/2/inverse_matrix_difference_vs_LOG_API_max_abs",
    "value": 2.0175688955070825e-06
  },
  {
    "json_pointer": "/per_frame/2/own_camera_roundtrip_xyz_m/n",
    "value": 268183
  },
  {
    "json_pointer": "/per_frame/2/own_camera_roundtrip_xyz_m/mean",
    "value": 6.573711714465906e-07
  },
  {
    "json_pointer": "/per_frame/2/own_camera_roundtrip_xyz_m/median",
    "value": 6.266072959416152e-07
  },
  {
    "json_pointer": "/per_frame/2/own_camera_roundtrip_xyz_m/p95",
    "value": 1.1811613207825872e-06
  },
  {
    "json_pointer": "/per_frame/2/own_camera_roundtrip_xyz_m/max",
    "value": 1.6911711923845567e-06
  },
  {
    "json_pointer": "/per_frame/2/own_camera_roundtrip_xyz_m/min",
    "value": 9.000505665821254e-08
  },
  {
    "json_pointer": "/per_frame/3/frame_id",
    "value": 3
  },
  {
    "json_pointer": "/per_frame/3/point_count",
    "value": 268620
  },
  {
    "json_pointer": "/per_frame/3/world_transform_difference_vs_Open3D_m/n",
    "value": 268620
  },
  {
    "json_pointer": "/per_frame/3/world_transform_difference_vs_Open3D_m/mean",
    "value": 8.167422166951699e-17
  },
  {
    "json_pointer": "/per_frame/3/world_transform_difference_vs_Open3D_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/3/world_transform_difference_vs_Open3D_m/p95",
    "value": 4.440892098500626e-16
  },
  {
    "json_pointer": "/per_frame/3/world_transform_difference_vs_Open3D_m/max",
    "value": 6.661338147750939e-16
  },
  {
    "json_pointer": "/per_frame/3/world_transform_difference_vs_Open3D_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/3/inverse_matrix_difference_vs_LOG_API_max_abs",
    "value": 3.470471899191807e-06
  },
  {
    "json_pointer": "/per_frame/3/own_camera_roundtrip_xyz_m/n",
    "value": 268620
  },
  {
    "json_pointer": "/per_frame/3/own_camera_roundtrip_xyz_m/mean",
    "value": 2.1456498417255855e-06
  },
  {
    "json_pointer": "/per_frame/3/own_camera_roundtrip_xyz_m/median",
    "value": 2.102662321169538e-06
  },
  {
    "json_pointer": "/per_frame/3/own_camera_roundtrip_xyz_m/p95",
    "value": 3.3727629457536474e-06
  },
  {
    "json_pointer": "/per_frame/3/own_camera_roundtrip_xyz_m/max",
    "value": 4.018469266994773e-06
  },
  {
    "json_pointer": "/per_frame/3/own_camera_roundtrip_xyz_m/min",
    "value": 1.2311485461408047e-06
  },
  {
    "json_pointer": "/per_frame/4/frame_id",
    "value": 4
  },
  {
    "json_pointer": "/per_frame/4/point_count",
    "value": 269051
  },
  {
    "json_pointer": "/per_frame/4/world_transform_difference_vs_Open3D_m/n",
    "value": 269051
  },
  {
    "json_pointer": "/per_frame/4/world_transform_difference_vs_Open3D_m/mean",
    "value": 8.469463623518939e-17
  },
  {
    "json_pointer": "/per_frame/4/world_transform_difference_vs_Open3D_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/4/world_transform_difference_vs_Open3D_m/p95",
    "value": 4.440892098500626e-16
  },
  {
    "json_pointer": "/per_frame/4/world_transform_difference_vs_Open3D_m/max",
    "value": 7.691850745534255e-16
  },
  {
    "json_pointer": "/per_frame/4/world_transform_difference_vs_Open3D_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/per_frame/4/inverse_matrix_difference_vs_LOG_API_max_abs",
    "value": 1.6885879432493311e-06
  },
  {
    "json_pointer": "/per_frame/4/own_camera_roundtrip_xyz_m/n",
    "value": 269051
  },
  {
    "json_pointer": "/per_frame/4/own_camera_roundtrip_xyz_m/mean",
    "value": 2.202071065203301e-06
  },
  {
    "json_pointer": "/per_frame/4/own_camera_roundtrip_xyz_m/median",
    "value": 2.2206264264919435e-06
  },
  {
    "json_pointer": "/per_frame/4/own_camera_roundtrip_xyz_m/p95",
    "value": 3.147112180419951e-06
  },
  {
    "json_pointer": "/per_frame/4/own_camera_roundtrip_xyz_m/max",
    "value": 3.525298781055933e-06
  },
  {
    "json_pointer": "/per_frame/4/own_camera_roundtrip_xyz_m/min",
    "value": 1.2850355519608802e-06
  },
  {
    "json_pointer": "/camera_centers/0/frame_id",
    "value": 0
  }
]
```

你的解释：待填写。

## d6_pairs

文件：[pair_summary.json](../../results/Week2_Day6/outputs/pair_check/pair_summary.json)

解释任务：同时给出重叠覆盖率与深度残差，注明遮挡和对应假设。

SHA256：`bf1bd6a81f98df7ce09873fcf53e4b970fc08c5b8489aefc238e1189019da219`

```json
[
  {
    "json_pointer": "/pairs/0/source_point_count",
    "value": 269051
  },
  {
    "json_pointer": "/pairs/0/positive_target_depth_count",
    "value": 269051
  },
  {
    "json_pointer": "/pairs/0/nonpositive_or_nonfinite_target_count",
    "value": 0
  },
  {
    "json_pointer": "/pairs/0/projected_inside_count_before_zbuffer",
    "value": 269051
  },
  {
    "json_pointer": "/pairs/0/zbuffer_visible_target_pixel_count",
    "value": 244209
  },
  {
    "json_pointer": "/pairs/0/projection_collisions_removed",
    "value": 24842
  },
  {
    "json_pointer": "/pairs/0/valid_target_depth_pixel_count",
    "value": 267129
  },
  {
    "json_pointer": "/pairs/0/overlap_pixel_count",
    "value": 238345
  },
  {
    "json_pointer": "/pairs/0/valid_target_coverage_fraction",
    "value": 0.892246817080886
  },
  {
    "json_pointer": "/pairs/0/signed_depth_residual_m/n",
    "value": 238345
  },
  {
    "json_pointer": "/pairs/0/signed_depth_residual_m/mean",
    "value": -0.001353752646114931
  },
  {
    "json_pointer": "/pairs/0/signed_depth_residual_m/median",
    "value": 0.0005890393187766296
  },
  {
    "json_pointer": "/pairs/0/signed_depth_residual_m/p95",
    "value": 0.01525860536491971
  },
  {
    "json_pointer": "/pairs/0/signed_depth_residual_m/max",
    "value": 1.2763583927221003
  },
  {
    "json_pointer": "/pairs/0/signed_depth_residual_m/min",
    "value": -1.2904211523277291
  },
  {
    "json_pointer": "/pairs/0/absolute_depth_residual_m/n",
    "value": 238345
  },
  {
    "json_pointer": "/pairs/0/absolute_depth_residual_m/mean",
    "value": 0.012044772424900513
  },
  {
    "json_pointer": "/pairs/0/absolute_depth_residual_m/median",
    "value": 0.005479463665533535
  },
  {
    "json_pointer": "/pairs/0/absolute_depth_residual_m/p95",
    "value": 0.02095816929915343
  },
  {
    "json_pointer": "/pairs/0/absolute_depth_residual_m/max",
    "value": 1.2904211523277291
  },
  {
    "json_pointer": "/pairs/0/absolute_depth_residual_m/min",
    "value": 5.309621853299973e-09
  },
  {
    "json_pointer": "/pairs/0/threshold_m",
    "value": 0.03
  },
  {
    "json_pointer": "/pairs/0/within_threshold_count",
    "value": 233186
  },
  {
    "json_pointer": "/pairs/0/predicted_behind_observation_count",
    "value": 1934
  },
  {
    "json_pointer": "/pairs/0/predicted_in_front_of_observation_count",
    "value": 3225
  },
  {
    "json_pointer": "/pairs/0/residual_threshold_used_to_remove_points",
    "value": false
  },
  {
    "json_pointer": "/pairs/0/interpretation",
    "value": "Projective depth agreement on overlap, not true correspondence or GT 3D accuracy. Discretization, occlusion, edges, depth and pose errors can all contribute."
  },
  {
    "json_pointer": "/pairs/0/source_frame",
    "value": 4
  },
  {
    "json_pointer": "/pairs/0/target_frame",
    "value": 0
  },
  {
    "json_pointer": "/pairs/1/source_point_count",
    "value": 267129
  },
  {
    "json_pointer": "/pairs/1/positive_target_depth_count",
    "value": 267129
  },
  {
    "json_pointer": "/pairs/1/nonpositive_or_nonfinite_target_count",
    "value": 0
  },
  {
    "json_pointer": "/pairs/1/projected_inside_count_before_zbuffer",
    "value": 262922
  },
  {
    "json_pointer": "/pairs/1/zbuffer_visible_target_pixel_count",
    "value": 249295
  },
  {
    "json_pointer": "/pairs/1/projection_collisions_removed",
    "value": 13627
  },
  {
    "json_pointer": "/pairs/1/valid_target_depth_pixel_count",
    "value": 269051
  },
  {
    "json_pointer": "/pairs/1/overlap_pixel_count",
    "value": 238623
  },
  {
    "json_pointer": "/pairs/1/valid_target_coverage_fraction",
    "value": 0.8869061999397884
  },
  {
    "json_pointer": "/pairs/1/signed_depth_residual_m/n",
    "value": 238623
  },
  {
    "json_pointer": "/pairs/1/signed_depth_residual_m/mean",
    "value": -0.001827726078577297
  },
  {
    "json_pointer": "/pairs/1/signed_depth_residual_m/median",
    "value": -0.0011815534179850928
  },
  {
    "json_pointer": "/pairs/1/signed_depth_residual_m/p95",
    "value": 0.014543023783101402
  },
  {
    "json_pointer": "/pairs/1/signed_depth_residual_m/max",
    "value": 1.2640171292980233
  },
  {
    "json_pointer": "/pairs/1/signed_depth_residual_m/min",
    "value": -1.2540329154281002
  },
  {
    "json_pointer": "/pairs/1/absolute_depth_residual_m/n",
    "value": 238623
  },
  {
    "json_pointer": "/pairs/1/absolute_depth_residual_m/mean",
    "value": 0.011786130833629479
  },
  {
    "json_pointer": "/pairs/1/absolute_depth_residual_m/median",
    "value": 0.005364699192572875
  },
  {
    "json_pointer": "/pairs/1/absolute_depth_residual_m/p95",
    "value": 0.02007842859985207
  },
  {
    "json_pointer": "/pairs/1/absolute_depth_residual_m/max",
    "value": 1.2640171292980233
  },
  {
    "json_pointer": "/pairs/1/absolute_depth_residual_m/min",
    "value": 3.5696333444690254e-08
  },
  {
    "json_pointer": "/pairs/1/threshold_m",
    "value": 0.03
  },
  {
    "json_pointer": "/pairs/1/within_threshold_count",
    "value": 233968
  },
  {
    "json_pointer": "/pairs/1/predicted_behind_observation_count",
    "value": 2095
  },
  {
    "json_pointer": "/pairs/1/predicted_in_front_of_observation_count",
    "value": 2560
  },
  {
    "json_pointer": "/pairs/1/residual_threshold_used_to_remove_points",
    "value": false
  },
  {
    "json_pointer": "/pairs/1/interpretation",
    "value": "Projective depth agreement on overlap, not true correspondence or GT 3D accuracy. Discretization, occlusion, edges, depth and pose errors can all contribute."
  },
  {
    "json_pointer": "/pairs/1/source_frame",
    "value": 0
  },
  {
    "json_pointer": "/pairs/1/target_frame",
    "value": 4
  },
  {
    "json_pointer": "/pose_estimation_performed",
    "value": false
  }
]
```

你的解释：待填写。

## d6_controls

文件：[comparison.json](../../results/Week2_Day6/outputs/controls/comparison.json)

解释任务：写一例实际观察、被固定的变量、公共集合以及结论的限制。

SHA256：`6e2299ca1e27540d8361ae0b89a48007158708937558509b5a1b998579499a36`

```json
[
  {
    "json_pointer": "/conditions/baseline/condition",
    "value": "baseline"
  },
  {
    "json_pointer": "/conditions/baseline/description",
    "value": "No intervention."
  },
  {
    "json_pointer": "/conditions/baseline/counts/unpooled_point_count",
    "value": 1340711
  },
  {
    "json_pointer": "/conditions/baseline/counts/voxel_point_count",
    "value": 28218
  },
  {
    "json_pointer": "/conditions/baseline/counts/voxel_size_m",
    "value": 0.02
  },
  {
    "json_pointer": "/conditions/baseline/counts/note",
    "value": "Voxel downsampling is a derived representation; raw frame/pixel identities are not retained in its vertices."
  },
  {
    "json_pointer": "/conditions/baseline/source_input_pixel_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/baseline/same_source_pixel_set_as_baseline",
    "value": true
  },
  {
    "json_pointer": "/conditions/baseline/same_source_world_delta_vs_baseline_m/n",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/baseline/same_source_world_delta_vs_baseline_m/mean",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/same_source_world_delta_vs_baseline_m/median",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/same_source_world_delta_vs_baseline_m/p95",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/same_source_world_delta_vs_baseline_m/max",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/same_source_world_delta_vs_baseline_m/min",
    "value": 0.0
  },
  {
    "json_pointer": "/conditions/baseline/delta_is_GT_error",
    "value": false
  },
  {
    "json_pointer": "/conditions/baseline/pair/source_point_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/baseline/pair/positive_target_depth_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/baseline/pair/nonpositive_or_nonfinite_target_count",
    "value": 0
  },
  {
    "json_pointer": "/conditions/baseline/pair/projected_inside_count_before_zbuffer",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/baseline/pair/zbuffer_visible_target_pixel_count",
    "value": 244209
  },
  {
    "json_pointer": "/conditions/baseline/pair/projection_collisions_removed",
    "value": 24842
  },
  {
    "json_pointer": "/conditions/baseline/pair/valid_target_depth_pixel_count",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/baseline/pair/overlap_pixel_count",
    "value": 238345
  },
  {
    "json_pointer": "/conditions/baseline/pair/valid_target_coverage_fraction",
    "value": 0.892246817080886
  },
  {
    "json_pointer": "/conditions/baseline/pair/signed_depth_residual_m/n",
    "value": 238345
  },
  {
    "json_pointer": "/conditions/baseline/pair/signed_depth_residual_m/mean",
    "value": -0.001353752646114931
  },
  {
    "json_pointer": "/conditions/baseline/pair/signed_depth_residual_m/median",
    "value": 0.0005890393187766296
  },
  {
    "json_pointer": "/conditions/baseline/pair/signed_depth_residual_m/p95",
    "value": 0.01525860536491971
  },
  {
    "json_pointer": "/conditions/baseline/pair/signed_depth_residual_m/max",
    "value": 1.2763583927221003
  },
  {
    "json_pointer": "/conditions/baseline/pair/signed_depth_residual_m/min",
    "value": -1.2904211523277291
  },
  {
    "json_pointer": "/conditions/baseline/pair/absolute_depth_residual_m/n",
    "value": 238345
  },
  {
    "json_pointer": "/conditions/baseline/pair/absolute_depth_residual_m/mean",
    "value": 0.012044772424900513
  },
  {
    "json_pointer": "/conditions/baseline/pair/absolute_depth_residual_m/median",
    "value": 0.005479463665533535
  },
  {
    "json_pointer": "/conditions/baseline/pair/absolute_depth_residual_m/p95",
    "value": 0.02095816929915343
  },
  {
    "json_pointer": "/conditions/baseline/pair/absolute_depth_residual_m/max",
    "value": 1.2904211523277291
  },
  {
    "json_pointer": "/conditions/baseline/pair/absolute_depth_residual_m/min",
    "value": 5.309621853299973e-09
  },
  {
    "json_pointer": "/conditions/baseline/pair/threshold_m",
    "value": 0.03
  },
  {
    "json_pointer": "/conditions/baseline/pair/within_threshold_count",
    "value": 233186
  },
  {
    "json_pointer": "/conditions/baseline/pair/predicted_behind_observation_count",
    "value": 1934
  },
  {
    "json_pointer": "/conditions/baseline/pair/predicted_in_front_of_observation_count",
    "value": 3225
  },
  {
    "json_pointer": "/conditions/baseline/pair/residual_threshold_used_to_remove_points",
    "value": false
  },
  {
    "json_pointer": "/conditions/baseline/pair/interpretation",
    "value": "Projective depth agreement on overlap, not true correspondence or GT 3D accuracy. Discretization, occlusion, edges, depth and pose errors can all contribute."
  },
  {
    "json_pointer": "/conditions/baseline/target_depth_unchanged",
    "value": true
  },
  {
    "json_pointer": "/conditions/baseline/reoptimization",
    "value": false
  },
  {
    "json_pointer": "/conditions/baseline/point_statistics_before_downsampling",
    "value": true
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/condition",
    "value": "ignore_relative_pose"
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/description",
    "value": "All camera clouds use the target camera pose; relative motions are ignored."
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/counts/unpooled_point_count",
    "value": 1340711
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/counts/voxel_point_count",
    "value": 37900
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/counts/voxel_size_m",
    "value": 0.02
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/counts/note",
    "value": "Voxel downsampling is a derived representation; raw frame/pixel identities are not retained in its vertices."
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/source_input_pixel_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_pixel_set_as_baseline",
    "value": true
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_world_delta_vs_baseline_m/n",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_world_delta_vs_baseline_m/mean",
    "value": 0.04503724319151547
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_world_delta_vs_baseline_m/median",
    "value": 0.0440525421131097
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_world_delta_vs_baseline_m/p95",
    "value": 0.059684102890784005
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_world_delta_vs_baseline_m/max",
    "value": 0.09545754924291244
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/same_source_world_delta_vs_baseline_m/min",
    "value": 0.032841497371152224
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/delta_is_GT_error",
    "value": false
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/source_point_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/positive_target_depth_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/nonpositive_or_nonfinite_target_count",
    "value": 0
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/projected_inside_count_before_zbuffer",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/zbuffer_visible_target_pixel_count",
    "value": 269051
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/projection_collisions_removed",
    "value": 0
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/valid_target_depth_pixel_count",
    "value": 267129
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/overlap_pixel_count",
    "value": 267048
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/valid_target_coverage_fraction",
    "value": 0.999696775715104
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/signed_depth_residual_m/n",
    "value": 267048
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/signed_depth_residual_m/mean",
    "value": 0.009753378951554172
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/signed_depth_residual_m/median",
    "value": 0.01399993896484375
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/signed_depth_residual_m/p95",
    "value": 0.14300012588500977
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/signed_depth_residual_m/max",
    "value": 1.2670000791549683
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/signed_depth_residual_m/min",
    "value": -1.3579999208450317
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/absolute_depth_residual_m/n",
    "value": 267048
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/absolute_depth_residual_m/mean",
    "value": 0.11620112779966771
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/absolute_depth_residual_m/median",
    "value": 0.039999961853027344
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/absolute_depth_residual_m/p95",
    "value": 0.7256499767303408
  },
  {
    "json_pointer": "/conditions/ignore_relative_pose/pair/absolute_depth_residual_m/max",
    "value": 1.3579999208450317
  }
]
```

你的解释：待填写。
