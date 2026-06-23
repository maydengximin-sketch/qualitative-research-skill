# 质性研究全流程助手 · Qualitative Research Skill

> 一个面向 **Claude Code / Claude Agent** 的质性研究（定性研究）方法学技能包：从立题、抽样、访谈、编码，到信效度、报告，覆盖整条研究链路。工具中立，适配 NVivo / MAXQDA / ATLAS.ti 乃至纯手工编码。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
![Lang](https://img.shields.io/badge/lang-中文-blue)
![Type](https://img.shields.io/badge/Claude-Skill-8A2BE2)
![Stage](https://img.shields.io/badge/coverage-立题→成文-success)
![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen)

> 给读研做访谈、编码、算 Kappa、被审稿人追着要 COREQ 的你。把"一项严谨的质性研究该怎么做"沉淀成一个 AI 能直接调用的技能包——少翻一次书，少踩一个坑。

---

## 📑 目录

- [这是什么 / 解决什么痛点](#-这是什么解决什么痛点)
- [为什么不是"问 AI 就行"](#-为什么不是问-ai-就行)
- [内容结构](#-内容结构)
- [七大阶段能帮你做什么](#-七大阶段能帮你做什么)
- [安装与使用](#-安装与使用)
- [真实使用场景示例](#-真实使用场景示例)
- [七条贯穿全程的设计原则](#-七条贯穿全程的设计原则)
- [方法学渊源](#-方法学渊源部分)
- [常见问题 FAQ](#-常见问题-faq)
- [免责声明 / 贡献 / 许可](#-免责声明)
- [☕ 赞赏支持](#-赞赏支持)

---

## ✨ 这是什么 / 解决什么痛点

质性研究最磨人的从来不是"不会"，而是**每一步都要回去翻方法书、对规范、查阈值**：

- 访谈提纲怎么问才不诱导？焦点小组几个人合适？
- 这批访谈到底该用扎根理论还是主题分析？两者怎么分？
- 三级编码层级老是混乱，开放码、范畴、核心范畴傻傻分不清？
- 审稿人要"编码者间信度"，Kappa 怎么算、要不要算、阈值多少？
- "访谈了 20 个人"算饱和吗？怎么向审稿人证明饱和了？
- 投稿要 COREQ 32 项，逐条对照好麻烦？

这个 Skill 把上面这些**全部沉淀成结构化的方法学文档 + 模板 + 工具 + 流程图**，让 AI 助手在你提问时**自动加载对应规范来作答**，而不是凭训练记忆"大概答一下"。

**适合人群**：研究生 / 博士生、青年教师、做用户研究 · 政策文本分析 · 田野访谈 · 内容分析的实践者，以及任何想系统补质性方法的人。

## 🤔 为什么不是"问 AI 就行"

直接问通用 AI，常见三个问题：① 方法术语混用（把"主题分析"当方法学）；② 无差别让你报 Kappa（其实建构主义范式不该报）；③ 阈值/规范记错或编造文献。

本 Skill 的不同之处：

- **范式优先的判断逻辑**：先帮你判断范式与方法学，再决定技术——比如它**不会无脑让你算 Kappa**，而是先看你是不是建构主义路径。
- **可追溯**：每份文档末尾附真实经典文献（Charmaz、Braun & Clarke、Lincoln & Guba、COREQ 原文……），不是空口white说。
- **带可执行产物**：访谈提纲、编码簿、知情同意书、COREQ 清单、Kappa 计算器、流程图，都能直接拿走用。

## 📦 内容结构

```
qualitative-research/
├── SKILL.md                       # 技能主文件（触发与导航）
├── references/                    # 七份方法学详解（核心知识库）
│   ├── 01-research-design.md      # 范式·方法学家谱·研究问题打磨
│   ├── 02-sampling.md             # 目的/理论抽样·样本量·信息丰富度
│   ├── 03-data-collection.md      # 访谈提纲·焦点小组·转录·伦理
│   ├── 04-coding-grounded-theory.md  # 扎根理论三流派·开放/主轴/选择性编码
│   ├── 05-coding-thematic.md      # Braun & Clarke 六步主题分析·内容分析
│   ├── 06-reliability-validity.md # Cohen's Kappa·NVivo编码比较·饱和·信实度
│   └── 07-reporting.md            # COREQ/SRQR·引语呈现·章节写作
├── diagrams/                      # 流程图与模型图（Mermaid，GitHub 直接渲染）
│   ├── grounded-theory.md         # 扎根理论编码流程·三级编码漏斗·模型结构模板
│   ├── thematic-analysis.md       # 主题分析六步·编码→主题层级·方法决策图
│   └── index.html                 # 离线渲染页，双击查看全部流程图并截图
├── templates/                     # 即用模板（填空即用）
│   ├── interview-guide-template.md   # 半结构访谈提纲
│   ├── codebook-template.md          # 编码簿
│   ├── coreq-checklist.md            # COREQ 32 项自检表
│   └── consent-form-template.md      # 知情同意书
└── tools/
    └── kappa-calculator/          # 离线 Kappa 一致性计算器（双击即用，无需联网）
        ├── index.html
        └── 使用说明.md
```

## 🧩 七大阶段能帮你做什么

| 阶段 | 你可以让 AI 做的事 | 对应文档 |
| --- | --- | --- |
| **1 研究设计** | 选范式（建构主义/后实证/批判/实用）、匹配方法学（扎根/现象学/个案/民族志/叙事/话语）、把宽泛兴趣收敛成可研究的 RQ | `01` |
| **2 抽样** | 设计目的/理论/最大差异抽样、用"信息丰富度"估样本量、写抽样论证段落 | `02` |
| **3 数据收集** | 生成不诱导的半结构访谈提纲、焦点小组脚本、探询问题、转录规范、伦理与知情同意 | `03` + 模板 |
| **4 编码分析** | 扎根理论三级编码、主题分析六步、内容分析；从语料起草初始码、归并范畴、抽提主题、建编码簿 | `04` `05` + `diagrams` |
| **5 信度效度** | 判断要不要报 ICR、算/解读 Cohen's Kappa、判定理论饱和、用 Lincoln & Guba 四标准做信实度论证 | `06` + Kappa 计算器 |
| **6 报告写作** | 按 COREQ/SRQR 自检、组织引语证据（含反例）、起草方法与发现章节、画概念模型 | `07` + 模板 |
| **7 可视化** | 生成扎根理论模型图、主题分析流程图，替换成你自己的范畴/主题 | `diagrams` |

## 🚀 安装与使用

### 方式一：作为 Claude Code 个人技能（推荐）
```bash
# 克隆到 Claude Code 的 skills 目录
git clone https://github.com/maydengximin-sketch/qualitative-research-skill.git \
  ~/.claude/skills/qualitative-research
```
Windows（PowerShell）：
```powershell
git clone https://github.com/maydengximin-sketch/qualitative-research-skill.git "$env:USERPROFILE\.claude\skills\qualitative-research"
```
之后在 Claude Code / Claude 里直接用自然语言提问，它会自动识别并加载本技能（无需手动 import）。

### 方式二：只用 Kappa 计算器
不装 Skill 也能用。直接双击 `tools/kappa-calculator/index.html`，**离线、无需联网**。支持四种输入：四格数值粘贴、逐条编码、NVivo 四格百分比、手动混淆矩阵，自动生成「可直接写进报告的文字」（含 κ、Po、Pe、有效样本数）。

### 方式三：直接取用流程图与模板
- `diagrams/` 下是扎根理论、主题分析的全套流程图（Mermaid 编写，GitHub 页面直接渲染）。双击 `diagrams/index.html` 可离线查看并截图，用于论文配图或科普分享。
- `templates/` 下的访谈提纲、编码簿、COREQ 清单、知情同意书，复制走替换 `【】` 占位即可。

## 💬 真实使用场景示例

把下面这些话直接发给装了本 Skill 的 Claude：

```text
· 帮我给"县域中学生短视频使用与自我认同"设计一份半结构访谈提纲
· 我有 12 份访谈转录，想建一个理论模型，该走扎根理论还是主题分析？怎么编码？
· 审稿人要我报编码一致性，帮我算 Kappa 并写进方法部分（我有两人编码的四格数据）
· 我访谈了 15 个人，怎么向审稿人论证已经达到理论饱和？
· 按 COREQ 32 项帮我逐条自检这份稿子，指出缺了哪些
· 帮我把这 8 个初始编码归并成范畴，并画出扎根理论模型图
· 我的研究是建构主义取向，到底要不要报编码者间信度？
```

## 🧭 七条贯穿全程的设计原则

1. **方法与问题匹配优先**——先定范式与方法学，再谈技术；不默认所有质性研究都用扎根理论。
2. **区分方法学与方法**——扎根理论是方法学，访谈是方法，不混用。
3. **编码服从分析目标**——描述性研究做主题/内容分析即可，不必硬套"建理论"。
4. **信度服从范式**——建构主义重信实度（trustworthiness），不无差别要求报 Kappa。
5. **饱和是过程不是数字**——要给判定证据，而非"访谈了 N 人所以饱和"。
6. **引语是证据不是装饰**——每个主题配代表性引语、标编号、含反例，反对 cherry-picking。
7. **全程反身性**——记录研究者立场、预设及其对编码的影响。

## 📚 方法学渊源（部分）

Creswell & Poth · Charmaz · Corbin & Strauss · Glaser & Strauss · Braun & Clarke · Patton · Malterud · Lincoln & Guba · Cohen · Landis & Koch · Tong et al.(COREQ) · O'Brien et al.(SRQR) · 陈向明 · 贾旭东。各文档末尾附具体文献条目。

## ❓ 常见问题 FAQ

**Q：我不是计算机背景，会用吗？**
A：会。装好后用大白话提问即可，不需要写代码。Kappa 计算器和流程图甚至双击就能用。

**Q：它能替代导师/方法书吗？**
A：不能。它帮你少走弯路、对齐规范，但最终方法决策与学术责任仍在你和导师。见免责声明。

**Q：只支持中文吗？**
A：默认中文交流与产出；涉及英文期刊投稿时会给中英术语对照、可产出英文方法段落。

**Q：扎根理论和主题分析到底怎么选？**
A：要"建新理论/讲机制"走扎根理论；只要"系统提炼主题"用主题分析。`diagrams/thematic-analysis.md` 里有一张决策图。

**Q：我的范式是建构主义，审稿人非要 Kappa 怎么办？**
A：`06` 文档专门讲了这个张力与应对（改用编码可靠性 TA 路径或在方法部分说明立场）。

## ⚠️ 免责声明

本技能包提供方法学指引与模板，**不替代**你所在学科/期刊/伦理委员会的具体规范，也不替代导师指导。Kappa 计算器与文档力求准确，但请以你目标期刊与统计教材为准。最终方法决策与学术责任由研究者承担。

## 🤝 贡献

欢迎 Issue / PR：补充方法学流派、修订阈值、增加模板与流程图、改进翻译、报告错别字。学术圈一起把它打磨得更好。

## 📄 许可

[MIT](./LICENSE) — 自由使用、修改、分发，保留版权声明即可。

---

## ☕ 赞赏支持

如果这个项目帮你少翻了几次方法书、少踩了几个审稿坑，欢迎请主包喝杯咖啡 ☕
**创作不易，你的一杯咖啡是我继续更新的动力～**（完全自愿，点个 ⭐ Star 就更开心啦）

| 支付宝 | 微信支付 |
| :---: | :---: |
| <img src="assets/alipay.jpg" width="240" alt="支付宝收款码"> | <img src="assets/wechat.jpg" width="240" alt="微信收款码"> |
| 秘境瑰宝 Mystery Realm | May |

> 也欢迎 Star ⭐ / Fork 🍴 / 分享给同样在做质性研究的同学，这对开源项目同样是莫大的支持 🙏
