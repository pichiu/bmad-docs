# Step 2a: User-Selected Techniques 深度分析

> 📄 原始檔案：`_bmad/core/workflows/brainstorming/steps/step-02a-user-selected.md`
> 📅 分析日期：2025-12-29

## 檔案概述

`step-02a-user-selected.md` 是四種技術選擇路徑中的第一種，提供用戶完全自主的技術瀏覽與選擇體驗。

**核心特色：**
- AI 扮演「技術圖書館員」角色
- 用戶完全主導選擇過程
- 提供分類瀏覽與詳細資訊
- 中性呈現，不推薦或引導

---

## 執行規則分析

### Mandatory Execution Rules

```markdown
## MANDATORY EXECUTION RULES (READ FIRST):
- ✅ YOU ARE A TECHNIQUE LIBRARIAN, not a recommender
- 🎯 LOAD TECHNIQUES ON-DEMAND from brain-methods.csv
- 📋 PREVIEW TECHNIQUE OPTIONS clearly and concisely
- 🔍 LET USER EXPLORE and select based on their interests
- 💬 PROVIDE BACK OPTION to return to approach selection
```

**角色定位：技術圖書館員**

| 面向 | 圖書館員做什麼 | 圖書館員不做什麼 |
|------|----------------|------------------|
| 資訊提供 | 客觀呈現技術選項 | 不推薦特定技術 |
| 導覽協助 | 協助分類瀏覽 | 不引導特定方向 |
| 細節說明 | 回答技術相關問題 | 不評價技術優劣 |
| 選擇支援 | 確認用戶選擇 | 不質疑用戶判斷 |

### Execution Protocols

```markdown
## EXECUTION PROTOCOLS:
- 🎯 Load brain techniques CSV only when needed for presentation
- ⚠️ Present [B] back option and [C] continue options
- 💾 Update frontmatter with selected techniques
- 📖 Route to technique execution after confirmation
- 🚫 FORBIDDEN making recommendations or steering choices
```

**禁止事項強調：**

「禁止推薦或引導選擇」是此路徑的核心原則，確保這是真正的用戶自選體驗。

---

## 技術載入機制

### On-Demand Loading

```markdown
### 1. Load Brain Techniques Library

Load techniques from CSV on-demand:

"Perfect! Let's explore our complete brainstorming techniques library.
I'll load all available techniques so you can browse and select exactly
what appeals to you.

**Loading Brain Techniques Library...**"

**Load CSV and parse:**
- Read `brain-methods.csv`
- Parse: category, technique_name, description, facilitation_prompts,
         best_for, energy_level, typical_duration
- Organize by categories for browsing
```

**載入流程圖：**

```
┌─────────────────────────────────────────────────────────────┐
│                  On-Demand CSV Loading                       │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  用戶選擇 [1] User-Selected                                  │
│              │                                               │
│              ▼                                               │
│  ┌─────────────────────────────────┐                        │
│  │ 讀取 brain-methods.csv          │                        │
│  └─────────────────────────────────┘                        │
│              │                                               │
│              ▼                                               │
│  ┌─────────────────────────────────┐                        │
│  │ 解析欄位：                       │                        │
│  │ • category                       │                        │
│  │ • technique_name                 │                        │
│  │ • description                    │                        │
│  │ • facilitation_prompts           │                        │
│  │ • best_for                       │                        │
│  │ • energy_level                   │                        │
│  │ • typical_duration               │                        │
│  └─────────────────────────────────┘                        │
│              │                                               │
│              ▼                                               │
│  ┌─────────────────────────────────┐                        │
│  │ 按類別組織技術                   │                        │
│  │ （7個類別，36+技術）             │                        │
│  └─────────────────────────────────┘                        │
│              │                                               │
│              ▼                                               │
│  呈現類別清單供用戶瀏覽                                      │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## 技術類別呈現

```markdown
### 2. Present Technique Categories

"**Our Brainstorming Technique Library - 36+ Techniques Across 7 Categories:**

**[1] Structured Thinking** (6 techniques)
- Systematic frameworks for thorough exploration and organized analysis
- Includes: SCAMPER, Six Thinking Hats, Mind Mapping, Resource Constraints

**[2] Creative Innovation** (7 techniques)
- Innovative approaches for breakthrough thinking and paradigm shifts
- Includes: What If Scenarios, Analogical Thinking, Reversal Inversion

**[3] Collaborative Methods** (4 techniques)
- Group dynamics and team ideation approaches for inclusive participation
- Includes: Yes And Building, Brain Writing Round Robin, Role Playing

**[4] Deep Analysis** (5 techniques)
- Analytical methods for root cause and strategic insight discovery
- Includes: Five Whys, Morphological Analysis, Provocation Technique

**[5] Theatrical Exploration** (5 techniques)
- Playful exploration for radical perspectives and creative breakthroughs
- Includes: Time Travel Talk Show, Alien Anthropologist, Dream Fusion

**[6] Wild Thinking** (5 techniques)
- Extreme thinking for pushing boundaries and breakthrough innovation
- Includes: Chaos Engineering, Guerrilla Gardening Ideas, Pirate Code

**[7] Introspective Delight** (5 techniques)
- Inner wisdom and authentic exploration approaches
- Includes: Inner Child Conference, Shadow Work Mining, Values Archaeology

**Which category interests you most? Enter 1-7...**"
```

**類別設計分析：**

| 類別 | 思維模式 | 能量等級 | 適用場景 |
|------|----------|----------|----------|
| Structured | 系統化、邏輯 | 中等 | 複雜問題分析 |
| Creative | 發散、創新 | 高 | 突破既有思維 |
| Collaborative | 團隊、互動 | 高 | 多元觀點整合 |
| Deep | 深度、分析 | 中等 | 根因探索 |
| Theatrical | 角色扮演、戲劇 | 高 | 換位思考 |
| Wild | 極端、突破 | 非常高 | 打破邊界 |
| Introspective | 內省、直覺 | 低到中 | 價值澄清 |

---

## 類別選擇處理

```markdown
### 3. Handle Category Selection

After user selects category:

**Present 3-5 techniques from selected category:**
For each technique:
- **Technique Name** (Duration: [time], Energy: [level])
- Description: [Brief clear description]
- Best for: [What this technique excels at]
- Example prompt: [Sample facilitation prompt]
```

**技術呈現格式範例：**

```
**1. SCAMPER Method** (Duration: 20-30 min, Energy: Moderate)
- Systematic creativity through seven lenses
  (Substitute/Combine/Adapt/Modify/Put/Eliminate/Reverse)
- Best for: Product improvement, innovation challenges,
           systematic idea generation
- Example prompt: "What could you substitute in your current
                  approach to create something new?"
```

**呈現設計原則：**

1. **資訊密度平衡**：足夠資訊做決策，不過度詳細
2. **實用導向**：包含 Best for 幫助判斷適用性
3. **具體範例**：提供實際 prompt 讓用戶預覽體驗

---

## 技術選擇互動

```markdown
### 4. Allow Technique Selection

"**Which techniques from this category appeal to you?**

You can:
- Select by technique name or number
- Ask for more details about any specific technique
- Browse another category
- Select multiple techniques for a comprehensive session

**Options:**
- Enter technique names/numbers you want to use
- [Details] for more information about any technique
- [Categories] to return to category list
- [Back] to return to approach selection
```

**互動流程圖：**

```
┌─────────────────────────────────────────────────────────────┐
│                  Technique Selection Flow                    │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│                   類別技術列表                               │
│                        │                                     │
│       ┌────────────────┼────────────────┐                   │
│       │                │                │                   │
│       ▼                ▼                ▼                   │
│  選擇技術        [Details]         [Categories]             │
│       │          要更多細節        返回類別清單             │
│       │                │                │                   │
│       ▼                ▼                ▼                   │
│  技術加入       顯示技術           回到類別                 │
│  選擇清單       完整說明           瀏覽頁面                 │
│       │                │                │                   │
│       │                └────────────────┘                   │
│       │                        │                            │
│       │                        │                            │
│       │      ┌─────────────────┘                            │
│       │      │                                               │
│       │      ▼                                               │
│       │  繼續探索                                            │
│       │  或選擇更多技術                                      │
│       │                                                      │
│       ▼                                                      │
│  完成選擇                                                    │
│  進入確認                                                    │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## 確認流程

```markdown
### 5. Handle Technique Confirmation

When user selects techniques:

**Confirmation Process:**
"**Your Selected Techniques:**
- [Technique 1]: [Why this matches their session goals]
- [Technique 2]: [Why this complements the first]
- [Technique 3]: [If selected, how it builds on others]

**Session Plan:**
This combination will take approximately [total_time] and focus on
[expected outcomes].

**Confirm these choices?**
[C] Continue - Begin technique execution
[Back] - Modify technique selection"
```

**確認資訊結構：**

| 項目 | 內容 | 目的 |
|------|------|------|
| 選擇清單 | 用戶選的技術 | 確認無誤 |
| 匹配說明 | 與會議目標的關聯 | 驗證選擇合理性 |
| 時間估計 | 總計所需時間 | 設定期望 |
| 預期成果 | 可能的產出 | 明確目標 |

---

## Frontmatter 更新

```markdown
### 6. Update Frontmatter and Continue

If user confirms:

**Update frontmatter:**
```yaml
---
selected_approach: 'user-selected'
techniques_used: ['technique1', 'technique2', 'technique3']
stepsCompleted: [1, 2]
---
```

**Append to document:**
```markdown
## Technique Selection

**Approach:** User-Selected Techniques
**Selected Techniques:**
- [Technique 1]: [Brief description and session fit]
- [Technique 2]: [Brief description and session fit]
- [Technique 3]: [Brief description and session fit]

**Selection Rationale:** [Content based on user's choices and reasoning]
```

**Route to execution:**
Load `./step-03-technique-execution.md`
```

---

## 成功與失敗指標

### Success Metrics

```markdown
## SUCCESS METRICS:
✅ Brain techniques CSV loaded successfully on-demand
✅ Technique categories presented clearly with helpful descriptions
✅ User able to browse and select techniques based on interests
✅ Selected techniques confirmed with session fit explanation
✅ Frontmatter updated with technique selections
✅ Proper routing to technique execution or back navigation
```

### Failure Modes

```markdown
## FAILURE MODES:
❌ Preloading all techniques instead of loading on-demand
❌ Making recommendations instead of letting user explore
❌ Not providing enough detail for informed selection
❌ Missing back navigation option
❌ Not updating frontmatter with technique selections
```

---

## 設計模式分析

### 1. Librarian Pattern（圖書館員模式）

AI 採取中性、服務導向的角色：
- 提供資訊而非建議
- 回應查詢而非主動推銷
- 尊重用戶的探索與選擇

### 2. Progressive Disclosure Pattern（漸進揭露模式）

資訊分層呈現：
- 第一層：類別概覽
- 第二層：類別內技術列表
- 第三層：單一技術詳細說明

### 3. Flexible Navigation Pattern（彈性導航模式）

多種導航選項：
- 類別間切換
- 返回上層
- 直接選擇
- 請求詳情

### 4. Confirmation Loop Pattern（確認迴圈模式）

選擇後必須確認：
- 防止誤選
- 提供修改機會
- 確保用戶理解選擇

---

## 與其他 Step 2 路徑的比較

| 面向 | 2a User-Selected | 2b AI-Recommended | 2c Random | 2d Progressive |
|------|------------------|-------------------|-----------|----------------|
| AI 角色 | 圖書館員 | 技術配對師 | 驚喜創造者 | 旅程設計師 |
| 用戶控制 | 完全 | 部分 | 最少 | 框架內自由 |
| 決策責任 | 用戶 | AI + 用戶 | 系統 | 結構化流程 |
| 適合場景 | 有偏好 | 信任專家 | 尋求突破 | 需要系統化 |

---

## 使用者體驗考量

### 優點

1. **完全控制**：用戶享有最大自主權
2. **探索樂趣**：可以瀏覽發現新技術
3. **學習機會**：過程中認識各種方法

### 潛在挑戰

1. **選擇困難**：36+ 技術可能造成選擇壓力
2. **時間消耗**：瀏覽選擇需要較多時間
3. **專業門檻**：需要一定了解才能做好選擇

### 改善建議

1. **快速篩選**：加入依目標篩選功能
2. **熱門標籤**：標示常用或推薦技術
3. **組合建議**：提供常見技術組合參考

---

## 小結

`step-02a-user-selected.md` 提供了完全用戶主導的技術選擇體驗：

1. **中性角色**：AI 作為圖書館員而非顧問
2. **分層瀏覽**：類別 → 技術 → 詳情的漸進揭露
3. **彈性導航**：支援多種瀏覽與選擇方式
4. **確認機制**：選擇後必須確認再進入執行

這種設計特別適合對創意技術有所了解、或想自主探索的用戶，體現了 BMAD 框架尊重用戶自主權的設計理念。
