# CCF Figure

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Claude%20%7C%20Codex-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Version-2.0-brightgreen?style=flat-square" />
  <img src="https://img.shields.io/badge/Source-DeepShare%20深度之眼-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square" />
</p>

<p align="center">
  A skill for generating publication-ready scientific figures from AI/CS research papers.<br>
  Classify paper type first, then select the optimal diagram structure automatically.
</p>

---

<!-- Chinese version (default) -->
## 中文说明

<details open>
<summary>点击展开 / 收起</summary>

### 是什么

`CCF Figure` 是一个专门为 AI / 计算机科学领域的研究人员设计，帮助你将论文内容转化为**顶会顶刊级科研配图**的工具。

核心理念来自「深度之眼」2026年6月11日发布的文章《科研绘图提示词第二弹》：  
**先判断论文类型，再选择最合适的图示结构**，而不是千篇一律地套用“左输入-中模型-右输出”三段式模板。

### 支持平台

| 平台 | 使用方式 |
|-----|---------|
| **Claude** | 自动加载 Skill，直接对话即可生成图像 |
| **Codex** | 自动加载 Skill，生成完整提示词后调用 GPT Image 2 |

### 功能特性

- **自动分类**：识别 7 种论文类型（方法 / 机制 / 评测 / 规律 / 机器人 / 交叉 / 综述）
- **结构自选**：从 11 种图示结构中自动匹配最优布局
- **完整提示词**：内置中英文双语提示词模板，可直接复制使用
- **五大翻车预防**：内置 Self-Check 清单，避免 AI 绘图的常见错误
- **迭代协议**：标准化修改流程，最多 3 轮迭代

### 支持的论文类型 × 图示结构

| 论文类型 | 推荐图示结构 |
|--------|------------|
| A · 方法类 | 方法总览图 / 模型架构图 |
| B · 机制/分析类 | 机制示意图（局部放大）/ 对比式方法图 |
| C · 评测/基准类 | 评测流程图 / 数据构建流程图 |
| D · 规律发现类 | 实验规律总结图 / 实验矩阵图 |
| E · 机器人/具身智能 | **闭环反馈图**（感知→规划→执行→反馈） |
| F · 交叉方向 | 跨学科应用框架图 |
| G · 综述/位置 | 分类树 / 时间线 / 对比矩阵 |

### 视觉规范摘要

| 属性 | 规则 |
|-----|------|
| 背景 | 纯白 `#FFFFFF` 或极浅灰 `#F5F5F5` |
| 风格 | 二维扁平化矢量 — 禁止 3D 透视 / 霓虹渐变 / 装饰纹理 |
| 配色 | 功能性配色；最多 3 个色彩群组；强调色限橙 / 青绿 / 深蓝 |
| 文字 | 水平排布；最多 2 种字号；中文标签 + 英文专有名词 |
| 目标刊会 | NeurIPS, ICML, ICLR, CVPR, ACL, Nature MI, IEEE TPAMI 等 |

### 安装方式

```bash
# 方式一：克隆到用户级 skills 目录（推荐，所有项目通用）
git clone https://github.com/your-username/CCF-Figure \
  ~/.ccf-figure

# 方式二：克隆到项目级 skills 目录（仅当前项目可用）
git clone https://github.com/your-username/CCF-Figure \
  ./CCF-Figure
