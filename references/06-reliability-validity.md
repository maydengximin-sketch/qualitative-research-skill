# 06 · 信度与效度：Kappa、理论饱和、信实度

> **先判断范式再决定指标**。后实证/内容分析重"编码者间信度（Kappa）"；建构主义重"信实度（trustworthiness）"。不要无差别地对所有质性研究都要求 Kappa（见 `05` 对 reflexive TA 的说明）。

## 一、编码者间信度（Intercoder Reliability, ICR）

### 何时该报
- ✅ 内容分析、定向/演绎编码、编码可靠性 TA、团队编码、后实证范式、医学/政策类期刊常要求。
- ⚠️ 建构主义扎根理论、反思性主题分析：ICR 与其认识论有张力，可不报或仅作辅助；若期刊坚持，需在方法部分说明立场。

### Cohen's Kappa（两名编码者）
公式：
```
κ = (Po − Pe) / (1 − Pe)
```
- **Po** = 观察一致率（两人编码一致的比例）
- **Pe** = 期望一致率（随机情况下的一致率）

混淆矩阵（二分：某码"有/无"）：
| | B 判=有 | B 判=无 |
| --- | --- | --- |
| **A 判=有** | a (都有) | b (A有B无) |
| **A 判=无** | c (A无B有) | d (都无) |

- Po = (a + d) / N
- Pe = [(a+b)(a+c) + (c+d)(b+d)] / N²
- N = a+b+c+d

### Kappa 解读阈值（Landis & Koch 1977，最常引用）
| κ | 一致性 |
| --- | --- |
| < 0 | 比随机还差 |
| 0.01–0.20 | 轻微 Slight |
| 0.21–0.40 | 一般 Fair |
| 0.41–0.60 | 中等 Moderate |
| 0.61–0.80 | 高度 Substantial |
| 0.81–1.00 | 几乎完美 Almost perfect |

> 期刊一般要求 κ ≥ 0.70（部分领域 ≥ 0.80）。报告时**同时给出 κ、Po、Pe、有效样本数、类目定义**，不要只丢一个 κ 值。

### 注意事项
- **Kappa 悖论**：当某一类目极不均衡（绝大多数都判"无"）时，即使 Po 很高，κ 也可能偏低。此时应同时报 Po、考虑 PABAK 或 Gwet's AC1。
- 多于两名编码者：用 Fleiss' Kappa 或 Krippendorff's α（α 还能处理缺失值与多种测量尺度，传播学常用）。
- ICR 不是越高越好就万事大吉——它只说明编码可复制，不保证编码"有效/有意义"。

### 配套工具
本 skill 自带离线计算器：`tools/kappa-calculator/index.html`，双击打开即可，支持四种输入（四格数值粘贴 / 逐条编码 / NVivo 四格百分比 / 手动混淆矩阵），直接生成可写进报告的文字。

## 二、NVivo 实操：编码比较查询（Coding Comparison Query）

NVivo 内置按"参考点/字符"计算 Kappa 的功能：
1. 两名编码者各自在**独立的 User Profile** 下对同一批资料编码（NVivo 以用户区分编码者）。
2. `Explore（探索）→ Coding Comparison（编码比较查询）`。
3. 选择 User Group A、User Group B，选择要比较的节点（编码）与资料范围。
4. NVivo 输出每个节点的 **Kappa、Agreement(%)、A and B、Not A and Not B、A and not B、B and not A**。
5. 把这四格百分比粘进本 skill 的计算器可复核，或直接用 NVivo 的 κ。
- 阈值同上（≥0.70/0.80）。NVivo 默认按字符或参考点计算，方法部分需说明计算单位。
- MAXQDA：`分析 → 编码者间一致性`，可按段落/句子设容差，输出一致百分比与 Kappa。

> 你电脑里 `Kappa比较/` 下的 `字码编写比较查询.xlsx`、`NVivo9-Coding-Comparison-Calculation-Examples.xls` 即此流程的导出与算例。

## 三、理论饱和（Theoretical / Data Saturation）

饱和 = **继续收集数据不再产生新的范畴、主题或属性**，且范畴间关系已稳定。

### 判定要点（给证据，别拍数字）
1. **明确饱和类型**：
   - 数据饱和（data saturation）：不再有新码/新主题。
   - 理论饱和（theoretical saturation，扎根理论）：核心范畴的属性与维度发展完备、关系稳定。
2. **给出操作化证据**，例如：
   - 编码追踪表：记录每次访谈**新增码数**，展示其趋于 0（如第 12 次后无新码）。
   - 设定停止规则：连续 2–3 次访谈无新主题即判饱和。
3. **报告时写清**：在第几次访谈/第几组达到饱和、用什么标准判断、是否做了"确认性"访谈。

### 常见错误
- 只说"访谈了 N 人达到饱和"而无任何追踪证据。
- 把"问不出新东西"等同饱和，而忽略理论层面的范畴发展。
- 在描述性主题分析里硬套"理论饱和"——可改称"数据/主题饱和"或讨论"信息丰富度"。

## 四、信实度：Lincoln & Guba 四标准（建构主义范式的"效度"）

| 标准 | 对应实证概念 | 实现策略 |
| --- | --- | --- |
| 可信性 Credibility | 内部效度 | 长期投入、三角验证、成员校验(member checking)、同行汇报(peer debriefing)、反例分析 |
| 可迁移性 Transferability | 外部效度 | 厚描述(thick description)，让读者判断可否迁移 |
| 可靠性 Dependability | 信度 | 审计追踪(audit trail)、编码一致性、过程透明 |
| 可确认性 Confirmability | 客观性 | 审计追踪、反身性、把结论锚定到数据 |
| （+ 真实性 Authenticity） | — | 公平呈现多元声音、促成行动 |

### 三角验证（Triangulation）四类型
数据三角（多来源/时间/人群）、方法三角（访谈+观察+文档）、研究者三角（多编码者）、理论三角（多视角解读）。

## 五、研究者反身性（Reflexivity）
- 记录并报告研究者的立场、预设、与对象的关系如何影响数据生成与解释。
- 工具：反身性日记、立场声明（positionality statement）、备忘录。
- 在建构主义研究中，反身性是**效度的一部分**而非可有可无。

## 六、信效度自检清单
- [ ] 已根据范式选择了恰当的质量标准（ICR vs 信实度）
- [ ] 若报 ICR：给了 κ + Po + Pe + N + 类目定义 + 计算单位
- [ ] 饱和有可追溯证据（追踪表/停止规则）
- [ ] 至少落实 2–3 项信实度策略并在文中点明
- [ ] 有反身性/立场声明
- [ ] 有审计追踪（保留编码版本、备忘录、决策记录）

## 关键参考
- Cohen (1960). A coefficient of agreement for nominal scales.
- Landis & Koch (1977). The measurement of observer agreement.
- McHugh (2012). Interrater reliability: the kappa statistic.
- Lincoln & Guba (1985). *Naturalistic Inquiry*.
- Nowell et al. (2017). Thematic analysis: striving to meet the trustworthiness criteria.
- Saunders et al. (2018). Saturation in qualitative research.
