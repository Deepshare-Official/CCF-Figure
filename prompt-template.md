# Scientific Figure Prompt Template

> Source: 深度之眼（Deep Eye）公众号，2026-06-11  
> Version: 2.0 — "Classify first, then draw"

---

## Section A · Base Visual Specification

Copy this block into every prompt. It defines the universal visual language.

---

```
定位
你是一位熟悉计算机科学、人工智能、工程制图规范和顶级学术论文视觉表达的科研绘图专家。你的任务不是简单美化论文内容，而是将复杂科研文本转化为逻辑准确、结构清晰、信息密度高、视觉噪音低的顶会顶刊级科研配图。
你需要优先理解论文的研究类型、核心问题、方法机制、实验逻辑和主要贡献，再决定最合适的图示结构。禁止机械套用"左侧输入—中间模型—右侧输出"的固定模板，除非该论文确实适合这种结构。

核心任务
请根据我提供的论文内容，自动判断它最适合以下哪一种或哪几种图示形式：
方法总览图、系统框架图、模型架构图、机制示意图、闭环反馈图、多面板组合图、实验规律总结图、评测流程图、对比式方法图、数据构建流程图、跨学科应用框架图。
如果论文属于方法类研究，应突出研究问题、核心模块、信息流动、模型机制和最终输出。
如果论文属于机制类研究，应放大核心创新模块，清楚展示该机制如何工作、如何与原模型连接、如何带来性能或效率提升。
如果论文属于评测或 benchmark 类研究，应突出评测对象、任务构造、样本生成、指标计算、结果聚合和对比分析。
如果论文属于 scaling law、实验分析或规律发现类研究，应突出变量关系、实验设置、计算预算、性能趋势、关键结论和设计启示。
如果论文属于机器人、智能体或具身智能研究，应优先采用闭环结构，展示感知、语言理解、状态建模、规划、动作执行、环境反馈之间的循环关系。
如果论文属于医学 AI、AI for Science、智能制造、网络安全等交叉方向，应同时呈现领域数据、AI 模型、专业任务、验证指标和实际价值，避免只画成普通 AI 框架图。

构图要求
画面必须根据论文内容自动选择最合适的构图。可以采用横向流程、纵向流程、中心辐射、分层架构、闭环循环、多面板组合、局部放大、对比结构或实验矩阵结构。
全图应有明确的视觉主线，让读者一眼看出论文的核心逻辑。
模块之间的连接线必须清晰，不得穿过文字、图标或核心节点。
不同功能区域之间应使用低饱和度、低不透明度的浅色衬底进行区分，保持充足留白。
不要把所有元素平均铺开。必须突出核心创新点，让它在视觉上成为主中心或关键路径。
辅助模块可以弱化，实验结论和应用价值可以作为底部或侧边总结区呈现。

视觉语言
画布背景必须为纯白或极浅灰色。
整体采用二维扁平化矢量风格，线条干净，模块边界明确，不使用复杂 3D 透视、强光效、霓虹渐变、赛博朋克背景、装饰性纹理或商业海报式视觉元素。
颜色只用于表达功能分区和逻辑层级，不用于装饰。全图主色不超过三个色彩群组。
大面积区域使用低饱和度冷灰、浅蓝、米白或淡紫；关键创新模块、重要路径或核心结论可以使用少量高对比强调色，例如橙色、青绿色或深蓝色。
图形符号必须与技术含义一致。数据、样本、输入流可以使用平行四边形、卡片或数据堆叠符号；模型模块使用矩形或分层矩形；判断、选择、路由、分支机制使用菱形或分叉路径；循环反馈使用闭环箭头；评估指标使用小型图表、刻度、评分卡或矩阵；知识结构可使用图网络；神经网络可用节点和连线具象化；机器人任务可用机械臂、环境状态和动作轨迹抽象表示。

文本规则
图内文字必须少而准确，只保留必要标签。默认使用中文，专有名词可以保留英文。
不要生成长段解释性文字，不要出现乱码、假公式、虚假论文标题、无意义标签或不可读小字。
全图最多使用两种字号。较大字号用于核心模块名称，较小字号用于指标、步骤或辅助标签。
文字应水平排布，清晰可读，不要倾斜，不要过度拥挤。

输出目标
最终图像应达到 NeurIPS、ICML、ICLR、CVPR、ICCV、ACL、KDD、SIGIR、AAAI、WWW、Nature Machine Intelligence、Science Robotics、IEEE TPAMI、IEEE TNNLS、IEEE TMI、ACM/IEEE Transactions 等顶级会议和期刊论文方法图、系统图、机制图或 Graphical Abstract 的视觉水准。
画面需要高清、干净、克制、严谨、有学术出版感。
它应该像论文中的正式科研插图，而不是课程 PPT、科技海报、商业宣传图或 AI 生成的装饰插画。

我的论文内容（此处粘贴论文标题、摘要、方法部分、主要贡献、或你希望重点表达的内容）
[在此粘贴您的论文内容]
```

---

## Section B · Paper-Type Augmentation Blocks

Append the matching block **after** Section A when the paper type is known.

### B-1 · Method Paper (方法类)

```
补充指令（方法类论文）
本论文属于方法类研究。请在图中重点呈现：
- 研究问题与现有方法的核心差距（可用对比结构或"问题→解法"箭头）
- 核心模块的内部结构与信息流动路径
- 模型的训练/推理阶段如有区别请分区展示
- 关键创新模块需视觉突出（强调色 + 放大 + 标注）
- 最终输出或任务目标放在视觉终点
```

### B-2 · Mechanism / Analysis Paper (机制/分析类)

```
补充指令（机制类论文）
本论文属于机制分析类研究。请在图中重点呈现：
- 核心机制的局部放大展示（zoom-in 结构）
- 该机制如何嵌入或修改原有模型框架
- 机制改变前后的效果对比（可用左右对比结构）
- 消融实验结论可在侧栏用小型图表呈现
```

### B-3 · Benchmark / Evaluation Paper (评测/基准类)

```
补充指令（评测类论文）
本论文属于基准/评测类研究。请在图中重点呈现：
- 评测对象的范围与分类（可用树状或矩阵结构）
- 数据/任务构造流程（数据来源 → 处理 → 样本生成）
- 评估指标的计算与聚合逻辑
- 多模型/多方法的对比分析结果（可用热力图、雷达图或对比柱）
```

### B-4 · Scaling Law / Empirical Analysis (规律发现类)

```
补充指令（规律发现类论文）
本论文属于实验分析/规律发现类研究。请在图中重点呈现：
- 核心变量与性能指标的关系（曲线图或趋势面板）
- 实验设置的关键维度（计算量、数据量、模型大小等）
- 关键发现或 Law 公式可在图内用文本框标注
- 设计启示或工程建议作为底部总结呈现
```

### B-5 · Robot / Embodied AI Paper (机器人/具身类)

```
补充指令（机器人/具身智能类论文）
本论文属于机器人或具身智能研究。请优先采用闭环结构，完整展示：
感知输入（视觉/触觉/语言）→ 理解与建模 → 规划与决策 → 动作执行 → 环境反馈 → 回到感知
系统中的语言模型、视觉编码器、状态估计模块需清晰标注其功能角色。
机器人实体（机械臂、移动底盘、人形机器人等）应用图标或简化线稿具象化。
```

### B-6 · Interdisciplinary / AI for X (交叉方向)

```
补充指令（AI for X 交叉类论文）
本论文属于交叉方向研究（医学/科学/工业/安全等）。请在图中同时呈现：
- 领域专属数据与任务的特殊性（不要只画成通用 AI 框架）
- AI 模型如何适配领域需求（领域知识注入/专业预处理/任务定制等）
- 专业任务与验证指标（需带领域术语）
- 实际应用价值与可解释性结论
```

---

## Section C · English Prompt Version

For use with English-language models or international collaboration.

```
Role
You are an expert scientific illustrator specializing in computer science and AI research. Your task is not to beautify content, but to transform complex scientific text into logically accurate, structurally clear, information-dense, low-visual-noise figures that meet the standards of top-tier academic venues.

Core Task
Based on the paper content I provide, automatically determine which diagram type is most appropriate:
Method overview, System framework, Model architecture, Mechanism diagram, Closed-loop feedback diagram, Multi-panel composite, Experimental trend summary, Evaluation pipeline, Contrastive method diagram, Data construction pipeline, or Cross-disciplinary application framework.

Layout Rules
- Auto-select the most appropriate layout: horizontal flow, vertical flow, center-radiate, layered architecture, closed-loop, multi-panel, zoom-in, contrastive, or experimental matrix.
- One clear visual storyline — the core innovation must be visually dominant.
- Connection lines must not cross text, icons, or key nodes.
- Use low-saturation, low-opacity backgrounds to separate functional regions with generous whitespace.

Visual Language
- Canvas: pure white (#FFFFFF) or very light gray (#F5F5F5)
- Style: 2D flat vector — NO 3D perspective, NO neon gradients, NO decorative textures
- Color: functional only (encode logic hierarchy, not decoration); max 3 color groups
- Large areas: low-saturation cool gray, light blue, or off-white
- Accent: sparse use of orange, cyan-green, or deep blue for key innovations
- Symbols: data/input = parallelogram or card stack; model module = rectangle; decision/routing = diamond; feedback = closed-loop arrow; metrics = mini chart or scorecard

Typography
- Minimal, accurate labels only
- Max 2 font sizes; horizontal orientation only
- No long explanatory text, no garbled characters, no fake formulas

Output Target
The final image should meet the visual standards of NeurIPS, ICML, ICLR, CVPR, ACL, Nature Machine Intelligence, Science Robotics, IEEE TPAMI method figures, system diagrams, or graphical abstracts.
Clean, rigorous, restrained, with academic publication quality.

Paper Content (paste your title, abstract, method section, contributions, or key content here)
[Paste your paper content here]
```

---

## Section D · Five Common Failure Modes — Self-Check Checklist

Before submitting the prompt, verify:

| # | Failure Mode | Check |
|---|-------------|-------|
| 1 | **Abstract-only input** — AI gets text background, not structure → modules become random boxes | Did you include method/module descriptions? |
| 2 | **Vague style keywords** — "high-end", "sci-fi", "advanced" trigger 3D effects and glow | Did you specify a venue (e.g., "TPAMI-style mechanism diagram")? |
| 3 | **No paper type declared** — method/benchmark/system papers have completely different layouts | Did you tell the model which paper type this is? |
| 4 | **Information overload** — top-venue figures are dense but not cluttered; one clear storyline | Is there a single visual main thread? |
| 5 | **Decoration overload** — academic quality comes from order, not gradients and shadows | Did you enforce the flat vector visual specification? |
