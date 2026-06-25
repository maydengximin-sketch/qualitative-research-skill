# Qualitative Research Skill · 质性研究全流程助手

**🌐 English | [简体中文](./README.md)**

> A qualitative research **methodology skill pack for Claude Code / Claude Agent**: covering the whole research chain — from framing the question, sampling, interviewing, and coding, to reliability/validity and reporting. Tool-neutral; works with NVivo / MAXQDA / ATLAS.ti or pure manual coding.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
![Lang](https://img.shields.io/badge/lang-中文%20|%20English-blue)
![Type](https://img.shields.io/badge/Claude-Skill-8A2BE2)
![Stage](https://img.shields.io/badge/coverage-topic→manuscript-success)
![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen)

> For the grad student running interviews, coding transcripts, computing Kappa, and getting chased by reviewers for COREQ. It distills "how to do a rigorous qualitative study" into a skill pack an AI can call directly — one less trip to the methods textbook, one less pitfall.

---

## 📑 Table of Contents

- [What is this / what pain does it solve](#-what-is-this--what-pain-does-it-solve)
- [Why not just "ask the AI"](#-why-not-just-ask-the-ai)
- [Repository structure](#-repository-structure)
- [What the seven stages can do for you](#-what-the-seven-stages-can-do-for-you)
- [Install & use](#-install--use)
- [Real usage examples](#-real-usage-examples)
- [Seven design principles running through everything](#-seven-design-principles-running-through-everything)
- [Methodological lineage](#-methodological-lineage-partial)
- [FAQ](#-faq)
- [Disclaimer / Contributing / License](#-disclaimer)
- [☕ Support](#-support)

---

## ✨ What is this / what pain does it solve

The grind of qualitative research is rarely "not knowing how" — it's that **every step sends you back to the methods books to check standards and thresholds**:

- How do you phrase interview questions so they don't lead? How many people make a good focus group?
- Should this set of interviews use grounded theory or thematic analysis? How do they differ?
- The three coding levels keep blurring — open codes, categories, core category, who's who?
- Reviewers want "inter-rater reliability" — how do you compute Kappa, should you even report it, what threshold?
- Does "20 interviews" count as saturation? How do you prove saturation to a reviewer?
- Submission requires the COREQ 32-item checklist — going line by line is tedious.

This Skill distills all of the above into **structured methodology documents + templates + tools + diagrams**, so the AI assistant **automatically loads the relevant standards when you ask**, instead of "roughly answering" from training memory.

**Who it's for**: master's / PhD students, early-career faculty, and practitioners doing user research · policy-text analysis · field interviews · content analysis — plus anyone wanting to systematically shore up their qualitative methods.

## 🤔 Why not just "ask the AI"

Asking a general AI directly tends to produce three problems: ① mixing up method terminology (treating "thematic analysis" as a methodology); ② indiscriminately telling you to report Kappa (which a constructivist paradigm shouldn't); ③ misremembering or fabricating thresholds / references.

What makes this Skill different:

- **Paradigm-first reasoning**: it first helps you pin down paradigm and methodology, then decides on technique — e.g. it **won't mindlessly tell you to compute Kappa**, but first checks whether you're on a constructivist path.
- **Traceable**: each document ends with real canonical references (Charmaz, Braun & Clarke, Lincoln & Guba, the original COREQ paper…), not empty claims.
- **Comes with usable deliverables**: interview guides, codebooks, consent forms, the COREQ checklist, a Kappa calculator, flow diagrams — all ready to take and use.

## 📦 Repository structure

```
qualitative-research/
├── SKILL.md                       # Skill main file (triggers & navigation)
├── references/                    # Seven methodology deep-dives (core knowledge base)
│   ├── 01-research-design.md      # Paradigms · methodology lineage · refining the RQ
│   ├── 02-sampling.md             # Purposive/theoretical sampling · sample size · information richness
│   ├── 03-data-collection.md      # Interview guides · focus groups · transcription · ethics
│   ├── 04-coding-grounded-theory.md  # Grounded theory's three schools · open/axial/selective coding
│   ├── 05-coding-thematic.md      # Braun & Clarke six-phase thematic analysis · content analysis
│   ├── 06-reliability-validity.md # Cohen's Kappa · NVivo coding comparison · saturation · trustworthiness
│   └── 07-reporting.md            # COREQ/SRQR · quote presentation · section writing
├── diagrams/                      # Flow & model diagrams (Mermaid, render directly on GitHub)
│   ├── grounded-theory.md         # GT coding flow · three-level coding funnel · model templates
│   ├── thematic-analysis.md       # Thematic six-phase · code→theme hierarchy · method decision tree
│   └── index.html                 # Offline render page — double-click to view all diagrams and screenshot
├── templates/                     # Ready-to-use templates (fill-in-the-blank)
│   ├── interview-guide-template.md   # Semi-structured interview guide
│   ├── codebook-template.md          # Codebook
│   ├── coreq-checklist.md            # COREQ 32-item self-check
│   └── consent-form-template.md      # Informed consent form
└── tools/
    └── kappa-calculator/          # Offline Kappa agreement calculator (double-click, no internet)
        ├── index.html
        └── 使用说明.md            # Usage notes (Chinese)
```

## 🧩 What the seven stages can do for you

| Stage | What you can have the AI do | Docs |
| --- | --- | --- |
| **1 Research design** | Choose a paradigm (constructivist/post-positivist/critical/pragmatic), match a methodology (grounded theory/phenomenology/case/ethnography/narrative/discourse), narrow a broad interest into a researchable RQ | `01` |
| **2 Sampling** | Design purposive/theoretical/maximum-variation sampling, estimate sample size via "information power", write the sampling rationale | `02` |
| **3 Data collection** | Generate non-leading semi-structured interview guides, focus group scripts, probes, transcription conventions, ethics & informed consent | `03` + templates |
| **4 Coding & analysis** | Grounded theory three-level coding, thematic six phases, content analysis; draft initial codes from data, merge categories, abstract themes, build a codebook | `04` `05` + `diagrams` |
| **5 Reliability & validity** | Decide whether to report ICR, compute/interpret Cohen's Kappa, determine theoretical saturation, argue trustworthiness via Lincoln & Guba's four criteria | `06` + Kappa calculator |
| **6 Reporting** | Self-check against COREQ/SRQR, organize quote evidence (incl. negative cases), draft Methods and Findings sections, draw a conceptual model | `07` + templates |
| **7 Visualization** | Generate grounded theory model diagrams and thematic analysis flow diagrams, swapped to your own categories/themes | `diagrams` |

## 🚀 Install & use

### Option 1: As a Claude Code personal skill (recommended)
```bash
# Clone into Claude Code's skills directory
git clone https://github.com/maydengximin-sketch/qualitative-research-skill.git \
  ~/.claude/skills/qualitative-research
```
Windows (PowerShell):
```powershell
git clone https://github.com/maydengximin-sketch/qualitative-research-skill.git "$env:USERPROFILE\.claude\skills\qualitative-research"
```
Then just ask in natural language in Claude Code / Claude — it auto-detects and loads this skill (no manual import). It works in both English and Chinese.

### Option 2: Just the Kappa calculator
No need to install the Skill. Double-click `tools/kappa-calculator/index.html` — **offline, no internet required**. It supports four input modes: 2×2 cell paste, item-by-item coding, NVivo four-cell percentages, and a manual confusion matrix, and auto-generates "text you can paste straight into your report" (incl. κ, Po, Pe, valid N).

### Option 3: Grab the diagrams and templates directly
- `diagrams/` holds the full set of grounded theory and thematic analysis flow diagrams (written in Mermaid, rendered directly on GitHub). Double-click `diagrams/index.html` to view offline and screenshot — for paper figures or explainer posts.
- The interview guide, codebook, COREQ checklist, and consent form under `templates/` — just copy and replace the `【】` placeholders.

## 💬 Real usage examples

Send these straight to a Claude that has this Skill installed:

```text
· Design a semi-structured interview guide for "short-video use and self-identity among county high-school students"
· I have 12 interview transcripts and want to build a theoretical model — grounded theory or thematic analysis? How do I code?
· A reviewer wants coding consistency reported — compute Kappa and write it into my Methods (I have two coders' 2×2 data)
· I interviewed 15 people — how do I argue to reviewers that theoretical saturation is reached?
· Self-check this manuscript against the COREQ 32 items and tell me what's missing
· Merge these 8 initial codes into categories and draw the grounded theory model diagram
· My study is constructivist — do I actually need to report inter-rater reliability?
```

## 🧭 Seven design principles running through everything

1. **Method–question fit first** — set paradigm and methodology before technique; don't default every qualitative study to grounded theory.
2. **Distinguish methodology from method** — grounded theory is a methodology, interviewing is a method; don't conflate them.
3. **Coding serves the analytic goal** — descriptive studies can use thematic/content analysis; no need to force "theory-building".
4. **Reliability serves the paradigm** — constructivism prizes trustworthiness; don't indiscriminately demand Kappa.
5. **Saturation is a process, not a number** — give evidence for the judgment, not "I interviewed N people so it's saturated".
6. **Quotes are evidence, not decoration** — each theme gets representative quotes, with IDs and negative cases; against cherry-picking.
7. **Reflexivity throughout** — record researcher positionality, assumptions, and their influence on coding.

## 📚 Methodological lineage (partial)

Creswell & Poth · Charmaz · Corbin & Strauss · Glaser & Strauss · Braun & Clarke · Patton · Malterud · Lincoln & Guba · Cohen · Landis & Koch · Tong et al. (COREQ) · O'Brien et al. (SRQR) · Chen Xiangming · Jia Xudong. Each document ends with specific reference entries.

## ❓ FAQ

**Q: I'm not from a computing background — can I use it?**
A: Yes. After installing, just ask in plain language; no coding needed. The Kappa calculator and diagrams even work on a double-click.

**Q: Can it replace my advisor / a methods textbook?**
A: No. It helps you avoid detours and align with standards, but the final methodological decisions and academic responsibility remain with you and your advisor. See the disclaimer.

**Q: Is it Chinese-only?**
A: No. It works in both English and Chinese — it talks and produces output in your language, and for English-journal submissions it gives bilingual terminology and can produce English Methods passages. (The core reference docs are currently written in Chinese; English contributions are welcome — see Contributing.)

**Q: Grounded theory vs. thematic analysis — how do I choose?**
A: Go grounded theory to "build new theory / explain mechanisms"; use thematic analysis to "systematically distill themes". There's a decision tree in `diagrams/thematic-analysis.md`.

**Q: My paradigm is constructivist but a reviewer insists on Kappa — what now?**
A: Doc `06` specifically addresses this tension and how to respond (switch to a coding-reliability TA path, or state your position in the Methods section).

## ⚠️ Disclaimer

This skill pack provides methodological guidance and templates. It **does not replace** the specific standards of your discipline / journal / ethics board, nor your advisor's supervision. The Kappa calculator and documents strive for accuracy, but defer to your target journal and statistics textbooks. Final methodological decisions and academic responsibility rest with the researcher.

## 🤝 Contributing

Issues / PRs welcome: add methodological schools, revise thresholds, add templates and diagrams, improve translations, report typos. Let's polish it together as a research community. **Help translating the reference docs into English is especially appreciated.**

## 📄 License

[MIT](./LICENSE) — free to use, modify, and distribute; just keep the copyright notice.

---

## ☕ Support

If this project saved you a few trips to the methods books or a few reviewer pitfalls, feel free to buy the maintainer a coffee ☕
**Creating this takes effort, and your coffee keeps the updates coming~** (Entirely voluntary — freeloading is totally fine; a ⭐ Star already makes my day.)

| Alipay | WeChat Pay |
| :---: | :---: |
| <img src="assets/alipay.jpg" width="240" alt="Alipay QR"> | <img src="assets/wechat.jpg" width="240" alt="WeChat Pay QR"> |
| 秘境瑰宝 Mystery Realm | May |

> Star ⭐ / Fork 🍴 / sharing with fellow qualitative researchers is just as much a help to an open-source project 🙏
