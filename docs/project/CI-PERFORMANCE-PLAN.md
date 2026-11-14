# CI 性能优化整体方案与当前交付状态

本方案面向上游模板与本书库：先按变更和真实依赖选择消费者，再把选中的工作分配到分片；未受影响且已有成功覆盖的部分不重新测试。浏览器完整作业以 900 秒为目标、严格低于 1200 秒为验收上限。托管实现只在模板修改、正式发布后用 `./tbook template update` 同步，下游维护自己的读取声明和可选执行拆分。

截至 2026-11-15，本次验收固定在下游采用合入源码 `735e459d9e290834ec503fe8f1b76246a8c06638`、正式模板 **0.12.1**（上游 `fe2aba4ac384d1a809507b2b39ac3071494012cd`）。两仓库该源码的整体正常 CI、Check、严格 Pages 和实际部署均成功；下游默认 main 的 67 个正常浏览器完整作业全部达到 15 分钟目标。相同源码的固定普通分支另已完成 normal／films／slow 首次验收，以及同分支、同源码、同 profiles 的未变更 auto 零重型执行。**固定源码验证已补齐；最终文档审查、PR、合入后的 CI／Pages 与终结判定仍由发布者负责，尚不宣称整个目标完成。** 后续作者主干独立推进到 `2fa…`，其锁、正文与派生数据属于另一输入样本，不追逐它改写本次验收源码。

## 1. 已交付与固定源码证据

已按“模板 P0 选择器→正式发布→下游工具升级→依据残余长尾改进分片”的顺序落地。模板早期采用经下游 [PR #280](https://github.com/the-omega-institute/trureturing-books/pull/280) 合入；依赖补全与重型 suite 拆分经 [PR #270](https://github.com/the-omega-institute/trureturing-books/pull/270) 合入 `6f2c50c4452c0b553183e892fd79983be4a50361`。该 PR 的 [CI 43598001205][consumer-pr] 整体与 Check 成功，18 份报告精确覆盖 63 父 suite／64 单元。对应严格 [Pages 43599886778][consumer-pages] 成功，实际部署 `7788502228` 精确对应 `6f2c50c…`；墙钟／作业合计为 1623／1614 秒。这些是历史成功证据。

历史主干 `4532a04e…` 的 [CI 43600373121][consumer-failed] 和 `05f34de9…` 的 [CI 43602419619][consumer-old-failed] 曾失败：188430 字节整份计划经环境变量传给进程触发 `E2BIG`，影响 validate、slides 和 Check。前者 18 个正常浏览器作业虽为 403–843 秒，也不能产生成功责任覆盖。上游 [PR #88](https://github.com/the-omega-institute/trureturing-books-template/pull/88) 改用计划／needs 文件传输；后续修复合并、正式 [v0.12.1 发布][up-release] 与下游工具升级均已完成，不再是待修复项。大型计划的理由按消费者合并计数，保留实际选择集合与失败汇总。

最终下游 [PR #293](https://github.com/the-omega-institute/trureturing-books/pull/293) 的 [CI 43618521680][adoption-pr-ci] 整体与 Check 成功（head `109fa9a8…`，被测 merge `b2159665…`），65 份报告精确覆盖 64 父 suite／65 单元。作者 [PR #292](https://github.com/the-omega-institute/trureturing-books/pull/292) 的两个新测试随后进入采用合入 `735e459d…`；其默认分支 [CI 43620613921][adoption-main-ci] 整体与 Check 成功，生产报告合并精确接受全部 67 份当前报告，覆盖 **66 父 suite／67 单元**，无漏测或重复。严格 [Pages 43620613650][adoption-main-pages] 成功，部署 **7791430455** 状态成功且 SHA 精确为 `735e459d…`，同时提供实际 films 责任证明；这是新部署，不是继承跳过。

固定普通分支 `ci/acceptance-v0121-735e459d` 指向完全相同的 `735e459d…`。[首次手动 auto 43623619560][branch-bootstrap] 整体与 Check 成功，共 147 个成功作业。因无同分支可比成功证明，normal／films／slow、五个导出作业、slides 和全部十部影片均按设计选中，属于刻意冷启动的验证成本。normal（0 frames）与 slow（1000 frames）各覆盖 **66 父 suite／67 单元／67 份精确报告**；全部 134 份报告的 SHA、run、attempt、runtime、Node 22.23.4、profile／frames、退出状态、source／workload 身份和计时均匹配，三份下载的 normal／films／slow 覆盖记录均与生产 `merge_reports(plan, 134 reports)` 结果一致。**该次不是 slow-only，也不是默认 main 的 slow 证明。**

随后[未变更 auto 43624850866][branch-unchanged] 在同一源码、同一分支继续请求 normal／films／slow（slow frames 启用），整体与 Check 成功。实际计划全部 tasks 为 false，normal／slow execution maps 与浏览器矩阵、films／slides／exports 集合精确为空；仅 **Plan affected work 与 Check** 执行成功。validate 整个作业跳过且没有步骤，其 setup、单测、结构、静态、EPUB 检查，以及导出、正常／slow 浏览器、影片、幻灯片均未启动。36 秒墙钟／31 成功作业秒是这一次同分支覆盖继承的实测，不是未来文档 PR 的保证。

这两次普通分支的责任证明与成本提示均不能为默认 main 播种。默认 main 的 67 份 normal 报告及实际 Pages／films 部署是前述独立证据；本记录没有默认 main 的 67 份 slow 报告或未变更 auto 实测。固定源码验收已结束，本次不重新审计既有源码或另开优化搜索。

## 2. 自然基线、根因与已测结果

墙钟、完整作业历时和作业历时合计是不同指标；作业秒包含 setup、运行、上传和 post，不是 CPU 时间或账单。排队另记。以下均为单次自然运行或明确标注的固定源码验收，输入、事件和缓存条件不同，不组成匹配 A/B，不计算节省百分比。

| 样本与源码范围 | 已核实数据 | 结论边界 |
| --- | --- | --- |
| 用户报告长尾时的下游 PR #270，head `991adb20…`，[43566928667][tail-baseline]，成功；61 suites／27825 assertions | 墙钟 2397 秒，成功作业合计 14616 秒；浏览器 1–8 片分别为 **2265、902、905、1452、980、1119、779、733 秒**。1/8 的浏览器步骤 2216 秒，setup 41 秒 | 1/8 为 37 分 45 秒，瓶颈在浏览器工作；不能用减少安装解释该长尾 |
| 历史健康采用前 main `1f914c80…`、模板 0.10.3，[43583109909][before-current]，成功；63 suites | 墙钟 1918 秒、成功作业合计 12629 秒；1–8 片为 **1341、1761、1612、1352、1528、1224、1019、945 秒**。各片创建至开始 1–2 秒 | 六片超过 20 分钟，八片均超过 15 分钟；排序变化已把最慢片移到 2/8，编号 1/8 不是固有原因 |
| 已采用拆分的 PR CI [43598001205][consumer-pr]，head `c80575a6…`、实际 merge checkout `a8abb4ac…`，整体成功 | 18 个正常浏览器完整作业 **470–855 秒**，最高 14 分 15 秒，全部不超过 900 秒；浏览器作业合计 11120 秒，各片创建至开始 2 秒。全工作流墙钟 1286 秒、作业合计 16692 秒 | 该次 63 父 suite／64 单元正常 profile 达标；全工作流还包含影片等工作，不能把关键路径改善等同总资源下降 |
| 最终采用 PR [43618521680][adoption-pr-ci]，64 父 suite／65 单元，整体成功 | 65 个正常浏览器完整作业 **103–552 秒**，浏览器合计 13785 秒；工作流墙钟 1304 秒、作业合计 19237 秒。四个影片作业为 572、800、1187、676 秒 | 当前定义缺少可比成本时各单元独立；不是已知成本的 18 片比较组，PR 成功也不提供默认分支覆盖 |
| 采用合入 main `735e459d…`，[43620613921][adoption-main-ci]，66 父 suite／67 单元，整体成功 | 67 个正常浏览器完整作业 **97–613 秒**，全部低于 900 秒；浏览器合计 **14211 秒**，各片创建至开始 2–4 秒。全工作流墙钟 **819 秒**、成功作业合计 **16255 秒** | 当前冷成本、每单元一片的默认分支实测；main 的影片按既定设计交给 Pages，不能与含影片的 PR 总量直接比较 |
| 同 SHA 严格 [Pages 43620613650][adoption-main-pages] | 墙钟 **1859 秒**、成功作业合计 **1113 秒**；首作业前排队 **741 秒**；build／deploy／确认分别为 1012／27／14 秒 | 实际全站组装、films 和精确 SHA 部署成功；排队与构建历时分列，不能把 1859 秒当纯构建成本 |
| 同 SHA 普通分支首次 [auto 43623619560][branch-bootstrap]，normal／films／slow，整体与 Check 成功 | 墙钟 **672 秒**、147 个成功作业合计 **29972 秒**；normal 67 个完整浏览器作业 **88–622 秒**，合计 **14051 秒**，各片排队 2–3 秒；slow 67 个为 **86–610 秒**，合计 **14689 秒**，各片排队 1–3 秒 | 两个 profile 全部低于 900 秒且严格低于 1200 秒；无同分支证明导致全量冷验收，29972 秒是验证专用成本，不是稳态节省、CPU 时间或账单 |
| 同 SHA、同普通分支、同 profiles 的[未变更 auto 43624850866][branch-unchanged]，整体与 Check 成功 | 墙钟 **36 秒**、成功作业合计 **31 秒**；仅规划与 Check，重型作业 **0 次**，执行映射、矩阵和媒体／导出集合精确为空 | 证明该次分支内成功覆盖继承和零 setup／重型执行；与首次冷验收不是匹配 A/B，不外推为默认 main 或未来运行 |

更早的 P0 自然基线仍保留：[PR #246 43484846290][early-pr] 墙钟／作业合计 2303／17538 秒，8 路浏览器 11504 秒、4 路影片 4260 秒，10 次整库恢复合计 507 秒；健康 main `882f596…` 的 [43515344955][early-main] 为 1464／9917 秒，浏览器 707–1297 秒、setup 33–42 秒。该基线原本就是五个导出作业，恢复各 5–7 秒，不能编造“九次安装变五次”的收益；这些较早样本也不与当前冷成本运行组成 A/B。

根因有两个：原先按排序后计数取模分配，并未按真实耗时均衡；同时整个 `self-referential-table` suite 曾达 918–1035 秒，单靠重新放置也难留足 15 分钟的安装余量。两次成功基线的 suite 累计运行时间 8376／8742 秒，固定八片即使理想均分也需约 1047／1093 秒，尚未计 setup，因此保留固定八片无法满足目标。

拆分保留原测试体：494 项其他检查与 4 项穷举转换检查，共 498 项断言，仍覆盖 1344 个转换和 2304 个标签状态；提取的原正文可完整重建。没有通过减少断言、转换、真实读取或缩短时限换取速度。历史 18 片成功 PR 的两个重型子单元实际运行约 533／554 秒，其完整作业为 591／601 秒。它们属于 Node 22.23.4 的远端正常 profile，不能外推为 slow 重型工作或未来运行的时限保证。

## 3. 选择、成功覆盖与各入口

[生产选择器](../../tools/ci/plan.py) 在安装、浏览器准备和缓存下载前输出实际被测树、差异、检查族、书籍、父 suite、影片、deck、导出格式及理由。[CI](../../.github/workflows/ci.yml) 与 [Pages](../../.github/workflows/pages.yml) 共用这套规则。选择解决“哪些工作需要执行”；成功覆盖解决“哪些未变责任可以继承”；成本提示只解决“所选工作怎样分片”。

| 入口 | 当前实现行为与证据范围 |
| --- | --- |
| PR | 核对实际 checkout 的双亲 merge 与事件 base/head；base 可前进到事件 base 的后继。合并累计 `merge-base…head` 与成功基准至实际 merge-tree 的差异，防止 base 前进或抵消改动漏测。开发分支 push 不重复触发。上下游均有实际 PR 成功样本 |
| main push | 从可追溯、可比的成功祖先累计比较；push 的 `before` 不充当成功证明。失败或取消留下的责任继续选中。上下游最终验收源码均有实际整体成功与 Check 成功样本 |
| 手动 | `selection_mode` 可为 `auto` 或 `full`；`base` 约束预期成功基准、`head` 核对实际 checkout，均不是任意书名过滤器。默认启用 slow；非默认分支的手动证明仅供同分支使用。上游实际 auto slow、同 HEAD 未变更 auto，以及下游固定分支的三 profile 首次验收／未变更 auto 均成功 |
| 定时 | 自有周三入口只规划 slow profile；成功覆盖与运行时／定义可比时继承，否则全量 slow。此行为有源码与 fixture 依据，此处没有声称已观察该版本的自然定时运行 |
| reusable／tag | 采用调用方事件和 ref，不发布可被继承的责任覆盖；`full` 保留完整诊断。被调用 schedule 按调用方责任处理。正式 v0.12.1 发布的被调用 CI 已实际成功，不代表每一种调用事件组合均实跑过 |
| Pages | 无站点影响且有有效成功部署证明时才跳过 build/deploy；否则完整组装全站，恢复未变单元、补建缺失单元并清理删除项。main／tag CI 的影片交由 Pages／Release 严格构建，这是既有行为，不重复计为本次节省 |

仅 `template.toml` 版本值变化、其余解析配置完全一致时，按真实元数据读者保留工具单测与站点重建；额外声明读者仍先匹配。无法证明这一窄类时按共享输入扩大，不能仅凭文件名免测。

normal、films、slow、pages 分别记录责任，工件保留 90 天；每个来源工作流最多查最近 100 个成功运行。验证仓库、工作流、分支、事件、完成成功状态、SHA、attempt、选择器版本、运行时及工具／检查签名和祖先关系，Pages 另核对实际成功部署。PR 工件不能成为默认分支的成功基准。影片从可信 CI／Pages 影片证明中选择较新的祖先；normal 成功不能清除影片责任，未实际构建影片的 Pages 不推进 films 覆盖。

缺失、过期、权限不足、历史不全或签名不可比使相应责任明确 **full fallback**；未知路径保守扩大。删除／改名按两树读取关系并集传播，删除的可执行对象不列入分片。损坏 schema、未知 suite、选择器异常或执行集合错误则让 plan／Check 失败，不能吞成空集合。首次升级若旧摘要不适用或没有可比成功证明，扩大执行是正确结果。

末尾稳定汇总检查 **Check** 使用 `always()` 汇总所有选中任务，并验证精确执行报告；选中任务失败、取消、缺失或意外跳过均不通过，只有计划排除的任务可以跳过。其名称不依赖动态片数。验收时 17:15 UTC 只读查询传统分支保护的 `required_status_checks` 端点，返回 404「Branch not protected」；这一观察不说明未检查的仓库 rulesets，也不能证明 Check 已设为强制门禁。本次未改任何仓库设置。

最终上游 `fe2aba4…` 的 [main CI 43614047104][up-normal] 整体与 Check 成功，墙钟 **540 秒**，两个正常浏览器完整作业 **130／104 秒**；严格 [Pages 43614047045][up-pages] 墙钟 **224 秒**、作业合计 **216 秒**，部署 `7790187706` 成功且精确对应该 SHA。[手动 auto slow 43614968976][up-slow] 成功，墙钟 **232 秒**，两份精确 slow 报告（1000 frames）与完整作业 **138／146 秒**匹配；normal、build、films、slides 以及 validate 的工具安装／单测／EPUB 均跳过，确为仅补缺失 slow。随后[同 HEAD auto 43615700363][up-unchanged] 成功，**38 秒墙钟／29 作业秒、重型执行零次**；normal／slow、导出、影片、幻灯片、工具链／单测／结构／静态／EPUB 均跳过，仅保留 manifest guard、规划与 Check。这是实际远端未变更选择，区别于本地条件性重放；下游固定分支另有上述独立验收，仍不构成默认 main 的 slow 证明。

另保留历史[纯文档 PR #79][docs-pr]：44 秒墙钟／35 作业秒、重型执行零次；其合入后 Pages 继承旧部署并跳过 build/deploy，不是新部署。最终下游文档 PR 尚未进行，不能用该历史上游样本替代。

## 4. 本书读取关系与变更命中

[dependencies.json](../../books/quantum-geometry/viz/tests/dependencies.json) 是完整额外读取摘要，不是测试白名单。模板隐式保留 suite 自身、对应对象目录与字面相对 JS import 闭包；跨页导航、动态文件读取和其他非局部输入由作者声明。路径从仓库根起算，禁止绝对路径、反斜线与 `..`；glob 使用 `fnmatch.fnmatchcase`，`*` 可跨 `/`，`**` 无额外递归含义。两树摘要都必须适用于实际读者；JSON 有效、模式有匹配或 suite 数量正确都不能独自证明完整性。这不是任意动态 I/O 分析器。

历史 PR #270 为 `comparison-oisc-engine`、`spherical-trihedron-cell` 各补全 25 条标准非 solid 额外读取，并为 CHSH 增加两个对象目录 glob；其他 60 份数组当时保持原样。`figureNoteChecks` 的 CHSH 调用没有过滤器，实际导航到这些页面，必须保留跨页边。后来补入 `triadic-nameless-sandbox` 的真实读取声明；当前共有 **64 份依赖条目**，不是 66 份。

作者 PR #292 新增的 `stereographic-relativization-sandbox`、`uncompleted-horizon-sandbox` 尚无条目，按现有规则在所属书籍、共享 theme/template 和通用共享输入变化时保守选中。已完成的限定核对确认二者属于既有 own-page／common-stage 类：各自 index/main/style、registry／锁、出版文本与元数据、共享测试／服务／解析／运行时／字体输入；二者均实际调用 solid，包含 solid-core 及其 vendor 输入。引用桥各实际打开 119 个出版输入；42 个生产影响选择案例覆盖自身、测试、registry、出版及共享输入，工程文档与所核对 skills 选择零读者，无当前目标的覆盖缺口。它们仍会在无实际读取的声明地图、统计 JSON 或不相关静态图变更时多选；这是保守回退的性能成本，本次不改源码补声明。

`stageFirstChecks` 的 citations 桥先读各出版语言的 SUMMARY 和全部已出版章节，再按可视化筛选；不能因某章没有指向该页面就移除读取。锁、registry、共享 frame、hub 缩略图上界、solid 实际消费者及影片模型反向读取继续保留。例如 `two-angle-addressing/model.js` 仍影响自身 suite 与影片 001／003／007／008；forgetting、gram 模型仍各影响自身与 CHSH 及实际影片消费者。共享输出的静态检查、导出和幻灯片责任与浏览器读者分开计算。

下表是 `735e459d…` 稳态、可比成功覆盖成立且已有声明适用于两树时的选择；两项未登记 suite 的保守附加选择明确计入，不能沿用历史 63 suite 时的精确数。

| 代表差异 | 当前浏览器选择 | 仍保留的责任 |
| --- | --- | --- |
| 本工程文档／已核对的本地 skill 文档 | 0 父 suite／0 单元 | 无实际或声明读者时影片、slides、exports、validate／setup 也为零；上游另保留 manifest guard |
| `comparison-oisc-engine/main.js` 或 `spherical-trihedron-cell/main.js` | 自身＋CHSH＋两项保守读者，4 父 suite／4 单元 | 书籍结构、静态检查及启用导出仍按出版输入选择 |
| 上述已声明对象自身的测试文件 | 自身＋两项保守读者，3 父 suite／3 单元 | 测试／导入定义的成本身份更新 |
| `figure-note-checks.mjs` | CHSH＋两项保守读者，3 父 suite／3 单元 | 保留全部实际跨页读者 |
| 重型 transition helper，或该父 suite 的 parts 声明发生变化 | 重型父 suite＋两项保守读者，3 父 suite／4 单元 | 重型两个单元均继承父 suite 完整输入关系 |
| 共享影片引擎 `theme/film/` 的实际输入 | 两项保守读者，2 父 suite／2 单元 | 实际影片消费者和共享出版责任照常选中；历史零浏览器结论不适用于当前缺声明读者 |
| 已出版章节／SUMMARY | 66 父 suite／67 单元 | citations 桥的实际读取、学术幻灯片及整书导出继续负责 |

新增页面、跨页 helper、语言、计算路径、lazy 资源或影片构造时，先核对读取构造与两树适用性，再更新自有摘要；未能证明的读者保守扩大。执行 parts 不是新增选择白名单：先选父 suite，再展开该父 suite 的全部声明 parts。选择器或责任语义升级会使旧签名失效，不能为追求零执行沿用失效证明。

## 5. 已采用的分片与缓存方案

[execution-parts.json](../../books/quantum-geometry/viz/tests/execution-parts.json) 仅将重型 suite 展开为 `checks`、`transitions`。[预算装箱器](../../tools/ci/viz_budget.py) 对已选单元按可信成功耗时乘 **1.25**，每片预留 **120 秒** setup，以 **900 秒**目标确定动态片数；耗时降序、同耗时按稳定名称、最轻片优先，结果可重复。成本必须为有限正数且不超过 86400 秒，匹配测试／导入／parts 定义；页面或数据变化记录 workload 变化，旧成本只作估计，不能免除新工作。normal 与 slow 使用各自成本和成功覆盖。

未知单元各自独立；空集合不创建矩阵作业或安装工具。每片非空、无重复，并集精确等于所选单元；不可分超预算单元明确标记，不能截断或丢弃。超过 256 个矩阵作业或无法在矩阵限制内装箱就显式失败。完全没有可比成本时，当前 66 父 suite／67 单元启动 **67 个作业**，采用合入已实际如此执行；冷启动的并发、排队、重复 setup 与总作业秒是实际代价。历史已有可信成本的成功 PR 将 63 父 suite／64 单元装为 **18 片**，证明已知成本路径可用；两者不是同集合、同缓存条件的 A/B，也不能用固定片数模拟替代当前实测。成本记录来自可比成功来源，不能为减少片数借用不可信 PR 或另一 profile 的计时。

[运行器](../../tools/node/viz-test.mjs) 用单调时钟记录子进程耗时；报告必须匹配本次 SHA、run、attempt、runtime、profile／frames 及完整预期单元集合，全部成功才能推进父 suite 覆盖。普通父 suite 路径仍执行整个独立脚本，不继承调用者残留的 part；显式 `#part` 才执行相应单元，拒绝未知、隐藏、重复或父子重叠选择。影片仍按精确集合生成至多四个非空分片，Slides 按 deck 执行；导出按格式合并选中书籍，保留整书全部启用语言和格式。

**1200 秒是实际完整作业的 rollout 验收上限，不是预测公式或未来保证。** 单元计时不含 setup、共享 server、上传、post 和排队；完整作业与排队必须另读远端数据。本书固定分支的 67 个 slow 完整作业已实测达到 900 秒目标，依据是该次 1000 frames 的独立报告；正常 profile 不代替 slow，普通分支不代替默认 main，现有工作流较长的故障诊断 timeout 也不等于性能目标。

缓存信任边界保持原样：PR 自产缓存、执行报告或成本不能升级为默认分支可信构建缓存、冻结状态或未来成本；只接收经来源核验的成功默认分支 Pages 构建工件及合法 Release，保留单元输入键、逐文件摘要和缺失／损坏冷构建。v0.12.1 [正式发布][up-release] 的被调用 CI 与严格示例站点成功，21 个资产／20 个缓存索引条目完整，资产大小及 GitHub SHA-256 与索引一致，索引实际下载并验摘要；没有声称所有 tar 均已下载。发布源码清单含 259 项，SHA-256 为 `a79c9d6aa655a5bb143a2fd14f9d7aea9bd835e422987b2028e4c6c8e8003425`；下游升级的托管字节与正式来源一致。Pages 输出受影响时必须完整组装和部署，不能以局部 CI 工件或旧站点替代。

## 6. 其余方案的取舍与维护成本

| 候选 | 当前决定与证据 | 改变决定所需条件及成本 |
| --- | --- | --- |
| 单次安装／按工具能力安装 | 已通过选择层消除零任务的安装；普通浏览器 setup 约 33–45 秒，远小于已确认浏览器长尾。暂不进一步拆安装协议 | 只有剩余实际重复安装成为显著关键路径，并在同集合、完整环境下证明净收益才采用；维护字体、Chromium、Node／Python 身份与失败路径，成本中 |
| 默认迁移预装镜像 | 保留现有可选能力、普通安装仍默认。[v0.11.0 镜像运行][image] 的实际 build/check/publish 作业 1850 秒，其中 image build 100、离线 exercise 14、容器书籍 check/build 1622、publish 102 秒；Actions 使用作业 87 秒，其中初始化容器 67、prepare 1、verify 12 秒 | 这证明能力可用，没有匹配的默认迁移净收益比较。采用需覆盖冷拉取与完整作业净收益，并承担 digest 固定、供应更新和普通安装回退，成本中至高 |
| 缓存传输拆包 | 暂缓。既有健康导出恢复仅 5–7 秒，先减少无关下载；没有当前残余传输瓶颈证据 | 只有传输仍显著影响关键路径，且实际字节、命中和缺包冷构建支持净收益时采用；生产者／查找器协议及逐文件摘要需同步，成本中 |
| 合并 CI／Pages 产物生产者 | 已采用无站点影响且有部署证明的 Pages 跳过；暂不改变有输出变化时的完整生产拓扑 | 需同 SHA、单元键、base URL、工具身份和完整输出集合的重复生产证据；跨事件信任、失败恢复与完整发布维护成本高 |

计划／needs 文件传输和理由体积问题均已修复并正式采用；其余候选维持上述取舍，本稿已补齐固定源码验收终态，不另开优化项目或承诺新的基准测试。下游长期维护一份真实依赖摘要和一份有限 parts 声明；模板维护选择／执行工具、两份工作流、覆盖与成本协议及回归。片数增加的资源成本和陈旧估计风险必须随自然运行记录，不能只报告最慢片变短。

## 7. 验收状态、边界与剩余责任

1. **已完成**：整体方案和既定三席审查、上游实现合入与正式 v0.12.1 发布、下游工具升级和本地依赖／parts 采用 PR 合入。既有工具回归、构建、导出、浏览器与审查证据沿用其原源码范围，不重复执行，也不以票数或测试库存代替运行验收。最终两仓库确切源码的整体 normal CI、Check、严格 Pages 和实际部署成功；下游默认 main 的 67 份精确 normal 报告及完整作业预算已验收。
2. **固定源码验证已完成**：`ci/acceptance-v0121-735e459d` 的首次 auto 43623619560 整体与 Check 成功，normal／slow 各 67 份精确报告及三 profile 覆盖记录均通过生产合并核对；两个 profile 的全部完整浏览器作业低于 900 秒目标和 1200 秒上限。随后 43624850866 在同 HEAD、同分支、同 profiles 下整体与 Check 成功，计划执行集合精确为空，validate／setup 与全部重型工作跳过。两次分别是冷验证和分支内继承证据，不构成默认 main 的 slow／未变更证明，不要求将后续作者的独立输入样本重新纳入本次验收。
3. **后续文档交付仍由发布者负责**：两次限定修订之间未进行正式文档评审或发布；本次最终修订只补权威终态并做必要文档检查。最终文档仍须独立审查、经 PR 合入 main，核对该次真实远端选择、合入后 CI 与 Pages 的部署或有效继承，再作整体目标的终结判定。不能预先宣称零工作或新部署；本次也不推断仓库 rulesets 或增设治理任务。

历史验证档案继续有效于原快照：P0 上游工具记录 1148 项／7 跳过及严格全构建 853.796 秒；当时下游正式输出为 1143 项／62 跳过（发现库存 1148 项），严格全构建 2002.201 秒，双语 HTML、六份 PDF、两份 EPUB、双语各 48 页 slides 与十部影片均实际生成，EPUBCheck 无错误。最终上游另有 1168 项工具记录／97 项可选环境跳过；各批次与平台跳过不混为最新下游实跑。原有限页面／资源／字体检查不重做；历史英文 academic PDF 50,167,829 字节超过 50,000,000 字节投稿上限、EPUB 手机浏览器预览宽度观察及 Apple Books 未实测仍保留，均不凭本次 CI 成功宣称解决。既有未引用图、影片历史来源及英文搜索索引警告也不以修改出版内容消除。

仅含本文件的差异，在**变更前相同源码已有可比 normal／films／slow 成功覆盖、两树读取关系适用且 Pages 有有效部署证明**的条件下，生产选择器的限定重放结果为零浏览器、影片、slides、exports、validate 和 setup，Pages `site=false`。本次文档路径、生产源码和该条件性前提未变，沿用第一次修订的重放，不重复执行。重放注入前提的文件覆盖适配器不生成 Git 提交或远端成功工件；固定普通分支新增的 slow 证明也不能使默认 main 自动具备该前提。上游／下游已发生的未变更 auto 与待发生的下游文档 PR 验收分别记录。

本次文档只核对差异、链接／路径、源码身份、指标范围和既有条件性重放的适用性，不重跑无关浏览器、渲染、导出或全工具测试。失败／取消运行不推进任何未完成责任；即使只改文档，真实下一次也须从最近可比成功祖先累计这些责任。一般失败路径须保留事实与诊断，需要时用手动 `selection_mode=full`；必要回退由模板正式版本与工具升级路径处理，不在下游修托管文件或丢失作者工作。900／1200 秒是本次实际浏览器作业的目标／验收上限，不是 suite 估计、工作流总时长限制或未来保证。

## 源码与证据入口

- [发布与影响选择契约](../PUBLISHING.md)、[升级手册](../UPGRADING.md)、[验证模型](../VERIFICATION.md)。
- [浏览器共享检查](../../tools/node/viz-testkit.mjs)、[引用桥](../../tools/node/viz-common.mjs)、[影片输入构造](../../tools/tbook/film_inputs.py)、[构建缓存](../../tools/tbook/buildcache.py)、[可信缓存来源](../../tools/ci/trusted_cache.py)。
- [CHSH 跨页调用](../../books/quantum-geometry/viz/tests/chsh-dial.test.mjs)、[实际跨页列表](../../books/quantum-geometry/viz/tests/figure-note-checks.mjs)、[重型父 suite](../../books/quantum-geometry/viz/tests/self-referential-table.test.mjs)、[穷举转换原正文](../../books/quantum-geometry/viz/tests/self-referential-table-transitions.mjs)。

[tail-baseline]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43566928667
[before-current]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43583109909
[consumer-pr]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43598001205
[consumer-pages]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43599886778
[consumer-failed]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43600373121
[consumer-old-failed]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43602419619
[up-normal]: https://github.com/the-omega-institute/trureturing-books-template/actions/runs/43614047104
[up-pages]: https://github.com/the-omega-institute/trureturing-books-template/actions/runs/43614047045
[up-slow]: https://github.com/the-omega-institute/trureturing-books-template/actions/runs/43614968976
[up-unchanged]: https://github.com/the-omega-institute/trureturing-books-template/actions/runs/43615700363
[docs-pr]: https://github.com/the-omega-institute/trureturing-books-template/actions/runs/43537043873
[up-release]: https://github.com/the-omega-institute/trureturing-books-template/releases/tag/v0.12.1
[image]: https://github.com/the-omega-institute/trureturing-books-template/actions/runs/43583106195
[adoption-pr-ci]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43618521680
[adoption-main-ci]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43620613921
[adoption-main-pages]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43620613650
[branch-bootstrap]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43623619560
[branch-unchanged]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43624850866
[early-pr]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43484846290
[early-main]: https://github.com/the-omega-institute/trureturing-books/actions/runs/43515344955
