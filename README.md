# 质性研究全流程助手 · Qualitative Research Skill

> 一个面向 **Claude Code / Claude Agent** 的质性研究（定性研究）方法学技能包：从立题、抽样、访谈、编码，到信效度、报告，覆盖整条研究链路。工具中立，适配 NVivo / MAXQDA / ATLAS.ti 乃至纯手工编码。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
![Lang](https://img.shields.io/badge/lang-中文-blue)
![Type](https://img.shields.io/badge/Claude-Skill-8A2BE2)

## ✨ 这是什么

把"怎么做一项严谨的质性研究"沉淀成一个可被 AI 助手直接调用的 **Skill**。当你向 Claude 提出任何质性研究相关问题（设计访谈提纲、编码、算 Kappa、判断饱和、对照 COREQ……），它会自动加载对应的方法学文档，按学界规范帮你完成，而不是凭空作答。

适合：研究生、青年教师、做用户研究 / 政策文本分析 / 田野访谈的实践者。

## 📦 内容结构

```
qualitative-research/
├── SKILL.md                       # 技能主文件（触发与导航）
├── references/                    # 七份方法学详解
│   ├── 01-research-design.md      # 范式·方法学家谱·研究问题打磨
│   ├── 02-sampling.md             # 目的/理论抽样·样本量·信息丰富度
│   ├── 03-data-collection.md      # 访谈提纲·焦点小组·转录·伦理
│   ├── 04-coding-grounded-theory.md  # 扎根理论三流派·开放/主轴/选择性编码
│   ├── 05-coding-thematic.md      # Braun & Clarke 六步主题分析·内容分析
│   ├── 06-reliability-validity.md # Cohen's Kappa·NVivo编码比较·饱和·信实度
│   └── 07-reporting.md            # COREQ/SRQR·引语呈现·章节写作
├── templates/                     # 即用模板
│   ├── interview-guide-template.md   # 半结构访谈提纲
│   ├── codebook-template.md          # 编码簿
│   ├── coreq-checklist.md            # COREQ 32 项自检表
│   └── consent-form-template.md      # 知情同意书
└── tools/
    └── kappa-calculator/          # 离线 Kappa 一致性计算器（双击即用，无需联网）
        ├── index.html
        └── 使用说明.md
```

## 🚀 安装与使用

### 方式一：作为 Claude Code 个人技能
```bash
# 克隆到 Claude Code 的 skills 目录
git clone https://github.com/<your-name>/qualitative-research-skill.git \
  ~/.claude/skills/qualitative-research
```
Windows（PowerShell）：
```powershell
git clone https://github.com/<your-name>/qualitative-research-skill.git "$env:USERPROFILE\.claude\skills\qualitative-research"
```
之后在 Claude Code 里直接提问即可，例如：
- "帮我给'县域中学生短视频使用'设计一份半结构访谈提纲"
- "我有 12 份访谈，想建一个理论模型，怎么编码？"
- "审稿人要我报编码一致性，帮我算 Kappa 并写进方法部分"
- "怎么论证我的研究达到了理论饱和？"
- "按 COREQ 帮我自检这篇稿子"

### 方式二：只用 Kappa 计算器
直接双击 `tools/kappa-calculator/index.html`，离线可用。支持四种输入：四格数值粘贴、逐条编码、NVivo 四格百分比、手动混淆矩阵，自动生成可写进报告的文字。

## 🧭 设计原则

1. **方法与问题匹配优先**——先定范式与方法学，再谈技术。
2. **信度服从范式**——不无差别地要求所有研究报 Kappa；建构主义重信实度。
3. **饱和是过程不是数字**——要给判定证据。
4. **引语是证据不是装饰**——含反例，反对 cherry-picking。
5. **全程反身性**——记录研究者立场及其对编码的影响。

## 📚 方法学渊源（部分）

Creswell & Poth · Charmaz · Corbin & Strauss · Braun & Clarke · Patton · Lincoln & Guba · Cohen · Landis & Koch · Tong et al.(COREQ) · 陈向明 · 贾旭东。各文档末尾附具体文献。

## ⚠️ 免责声明

本技能包提供方法学指引与模板，**不替代**你所在学科/期刊/伦理委员会的具体规范，也不替代导师指导。最终方法决策与学术责任由研究者承担。

## 🤝 贡献

欢迎 Issue / PR：补充方法学流派、修订阈值、增加模板、翻译。

## 📄 许可

[MIT](./LICENSE) — 自由使用、修改、分发，保留版权声明即可。
