# NeuronHub
🧠Your Personal Data Nexus – Where Intelligence Meets Convenience
💡个人数据中枢
# 技术栈
Dart 后端（shelf或其它框架）、Flutter 前端、PostgreSQL 数据库、Nginx 代理，然后通过 Docker 和 MicroK8s 部署

# 任务进度
- ⬜数据可视化用图表库，使用 `flutter/material` 的 `DataTable` 和 `ECharts`（通过 `echarts_flutter` 包）实现数据可视化，使用 **Fluent UI** 或 **D3.js** 在 Flutter 前端生成数据看板（文档更新趋势、关键词云、文档关联图谱）Flutter动态图表（class ChartWidget）（使用 `fl_chart` 实现数据可视化）
- ⬜多人实时协作
- ⬜在手机（Flutter 前端）和电脑同时编辑同一文档，跨平台实时同步。
- ⬜现代UI如Flutter的动画效果[Flutter 动态粒子效果](https://pub.dev/packages/particles)  
- ⬜自动化备份，备份功能集成到应用内，一键导出/导入
  - （不考虑目前）甚至支持云存储（如 Dropbox、Google Drive）
  - ⬜备份功能可以设计成定期生成数据库备份（定期备份功能）备份功能通过定期将数据库导出为SQL文件或压缩包，用户可以下载，导入时上传文件恢复。备份功能可以通过pg_dump和自定义脚本实现，导出为SQL或压缩文件，导入时用psql恢复。
  - ⬜增量备份: 仅备份修改过的文档和文件（节省空间）
- ⬜管理笔记、任务
- ⬜集成 AI 功能， AI 辅助（如自动生成报告摘要）
- ⬜实时数据看板，展示用户的各种数据，如 GitHub 活动、天气、新闻，并通过自动化脚本生成报告。用ECharts或D3.js在Web端展示数据趋势
- ⬜通过K8s的持久化存储（如PersistentVolume）来增强数据持久化（自动化备份方案：K8s CronJob配置）
- ⬜动态仪表盘
- （暂不考虑）实时聊天功能
- ⬜用户自定义主题，动态主题切换（暗黑/霓虹模式），“暗物质模式”：点击后界面切换为全黑 + 粒子特效（用 Flutter 的 `particles` 库）Flutter 动态主题（`MaterialColor` + `ThemeProvider`） 
- ⬜自动化报告生成（PDF 或 HTML）
- ⬜案例：[3D 地球渲染示例](https://github.com/fluttercommunity/flutter_earth)  
- ⬜任务管理应用，结合时间追踪和数据可视化
- ⬜支持Markdown、附件
- ⬜用户可以存储笔记、任务、文件，支持搜索、标签分类，支持存储多种数据类型：文本笔记、图片、文件、任务清单、联系信息等
- ⬜版本历史（记录每个文件的修改历史）（Git版本控制）
- ⬜数据分类与标签系统（支持多级标签分类），可以先搞基础标签系统（每个文件可添加多个标签）
- ⬜展示数据统计（如任务完成率、文件存储趋势、标签分布）
- ⬜实时搜索：输入时自动过滤数据（结合 `debounce` 优化性能）。
- ⬜支持选择备份文件上传并恢复（显示恢复进度），文件上传/下载：支持拖拽上传和进度条显示。
- ⬜用户注册/登录（可选，或使用 JWT 无状态认证）
- ⬜支持创建、编辑、分类、标签化的 Markdown 文档（如笔记、技术文档、项目记录）。
  - 内置实时预览、语法高亮、图片附件支持。
  - 支持上传任意文件（PDF、代码、图片），与文档关联。
  - 统计文档字数、分类分布、关键词热度（通过 Elasticsearch 或 PostgreSQL 全文搜索）
- （不考虑目前）数据库加密存储（使用 `pgcrypto` 或 `Dart` 的加密库）。
  - （不考虑目前）备份文件分片存储（如 AWS S3 或 MinIO 对象存储，但本地可简化为分目录存储）。
- ⬜通过`dart:io`调用Python编写的`transformers`模型生成笔记摘要 
- ⬜使用PostgreSQL `pg_vector`实现语义搜索  
- ⬜动态二维码生成
- ⬜用 Dart 编写脚本，自动将文档同步到 GitHub/GitLab（Markdown 文件托管）或生成 PDF 版本。

# 附录
符号：⬜✅🧠🌐🎛️⚡💡✨