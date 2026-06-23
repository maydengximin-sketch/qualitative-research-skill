# 主题分析：六步流程图与结构图

> Mermaid 图，GitHub 可直接渲染。需要图片时打开同目录 `index.html` 截图，或贴到 https://mermaid.live 导出。
> 配套方法说明见 [`../references/05-coding-thematic.md`](../references/05-coding-thematic.md)。

## 图 1 · Braun & Clarke 反思性主题分析六步（含迭代回环）

注意：主题分析**不是一条直线**，第 4 步检验主题时常需回到第 2/3 步反复修订。

```mermaid
flowchart TD
    S1[1. 熟悉数据<br/>反复阅读·记初步想法] --> S2[2. 生成初始编码<br/>系统覆盖全数据]
    S2 --> S3[3. 生成候选主题<br/>把编码聚类成模式]
    S3 --> S4{4. 检验主题<br/>层1:对照编码片段<br/>层2:对照整个数据集}
    S4 -- 主题不成立/需重组 --> S2
    S4 -- 通过 --> S5[5. 定义与命名<br/>写每个主题的故事+精炼名]
    S5 --> S6[6. 撰写报告<br/>引语证据+分析叙述]
    S6 --> ANS[回应研究问题]

    style S4 fill:#fff3cd,stroke:#b7791f
    style S6 fill:#e7efff,stroke:#2563eb
    style ANS fill:#d1f0e0,stroke:#138a5b
```

## 图 2 · 编码 → 主题的层级结构（主题 ≠ 编码汇总）

主题是围绕一个**中心组织概念**的模式，不是"关于某话题的所有说法"的堆叠。

```mermaid
flowchart TD
    subgraph DATA[数据]
        d1[数据片段] 
        d2[数据片段]
        d3[数据片段]
        d4[数据片段]
        d5[数据片段]
    end
    d1 --> co1[编码1]
    d2 --> co1
    d3 --> co2[编码2]
    d4 --> co3[编码3]
    d5 --> co4[编码4]
    co1 --> st1[子主题 1.1]
    co2 --> st1
    co3 --> st2[子主题 1.2]
    co4 --> st2
    st1 --> T1[[主题 1<br/>中心组织概念]]
    st2 --> T1

    style T1 fill:#fff3cd,stroke:#b7791f,stroke-width:2px
    style DATA fill:#f5f7fb,stroke:#d8deea
```

## 图 3 · 主题分析的四种取向（编码前先声明）

```mermaid
flowchart LR
    Q{两个维度<br/>怎么定?}
    Q --> A[归纳 Inductive<br/>编码从数据生]
    Q --> B[演绎 Deductive<br/>编码来自既有理论]
    Q --> C[语义 Semantic<br/>贴近字面意义]
    Q --> D[潜义 Latent<br/>挖掘背后假设/意识形态]

    style Q fill:#fff3cd,stroke:#b7791f
    style A fill:#e7f7ef,stroke:#138a5b
    style B fill:#e7efff,stroke:#2563eb
    style C fill:#e7f7ef,stroke:#138a5b
    style D fill:#fdeef5,stroke:#c2417a
```

## 图 4 · 该用哪种分析？方法决策图

```mermaid
flowchart TD
    Q1{研究目标是?} 
    Q1 -- 建构新理论/机制模型 --> GT[扎根理论<br/>见 grounded-theory.md]
    Q1 -- 提炼跨数据的主题模式 --> Q2{要报<br/>编码者间一致性吗?}
    Q1 -- 大规模文本+类目+频次 --> CA[质性内容分析]
    Q2 -- 否·解释性·建构主义 --> RTA[反思性主题分析<br/>Braun & Clarke]
    Q2 -- 是·偏描述·后实证 --> CRTA[编码可靠性 TA<br/>+ 报 Kappa]

    style GT fill:#fff3cd,stroke:#b7791f
    style RTA fill:#d1f0e0,stroke:#138a5b
    style CRTA fill:#e7efff,stroke:#2563eb
    style CA fill:#fdeef5,stroke:#c2417a
```

> 关键提醒：反思性主题分析（RTA）的认识论与"编码者间信度/Kappa"有张力——**RTA 路径默认不报 Kappa**。若期刊硬要一致性，走 CRTA 分支并相应调整范式声明（详见 05 与 06 文档）。
