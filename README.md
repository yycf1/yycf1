# yycf1

**AI applications · Agents · Developer tools**

围绕文献研究、代码修复和开发流程，构建可以运行、验证和回看的 AI 应用。
目前主要使用 Python，关注检索证据、工具执行边界，以及测试反馈如何帮助 Agent 完成任务。

[Projects](#selected-projects) · [Engineering notes](#engineering-notes)

## Selected projects

### [Paper Research Agent](https://github.com/yycf1/paper-research-agent)

**个人科研文献阅读助手** — 从论文检索、导入和精读，到带来源的问答与跨论文比较。

结合向量检索、BM25 和重排组织证据；保留原文引用与内容版本，通过 Web、CLI 和 MCP 使用共用工具。

`Python` `FastAPI` `LangGraph` `Chroma` `React / TypeScript`

[架构](https://github.com/yycf1/paper-research-agent/blob/main/docs/architecture.md) · [使用说明](https://github.com/yycf1/paper-research-agent/blob/main/docs/usage.md) · [验证记录](https://github.com/yycf1/paper-research-agent/blob/main/docs/validation.md)

### [RepairLab](https://github.com/yycf1/repairlab)

**代码仓库修复与验证 Agent** — 根据源码、行为约定和测试反馈定位问题，修改补丁并在干净副本中验收。

将测试证据绑定到当前补丁，逐项核对关键用例；工作台提供执行记录、Git diff 和验收报告，支持本地可信执行与 Docker runner。

`Python` `Pydantic` `pytest` `FastAPI` `SQLite` `Docker`

[架构](https://github.com/yycf1/repairlab/blob/main/docs/%E6%9E%B6%E6%9E%84%E8%AF%B4%E6%98%8E.md) · [评测与复跑](https://github.com/yycf1/repairlab/tree/main/docs/evaluation) · [CI](https://github.com/yycf1/repairlab/actions)

### [Session Trash](https://github.com/yycf1/dsh-plugin-delete-session)

**开发工具小项目** — 为 DeepSeek Harness 提供会话删除、撤销和本地回收站，关注失败回滚与文件操作边界。社区插件。

`JavaScript` `Plugin development`

## Engineering notes

- [工具权限与任务意图](https://github.com/yycf1/paper-research-agent/blob/main/docs/intent-and-permissions.md)：将模型决策与宿主执行约束分开。
- [结构化验收与关键用例](https://github.com/yycf1/repairlab/blob/main/docs/%E7%BB%93%E6%9E%84%E5%8C%96%E9%AA%8C%E6%94%B6%E4%B8%8E%E5%85%B3%E9%94%AE%E7%94%A8%E4%BE%8B.md)：确认哪些测试真正运行，以及哪些结果足以支持补丁通过。
- [修复机制的离线复跑](https://github.com/yycf1/repairlab/tree/main/docs/evaluation)：固定样例、预期结果与运行条件，区分脚本演示和真实模型评测。

实现细节、复现命令及当前边界记录在各项目仓库中。
