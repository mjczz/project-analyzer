# Project Analyzer - Path Guide

## 🎯 Core Principle

**Analysis documents are ALWAYS saved inside the `ai-analysis-docs/` directory of the project being analyzed**

## 📁 Directory Structure Rules

### Correct Path Structure

```
[project being analyzed]/
├── [project's original files and directories]
├── [other project files]
└── ai-analysis-docs/              ← Analysis documents created here
    ├── changelog.md
    ├── [project-name]-analysis.md
    ├── [project-name]-progress-tracking.md
    ├── analysis-todo.md
    ├── topics/
    │   ├── 01-project-basic-info.md
    │   ├── 02-project-structure.md
    │   └── ...
    └── assets/
```

## 📍 Specific Examples

### Example 1: Analyzing Kubernetes Project

**User Command**: `Analyze /Users/ccc/work/todo/kubernetes`

**Document Save Location**:
```
/Users/ccc/work/todo/kubernetes/ai-analysis-docs/
├── changelog.md
├── kubernetes-analysis.md
├── kubernetes-progress-tracking.md
├── analysis-todo.md
├── topics/
│   ├── 01-project-basic-info.md
│   ├── 02-project-structure.md
│   └── ...
└── assets/
```

### Example 2: Analyzing Current Directory

**User Command**: `Analyze .` or `Analyze current directory`

**Document Save Location**:
```
./ai-analysis-docs/
├── changelog.md
├── [current-directory-name]-analysis.md
├── [current-directory-name]-progress-tracking.md
├── analysis-todo.md
├── topics/
└── assets/
```

### Example 3: Analyzing Relative Path Project

**User Command**: `Analyze ../my-project`

**Document Save Location**:
```
../my-project/ai-analysis-docs/
├── changelog.md
├── my-project-analysis.md
├── my-project-progress-tracking.md
├── analysis-todo.md
├── topics/
└── assets/
```

## ❌ Incorrect Examples

### Don't use paths like these:

```
❌ /Users/ccc/.openclaw/workspace/[project-name]/ai-analysis-docs/
❌ ~/analysis-results/[project-name]/
❌ /tmp/analysis/[project-name]/
❌ [any other location outside the project]
```

## ✅ Correct Examples

### Should use paths like these:

```
✅ /Users/ccc/work/todo/kubernetes/ai-analysis-docs/
✅ ./ai-analysis-docs/ (current directory)
✅ ../my-project/ai-analysis-docs/ (relative path)
✅ [project-path]/ai-analysis-docs/ (generic form)
```

## 🔍 Path Resolution Rules

### Absolute Path
- Input: `/Users/ccc/work/todo/kubernetes`
- Output: `/Users/ccc/work/todo/kubernetes/ai-analysis-docs/`

### Relative Path
- Input: `./my-project`
- Output: `./my-project/ai-analysis-docs/`

### Current Directory
- Input: `.` or `current directory`
- Output: `./ai-analysis-docs/`

## 🎯 Why This Design?

### 1. **Strong Project Association**
Analysis documents are closely associated with the project, saving them inside the project facilitates:
- Project version control
- Team sharing of analysis results
- Analysis and code synchronous updates

### 2. **Easy Management**
- One project, one analysis directory
- Analysis results move with the project
- Analysis documents automatically deleted when project is deleted

### 3. **Version Control Friendly**
- Can add analysis documents to Git
- Analysis history managed together with project history
- Team collaboration can share analysis insights

### 4. **Clean Paths**
- No need for additional workspace directories
- Analysis documents always relative to project location
- Reduces possibility of path confusion

## 📝 Implementation Notes

### When Creating Directories
```bash
# Ensure creating inside the project being analyzed
mkdir -p [project-path]/ai-analysis-docs/topics
mkdir -p [project-path]/ai-analysis-docs/assets
```

### When Saving Files
```bash
# All files saved inside the project
changelog_path = "[project-path]/ai-analysis-docs/changelog.md"
main_report_path = "[project-path]/ai-analysis-docs/[project-name]-analysis.md"
topics_dir = "[project-path]/ai-analysis-docs/topics/"
```

### When Reporting Paths
```bash
# When reporting to users, use full paths
echo "Analysis files saved: [project-path]/ai-analysis-docs/[project-name]-analysis.md"
```

## 🔄 Migration Guide

If you previously used other path structures, you can migrate as follows:

### Old Structure → New Structure
```
Old: /Users/ccc/.openclaw/workspace/kubernetes/ai-analysis-docs/
New: /Users/ccc/work/todo/kubernetes/ai-analysis-docs/

Migration Commands:
mv /Users/ccc/.openclaw/workspace/kubernetes/ai-analysis-docs/ \
   /Users/ccc/work/todo/kubernetes/ai-analysis-docs/
```

## 💡 Best Practices

1. **Consistency**: Always save analysis documents in the `ai-analysis-docs/` directory inside the project
2. **Ignore Rules**: Consider whether to ignore analysis documents in the project's `.gitignore`
3. **Team Sharing**: If the team shares analysis results, add analysis documents to version control
4. **Regular Cleanup**: Analysis documents are deleted when the project is deleted

---

*This document ensures all analysis documents are saved in the correct location, which is the ai-analysis-docs/ directory inside the project being analyzed*