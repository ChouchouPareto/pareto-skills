# Pareto Skills

这是 ChouchouPareto 的个人 Skill 合集仓库，用于统一管理产品、写作、需求沟通和工作场景中可复用的 AI 工作流。

## Skills

| 目录 | 调用名称 | 用途 |
|---|---|---|
| [`skills/prdput-skill`](skills/prdput-skill) | `$prdput-skill` | 通过创作者强参与的流程，协作撰写、评审和定稿传统、0→1及 AI/Agent 产品 PRD。 |
| [`skills/quick-requirement-distillation`](skills/quick-requirement-distillation) | `$distill-user-requirements` | 通过少量高价值追问，将模糊、零散或冲突的表达收敛为清晰需求。 |
| [`skills/product-analysis`](skills/product-analysis) | `$product-analysis` | 从可观察的界面、交互和产物证据中拆解 AI 产品、Agent 合约和产品架构。 |
| [`skills/human-writing-standard`](skills/human-writing-standard) | `$human-writing` | 通用中文选题、创作和改稿，强调自然中文节奏与真实思考痕迹。 |
| [`skills/work-slacking-emergency`](skills/work-slacking-emergency) | `$work-slacking-emergency` | 面向结果未达成、领导催问和工作去留风险的紧急向上沟通。 |
| [`skills/personal-ip-companion`](skills/personal-ip-companion) | `$personal-ip-companion` | 个人影响力策略、真实素材共创、制作复盘与私有本地记忆接续；不自动发布。 |

## 仓库结构

```text
pareto-skills/
├── README.md
└── skills/
    ├── prdput-skill/
    ├── quick-requirement-distillation/
    ├── product-analysis/
    ├── human-writing-standard/
    ├── work-slacking-emergency/
    └── personal-ip-companion/
```

每个 Skill 至少包含一份 `SKILL.md`，并可按需要包含：

- `agents/openai.yaml`：界面显示名称、说明和默认调用提示。
- `references/`：在特定路线中才需读取的详细规则。
- `scripts/`：可重复执行的验证或处理脚本。
- `assets/`：图标等输出或展示资源。

## 安装单个 Skill

克隆仓库：

```bash
git clone https://github.com/ChouchouPareto/pareto-skills.git
```

将需要的 Skill 文件夹复制到 Codex Skill 目录：

```bash
cp -R pareto-skills/skills/prdput-skill ~/.codex/skills/
```

重新打开 Codex 任务后，使用对应的 `$skill-name` 调用。

## 来源整理说明

该仓库对原来分散的 Skill 进行统一归档，原仓库保留，不在本次整理中删除或替换。

- `quick-requirement-distillation`：来自同名原仓库。
- `work-slacking-emergency`：来自同名原仓库。
- `human-writing-standard`：使用本地保存的完整 1.3.1 标准版，用于补全原 GitHub 仓库中未上传的文件。
- `product-analysis`：整理自产品拆解项目中的 Skill 目录。
- `prdput-skill`：基于 AI 产品经理课程资料与创作者强参与原则新建。
- `personal-ip-companion`：从个人IP策略讨论与公开研究中提炼的通用协作方法。个人资料和实际任务记忆存于仓库外，不随技能发布。

## License

各 Skill 保留其目录内已有的许可证和授权信息。未附带许可证的内容不默认授予额外权利。
