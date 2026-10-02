# 日本租房领域文档地图

本目录提供完整地图，不是另一技能入口。先按任务选普通 reference，再在需要时打开附录；无需一次加载全部文件。

## 入口与编排

- [skill-reference.md](skill-reference.md)：领域用途、核心规则、任务导航与按需读取规则，唯一技能入口。
- [主agent](references/main-agent.md)：整理条件、优先级与核验方法，安排范围和并行资源，处理升级决策及用户沟通。
- [工作流程 DAG](references/workflow.md)：整体依赖、批次并行与单套房源内部流程，两张 Mermaid 无环图。
- [交接与结果约定](references/contracts.md)：条件档案、收集交接、房源分派、复核输入及回传、逐套结果和统一交付格式。

## 收集与统一归并

- [网站／区域收集](references/collect-area.md)：共通条件站内筛选、列表补筛、范围覆盖与增量候选交接。
- [独立 merge resolver](references/merge-resolver.md)：跨网站与区域去重、身份和事实冲突协调、候选队列、归并排序与统一文档维护。

## 逐房源核验与复核

- [完整房源核验](references/verify-property.md)：身份与募集状态、费用合同、户型实景、通勤、特殊条件，以及负责人自行创建复核agent。
- [独立房源复核](references/review-property.md)：检查原始来源、证据范围和条件判定，向房源负责人回传问题并复核修正。
- [特殊条件核验](references/verify-special.md)：依用户条件设计通过标准和证据方案，再按房源独立查证；不预设网络或其他偏好。
- [住宅网络核验](references/internet.md)：仅有网络要求时读取，分开接入介质、覆盖与已装状态、共享容量、速率及可开通性。

## 按需附录

- [房源网站参考](references/appendix/housing-sites.md)：需选择查询入口、补充来源或解释站点能力时读取；由收集流程调用。
- [光纤参考](references/appendix/fiber-reference.md)：网络要求涉及技术名词、接入类型或证据理解时读取；配合住宅网络核验使用。
- [提供商反查](references/appendix/provider-reverse-lookup.md)：适合从提供商覆盖或导入楼栋反查在租房源时读取；结果回到共通初筛与逐户核验主流程。

## 技能元数据

- [agents/openai.yaml](agents/openai.yaml)：展示名称、简述及默认调用提示，不是独立技能入口。

本包没有需要额外加载的 scripts 或 assets；不为空目录创建占位内容。
