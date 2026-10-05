# Zlearning

[中文](#中文介绍) · [English](#english-overview)

## 中文介绍

Zlearning 是面向零基础、跨领域学习者和企业技术培训场景的 GitHub Copilot Skill。它把“专业上正确但新手看不懂”的知识，重构为准确、渐进、可复述、可练习、可验收的课程内容。

### 适用场景

- 通俗解释概念、原理、区别和关系；
- 梳理知识地图、端到端机制链路与前置依赖；
- 改写或整合培训材料、课程讲义和学习资料；
- 生成中英文独立 Word 课程，并按需派生 PDF/PPT；
- 设计案例、练习、答案和分层能力测评；
- 审计技术准确性、新手友好度、双语一致性和 Office 交付质量。

尤其适合云计算、虚拟化、存储、网络、灾备、AI，以及 TAC/FAE 技术支持与企业培训。

### 核心方法

Zlearning 使用 MAPS 作为内部推演框架，但不要求正文机械套用模板：

1. **Map**：建立知识地图，明确定位和概念关系；
2. **Aim**：说明没有该技术时的问题及其价值；
3. **Picture**：按认知风险选择生活类比或直接演示；
4. **Steps**：拆解输入、判断、动作、输出和交接；
5. **Scenario**：放入真实业务、运维或排障场景；
6. **Seal**：补充辨析、成立边界与记忆锚点。

### 关键质量门禁

- **术语依赖与首次定义**：先建立依赖图和首次出现台账，避免循环解释。
- **学习主线与价值入口**：先让学习者看见课程走向、现实问题和学习价值。
- **解释模式选择**：支持 `concept_first_analogy`、`analogy_first` 和 `direct_demonstration`。
- **语义层隔离**：生活类比、正式机制和真实业务案例不混写。
- **机制与覆盖台账**：区分名称被提及和真正完成教学。
- **能力进阶**：覆盖 Recognize、Explain、Reconstruct、Troubleshoot。
- **范围回归**：改善呈现不等于扩大知识范围。
- **双语等值与交付验收**：检查技术密度、结构、Office 可用性、视觉质量、版本和哈希。

### 使用时需要提供什么

最低只需提供 **主题或任务**，例如“解释 RAID 5”或“把这些资料做成新手课程”。为了让结果更贴合实际，建议同时提供：

1. **主题与目标**：希望解释、改写、整合、审计还是生成完整课程；
2. **学习者**：受众角色、已有基础及工作场景；
3. **来源材料**：Word、PDF、PPT、网页、现有课程或指定参考资料；没有材料时也可直接说明主题；
4. **范围与边界**：必须保留、需要删除、不要展开的内容，以及适用产品/版本；
5. **语言与交付格式**：中文、英文或双语，以及 Word、PDF、PPT 或仅聊天回答；
6. **深度与用途**：快速认识、系统自学、课堂培训、认证考试或技术支持；
7. **特别要求**：案例、练习、答案、页数、品牌风格、截止时间等。

信息不完整时，Zlearning 会先使用已知内容推进；只有缺失项会显著改变课程范围或交付方式时才提问。涉及完整课程且用户未指定格式时，默认规则如下。

### 最简使用 Prompt

```text
请使用 Zlearning 处理以下任务：
主题/任务：[要解释或制作的内容]
学习者：[受众及基础]
来源材料：[文件或链接；没有可写“无”]
必须保留：[核心范围]
不要展开：[排除范围]
语言与格式：[例如：英文 Word]
用途与深度：[例如：新人自学课程]
其他要求：[案例、练习、产品版本等]
```

### 默认交付规则

完整课程默认生成两个独立的 Word 主版本：中文版和英文版。正式生成前确认是否同时需要 PDF 与 PPT/PPTX。不同语言和格式应共享同一内容基线、术语表、技术结论、案例参数和练习范围。

## English Overview

Zlearning is a GitHub Copilot Skill for beginners, cross-domain learners, and enterprise technical training. It turns technically correct but difficult material into courses that are accurate, progressive, explainable, practice-ready, and verifiable.

### Use Cases

- Explain concepts, mechanisms, differences, and relationships in accessible language.
- Build knowledge maps, prerequisite chains, and end-to-end technical flows.
- Rewrite or consolidate training materials, course notes, and learning resources.
- Produce separate Chinese and English Word courses, with optional PDF/PPT derivatives.
- Design scenarios, exercises, answer keys, and progressive competency assessments.
- Audit technical accuracy, beginner accessibility, bilingual equivalence, and Office delivery quality.

It is especially useful for cloud computing, virtualization, storage, networking, disaster recovery, AI, TAC/FAE support, and enterprise enablement.

### Core Method

Zlearning uses MAPS as an internal reasoning framework without forcing a repetitive writing template:

1. **Map** — locate the concept and establish its relationships.
2. **Aim** — explain the problem it solves and the value it provides.
3. **Picture** — choose a safe analogy or direct demonstration.
4. **Steps** — trace input, decision, action, output, and handoff.
5. **Scenario** — apply the mechanism to a realistic work situation.
6. **Seal** — clarify boundaries, distinctions, and a memorable anchor.

### Quality Gates

- **Term dependencies and first definitions** prevent circular explanations.
- **Learning journey and value entry** show learners where the course is going and why it matters.
- **Explanation-mode selection** supports `concept_first_analogy`, `analogy_first`, and `direct_demonstration`.
- **Semantic-layer separation** keeps analogies, formal mechanisms, and business scenarios distinct.
- **Mechanism and coverage ledgers** distinguish a mentioned term from a concept that has truly been taught.
- **Capability progression** covers Recognize, Explain, Reconstruct, and Troubleshoot.
- **Scope regression** ensures presentation improvements do not expand the approved knowledge scope.
- **Bilingual and delivery validation** checks technical depth, structure, Office usability, visual quality, versions, and hashes.

### What to Provide

At minimum, provide a **topic or task**, such as “Explain RAID 5” or “Turn these references into a beginner course.” For a more targeted result, include:

1. **Topic and objective** — explain, rewrite, consolidate, audit, or create a complete course;
2. **Learners** — audience roles, prior knowledge, and work context;
3. **Source material** — Word, PDF, PPT, web pages, existing courses, or named references; a topic alone is also acceptable;
4. **Scope and boundaries** — required content, exclusions, depth limits, and applicable product/version;
5. **Language and deliverable** — Chinese, English, or bilingual; Word, PDF, PPT, or chat only;
6. **Depth and use** — quick introduction, self-study, instructor-led training, certification, or support enablement;
7. **Special requirements** — cases, exercises, answer keys, length, brand style, deadline, and similar constraints.

If information is incomplete, Zlearning proceeds with what is known and asks only when a missing choice would materially change the scope or deliverable.

### Minimal Usage Prompt

```text
Use Zlearning for this task:
Topic/task: [what to explain or create]
Learners: [audience and prior knowledge]
Source material: [files or links; write “none” if unavailable]
Must include: [core scope]
Do not expand: [excluded scope]
Language and format: [for example, English Word]
Purpose and depth: [for example, beginner self-study course]
Other requirements: [cases, exercises, product version, and so on]
```

### Default Delivery

A complete course normally produces two independent Word baselines: one Chinese and one English. PDF and PPT/PPTX outputs are confirmed before production. Every language and format must share the same content baseline, terminology, technical conclusions, case parameters, and exercise scope.

## 一句话安装 / Install with One Prompt

无需手动执行命令。将下面整段 Prompt 复制到具备文件和终端操作能力的 AI 编程工具中即可：

```text
请把 https://github.com/550YU/Zlearning 的最新 main 分支安装为当前项目的项目级 AI Skill。先检查当前项目已有的 Skill 目录规范；如果没有明确规范，就安装到 .github/skills/Zlearning。下载并保留完整的 SKILL.md 和 references 目录。若目标位置已有不同内容，先创建带时间戳的备份，禁止直接覆盖。安装后核对文件列表，并验证所有文件可读取、SKILL.md 存在且 SHA-256 校验无复制差异。不要删除用户级原件，也不要把临时下载目录或嵌套的 .git 目录留在项目中。最后报告安装路径、文件数、版本或提交号和验证结果。
```

Copy the following prompt into an AI coding tool that can access files and run terminal commands:

```text
Install the latest main branch of https://github.com/550YU/Zlearning as a project-level AI Skill in the current project. First detect and follow any existing project Skill-directory convention; if none exists, install it at .github/skills/Zlearning. Preserve the complete SKILL.md file and references directory. If the destination already contains different content, create a timestamped backup before replacing anything. After installation, compare the file list, confirm that every file is readable, verify that SKILL.md exists, and use SHA-256 hashes to ensure the copied files match. Do not remove any user-level installation, and do not leave a temporary download directory or nested .git directory in the project. Finally report the installation path, file count, installed version or commit, and validation result.
```

> The AI tool must have permission to access the project files and GitHub. / AI 工具需要具备项目文件与 GitHub 访问权限。

## 使用示例 / Example Prompts

- “用 Zlearning 给零基础学员解释 RAID 5 和 RAID 10 的区别。”
- “把这些存储资料整合成一套中英文独立 Word 课程。”
- “检查课程是否存在术语前置依赖、机制断链或双语密度不一致。”
- “Use Zlearning to explain RAID 5 and RAID 10 to first-time learners.”
- “Turn these storage references into separate Chinese and English Word courses.”
- “Audit this course for missing prerequisites, broken mechanism chains, and bilingual depth gaps.”

## 仓库结构 / Repository Structure

```text
Zlearning/
├── SKILL.md
├── LICENSE
├── README.md
└── references/
    ├── answer-template.md
    ├── course-audit-checklist.md
    ├── course-delivery-checklist.md
    ├── examples.md
    └── quality-checklist.md
```

## 参考文件 / References

- `answer-template.md` — 标准解释结构 / standard explanation structure
- `course-audit-checklist.md` — 技术、认知与一致性审计 / technical, cognitive, and consistency audit
- `course-delivery-checklist.md` — Word/PDF/PPT 交付验收 / Word, PDF, and PPT delivery validation
- `examples.md` — 解释模式与机制示例 / explanation-mode and mechanism examples
- `quality-checklist.md` — 回答级质量检查 / response-level quality checks

## 设计原则 / Design Principles

- 通俗不等于删除必要术语。Accessibility does not mean removing essential terminology.
- 类比建立直觉，但不替代正式定义。Analogies build intuition but never replace formal mechanisms.
- 先讲主干，再讲影响判断的边界。Teach the main path before the boundaries that affect decisions.
- 产品事实应绑定版本、配置、兼容范围和可靠来源。Product claims must be tied to versions, configurations, compatibility scope, and reliable sources.
- 测试结果是有限证据，不是超范围证明。A test result is bounded evidence, not proof beyond its scope.

## 许可证 / License

基于 [MIT License](LICENSE) 发布。Released under the [MIT License](LICENSE).