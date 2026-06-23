# 扎根理论：编码流程图与模型结构图

> 下列图使用 Mermaid，GitHub 与多数 Markdown 编辑器可直接渲染。需要图片（发小红书/插论文）时，打开同目录 `index.html` 一键查看并截图，或把代码贴到 https://mermaid.live 导出 SVG/PNG。
> 配套方法说明见 [`../references/04-coding-grounded-theory.md`](../references/04-coding-grounded-theory.md)。

## 图 1 · 扎根理论操作循环（含理论抽样与饱和）

这是扎根理论区别于一般编码的核心——**收集与分析交替进行、由浮现的范畴驱动下一轮抽样，直到理论饱和**。

```mermaid
flowchart TD
    A[确定研究问题<br/>过程/机制取向] --> B[初始抽样<br/>目的抽样起步]
    B --> C[收集数据<br/>访谈/观察/文档]
    C --> D[开放编码<br/>逐行贴标签·实境码]
    D --> E[持续比较<br/>事件↔事件 码↔码]
    E --> F[主轴编码<br/>归并范畴·建立关系]
    F --> G[写理论备忘录<br/>记录范畴含义与关系]
    G --> H{理论饱和?<br/>新数据不再<br/>产生新范畴/属性}
    H -- 否 --> I[理论抽样<br/>针对范畴空白<br/>决定下一步抽谁]
    I --> C
    H -- 是 --> J[选择性编码<br/>确定核心范畴]
    J --> K[提炼故事线<br/>构建理论/模型]
    K --> L[输出概念模型图<br/>+ 命题关系]

    style H fill:#fff3cd,stroke:#b7791f
    style L fill:#d1f0e0,stroke:#138a5b
    style G fill:#e7efff,stroke:#2563eb
```

## 图 2 · 三级编码漏斗（数据 → 理论的抽象升级）

```mermaid
flowchart TD
    subgraph L1[开放编码 Open Coding · 贴近数据]
        a1[原始语句1] --> c1[初始概念]
        a2[原始语句2] --> c1
        a3[原始语句3] --> c2[初始概念]
        a4[原始语句4] --> c3[实境码]
    end
    subgraph L2[主轴编码 Axial Coding · 建立关系]
        c1 --> cat1[范畴 A]
        c2 --> cat1
        c3 --> cat2[范畴 B]
    end
    subgraph L3[选择性编码 Selective Coding · 整合理论]
        cat1 --> core[核心范畴]
        cat2 --> core
        core --> theory[扎根理论/模型]
    end

    style L1 fill:#f5f7fb,stroke:#d8deea
    style L2 fill:#eef4ff,stroke:#c7d7f5
    style L3 fill:#e7f7ef,stroke:#9fe0c0
    style core fill:#fff3cd,stroke:#b7791f
    style theory fill:#d1f0e0,stroke:#138a5b
```

## 图 3 · 三流派编码语言对照

标题与正文必须用同一流派，**切忌混用**（详见 04 文档）。

```mermaid
flowchart LR
    subgraph G[经典 Glaser]
        g1[实质编码] --> g2[理论编码]
    end
    subgraph S[程序化 Strauss & Corbin]
        s1[开放编码] --> s2[主轴编码] --> s3[选择性编码]
    end
    subgraph C[建构主义 Charmaz]
        c1[初始编码] --> c2[聚焦编码] --> c3[理论编码]
    end

    style G fill:#f5f7fb,stroke:#647084
    style S fill:#eef4ff,stroke:#2563eb
    style C fill:#fdeef5,stroke:#c2417a
```

## 图 4 · Strauss & Corbin 编码范式（主轴编码用）

主轴编码把零散范畴围绕一个现象重新组织时的关系骨架。

```mermaid
flowchart LR
    A[因果条件<br/>Causal] --> P((现象<br/>Phenomenon))
    B[脉络/情境<br/>Context] --> P
    C[中介条件<br/>Intervening] --> P
    P --> D[行动/互动策略<br/>Action/Interaction]
    D --> E[结果<br/>Consequences]

    style P fill:#fff3cd,stroke:#b7791f
    style E fill:#d1f0e0,stroke:#138a5b
```

## 图 5 · 扎根理论模型结构模板（填空即用）

把你的核心范畴与主范畴替换进去，即得论文里的"理论模型图"。

```mermaid
flowchart TD
    COND[前因条件<br/>主范畴①②] --> CORE{核心范畴<br/>你的理论中心}
    CONTEXT[情境/脉络<br/>主范畴③] -. 调节 .-> CORE
    CORE --> STRAT[行动策略<br/>主范畴④⑤]
    STRAT --> OUTCOME[结果/效应<br/>主范畴⑥]
    OUTCOME -. 反馈循环 .-> COND

    style CORE fill:#fff3cd,stroke:#b7791f,stroke-width:2px
    style OUTCOME fill:#d1f0e0,stroke:#138a5b
    style COND fill:#e7efff,stroke:#2563eb
```

> 提示：模型图不是装饰，箭头要能对应到你数据里支撑的命题（如"前因→核心"对应某条范畴间关系），并在正文逐条论证。
