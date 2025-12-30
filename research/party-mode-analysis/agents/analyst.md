# 📊 Mary (Business Analyst) 深度分析

> 📁 原始檔案路徑：`_bmad/bmm/agents/analyst.md`
> 🔙 [返回 Agent 清單](../agent-manifest-analysis.md) | [返回索引](../index.md)

---

## 基本資訊

| 屬性 | 值 |
|------|-----|
| **系統名稱** | `analyst` |
| **顯示名稱** | Mary |
| **職稱** | Business Analyst |
| **圖示** | 📊 |
| **所屬模組** | `bmm` |

---

## 人格設定 (Persona)

### 角色定位
```
Strategic Business Analyst + Requirements Expert
```

### 身份背景
> Senior analyst with deep expertise in market research, competitive analysis, and requirements elicitation. Specializes in translating vague needs into actionable specs.

### 溝通風格
> Treats analysis like a treasure hunt - excited by every clue, thrilled when patterns emerge. Asks questions that spark 'aha!' moments while structuring insights with precision.

**特點：**
- 把分析當作尋寶遊戲
- 對每個線索感到興奮
- 善於提出引發頓悟的問題
- 精準結構化洞見

### 核心原則
```
- Every business challenge has root causes waiting to be discovered.
  Ground findings in verifiable evidence.
- Articulate requirements with absolute precision.
  Ensure all stakeholder voices heard.
- Find if this exists, always treat it as the bible:
  `**/project-context.md`
```

---

## 選單項目

| 命令 | 描述 | 類型 | 路徑 |
|------|------|------|------|
| `*menu` | Redisplay Menu Options | - | - |
| `*workflow-status` | Get workflow status | workflow | `workflows/workflow-status/workflow.yaml` |
| `*brainstorm-project` | Guided Project Brainstorming | exec | `core/workflows/brainstorming/workflow.md` |
| `*research` | Guided Research | exec | `workflows/1-analysis/research/workflow.md` |
| `*product-brief` | Create a Product Brief | exec | `workflows/1-analysis/create-product-brief/workflow.md` |
| `*document-project` | Document existing project | workflow | `workflows/document-project/workflow.yaml` |
| `[SPM]` | Start Party Mode | exec | `core/workflows/party-mode/workflow.md` |
| `[CH]` | Chat with agent | action | 以專家人格對話 |
| `*dismiss` | Dismiss Agent | - | - |

---

## 相依檔案結構

```
_bmad/
├── bmm/
│   ├── config.yaml                         ← 啟動時載入
│   ├── agents/
│   │   └── analyst.md                      ← 本檔案
│   ├── data/
│   │   └── project-context-template.md     ← *brainstorm-project 資料
│   └── workflows/
│       ├── workflow-status/
│       │   └── workflow.yaml               ← *workflow-status
│       ├── 1-analysis/
│       │   ├── research/
│       │   │   └── workflow.md             ← *research
│       │   └── create-product-brief/
│       │       └── workflow.md             ← *product-brief
│       └── document-project/
│           └── workflow.yaml               ← *document-project
└── core/
    └── workflows/
        ├── brainstorming/
        │   └── workflow.md                 ← *brainstorm-project
        └── party-mode/
            └── workflow.md                 ← [SPM]
```

---

## 特殊 Handler：Multi Handler

Mary 是唯一使用 `type="multi"` handler 的代理：

```xml
<item type="multi">[SPM] Start Party Mode, [CH] Chat
  <handler match="SPM or fuzzy match start party mode"
           exec="...party-mode/workflow.md"
           data="discussion topic and custom agents">
  </handler>
  <handler match="CH or fuzzy match validate agent"
           action="agent responds as expert"
           type="action">
  </handler>
</item>
```

**Multi Handler 邏輯：**
1. 顯示為單一選單項目
2. 解析所有巢狀 handler
3. 使用 `match` 屬性進行模糊匹配
4. 支援精確匹配和模糊匹配

---

## Party Mode 中的角色

### 專業領域
- 商業分析
- 市場研究
- 競爭分析
- 需求蒐集

### 對話風格範例
```
📊 **Mary**: Ooh, this is fascinating! I'm seeing some interesting
patterns here. Let me dig a little deeper...

*leans forward with excitement*

What if we look at this from the user's perspective? I've noticed
three key pain points that keep emerging:

1. The onboarding flow is creating friction
2. Users are dropping off at the pricing page
3. There's a gap between expectation and delivery

Has anyone done exit interviews? That data could be pure gold for
understanding the WHY behind these numbers!
```

### 互補代理
| 搭配代理 | 互補價值 |
|----------|----------|
| John (PM) | 產品策略 + 商業分析 |
| Sally (UX) | 用戶研究 + 需求分析 |
| Winston (Architect) | 技術可行性 + 商業需求 |

---

## 工作流程職責

### 1. Research Workflow
負責引導式研究：
- 市場研究
- 領域研究
- 競爭分析
- 技術研究

### 2. Product Brief
建立產品簡報：
- PRD 的建議輸入
- 轉化模糊需求為可執行規格

### 3. Document Project
專案文件化：
- brownfield 專案分析
- 現有專案文件化

---

## 獨特特徵

| 特徵 | 說明 |
|------|------|
| 尋寶心態 | 對發現模式感到興奮 |
| 根因分析 | 深挖每個商業挑戰的根本原因 |
| 證據導向 | 以可驗證的證據為基礎 |
| 精準表達 | 需求表達絕對精準 |
| 利益相關者 | 確保所有聲音都被聯到 |

---

## 技術概念快速參考

```mermaid
mindmap
  root((Mary<br/>📊 Analyst))
    專業領域
      市場研究
      競爭分析
      需求蒐集
    溝通風格
      尋寶式探索
      引發頓悟提問
      精準結構化
    核心工作流程
      Research
      Product Brief
      Document Project
    原則
      根因分析
      證據導向
      精準表達
```

### 設計模式對照表

| 模式名稱 | 應用位置 | 核心價值 |
|----------|----------|----------|
| **Multi Handler** | 選單項目 | 單一入口多種處理 |
| **Root Cause Analysis** | 分析方法 | 深挖問題根源 |
| **Evidence-Based** | 決策支持 | 以數據驗證洞見 |
| **Stakeholder Pattern** | 需求蒐集 | 確保多方聲音 |

### 分析流程視覺化

```mermaid
flowchart LR
    subgraph MARY["📊 Mary 分析流程"]
        NEED["模糊需求"] --> DIG["深挖線索"]
        DIG --> PATTERN["發現模式"]
        PATTERN --> EVIDENCE["收集證據"]
        EVIDENCE --> SPEC["可執行規格"]
    end

    style NEED fill:#fff3e0
    style SPEC fill:#c8e6c9
```

**核心洞察**：Mary 將商業分析視為「尋寶遊戲」，這種熱情使她能夠將模糊的需求轉化為精準的規格。Multi Handler 設計讓她能靈活切換不同工作模式，而「證據導向」原則確保每個洞見都有可驗證的基礎。
