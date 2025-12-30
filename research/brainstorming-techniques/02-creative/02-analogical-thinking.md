# Analogical Thinking

> 類比思維 - 從遠處借智慧，從熟悉解陌生

## 基本資訊

| 屬性 | 值 |
|------|-----|
| 類別 | Creative |
| 能量等級 | 中 |
| 建議時長 | 30-45 分鐘 |
| 參與人數 | 1-10 人 |
| 難度 | 中-高 |

## 技術概述

**Analogical Thinking**（類比思維）是一種透過識別不同領域間結構相似性來解決問題的技術。將一個領域（源域）的成功模式映射到另一個領域（目標域），產生創新解決方案。類比距離越遠，創新潛力越大。

```mermaid
flowchart LR
    subgraph Source[源域 - 熟悉領域]
    S1[問題結構]
    S2[解決模式]
    S3[成功要素]
    end

    subgraph Mapping[映射過程]
    M[識別結構<br/>相似性]
    end

    subgraph Target[目標域 - 待解問題]
    T1[對應問題]
    T2[適應方案]
    T3[創新解決]
    end

    S1 --> M
    S2 --> M
    S3 --> M
    M --> T1
    M --> T2
    M --> T3

    style M fill:#fff9c4
```

## 歷史背景

類比思維在科學史上有重要地位：
- **克普勒**：用行星與磁鐵的類比發現行星運動定律
- **達爾文**：從馬爾薩斯人口論類比到物種演化
- **沃森與克里克**：DNA 雙螺旋結構的發現

認知科學家 Dedre Gentner 的「結構映射理論」(Structure-Mapping Theory) 為類比思維提供了系統性框架。

## 核心原理

### 類比的層次

```mermaid
graph TD
    subgraph 表面類比
    A1[外觀相似]
    A2[容易發現]
    A3[創新性低]
    end

    subgraph 結構類比
    B1[關係相似]
    B2[需要洞察]
    B3[創新性高]
    end

    subgraph 深層類比
    C1[原理相似]
    C2[跨領域]
    C3[突破性創新]
    end

    A1 --> B1 --> C1

    style C1 fill:#c8e6c9
```

### 類比距離與創新

| 類比距離 | 範例 | 創新潛力 |
|----------|------|----------|
| 近距離 | 同產業內的最佳實踐 | 低 - 漸進改善 |
| 中距離 | 相關產業的做法 | 中 - 有意義的創新 |
| 遠距離 | 完全不同領域的模式 | 高 - 突破性創新 |

## 執行步驟

```mermaid
sequenceDiagram
    participant F as 引導者
    participant T as 團隊

    F->>T: 明確描述目標問題
    F->>T: 抽象化：識別核心結構/關係
    F->>T: 搜尋類比：找到結構相似的源域
    T->>T: 深入探索源域的解決方案
    F->>T: 映射：將解決模式轉移到目標域
    T->>T: 適應：調整以符合目標域特性
    F->>T: 評估並發展最佳方案
```

### 詳細步驟

#### 步驟 1：問題抽象化（10分鐘）

1. **描述具體問題**
   - 例：「如何讓用戶更快找到想要的產品？」

2. **抽取核心結構**
   - 關鍵要素：搜尋者、大量選項、匹配需求
   - 核心關係：導航、篩選、推薦

3. **形成抽象描述**
   - 「在大量選項中快速找到最佳匹配」

#### 步驟 2：搜尋類比（15分鐘）

**提問引導：**
- 「還有什麼領域需要解決類似問題？」
- 「自然界如何解決這個問題？」
- 「其他產業如何處理這種情況？」

**類比來源：**

```mermaid
mindmap
  root((類比來源))
    自然界
      動物行為
      生態系統
      物理現象
    其他產業
      零售
      醫療
      娛樂
      金融
    歷史
      古代解決方案
      演化過程
    日常生活
      家庭活動
      運動比賽
      社交互動
```

#### 步驟 3：深入探索源域（10分鐘）

- 了解源域解決方案的細節
- 識別成功的關鍵因素
- 理解背後的原理

#### 步驟 4：映射與適應（15分鐘）

1. **直接映射**
   - 源域的 A → 目標域的 A'
   - 源域的 B → 目標域的 B'

2. **適應調整**
   - 考慮目標域的特殊約束
   - 修改以符合實際情況

## 類比範例

### 案例：電商搜尋優化

**目標問題**：用戶在電商網站找不到想要的產品

**類比探索**：

| 源域 | 解決模式 | 映射到電商 |
|------|----------|------------|
| 圖書館員 | 詢問需求後推薦 | 對話式搜尋助手 |
| 約會 App | 雙向匹配算法 | 產品與用戶雙向匹配 |
| 超市貨架 | 視覺分區引導 | 視覺化分類導航 |
| 蜜蜂採蜜 | 舞蹈溝通位置 | 社群分享發現 |
| GPS 導航 | 即時路線規劃 | 個人化購物路徑 |

### 歷史性類比創新

```mermaid
timeline
    title 改變世界的類比創新
    section 科學
        1600s : 克普勒<br/>行星如磁鐵
        1800s : 達爾文<br/>演化如經濟競爭
    section 技術
        1900s : 飛機<br/>如鳥類飛行
        1940s : 電腦記憶體<br/>如人類記憶
    section 商業
        1990s : 亞馬遜<br/>網站如實體書店
        2000s : Uber<br/>乘車如叫外送
```

## 引導提示

### 尋找類比的問題

| 問題類型 | 提問 |
|----------|------|
| 自然類比 | 「自然界如何解決這個問題？」|
| 產業類比 | 「哪個產業已經解決了類似問題？」|
| 歷史類比 | 「歷史上有類似的挑戰嗎？」|
| 系統類比 | 「什麼系統有相似的結構？」|

### 深化類比的問題

| 問題 | 目的 |
|------|------|
| 這個類比的核心原理是什麼？ | 提取可遷移的原則 |
| 這在源域為什麼有效？ | 理解成功因素 |
| 目標域有什麼不同？ | 識別需要調整的地方 |

## 適用場景

### 最佳使用時機

```mermaid
flowchart TD
    A[考慮使用類比思維]

    A --> B[面臨新問題]
    A --> C[需要跨領域創新]
    A --> D[既有方案失效]
    A --> E[學習新概念]

    B --> F[尋找結構相似的已解決問題]
    C --> F
    D --> F
    E --> F

    F --> G[應用類比思維]
```

## 注意事項

### 類比的陷阱

```mermaid
graph TD
    subgraph 常見錯誤
    E1[表面類比陷阱] --> E1a[只看外觀相似]
    E2[錯誤映射] --> E2a[忽略關鍵差異]
    E3[過度延伸] --> E3a[將類比推太遠]
    end

    subgraph 解決方法
    S1[深入結構層面]
    S2[明確標注差異]
    S3[測試類比邊界]
    end

    E1 --> S1
    E2 --> S2
    E3 --> S3
```

### Do's & Don'ts

**Do's（應該做）**
- 尋找結構相似而非表面相似
- 明確類比的邊界
- 測試映射的有效性
- 嘗試遠距離類比

**Don'ts（不應該做）**
- 停留在表面類比
- 忽略領域差異
- 強行套用不適合的類比
- 只用熟悉領域的類比

## 變體技術

### 1. 強制類比
- 隨機選擇一個領域
- 強制尋找與問題的連結
- 類似 Random Stimulation

### 2. 類比頭腦風暴
- 快速產生多個類比
- 不評判，只記錄
- 之後選擇最有潛力的深入

### 3. 逆向類比
- 思考你的解決方案可以用在哪裡
- 從目標域反推源域

## 與其他技術的結合

```mermaid
flowchart LR
    AT[Analogical Thinking]

    subgraph 增強類比
    BM[Biomimetic] --> AT
    CP[Cross-Pollination] --> AT
    MM[Metaphor Mapping] --> AT
    end

    subgraph 類比後續
    AT --> FP[First Principles]
    AT --> SC[SCAMPER]
    end
```

## 培養類比能力的方法

1. **廣泛閱讀**
   - 閱讀不同領域的書籍
   - 關注科普和跨領域內容

2. **保持好奇**
   - 問「這是怎麼運作的？」
   - 觀察日常事物的結構

3. **練習轉換**
   - 嘗試用不同方式解釋同一件事
   - 為複雜概念找簡單類比

4. **建立類比庫**
   - 收集有啟發性的類比
   - 記錄跨領域的成功案例

## 參考資源

- [MIT Sloan: Unlock Creativity Through Analogical Thinking](https://sloanreview.mit.edu/article/unlock-creativity-through-analogical-thinking/)
- [Cambridge: Analogical Thinking in Problem-Solving and Creativity](https://www.cambridge.org/core/books/abs/rethinking-creativity/analogical-thinking-in-problemsolving-and-creativity/0B0E49277F5608EEA7FBF7185C057B86)
- [LearningMole: Harnessing the Power of Comparative Reasoning](https://learningmole.com/analogical-thinking-comparisons-solutions/)
- [ScienceDirect: Cross-domain Analogical Reasoning](https://www.sciencedirect.com/science/article/abs/pii/S1871187125000574)

---

*返回 [Creative 類別](./index.md) | [技術總覽](../index.md)*
