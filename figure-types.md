# Figure Types Reference

> Mapping of paper types → diagram structures, with visual design notes and failure analysis.  
> Source: 深度之眼（Deep Eye）2026-06-11 | Version 2.0

---

## Section 1 · Paper Type × Diagram Structure Master Table

| Paper Type | Typical Signals | Primary Diagram | Secondary Options | Visual Focus |
|-----------|----------------|-----------------|-------------------|-------------|
| **A · Method** | New model / framework / loss / training strategy | Method Overview / Model Architecture | Layered pipeline, Contrastive method | Core module hierarchy + information flow |
| **B · Mechanism** | Ablation, probing, attention, module analysis | Mechanism Zoom-in / Contrastive | Multi-panel, Ablation matrix | Innovation mechanism + before/after contrast |
| **C · Benchmark** | New dataset / evaluation suite / leaderboard | Evaluation Pipeline / Data Construction | Multi-panel comparison, Taxonomy tree | Task construction + metric aggregation |
| **D · Scaling Law** | Compute curves, performance trend, law fitting | Trend Panel / Experimental Matrix | Variable-relationship diagram | Variable relationships + design implications |
| **E · Robot / Embodied** | Perception-action loop, manipulation, navigation | **Closed-Loop Feedback Diagram** | System framework, State diagram | Full sensing→planning→acting→feedback cycle |
| **F · AI for X** | Medical AI, AI4Science, smart manufacturing, cybersecurity | Cross-domain Application Framework | System architecture with domain labels | Domain data + AI model + task + validation |
| **G · Survey** | Literature taxonomy, roadmap, comparison | Taxonomy Tree / Timeline / Comparison Matrix | Multi-panel historical overview | Coverage breadth + classification logic |

---

## Section 2 · 11 Diagram Types — Design Specifications

### 1. Method Overview (方法总览图)

**When to use**: Method papers that need to show the full pipeline from input to output.

**Structure**: Multi-stage horizontal or vertical flow with labeled modules.

**Visual rules**:
- Core innovation module(s): accent color background + larger text
- Support modules: neutral gray background
- Arrows: directional, labeled with data type/format where useful
- Avoid putting everything at equal visual weight

**Example papers**: Most NeurIPS/ICML method papers, e.g., Transformer variants, diffusion models

---

### 2. System Framework (系统框架图)

**When to use**: End-to-end systems with multiple distinct components or subsystems.

**Structure**: Layered or hierarchical blocks showing component relationships.

**Visual rules**:
- Group components by function with subtle background zones
- Interface/API boundaries shown as dashed lines or connectors
- Data storage shown as cylinder or stacked card symbols

**Example papers**: RAG systems, multi-agent frameworks, production ML pipelines

---

### 3. Model Architecture (模型架构图)

**When to use**: Neural network architectures where internal structure matters.

**Structure**: Layer-by-layer vertical or modular block diagram.

**Visual rules**:
- Encoders, decoders, attention heads shown as labeled blocks
- Skip connections and residuals shown as bypass arrows
- Dimensionality labels optional but encouraged for transformers

**Example papers**: ViT variants, U-Net variants, LLM architecture papers

---

### 4. Mechanism Diagram (机制示意图)

**When to use**: Papers where a specific sub-mechanism (e.g., attention, routing, gating) is the key contribution.

**Structure**: Zoom-in on a single module, showing internal operations step-by-step.

**Visual rules**:
- Use a "magnifying glass" visual metaphor to show zoom-in context
- Show the mechanism's input/output interface with the broader model
- Mathematical operations (softmax, cross-attention, etc.) shown symbolically, not as formulas

**Example papers**: Sparse attention, mixture-of-experts routing, new normalization methods

---

### 5. Closed-Loop Feedback Diagram (闭环反馈图)

**When to use**: Robots, embodied AI, RLHF, active learning — any system with cyclical feedback.

**Structure**: Circular or elliptical flow: Perceive → Understand → Plan → Act → Observe → repeat.

**Visual rules**:
- **Mandatory closed-loop arrow** — the cycle must visually close
- Environment/world shown as a distinct external element (e.g., background zone)
- Robot/agent shown as a central entity or icon
- Each loop phase labeled and color-coded

**Example papers**: RT-2, EmbodiedGPT, RLHF papers, autonomous driving systems

---

### 6. Multi-Panel Composite (多面板组合图)

**When to use**: Papers with multiple distinct contributions, modalities, or experimental settings.

**Structure**: 2×2, 3×1, or asymmetric panel grid.

**Visual rules**:
- Each panel has its own label (a), (b), (c)...
- Panels share a consistent color palette and font size
- Use thin borders or background zones to separate panels without heavy frames
- One panel should be visually dominant if there is a primary contribution

**Example papers**: Multi-modal papers, papers with qualitative + quantitative results combined

---

### 7. Experimental Trend Summary (实验规律总结图)

**When to use**: Scaling law papers, empirical analysis, hyperparameter sensitivity studies.

**Structure**: Trend line panels, scatter plots, or annotated curves.

**Visual rules**:
- Axes must be clearly labeled with units
- Key inflection points or law boundaries annotated with callout boxes
- Multiple curves: use distinct line styles AND colors (for print accessibility)
- Summary conclusion shown as a text box or banner at bottom

**Example papers**: Chinchilla scaling laws, LLM compute-optimal training, learning rate sensitivity

---

### 8. Evaluation Pipeline (评测流程图)

**When to use**: Benchmark papers, evaluation framework papers, metric design papers.

**Structure**: Sequential pipeline from raw data to final metrics/leaderboard.

**Visual rules**:
- Data source → preprocessing → task construction → model input → model output → metric computation → result aggregation
- Sample examples shown as small cards or thumbnails inline
- Metric formulas referenced symbolically (not typed out in full)

**Example papers**: MMLU, HumanEval, BenchmarkX papers, standardized evaluation frameworks

---

### 9. Contrastive Method Diagram (对比式方法图)

**When to use**: Papers that contrast the proposed method against prior work or baselines.

**Structure**: Left (prior approach) vs. Right (proposed approach), or Top vs. Bottom split.

**Visual rules**:
- Use consistent module notation across both sides for fair comparison
- Problems with prior method shown with warning icons or crossed-out elements
- Improvements in proposed method highlighted with green checkmarks or accent color
- Avoid making the prior method look "wrong" — it was state-of-the-art in its time

**Example papers**: Any paper with "unlike prior work..." structure in the intro

---

### 10. Data Construction Pipeline (数据构建流程图)

**When to use**: Dataset papers, data-centric AI papers, synthetic data generation papers.

**Structure**: Source → Collection/Crawling → Filtering → Annotation → Quality Control → Final Dataset.

**Visual rules**:
- Volume numbers (e.g., "120M samples") shown at each pipeline stage
- Filtering criteria shown as diamond decision nodes
- Human annotation shown as person icons
- Final dataset statistics summarized in a small table or badge

**Example papers**: LAION, DataComp, synthetic pretraining data papers

---

### 11. Cross-Disciplinary Application Framework (跨学科应用框架图)

**When to use**: Medical AI, climate AI, biology, chemistry, materials science + AI papers.

**Structure**: Domain-specific data zone + AI model zone + specialized task zone + impact/validation zone.

**Visual rules**:
- Domain data symbols must reflect the specific field (e.g., MRI scans, molecular graphs, sensor readings)
- AI component shown in the middle, clearly connected to domain inputs/outputs
- Clinical/scientific validation shown with domain-appropriate metrics (not just accuracy/F1)
- Application value or deployment context shown as the final output zone

**Example papers**: AlphaFold variants, medical image segmentation, climate downscaling

---

## Section 3 · Five Common Failure Modes

> From: 深度之眼 2026-06-11 analysis of AI-generated scientific figures

---

### Failure 1 · Abstract-Only Input

**Problem**: The abstract summarizes results, not structure. If you only give the AI an abstract, it will create random boxes connected by arrows with no logical basis.

**Fix**: Always include the method section, key module descriptions, or bullet-point contributions. The abstract alone is necessary but not sufficient.

**Prompt diagnosis**: If a user pastes only an abstract, respond:
> "I can start from the abstract, but the figure will be more accurate if you also provide the method section or describe the key modules and their relationships. Shall I proceed with the abstract, or can you add more?"

---

### Failure 2 · Vague Style Keywords

**Problem**: Words like "high-end", "sci-fi feel", "technology aesthetic", "advanced look" all push the model toward 3D renders, glowing lights, blue-black cyberpunk backgrounds, and holographic decorations — the opposite of academic quality.

**Fix**: Replace vague style words with specific venue/format references:
- ❌ "make it look high-end and technological"
- ✅ "IEEE TPAMI-style mechanism diagram: flat vector, white background, clean lines"
- ✅ "NeurIPS-quality method overview: 2D, functional color only, no decoration"

---

### Failure 3 · Paper Type Not Declared

**Problem**: Method papers, evaluation papers, and system papers have fundamentally different visual logic. If you don't specify the type, the AI defaults to a generic "left→center→right" flow, which is wrong for most paper types.

**Fix**: Always declare the paper type in the prompt, and use the matching Section B block from `prompt-template.md`. The SKILL.md Step 2 classifier should run before any prompt assembly.

---

### Failure 4 · Information Overload

**Problem**: Users sometimes think "more elements = higher quality". But top-venue figures are information-dense with a **clear visual storyline**, not cluttered. Overcrowded figures with 15+ modules, 30+ arrows, and full-paragraph labels are rejected in peer review.

**Fix**: Ask: "What is the one thing this figure must communicate?" Structure the visual around that single thread. Demote supporting modules to smaller or grayed-out elements. Move supplementary data to a caption or appendix.

**Capacity guideline**:
| Figure size | Max primary modules | Max arrows |
|------------|--------------------|-----------| 
| Single column | 5–7 | 6–10 |
| Full-page | 8–12 | 12–18 |

---

### Failure 5 · Decoration Overload

**Problem**: Academic figures signal quality through **order and restraint**: precise structure, correct symbols, generous whitespace, unified color logic. Not through gradients, shadows, glows, or textures.

**Fix**: Enforce the flat vector specification explicitly. If the model generates decorative elements, add a negative constraint:
```
禁止使用：3D透视、阴影、发光效果、渐变背景、霓虹色、纹理填充、商业海报风格元素
```

Or in English:
```
Prohibited: 3D perspective, drop shadows, glow effects, gradient backgrounds, 
neon colors, texture fills, commercial poster visual elements.
```

---

## Section 4 · Quick Diagnosis Flowchart

```
User provides paper content
         │
         ▼
Is it only an abstract?
    YES → Request method/modules first
    NO  ▼
         │
Classify paper type (A–G from Section 1)
         │
         ▼
Select diagram structure from column 3
         │
         ▼
Assemble prompt:
  Section A (base spec) + Section B (type augment) + user content
         │
         ▼
Run Five-Failure self-check (Section 3)
         │
         ▼
Generate image
         │
         ▼
Does result pass visual spec?
    NO → Identify failure mode → adjust prompt → regenerate
    YES → Deliver to user
```
