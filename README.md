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

### Default Delivery

A complete course normally produces two independent Word baselines: one Chinese and one English. PDF and PPT/PPTX outputs are confirmed before production. Every language and format must share the same content baseline, terminology, technical conclusions, case parameters, and exercise scope.

## 安装 / Installation

### 项目级安装 / Project-level installation (recommended)

```text
.github/
└── skills/
    └── Zlearning/
        ├── SKILL.md
        └── references/
```

```bash
git clone https://github.com/550YU/Zlearning.git .github/skills/Zlearning
```

### 用户级安装 / User-level installation

将仓库内容复制到 Copilot 用户 Skills 目录中的 `Zlearning` 文件夹。实际路径取决于本机配置。

Copy the repository into a `Zlearning` folder under your Copilot user Skills directory. The exact path depends on your local Copilot configuration.

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