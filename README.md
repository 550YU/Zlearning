# Zlearning

面向零基础、跨领域学习者和企业技术培训场景的 GitHub Copilot Skill。它将“专业上正确但新手看不懂”的知识，重构为准确、渐进、可复述、可练习、可验收的课程内容。

> Beginner-friendly technical explanation and bilingual course-development skill for GitHub Copilot.

## 适用场景

当任务涉及以下内容时使用 Zlearning：

- 通俗解释概念、原理、区别和关系；
- 梳理知识地图、端到端机制链路与前置依赖；
- 改写或整合培训材料、课程讲义和学习资料；
- 生成或完善中英文独立 Word 课程；
- 设计案例、练习、答案和分层能力测评；
- 审计课程的技术准确性、新手友好度、双语一致性和 Office 交付质量。

尤其适合云计算、虚拟化、存储、网络、灾备、AI、TAC/FAE 技术支持与企业培训场景。

## 核心方法

Zlearning 以 MAPS 为内部推演框架，但不要求正文机械套用模板：

1. **Map**：建立知识地图，明确定位和概念关系；
2. **Aim**：说明没有该技术时的问题及其价值；
3. **Picture**：按认知风险选择生活类比或直接演示；
4. **Steps**：拆解输入、判断、动作、输出和交接；
5. **Scenario**：放入真实业务、运维或排障场景；
6. **Seal**：补充辨析、成立边界与记忆锚点。

## 关键质量门禁

- **术语依赖与首次定义**：先建立术语依赖图和首次出现台账，避免用未解释术语反向解释前置知识。
- **四段价值入口**：人物需求 → 遇到的问题 → 为什么需要该技术 → 实现后的效果。
- **解释模式选择**：支持 `concept_first_analogy`、`analogy_first` 和 `direct_demonstration`。
- **语义层隔离**：生活类比、正式技术机制和真实业务案例不得混写。
- **机制台账**：覆盖目标、可见信息、判断或动作、结果及下一环节交接。
- **覆盖台账**：区分 `mentioned` 与真正完成教学的 `covered`。
- **能力进阶**：练习与测评覆盖 Recognize、Explain、Reconstruct、Troubleshoot。
- **双语等值**：中文与英文独立成品保持结构、技术密度、案例逻辑与边界一致。
- **交付验收**：检查 DOCX/PDF/PPT 可打开性、视觉排版、乱码、结构、表格、版本和哈希。

## 课程交付默认规则

完整课程任务默认生成两个独立的 Word 主版本：中文版和英文版。正式生成前会确认是否同时需要同版 PDF 与 PPT/PPTX。不同语言和格式应使用同一内容基线、术语表、技术结论、案例参数与练习范围。

## 安装

### 项目级安装（推荐）

将本仓库内容放入目标项目：

```text
.github/
└── skills/
    └── Zlearning/
        ├── SKILL.md
        └── references/
```

克隆示例：

```bash
git clone https://github.com/550YU/Zlearning.git .github/skills/Zlearning
```

### 用户级安装

也可将仓库内容复制到 Copilot 用户 Skills 目录中的 `Zlearning` 文件夹。实际路径取决于本机 Copilot 配置。

## 使用示例

- “用 Zlearning 给零基础学员解释 RAID 5 和 RAID 10 的区别。”
- “把这些存储资料整合成一套中英文独立 Word 课程。”
- “检查这门虚拟化课程是否存在术语前置依赖、机制断链或双语密度不一致。”
- “围绕一个 TAC 故障案例设计 Recognize 到 Troubleshoot 四级练习。”

## 仓库结构

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

## References

- `answer-template.md`：标准解释结构模板；
- `course-audit-checklist.md`：课程技术、认知与一致性审计；
- `course-delivery-checklist.md`：Word/PDF/PPT 文件交付验收；
- `examples.md`：解释模式、类比映射和机制示例；
- `quality-checklist.md`：回答级质量检查。

## 设计原则

- 通俗不等于删除必要术语；
- 类比用于建立心智画面，不能替代正式技术定义；
- 先讲主干，再讲会影响正确判断的边界；
- 产品事实应绑定版本、配置、兼容性范围与可靠来源；
- 测试结果是有限证据，不应被写成超出其范围的证明；
- 面向学员的正文不应暴露作者侧审计规则或机械写作模板。

## License

Released under the [MIT License](LICENSE).