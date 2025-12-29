# BMAD-METHOD Deep Dive

> 針對 [BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD) 框架的深度技術分析與研究文件

## 概述

本專案提供 BMAD-METHOD 框架的深入技術分析，以繁體中文撰寫，旨在幫助開發者和技術人員深入理解 BMAD 框架的內部運作機制、設計模式與實作細節。

### 什麼是 BMAD-METHOD？

BMAD-METHOD 是一個多代理 AI 協作框架，提供：
- 多個專業 AI 代理（Architect、Developer、PM 等）
- 結構化的工作流程（Workflow）系統
- Party Mode 多代理協作對話
- 完整的軟體開發生命週期支援

## 研究內容

### Party Mode Workflow 完整分析

**位置：** [`research/party-mode-analysis/`](./research/party-mode-analysis/)

Party Mode 是 BMAD 框架中的獨特互動式工作流程，能夠協調多個 AI 代理進行自然對話。

**分析內容包含：**

| 文件 | 分析重點 |
|------|----------|
| [workflow-analysis.md](./research/party-mode-analysis/workflow-analysis.md) | 主工作流程架構與設計模式 |
| [step-01-analysis.md](./research/party-mode-analysis/step-01-analysis.md) | 代理載入與初始化流程 |
| [step-02-analysis.md](./research/party-mode-analysis/step-02-analysis.md) | 多代理對話協調引擎 |
| [step-03-analysis.md](./research/party-mode-analysis/step-03-analysis.md) | 優雅退出與狀態清理 |
| [agent-manifest-analysis.md](./research/party-mode-analysis/agent-manifest-analysis.md) | 代理清單與人格定義 |
| [config-analysis.md](./research/party-mode-analysis/config-analysis.md) | 核心配置系統 |

**代理深度分析：**

| 代理 | 角色 | 分析連結 |
|------|------|----------|
| 🧙 BMad Master | 平台專家/協調者 | [bmad-master.md](./research/party-mode-analysis/agents/bmad-master.md) |
| 📊 Mary | Business Analyst | [analyst.md](./research/party-mode-analysis/agents/analyst.md) |
| 🏗️ Winston | Architect | [architect.md](./research/party-mode-analysis/agents/architect.md) |
| 💻 Amelia | Developer | [dev.md](./research/party-mode-analysis/agents/dev.md) |
| 📋 John | Product Manager | [pm.md](./research/party-mode-analysis/agents/pm.md) |
| 🚀 Barry | Quick Flow Solo Dev | [quick-flow-solo-dev.md](./research/party-mode-analysis/agents/quick-flow-solo-dev.md) |
| 🏃 Bob | Scrum Master | [sm.md](./research/party-mode-analysis/agents/sm.md) |
| 🧪 Murat | Test Architect | [tea.md](./research/party-mode-analysis/agents/tea.md) |
| 📚 Paige | Technical Writer | [tech-writer.md](./research/party-mode-analysis/agents/tech-writer.md) |
| 🎨 Sally | UX Designer | [ux-designer.md](./research/party-mode-analysis/agents/ux-designer.md) |

## 專案結構

```
bmad-docs/
├── README.md                      # 本文件
├── research/
│   └── party-mode-analysis/       # Party Mode 深度分析
│       ├── index.md               # 分析索引
│       ├── workflow-analysis.md   # 工作流程分析
│       ├── step-01-analysis.md    # 步驟 1 分析
│       ├── step-02-analysis.md    # 步驟 2 分析
│       ├── step-03-analysis.md    # 步驟 3 分析
│       ├── config-analysis.md     # 配置分析
│       ├── agent-manifest-analysis.md  # 代理清單分析
│       └── agents/                # 各代理深度分析
│           ├── bmad-master.md
│           ├── analyst.md
│           ├── architect.md
│           ├── dev.md
│           ├── pm.md
│           ├── quick-flow-solo-dev.md
│           ├── sm.md
│           ├── tea.md
│           ├── tech-writer.md
│           └── ux-designer.md
└── _bmad/                         # BMAD 框架安裝（用於實際測試）
```

## 關鍵發現

### 設計模式

1. **Micro-file Architecture** - 每個步驟獨立成檔，遵循單一職責原則
2. **Frontmatter State Tracking** - 使用 YAML frontmatter 追蹤工作流程狀態
3. **Intelligent Agent Selection** - 根據主題分析自動選擇 2-3 個最相關代理
4. **Character Consistency** - 嚴格遵循代理人格設定

### Party Mode 流程

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│   Step 1     │     │   Step 2     │     │   Step 3     │
│ Agent Loading│──▶  │ Discussion   │──▶  │ Graceful     │
│              │     │ Orchestration│     │ Exit         │
└──────────────┘     └──────────────┘     └──────────────┘
```

## 參考資源

- [BMAD-METHOD GitHub](https://github.com/bmad-code-org/BMAD-METHOD)
- [Party Mode 官方文件](https://github.com/bmad-code-org/BMAD-METHOD/blob/main/docs/modules/bmm-bmad-method/party-mode.md)

## 授權

本研究文件僅供學習與研究用途。BMAD-METHOD 框架的原始授權請參閱其官方倉庫。
