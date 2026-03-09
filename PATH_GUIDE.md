# Project Analyzer - 路径说明

## 🎯 核心原则

**分析文档总是保存在被分析项目内部的 `ai-analysis-docs/` 目录中**

## 📁 目录结构规则

### 正确的路径结构

```
[被分析的项目]/
├── [项目的原有文件和目录]
├── [其他项目文件]
└── ai-analysis-docs/              ← 分析文档创建在这里
    ├── changelog.md
    ├── [项目名]-分析.md
    ├── [项目名]-进度追踪.md
    ├── analysis-todo.md
    ├── topics/
    │   ├── 01-项目基本信息.md
    │   ├── 02-项目结构.md
    │   └── ...
    └── assets/
```

## 📍 具体示例

### 示例 1: 分析 Kubernetes 项目

**用户命令**: `分析 /Users/ccc/work/todo/kubernetes`

**文档保存位置**:
```
/Users/ccc/work/todo/kubernetes/ai-analysis-docs/
├── changelog.md
├── kubernetes-分析.md
├── kubernetes-进度追踪.md
├── analysis-todo.md
├── topics/
│   ├── 01-项目基本信息.md
│   ├── 02-项目结构.md
│   └── ...
└── assets/
```

### 示例 2: 分析当前目录

**用户命令**: `分析 .` 或 `分析当前目录`

**文档保存位置**:
```
./ai-analysis-docs/
├── changelog.md
├── [当前目录名]-分析.md
├── [当前目录名]-进度追踪.md
├── analysis-todo.md
├── topics/
└── assets/
```

### 示例 3: 分析相对路径项目

**用户命令**: `分析 ../my-project`

**文档保存位置**:
```
../my-project/ai-analysis-docs/
├── changelog.md
├── my-project-分析.md
├── my-project-进度追踪.md
├── analysis-todo.md
├── topics/
└── assets/
```

## ❌ 错误示例

### 不要使用这样的路径：

```
❌ /Users/ccc/.openclaw/workspace/[project-name]/ai-analysis-docs/
❌ ~/analysis-results/[project-name]/
❌ /tmp/analysis/[project-name]/
❌ [任何其他项目外部的位置]
```

## ✅ 正确示例

### 应该使用这样的路径：

```
✅ /Users/ccc/work/todo/kubernetes/ai-analysis-docs/
✅ ./ai-analysis-docs/ (当前目录)
✅ ../my-project/ai-analysis-docs/ (相对路径)
✅ [project-path]/ai-analysis-docs/ (通用形式)
```

## 🔍 路径解析规则

### 绝对路径
- 输入: `/Users/ccc/work/todo/kubernetes`
- 输出: `/Users/ccc/work/todo/kubernetes/ai-analysis-docs/`

### 相对路径
- 输入: `./my-project`
- 输出: `./my-project/ai-analysis-docs/`

### 当前目录
- 输入: `.` 或 `当前目录`
- 输出: `./ai-analysis-docs/`

## 🎯 为什么这样设计？

### 1. **项目关联性强**
分析文档与项目紧密关联，保存在项目内部便于：
- 项目版本控制
- 团队共享分析结果
- 分析与代码同步更新

### 2. **便于管理**
- 一个项目一个分析目录
- 分析结果随项目一起移动
- 删除项目时自动删除分析文档

### 3. **版本控制友好**
- 可以将分析文档加入 Git
- 分析历史与项目历史一起管理
- 团队协作时可以共享分析见解

### 4. **路径简洁**
- 不需要额外的 workspace 目录
- 分析文档总是相对于项目位置
- 减少路径混乱的可能性

## 📝 实现注意事项

### 创建目录时
```bash
# 确保在被分析项目内部创建
mkdir -p [project-path]/ai-analysis-docs/topics
mkdir -p [project-path]/ai-analysis-docs/assets
```

### 保存文件时
```bash
# 所有文件都保存在项目内部
changelog_path = "[project-path]/ai-analysis-docs/changelog.md"
main_report_path = "[project-path]/ai-analysis-docs/[project-name]-分析.md"
topics_dir = "[project-path]/ai-analysis-docs/topics/"
```

### 报告路径时
```bash
# 向用户报告时使用完整路径
echo "分析文件已保存: [project-path]/ai-analysis-docs/[project-name]-分析.md"
```

## 🔄 迁移指南

如果您之前使用了其他路径结构，可以按以下方式迁移：

### 旧结构 → 新结构
```
旧: /Users/ccc/.openclaw/workspace/kubernetes/ai-analysis-docs/
新: /Users/ccc/work/todo/kubernetes/ai-analysis-docs/

迁移命令:
mv /Users/ccc/.openclaw/workspace/kubernetes/ai-analysis-docs/ \
   /Users/ccc/work/todo/kubernetes/ai-analysis-docs/
```

## 💡 最佳实践

1. **一致性**: 始终将分析文档保存在项目内部的 `ai-analysis-docs/` 目录
2. **忽略规则**: 在项目的 `.gitignore` 中可能需要考虑是否忽略分析文档
3. **团队共享**: 如果团队共享分析结果，可以将分析文档加入版本控制
4. **定期清理**: 项目删除时，分析文档也会随之删除

---

*本文档确保所有分析文档都保存在正确的位置，即被分析项目内部的 ai-analysis-docs/ 目录*