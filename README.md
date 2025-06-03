# NeuronHub
🧠Your Personal Data Nexus – Where Intelligence Meets Convenience

💡您的个人数据中心——智慧与便捷在此相遇

🚧 施工中！
（开发进度：0.03% | 预计完工：等我秃了再说）

## 技术栈
- Dart 后端（shelf 或其它框架）
- Flutter 前端
- PostgreSQL 数据库
- Nginx 代理
- Docker 和 MicroK8s 部署
## 任务进度
### 1. 基础架构搭建
- ⬜ **Dart + Flutter 核心功能实现**
  - ⬜使用 Dart 和 Flutter 搭建最简陋的界面，支持以下核心功能：
    - ⬜用户注册/登录（可选，或使用 JWT 无状态认证）
    - ⬜创建、编辑、分类、标签化的 Markdown 文档
    - ⬜支持搜索、标签分类
    - ⬜支持存储文本笔记、图片、文件、任务清单
- ⬜ **本地运行测试**
  - ⬜确保应用能在本地跑起来，核心功能可用
- ⬜ **Docker 镜像打包**
  - ⬜根据所属功能包的不同打包为不同的镜像
  - ⬜确保镜像能在 Docker 中运行正常
- ⬜ **部署到 MicroK8s**
  - ⬜将 Docker 镜像部署到 MicroK8s，确保服务正常运行

### 2. 数据存储与同步
- ⬜ **PostgreSQL 数据库集成**
  - ⬜使用 PostgreSQL 存储用户数据、文档、任务等
- ⬜ **版本历史（Git 版本控制）**
  - ⬜记录每个文件的修改历史
- ⬜ **实时数据同步**
  - ⬜在手机（Flutter 前端）和电脑同时编辑同一文档，跨平台实时同步
- ⬜ **自动化备份**
  - ⬜备份功能集成到应用内，一键导出/导入
  - ⬜定期生成数据库备份（定期备份功能）
  - ⬜增量备份：仅备份修改过的文档和文件（节省空间）
  - ⬜备份文件上传/下载：支持拖拽上传和进度条显示

### 3. 数据可视化与看板
- ⬜ **数据可视化用图表库**
  - ⬜使用 `flutter/material` 的 `DataTable` 和 `ECharts`（通过 `echarts_flutter` 包）实现数据可视化
  - ⬜使用 **Fluent UI** 或 **D3.js** 在 Flutter 前端生成数据看板（文档更新趋势、关键词云、文档关联图谱）
  - ⬜Flutter 动态图表（class ChartWidget）（使用 `fl_chart` 实现数据可视化）
- ⬜ **实时数据看板**
  - ⬜展示用户的各种数据，如 GitHub 活动、天气、新闻
  - ⬜通过自动化脚本生成报告
  - ⬜用 ECharts 或 D3.js 在 Web 端展示数据趋势
- ⬜ **动态仪表盘**
  - ⬜支持动态更新的数据仪表盘

### 4. 用户界面与体验
- ⬜ **现代 UI 如 Flutter 的动画效果**
  - ⬜[Flutter 动态粒子效果](https://pub.dev/packages/particles)
- ⬜ **用户自定义主题，动态主题切换**
  - ⬜暗/霓虹模式
  - ⬜“暗物质模式”：点击后界面切换为全黑 + 粒子特效（用 Flutter 的 `particles` 库）
  - ⬜Flutter 动态主题（`MaterialColor` + `ThemeProvider`）
- ⬜ **实时搜索**
  - ⬜输入时自动过滤数据（结合 `debounce` 优化性能）

### 5. 高级功能与集成
- ⬜ **多人实时协作**
  - ⬜支持多人同时编辑同一文档
- ⬜ **集成 AI 功能，AI 辅助**
  - ⬜自动生成报告摘要
  - ⬜通过 `dart:io` 调用 Python 编写的 `transformers` 模型生成笔记摘要
- ⬜ **语义搜索**
  - ⬜使用 PostgreSQL `pg_vector` 实现语义搜索
- ⬜ **自动化报告生成**
  - ⬜PDF 或 HTML 格式
- ⬜ **动态二维码生成**
- ⬜ **任务管理应用**
  - ⬜结合时间追踪和数据可视化
- ⬜ **支持 Markdown、附件**
  - ⬜内置实时预览、语法高亮、图片附件支持
  - ⬜支持上传任意文件（PDF、代码、图片），与文档关联
  - ⬜统计文档字数、分类分布、关键词热度（通过 Elasticsearch 或 PostgreSQL 全文搜索）
- ⬜ **数据统计**
  - ⬜展示任务完成率、文件存储趋势、标签分布
- ⬜ **案例：[3D 地球渲染示例](https://github.com/fluttercommunity/flutter_earth)**
  - ⬜增加炫酷的 3D 地球渲染功能，展示数据分布等

### 6. 扩展功能（可选）
- ⬜ **数据库加密存储**
  - ⬜使用 `pgcrypto` 或 `Dart` 的加密库
- ⬜ **备份文件分片存储**
  - ⬜如 AWS S3 或 MinIO 对象存储，但本地可简化为分目录存储
- ⬜ **支持云存储（如 Dropbox、Google Drive）**
- ⬜ **实时聊天功能**
- ⬜ **通过 `dart:io` 编写脚本，自动将文档同步到 GitHub/GitLab（Markdown 文件托管）或生成 PDF 版本**

## 附录
符号：⬜✅🧠🌐🎛️⚡💡✨