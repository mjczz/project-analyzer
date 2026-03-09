# project-analyzer

A comprehensive open source project analysis skill for OpenClaw agents.

## Features

- 📋 12-step complete analysis process + 8-step deep analysis option
- 🔬 Three analysis modes: Quick Assessment, Standard Analysis, Deep Dive
- 📊 Mermaid visualization diagrams (architecture diagrams, flowcharts, dependency diagrams, etc.)
- 💻 Local project analysis support (no GitHub API required)
- 💻 Source code-level deep analysis capability (function call chains, data structures, implementation mechanisms)
- 📈 **Progressive Documentation Creation**: Create independent documents for each topic immediately
- 📁 **Structured File Organization**: Automatically generate project directories and categorized files
- 🔄 **Real-time Progress Tracking**: View analysis progress and status at any time
- 📝 **Change Log Recording**: Automatically record all document creation activities
- 💾 **Incremental Save Mechanism**: Prevent data loss and ensure content safety
- 🎯 Systematic analysis framework based on Kubernetes analysis methodology

## Use Cases

### Quick Assessment Mode
- Quick project overview understanding
- Technical selection decisions
- Preliminary quality assessment

### Standard Analysis Mode
- Analyze open source project architecture
- Evaluate GitHub repository quality
- Understand tech stack and dependencies
- Learn excellent code organization practices

### Deep Analysis Mode
- Source code-level mechanism dissection
- Performance and security analysis
- Implementation details and best practices
- Technical in-depth research

## Usage

When users ask to analyze an open source project (e.g., "analyze facebook/react"), the skill will automatically:

1. Create structured project directories
2. Analyze each topic step by step (create and save each topic document immediately upon completion)
3. Create independent documents for each topic
4. Update progress tracking documents in real-time
5. Generate visualization diagrams
6. Integrate main comprehensive reports
7. Provide complete project analysis documentation suite

### 📁 Generated Documentation Structure

```
[project-name]/
└── ai-analysis-docs/                   # Unified storage for all analysis documents
    ├── changelog.md                   # Analysis change log ✨
    ├── [project-name]-analysis.md     # Main comprehensive report
    ├── [project-name]-progress-tracking.md  # Real-time progress tracking
    ├── analysis-todo.md               # Analysis TODO list
    ├── topics/                        # 12-20 independent topic documents
    │   ├── 01-project-basic-info.md
    │   ├── 02-project-structure.md
    │   └── ...
    └── assets/                        # Diagrams and resources
        ├── diagrams/
        └── images/
```

## Analysis Topics

### Standard Analysis (12 Topics)
1. 📋 Project Basic Information
2. 🏗️ Project Structure
3. 🛠️ Tech Stack
4. 🎯 Core Features
5. 🏛️ Architecture Design
6. 📊 Code Quality
7. 📚 Documentation Quality
8. 📈 Project Activity
9. ✅ Strengths/Weaknesses
10. 🎯 Use Cases
11. 💡 Learning Value
12. 📝 Summary

### Deep Analysis (Additional 8 Topics)
13. 🔧 Source Code Deep Dive
14. ⚙️ Implementation Mechanics Analysis
15. 🔍 Key Component Analysis
16. 📐 Protocol & Interface Analysis
17. 🚀 Workflow Tracing
18. 🛡️ Security Analysis
19. ⚡ Performance Analysis
20. 🧪 Testing Strategy Analysis

## Installation

Install via OpenClaw skills CLI:

```bash
npx skills add [your-username]/project-analyzer
```

Or manual installation:

```bash
# Clone to skills directory
git clone https://github.com/[your-username]/project-analyzer ~/.openclaw/skills/project-analyzer

# Or
git clone https://github.com/[your-username]/project-analyzer ~/.agents/skills/project-analyzer
```

## File Structure

```
project-analyzer/
├── SKILL.md                    # Skill definition and usage guide
├── TEMPLATE.md                 # Analysis template (standard + deep analysis)
├── CHANGELOG_TEMPLATE.md       # Change log template ✨
├── WORKFLOW.md                 # Progressive analysis workflow
├── DOCUMENTATION_GUIDELINES.md # Documentation organization standards and naming conventions
├── EXAMPLE_WORKFLOW.md         # Progressive documentation creation examples
├── INTEGRATION_SUMMARY.md      # Kubernetes analysis methodology integration summary
├── README.md                   # This file
└── .gitignore
```

## Related Skills

- `github` - GitHub API access
- `pretty-mermaid` - Mermaid diagram rendering
- `coding-router` - Deep code architecture analysis

## Analysis Methodology

This skill adopts a systematic analysis methodology inspired by the Kubernetes source code analysis framework:

- **From Architecture to Implementation**: Understand overall architecture first, then dive into code implementation
- **Flow-Driven**: Understand code paths through actual workflows
- **Visual + Code**: Mermaid diagrams + code annotations
- **Continuable**: Provide guides and templates for continued analysis
- **Practice-Oriented**: Include configuration examples and troubleshooting guides

See `WORKFLOW.md` for complete analysis workflow guidance.

## License

MIT

## Author

Created by [Your Name]

---

*Project creation time: 2026-03-09*