---
name: find-rental-in-japan
description: 搜索、筛选和核验日本租房房源。用于按预算、通勤、户型及特殊条件找房，或复核收藏房源；支持按区域并行收集、按具体房源核验与独立复核，并输出带来源的统一比较结果。
---

# 日本租房搜索与核验

本领域统一处理日本租房搜索、筛选、逐房源核验及结果归并；只有本文件是技能入口，具体能力与知识材料使用普通 reference 文档组织。

主agent只负责条件、优先级、验证方法、编排、进度沟通与升级决策。收集agent按网站或区域并行，先做共通条件的站内筛选和列表补筛；独立merge resolver去重、协调事实冲突、归并排序及维护统一文档；各房源agent并行负责一套或少量房源的完整核验，并自行创建独立复核agent，修正后再交付。

完整文档地图见 [contents.md](contents.md)。按下列任务进入相关 reference，不默认读取全部文档或附录。

## 常见任务导航

| 当前任务 | 读取文件 |
|---|---|
| 接收请求、整理条件、安排优先级与验证方法、编排及处理升级 | [main-agent.md](references/main-agent.md) |
| 负责一个站点或区域的房源收集 | [collect-area.md](references/collect-area.md) |
| 跨区域去重、协调事实冲突、归并排序及维护统一文档 | [merge-resolver.md](references/merge-resolver.md) |
| 负责一套或少量房源的完整核验，并创建独立复核agent | [verify-property.md](references/verify-property.md) |
| 受房源agent委派，独立复核证据、身份与条件判定 | [review-property.md](references/review-property.md) |
| 为特殊条件制定方法，或执行专项核验 | [verify-special.md](references/verify-special.md) |
| 用户要求光纤、高速LAN或特定网络质量 | [internet.md](references/internet.md) |
| 准备任务交接或提交结果 | [contracts.md](references/contracts.md) |
| 查看整体依赖与并行关系 | [workflow.md](references/workflow.md) |

未指定角色时承担主agent职责。只加载当前角色和条件需要的reference；子agent沿对应普通文档读取，不将每个角色注册为新技能。

## 按需附录

- 需要选择或补充房源网站、判断来源覆盖时 → [房源网站参考](references/appendix/housing-sites.md)，由收集流程按需调用。
- 用户有光纤或住宅网络要求、需要理解接入方式及技术证据时 → 先读 [住宅网络核验](references/internet.md)，再按问题读取 [光纤参考](references/appendix/fiber-reference.md)。
- 特殊要求适合从提供商覆盖楼栋反查在租房源时 → [提供商反查](references/appendix/provider-reverse-lookup.md)。这是补充入口，反查候选仍须共通初筛、去重和逐户核验。

## 共用原则

- 以当前用户条件为准。预算、面积、房间大小、网络方案、礼金、通勤偏好和例外均由本次任务确定。
- 共通条件先用网站筛选器，再补查列表字段；随后由merge resolver去重归并，按具体房源并行完整核验。不能先对全量广告做深查。
- 特殊条件用与所需事实匹配的独立证据核验；装修、布局等定性条件看详情、户型与适用房间照片，不用广告标签或楼龄代替判断。
- 每套房源有一个明确负责人；缺证不阻塞其他房源。独立复核由该负责人创建和跟进，主agent不逐套微观复核。
- 保留事实、来源、查询时间和适用范围。楼栋设备、具体房号及广告条件分别对应，冲突写明。
- 按当前环境可用的并行能力安排任务，不绑定模型或运行时调用。没有独立agent能力时顺序执行相同职责，并标明“仅自查，未独立复核”，不能伪装角色独立。
- 本技能用于搜索、核验和整理。联系中介、提交个人资料、预约、申请与签约按用户另行授权处理。
