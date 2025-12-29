# Brain Methods CSV 深度分析

> 📄 原始檔案：`_bmad/core/workflows/brainstorming/brain-methods.csv`
> 📅 分析日期：2025-12-29

## 檔案概述

`brain-methods.csv` 是 Brainstorming Workflow 的創意技術資料庫，包含 62 種腦力激盪技術，是整個工作流程的核心知識庫。

**檔案特性：**
- CSV 格式，易於解析與擴展
- 62 種技術，涵蓋 10 個類別
- 每種技術包含完整的引導資訊
- 按需載入，效能優化

---

## 資料結構分析

### CSV 欄位

```
category,technique_name,description
```

**欄位說明：**

| 欄位 | 類型 | 用途 |
|------|------|------|
| `category` | String | 技術類別分類 |
| `technique_name` | String | 技術名稱 |
| `description` | String | 包含說明、引導提示、適用場景的完整描述 |

### Description 欄位結構

Description 欄位實際上包含多個子資訊，以自然語言形式編碼：

```
[技術說明] - [引導提示] by asking '[問題1]' '[問題2]' to [期望效果]
```

**範例解析：**

```
"Systematic creativity through seven lenses for methodical product improvement
and innovation - Substitute (what could you substitute), Combine (what could
you combine), Adapt (how could you adapt), Modify (what could you modify),
Put to other uses, Eliminate, Reverse"
```

解構：
- **技術說明**: Systematic creativity through seven lenses
- **適用場景**: methodical product improvement and innovation
- **引導提示**: Substitute, Combine, Adapt, Modify, Put, Eliminate, Reverse

---

## 技術類別統計

### 類別分布

| 類別 | 技術數量 | 百分比 | 核心特性 |
|------|----------|--------|----------|
| creative | 11 | 17.7% | 創新思維、突破框架 |
| deep | 8 | 12.9% | 深度分析、根因探索 |
| wild | 8 | 12.9% | 極端思維、打破邊界 |
| structured | 7 | 11.3% | 系統化、結構分析 |
| introspective_delight | 6 | 9.7% | 內在探索、價值澄清 |
| theatrical | 6 | 9.7% | 角色扮演、換位思考 |
| collaborative | 5 | 8.1% | 團隊協作、多元觀點 |
| cultural | 4 | 6.5% | 文化跨界、傳統智慧 |
| quantum | 3 | 4.8% | 量子啟發思維 |
| biomimetic | 3 | 4.8% | 仿生設計、自然智慧 |

### 類別分布圖

```
┌─────────────────────────────────────────────────────────────┐
│                   Category Distribution                      │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  creative        ████████████████████████████████████ 11    │
│  deep            ████████████████████████████ 8             │
│  wild            ████████████████████████████ 8             │
│  structured      ████████████████████████ 7                 │
│  introspective   ████████████████████ 6                     │
│  theatrical      ████████████████████ 6                     │
│  collaborative   ████████████████ 5                         │
│  cultural        ████████████ 4                             │
│  quantum         ████████ 3                                 │
│  biomimetic      ████████ 3                                 │
│                                                              │
│  Total: 62 techniques                                       │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## 各類別技術詳解

### 1. Collaborative（協作）- 5 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Yes And Building | 肯定式累加 | 團隊創意建構 |
| Brain Writing Round Robin | 沉默書寫輪流 | 內向者友善 |
| Random Stimulation | 隨機刺激連結 | 打破心理障礙 |
| Role Playing | 角色扮演觀點 | 利害關係人同理 |
| Ideation Relay Race | 限時接力創意 | 高能量突破 |

**類別特色：**
- 強調團隊動力
- 支援多元聲音
- 建立共識與活力

### 2. Creative（創意）- 11 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| What If Scenarios | 假設情境探索 | 打破既有假設 |
| Analogical Thinking | 類比思維 | 跨領域遷移 |
| Reversal Inversion | 反轉思維 | 揭示隱藏假設 |
| First Principles Thinking | 第一性原理 | 根本創新 |
| Forced Relationships | 強迫關聯 | 意外連結 |
| Time Shifting | 時間轉換 | 時間維度探索 |
| Metaphor Mapping | 隱喻映射 | 抽象具體化 |
| Cross-Pollination | 跨界授粉 | 產業遷移 |
| Concept Blending | 概念融合 | 創造新類別 |
| Reverse Brainstorming | 反向腦力激盪 | 問題發現 |
| Sensory Exploration | 感官探索 | 多感官思維 |

**類別特色：**
- 最大類別，技術最多
- 強調創新突破
- 適合發散思維階段

### 3. Deep（深度）- 8 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Five Whys | 五個為什麼 | 根因分析 |
| Morphological Analysis | 形態分析 | 系統組合 |
| Provocation Technique | 挑釁技術 | 荒謬啟發 |
| Assumption Reversal | 假設反轉 | 範式轉移 |
| Question Storming | 問題風暴 | 正確問題定義 |
| Constraint Mapping | 約束映射 | 限制突破 |
| Failure Analysis | 失敗分析 | 學習經驗 |
| Emergent Thinking | 湧現思維 | 有機發展 |

**類別特色：**
- 強調分析深度
- 適合問題解決
- 收斂思維導向

### 4. Introspective Delight（內省喜悅）- 6 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Inner Child Conference | 內在小孩會議 | 純真好奇 |
| Shadow Work Mining | 陰影工作挖掘 | 潛意識探索 |
| Values Archaeology | 價值考古 | 核心價值澄清 |
| Future Self Interview | 未來自我訪談 | 長期視角 |
| Body Wisdom Dialogue | 身體智慧對話 | 直覺探索 |
| Permission Giving | 許可給予 | 解除自我限制 |

**類別特色：**
- 個人內在探索
- 情感與價值導向
- 適合個人發展議題

### 5. Structured（結構）- 7 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| SCAMPER Method | 七鏡頭系統創意 | 產品改進 |
| Six Thinking Hats | 六頂思考帽 | 全面分析 |
| Mind Mapping | 心智圖 | 視覺化思考 |
| Resource Constraints | 資源約束 | 極端限制創意 |
| Decision Tree Mapping | 決策樹映射 | 路徑探索 |
| Solution Matrix | 解決方案矩陣 | 系統組合 |
| Trait Transfer | 特質轉移 | 成功模式借用 |

**類別特色：**
- 框架明確
- 易於執行
- 適合團隊統一使用

### 6. Theatrical（戲劇）- 6 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Time Travel Talk Show | 時空旅行脫口秀 | 時間視角 |
| Alien Anthropologist | 外星人類學家 | 局外人觀點 |
| Dream Fusion Laboratory | 夢想融合實驗室 | 逆向工程 |
| Emotion Orchestra | 情緒交響樂 | 多情緒視角 |
| Parallel Universe Cafe | 平行宇宙咖啡館 | 替代現實 |
| Persona Journey | 人格旅程 | 原型智慧 |

**類別特色：**
- 高度創意與趣味
- 角色扮演元素
- 適合打破常規

### 7. Wild（狂野）- 8 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Chaos Engineering | 混沌工程 | 壓力測試 |
| Guerrilla Gardening Ideas | 游擊園藝想法 | 意外種植 |
| Pirate Code Brainstorm | 海盜守則腦力激盪 | 無視規則 |
| Zombie Apocalypse Planning | 殭屍末日規劃 | 極端生存 |
| Drunk History Retelling | 醉酒歷史重述 | 去除濾鏡 |
| Anti-Solution | 反解決方案 | 破壞性創意 |
| Quantum Superposition | 量子疊加 | 矛盾共存 |
| Elemental Forces | 元素力量 | 自然隱喻 |

**類別特色：**
- 最挑戰舒適區
- 高能量需求
- 適合突破僵局

### 8. Biomimetic（仿生）- 3 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Nature's Solutions | 自然解決方案 | 生物策略 |
| Ecosystem Thinking | 生態系統思維 | 系統關係 |
| Evolutionary Pressure | 演化壓力 | 優化迭代 |

**類別特色：**
- 向自然學習
- 長期驗證的智慧
- 適合產品設計

### 9. Quantum（量子）- 3 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Observer Effect | 觀察者效應 | 測量影響 |
| Entanglement Thinking | 糾纏思維 | 隱藏連結 |
| Superposition Collapse | 疊加崩塌 | 約束決策 |

**類別特色：**
- 量子物理啟發
- 抽象概念具體化
- 適合複雜系統

### 10. Cultural（文化）- 4 技術

| 技術 | 核心概念 | 適用情境 |
|------|----------|----------|
| Indigenous Wisdom | 原住民智慧 | 傳統知識 |
| Fusion Cuisine | 融合料理 | 文化混搭 |
| Ritual Innovation | 儀式創新 | 體驗設計 |
| Mythic Frameworks | 神話框架 | 原型敘事 |

**類別特色：**
- 文化多元性
- 人類學視角
- 適合體驗設計

---

## 技術特性矩陣

### 能量等級分布

```
┌─────────────────────────────────────────────────────────────┐
│                    Energy Level Distribution                 │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  High Energy (高能量)                                        │
│  ┌──────────────────────────────────────────────────────┐   │
│  │ collaborative: Yes And, Ideation Relay               │   │
│  │ creative: What If, First Principles                  │   │
│  │ wild: Chaos Engineering, Pirate Code, Zombie        │   │
│  │ theatrical: Time Travel, Emotion Orchestra          │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  Medium Energy (中等能量)                                    │
│  ┌──────────────────────────────────────────────────────┐   │
│  │ structured: SCAMPER, Six Thinking Hats, Mind Mapping│   │
│  │ deep: Five Whys, Morphological Analysis             │   │
│  │ creative: Analogical, Metaphor Mapping              │   │
│  │ biomimetic: Nature's Solutions, Ecosystem Thinking  │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  Low Energy (低能量)                                         │
│  ┌──────────────────────────────────────────────────────┐   │
│  │ introspective: Inner Child, Values Archaeology      │   │
│  │ collaborative: Brain Writing Round Robin            │   │
│  │ deep: Question Storming, Emergent Thinking         │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### 思維模式對應

| 思維模式 | 適合類別 | 代表技術 |
|----------|----------|----------|
| Divergent（發散） | creative, wild, theatrical | What If, Chaos Engineering |
| Convergent（收斂） | structured, deep | SCAMPER, Five Whys |
| Analytical（分析） | deep, structured | Morphological Analysis |
| Intuitive（直覺） | introspective, cultural | Body Wisdom, Indigenous Wisdom |
| Collaborative（協作） | collaborative | Yes And, Brain Writing |

---

## 使用模式建議

### 階段匹配

| 創意階段 | 推薦類別 | 原因 |
|----------|----------|------|
| 探索（Exploration） | creative, wild | 最大化想法多樣性 |
| 分析（Analysis） | deep, structured | 組織與理解 |
| 發展（Development） | structured, collaborative | 精煉與建構 |
| 行動（Action） | structured, deep | 規劃與評估 |

### 場景匹配

| 場景 | 推薦技術 |
|------|----------|
| 產品創新 | SCAMPER, Cross-Pollination, Nature's Solutions |
| 問題解決 | Five Whys, Constraint Mapping, Reversal Inversion |
| 團隊建設 | Yes And, Role Playing, Six Thinking Hats |
| 個人發展 | Values Archaeology, Future Self Interview |
| 策略規劃 | Decision Tree, Scenario Planning, Morphological Analysis |

---

## 資料結構最佳化建議

### 當前限制

1. **單一 description 欄位**：多種資訊混合
2. **缺少額外元資料**：能量等級、時長需從描述推斷
3. **引導提示不一致**：有些詳細，有些簡略

### 建議擴展結構

```csv
category,technique_name,description,energy_level,typical_duration,facilitation_prompts,best_for
```

**新增欄位說明：**

| 欄位 | 類型 | 範例值 |
|------|------|--------|
| `energy_level` | Enum | high, medium, low |
| `typical_duration` | String | 15-20 min |
| `facilitation_prompts` | String | "What if...?;How would...?" |
| `best_for` | String | "problem solving, innovation" |

---

## 與其他框架的對照

### IDEO Design Methods

| Brain Methods 類別 | IDEO 對應 |
|--------------------|-----------|
| collaborative | Extreme Users, Bodystorming |
| structured | Journey Mapping, How Might We |
| deep | Root Cause Analysis |

### TRIZ

| Brain Methods 技術 | TRIZ 對應 |
|--------------------|-----------|
| Reversal Inversion | 原則 13: 反轉 |
| Morphological Analysis | 對應工具存在 |
| Resource Constraints | 原則 35: 參數變化 |

---

## 小結

`brain-methods.csv` 是 Brainstorming Workflow 的創意技術資料庫：

1. **豐富的技術庫**：62 種技術，10 個類別
2. **多元覆蓋**：從結構化到狂野，從團隊到個人
3. **可擴展設計**：CSV 格式易於新增技術
4. **按需載入**：優化效能，避免初始化負擔

這個資料庫體現了 BMAD 框架對創意方法論的深度整合，提供了從保守到激進、從個人到團隊的完整創意工具箱。
