# project-analyzer

A comprehensive open source project analysis skill for OpenClaw agents.

## 功能特性

- 📋 12 步完整分析流程 + 8 步深度分析选项
- 🔬 三种分析模式：快速评估、标准分析、深度剖析
- 📊 Mermaid 可视化图表（架构图、流程图、依赖图等）
- 🔍 GitHub API 集成（自动获取 star、结构、活跃度）
- 💻 源码级深度分析能力（函数调用链、数据结构、实现机制）
- 📈 **渐进式文档创建**：每个主题立即创建独立文档
- 📁 **结构化文件组织**：自动生成项目目录和分类文件
- 🔄 **实时进度追踪**：随时查看分析进度和状态
- 💾 **增量保存机制**：防止数据丢失，确保内容安全
- 🎯 基于 Kubernetes 分析方法论的系统化分析框架

## 适用场景

### 快速评估模式
- 快速了解项目概况
- 技术选型决策
- 初步质量评估

### 标准分析模式
- 分析开源项目架构
- 评估 GitHub 仓库质量
- 理解技术栈和依赖关系
- 学习优秀的代码组织方式

### 深度分析模式
- 源码级机制剖析
- 性能和安全性分析
- 实现细节和最佳实践
- 技术深度研究

## 使用方法

当用户要求分析开源项目时（如"分析 facebook/react"），skill 会自动：

1. 创建结构化项目目录
2. 逐个主题进行分析（每个主题完成后立即保存）
3. 为每个主题创建独立文档
4. 实时更新进度追踪文档
5. 生成可视化图表
6. 整合主综合报告
7. 提供完整的项目分析文档套件

### 📁 生成的文档结构

```
[project-name]/
└── ai-analysis-docs/                   # 所有分析文档统一存放
    ├── [project-name]-分析.md         # 主综合报告
    ├── [project-name]-进度追踪.md     # 实时进度追踪
    ├── analysis-todo.md               # 分析待办清单
    ├── topics/                        # 12-20个独立主题文档
    │   ├── 01-项目基本信息.md
    │   ├── 02-项目结构.md
    │   └── ...
    └── assets/                        # 图表和资源
        ├── diagrams/
        └── images/
```

## 分析主题

### 标准分析 (12 主题)
1. 📋 项目基本信息
2. 🏗️ 项目结构
3. 🛠️ 技术栈
4. 🎯 核心功能
5. 🏛️ 架构设计
6. 📊 代码质量
7. 📚 文档质量
8. 📈 项目活跃度
9. ✅ 优点/缺点
10. 🎯 适用场景
11. 💡 学习价值
12. 📝 总结

### 深度分析 (附加 8 主题)
13. 🔧 源码深度分析
14. ⚙️ 实现机制剖析
15. 🔍 关键组件解析
16. 📐 协议与接口分析
17. 🚀 工作流程追踪
18. 🛡️ 安全性分析
19. ⚡ 性能分析
20. 🧪 测试策略分析

## 安装

通过 OpenClaw skills CLI 安装：

```bash
npx skills add [your-username]/project-analyzer
```

或手动安装：

```bash
# 克隆到 skills 目录
git clone https://github.com/[your-username]/project-analyzer ~/.openclaw/skills/project-analyzer

# 或
git clone https://github.com/[your-username]/project-analyzer ~/.agents/skills/project-analyzer
```

## 文件结构

```
project-analyzer/
├── SKILL.md                    # Skill 定义和使用指南
├── TEMPLATE.md                 # 分析模板（标准 + 深度分析）
├── WORKFLOW.md                 # 渐进式分析工作流程
├── DOCUMENTATION_GUIDELINES.md # 文档组织规范和命名约定
├── EXAMPLE_WORKFLOW.md         # 渐进式文档创建示例
├── INTEGRATION_SUMMARY.md      # Kubernetes 分析方法论整合总结
├── README.md                   # 本文件
└── .gitignore
```

## 相关 Skills

- `github` - GitHub API 访问
- `pretty-mermaid` - Mermaid 图表渲染
- `coding-router` - 代码架构深度分析

## 分析方法论

本 skill 采用系统化的分析方法论，灵感来源于 Kubernetes 源码分析框架：

- **从架构到实现**: 先理解整体架构，再深入代码实现
- **流程驱动**: 通过实际工作流程理解代码路径
- **图文并茂**: Mermaid 图表 + 代码注释
- **可延续性**: 提供继续分析的指南和模板
- **实战导向**: 包含配置示例和故障排查

详见 `WORKFLOW.md` 获取完整的分析工作流程指导。

## License

MIT

## 作者

Created by [Your Name]

---

*项目创建时间：2026-03-09*
