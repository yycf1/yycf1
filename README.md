# yycf1

**AI applications · Agents · Developer tools**

围绕文献研究、编程 Agent 和开发流程，构建能跑起来、能验证、能回看的 AI 应用。
目前主要使用 Python，关注检索证据、工具执行的边界，以及执行过程怎么被记录和复现。

[Projects](#selected-projects) · [Engineering notes](#engineering-notes)

## Selected projects

### [Paper Research Agent](https://github.com/yycf1/paper-research-agent)

**个人科研文献阅读助手** — 从论文检索、导入和精读，到带来源的问答与跨论文比较。

结合向量检索、BM25 和重排组织证据；保留原文引用与内容版本，通过 Web、CLI 和 MCP 使用共用工具。

`Python` `FastAPI` `LangGraph` `Chroma` `React / TypeScript`

[架构](https://github.com/yycf1/paper-research-agent/blob/main/docs/architecture.md) · [使用说明](https://github.com/yycf1/paper-research-agent/blob/main/docs/usage.md) · [验证记录](https://github.com/yycf1/paper-research-agent/blob/main/docs/validation.md)

### [EasyCode](https://github.com/yycf1/easycode)

**极简编程 Agent** — 给它一个目录和一句任务，它读代码、改文件、在加固容器里跑命令，做完用中文总结。

学习参考 pi 的极简架构：手写 86 行 agent 循环与原生 tool_calls，用四个最小工具完成读写与执行，编辑要求精确且唯一匹配；bash 默认进一次性加固容器；SQLite 事件流配合 SSE，让每一步决策都能回看。

`Python` `FastAPI` `SQLite` `Docker` `原生 tool_calls`

[README](https://github.com/yycf1/easycode) · [验证记录](https://github.com/yycf1/easycode/blob/main/docs/%E9%AA%8C%E8%AF%81%E8%AE%B0%E5%BD%95.md)

### [Session Trash](https://github.com/yycf1/dsh-plugin-delete-session)

**开发工具小项目** — 为 DeepSeek Harness 提供会话删除、撤销和本地回收站，关注失败回滚与文件操作边界。社区插件。

`JavaScript` `Plugin development`

## Engineering notes

- [工具权限与任务意图](https://github.com/yycf1/paper-research-agent/blob/main/docs/intent-and-permissions.md)：把模型决策和宿主执行约束分开。
- [命令执行的沙箱边界](https://github.com/yycf1/easycode/blob/main/docs/Docker%E5%AE%B9%E5%99%A8%E9%9A%94%E7%A6%BB%E9%80%9F%E8%AE%B0.md)：把不可控的 shell 关进一次性容器，限制网络、权限与资源。
- [验证记录：只写跑过的](https://github.com/yycf1/easycode/blob/main/docs/%E9%AA%8C%E8%AF%81%E8%AE%B0%E5%BD%95.md)：每次改动跑了什么、结果如何、留下哪些边界。

实现细节、复现命令及当前边界记录在各项目仓库中。
