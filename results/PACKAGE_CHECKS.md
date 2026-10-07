# 整理与代码检查记录

2026-10-07 在精简前的完整副本源码上执行七天检查，沿用本机 `wm_geometry` 环境。原始 `D:\WM_Study` 文件夹没有修改；历史真实实验没有重跑。

| 日次 | 结果 | 本次重新检查证据 |
|---|---:|---|
| Day1 | 14/14 | [JSON](package_validation/Day1_check.json) · [Log](package_validation/Day1_check.log) |
| Day2 | 18/18 | [JSON](package_validation/Day2_check.json) · [Log](package_validation/Day2_check.log) |
| Day3 | 15/15 | [JSON](package_validation/Day3_check.json) · [Log](package_validation/Day3_check.log) |
| Day4 | 20/20 | [JSON](package_validation/Day4_check.json) · [Log](package_validation/Day4_check.log) |
| Day5 | 20/20 | [JSON](package_validation/Day5_check.json) · [Log](package_validation/Day5_check.log) |
| Day6 | 22/22 | [JSON](package_validation/Day6_check.json) · [Log](package_validation/Day6_check.log) |
| Day7 | 24/24 | [JSON](package_validation/Day7_check.json) · [Log](package_validation/Day7_check.log) |

总计 **133/133 通过**，每日实际 Python 源码及 Day1/2 参考模块共 **50 个文件通过语法解析**。Day3 使用 unittest，记录为 `success=true, tests_run=15`；其他日期记录通过数与总数。

Day4–6 初次运行的临时目录操作受到系统沙箱限制，出现 WinError 5；对相同源码在沙箱外重新执行后，20/20、20/20、22/22 全部通过。上述 JSON 和日志是最终通过的运行，没有修改几何实现以绕过检查。

此检查是在精简前的完整源码副本上执行的历史记录；精简版保留最终 JSON 与日志，不附验证工具或完整源码。


修正后的历史证据采集为 17/17 found，见 [归档索引](archive_index/evidence_index.md)。它确认所选文件与声明可读取，不替代代码运行，也不认证物理真值精度。

合成检查通过不等于重新完成 South Building 重建、Redwood 全流程或新视角评测。原实验数字仍来自历史记录，来源详见 [SOURCE_INDEX](../SOURCE_INDEX.md)。
