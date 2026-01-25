# DKU Programs Hub

## 仓库用途

- **面向对象**：参与 DKU-小X宝社区公益项目的学生团队、导师（Mentor）、监督委员会（PMC）成员。
- **核心用途**：
  - **项目成员指引**：存放项目启动必读文档（如 `Program_guideline/1_quick_start_and_must_know.md`），帮助新同学快速理解项目背景、角色与合规要求。
  - **公共信息同步**：集中记录公共资源链接、推荐工具、重要公告等（如 `Public_resources/tools_kit_101.md`）。
  - **项目进度管理**：通过各项目目录、进度文档和里程碑记录，帮助团队对齐进展。
  - **Issue 处理与协作**：使用 GitHub Issues 协调需求、Bug、问题反馈和讨论。

> **一句话理解本仓库**：这是 DKU-小X宝公益项目在 GitHub 上的“公共中控台”，所有团队都在这里对齐信息和进度。

## 目录结构（当前）

- **`Program_guideline/`**：项目启动与合规相关指南
  - `1_quick_start_and_must_know.md`：DKU-小X宝社区创新校园项目 Quick Start & Must-Know 指南（新加入同学务必完整阅读）。
- **`Public_resources/`**：公共资源与工具箱
  - `tools_kit_101.md`：社区推荐的技术工具箱与资源链接。
- **`Project_charts/`**：项目进度与结构图（可根据需要补充不同项目的进度表、架构图等）。

> 后续如果有新的项目子仓库或文档，请尽量保持命名清晰，并在本 README 中补充简要说明。

## 如何使用这个仓库

### 1. 新成员 Quick Start

- **Step 1：加入组织与沟通渠道**
  - 确保已加入项目微信群和本 GitHub 组织/仓库。
  - 根据 `Program_guideline/1_quick_start_and_must_know.md` 中的 Quick Start 清单，完成飞书知识库开通、小X宝社区志愿者实名登记等步骤。
- **Step 2：完整阅读指南**
  - 优先阅读：`Program_guideline/1_quick_start_and_must_know.md`。
  - 同时浏览：`Public_resources/tools_kit_101.md`，了解可用工具和资源。
- **Step 3：对齐角色与分工**
  - 在你所在项目组内部明确 Leader、备选 Leader 和各成员分工。
  - 与 Mentor 做一次期望对齐（可以在线上完成）。

### 2. 项目进度管理建议

- **按项目建立清晰结构**（示例）：
  - `Project_charts/<project_name>/` 目录下，维护：
    - `timeline.md` 或进度表（关键里程碑、负责人、预期时间）。
    - `notes.md` 或会议纪要。
- **使用 Issue 跟踪具体事项**：
  - 新需求、Bug、阻塞问题、合规疑问等，优先在 Issue 中记录，方便 Mentor 和 PMC 追踪。
  - 建议使用标签（labels）区分：`question`、`bug`、`enhancement`、`compliance` 等。

### 3. Issue 使用规范（建议）

- **创建 Issue 时请尽量包含**：
  - **标题**：简要说明问题/需求（如：`[Project A] 用户访谈问卷合规性确认`）。
  - **背景**：相关项目、场景、当前进展。
  - **预期结果**：你希望得到哪种帮助/决策（例如：批准/否决/给出修改建议）。
  - **截止时间（如有）**：如果与里程碑相关，请标注时间。
- **处理流程建议**：
  - 创建者先分配给对应项目 Leader 或 Mentor。
  - 复杂合规/风险问题可 @ PMC 成员共同参与讨论。
  - 问题解决后关闭 Issue，并在必要时链接到对应文档或代码提交。

## 贡献与协作约定

- **提交前自查**：
  - 不要上传任何含有患者/家庭等个人隐私信息的原始数据或截图。
  - 提交文档时保持命名规范、结构清晰，方便其他团队快速理解和复用。
- **建议的协作方式**：
  - 利用 Pull Request（PR）进行较大变更，方便 Mentor/PMC Review。
  - 小范围、低风险文档更新可以直接在分支上修改，但仍建议在 Commit 信息中写明“why”。

## 后续可以继续完善的方向

- 为每个具体项目增加单独的 `README` 或说明文件，并在本仓库 `README` 中集中索引。
- 补充 `Project_charts/` 中的项目进度模板（例如甘特图、里程碑示例）。
- 根据实践，不定期更新 `Public_resources/` 中的工具与资源链接。

> 如果你是新加入的同学：从本 README 开始，再顺着 `Program_guideline/1_quick_start_and_must_know.md` 一路读下去，就能对整个 DKU-小X宝公益项目有一个比较完整的认识。
