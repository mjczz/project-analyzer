# project-analyzer

A comprehensive open source project analysis skill for OpenClaw agents.

## 功能特性

- 📋 12 步完整分析流程
- 📊 Mermaid 可视化图表（架构图、流程图、依赖图等）
- 🔍 GitHub API 集成（自动获取 star、结构、活跃度）
- 📈 进度汇报机制（每个主题完成后汇报 X/12）
- 💾 自动保存分析结果

## 适用场景

- 分析开源项目架构
- 评估 GitHub 仓库质量
- 理解技术栈和依赖关系
- 学习优秀的代码组织方式

## 使用方法

当用户要求分析开源项目时（如"分析 facebook/react"），skill 会自动：

1. 读取分析模板
2. 收集项目信息（通过 GitHub API）
3. 逐个主题分析并汇报进度
4. 生成可视化图表
5. 保存完整的分析报告

## 分析主题

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

## 相关 Skills

- `github` - GitHub API 访问
- `pretty-mermaid` - Mermaid 图表渲染
- `coding-router` - 代码架构深度分析

## License

MIT

## 作者

Created by [Your Name]

---

*项目创建时间：2026-03-09*
