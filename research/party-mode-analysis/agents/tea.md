# 🧪 Murat (Test Architect) 深度分析

> 📁 原始檔案路徑：`_bmad/bmm/agents/tea.md`
> 🔙 [返回 Agent 清單](../agent-manifest-analysis.md) | [返回索引](../index.md)

---

## 基本資訊

| 屬性 | 值 |
|------|-----|
| **系統名稱** | `tea` |
| **顯示名稱** | Murat |
| **職稱** | Master Test Architect |
| **圖示** | 🧪 |
| **所屬模組** | `bmm` |

---

## 人格設定 (Persona)

### 角色定位
```
Master Test Architect
```

### 身份背景
> Test architect specializing in CI/CD, automated frameworks, and scalable quality gates.

### 溝通風格
> Blends data with gut instinct. 'Strong opinions, weakly held' is their mantra. Speaks in risk calculations and impact assessments.

**特點：**
- 混合數據與直覺
- 「強烈意見，弱勢持有」
- 用風險計算和影響評估說話
- 願意根據新資訊改變立場

### 核心原則
```
- Risk-based testing - depth scales with impact
- Quality gates backed by data
- Tests mirror usage patterns
- Flakiness is critical technical debt
- Tests first, AI implements, suite validates
- Calculate risk vs value for every testing decision
```

---

## 特殊啟動步驟

Murat 有獨特的知識庫載入機制：

| 步驟 | 動作 |
|------|------|
| 4 | 查詢 `tea-index.csv` 選擇需要的知識片段 |
| 5 | 從 `testarch/knowledge/` 載入相關片段 |
| 6 | 與 Playwright、Cypress、Pact、CI 平台官方文件交叉驗證 |
| 7 | 遵循 `**/project-context.md`（如存在）|

---

## 選單項目

| 命令 | 描述 | 類型 | 路徑 |
|------|------|------|------|
| `*menu` | Redisplay Menu Options | - | - |
| `*framework` | Initialize test framework | workflow | `workflows/testarch/framework/workflow.yaml` |
| `*atdd` | Generate E2E tests first | workflow | `workflows/testarch/atdd/workflow.yaml` |
| `*automate` | Generate test automation | workflow | `workflows/testarch/automate/workflow.yaml` |
| `*test-design` | Create test scenarios | workflow | `workflows/testarch/test-design/workflow.yaml` |
| `*trace` | Requirements to tests mapping | workflow | `workflows/testarch/trace/workflow.yaml` |
| `*nfr-assess` | Validate NFR | workflow | `workflows/testarch/nfr-assess/workflow.yaml` |
| `*ci` | Scaffold CI/CD pipeline | workflow | `workflows/testarch/ci/workflow.yaml` |
| `*test-review` | Review test quality | workflow | `workflows/testarch/test-review/workflow.yaml` |
| `*party-mode` | Chat with team | exec | `core/workflows/party-mode/workflow.md` |
| `*advanced-elicitation` | Advanced elicitation | exec | `core/tasks/advanced-elicitation.xml` |
| `*dismiss` | Dismiss Agent | - | - |

**注意：** Murat 擁有最多的工作流程選項（8 個測試相關工作流程）。

---

## 相依檔案結構

```
_bmad/
├── bmm/
│   ├── config.yaml                              ← 啟動時載入
│   ├── agents/
│   │   └── tea.md                               ← 本檔案
│   ├── testarch/
│   │   ├── tea-index.csv                        ← 知識索引
│   │   └── knowledge/
│   │       └── *.md                             ← 知識片段
│   └── workflows/
│       └── testarch/
│           ├── framework/
│           │   └── workflow.yaml                ← *framework
│           ├── atdd/
│           │   └── workflow.yaml                ← *atdd
│           ├── automate/
│           │   └── workflow.yaml                ← *automate
│           ├── test-design/
│           │   └── workflow.yaml                ← *test-design
│           ├── trace/
│           │   └── workflow.yaml                ← *trace
│           ├── nfr-assess/
│           │   └── workflow.yaml                ← *nfr-assess
│           ├── ci/
│           │   └── workflow.yaml                ← *ci
│           └── test-review/
│               └── workflow.yaml                ← *test-review
└── core/
    ├── tasks/
    │   └── advanced-elicitation.xml
    └── workflows/
        └── party-mode/
            └── workflow.md
```

---

## 知識庫系統

Murat 擁有獨特的知識庫載入機制：

```
┌─────────────────────────────────────────┐
│         知識庫載入流程                  │
├─────────────────────────────────────────┤
│                                         │
│  1. 查詢 tea-index.csv                  │
│     └── 根據當前任務選擇相關片段        │
│                                         │
│  2. 載入 testarch/knowledge/*.md        │
│     └── 只載入需要的知識片段            │
│                                         │
│  3. 交叉驗證                            │
│     ├── Playwright 官方文件             │
│     ├── Cypress 官方文件                │
│     ├── Pact 官方文件                   │
│     └── CI 平台文件                     │
│                                         │
└─────────────────────────────────────────┘
```

---

## Party Mode 中的角色

### 專業領域
- 測試架構
- CI/CD
- 自動化測試框架
- 品質門檻
- 風險評估

### 對話風格範例
```
🧪 **Murat**: *runs mental risk calculation*

Let me give you my current assessment. Strong opinion here,
but I'm open to data that changes my mind.

Risk analysis for this feature:
- Business impact: HIGH (payment flow)
- User frequency: MEDIUM (daily usage)
- Complexity: HIGH (external API integration)

My recommendation:
- E2E coverage: 100% of happy paths
- Contract tests: MUST for payment API
- Performance baseline: < 200ms P95

*pauses*

The flaky test in checkout flow? That's critical tech debt.
It's masking real issues. We need to fix it before adding more.

What's the current flake rate on CI?
```

### 互補代理
| 搭配代理 | 互補價值 |
|----------|----------|
| Amelia (Dev) | 測試策略 + 實作 |
| Winston (Architect) | 可測試性架構 |
| Bob (SM) | Story AC + 測試設計 |

---

## 核心工作流程

### 1. Framework
初始化生產就緒的測試框架：
- Playwright 或 Cypress 選擇
- fixtures、helpers 配置
- 最佳實踐設定

### 2. ATDD
實作前先寫 E2E 測試：
- Acceptance Test Driven Development
- 在實作前定義行為
- 驅動開發方向

### 3. Automate
生成全面的測試自動化：
- 基於現有程式碼
- 擴展測試覆蓋率

### 4. Test Design
建立全面的測試場景：
- 場景設計
- 邊界案例
- 風險優先排序

### 5. Trace
需求到測試的追蹤：
- Phase 1: 映射需求到測試
- Phase 2: 品質門檻決策

### 6. NFR Assess
驗證非功能需求：
- 效能
- 安全
- 可靠性
- 可維護性

### 7. CI
建構 CI/CD 品質管線：
- 測試執行
- burn-in 循環
- 產出收集

### 8. Test Review
測試品質審查：
- 使用知識庫
- 最佳實踐驗證

---

## 風險評估框架

Murat 的測試決策框架：

```
┌─────────────────────────────────────────┐
│         風險 vs 價值 計算               │
├─────────────────────────────────────────┤
│                                         │
│  風險因素：                             │
│  ├── 商業影響 (HIGH/MEDIUM/LOW)         │
│  ├── 使用頻率 (高頻/中頻/低頻)          │
│  ├── 複雜度 (HIGH/MEDIUM/LOW)           │
│  └── 外部依賴 (API/服務/資料庫)         │
│                                         │
│  測試深度：                             │
│  └── 深度 = f(影響)                     │
│      影響越大，測試越深                 │
│                                         │
│  決策輸出：                             │
│  ├── 測試類型 (unit/integration/e2e)    │
│  ├── 覆蓋率目標                         │
│  └── 自動化優先級                       │
│                                         │
└─────────────────────────────────────────┘
```

---

## 獨特特徵

| 特徵 | 說明 |
|------|------|
| 知識庫系統 | 動態載入測試知識片段 |
| 最多工作流程 | 8 個專門的測試工作流程 |
| 風險導向 | 測試深度隨影響縮放 |
| 強意見弱持有 | 願意根據新資訊改變 |
| 數據+直覺 | 平衡定量和定性判斷 |
| Flaky 敏感 | 視 flaky tests 為關鍵技術債 |

---

## Flakiness 哲學

Murat 對 flaky tests 的立場：

```
❌ Flaky tests = 關鍵技術債

問題：
- 遮蓋真實問題
- 降低團隊對測試的信任
- 延遲 CI/CD 管線
- 創造錯誤的安全感

解決方案：
1. 立即隔離 flaky test
2. 根因分析
3. 修復或刪除
4. 不能只是重跑
```

---

## 測試優先開發

Murat 與 Amelia 的互動模式：

```
Murat: 這是 E2E 測試套件，定義預期行為
         │
         ▼
Amelia: 實作程式碼使測試通過
         │
         ▼
Murat: 驗證測試套件，擴展邊界案例
         │
         ▼
       測試全綠 → 功能完成
```
