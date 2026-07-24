# 1. 理解企业调查工作流（Understanding Today's Investigation Workflow）

## 研究目标（Research Objective）

在定义产品方案之前，首先需要回答一个问题：

> **企业调查人员（Investigator）今天究竟是如何完成一项调查工作的？**

相比直接分析某一款调查产品，本章节更加关注真实业务场景中的调查流程，理解法务、合规、反欺诈及金融犯罪调查团队的实际工作方式。

本次研究主要围绕以下四个问题展开：

- 企业调查通常由什么事件触发？
- 调查员如何收集、组织和分析证据？
- 调查过程中哪些环节最耗费时间？
- 哪些工作最适合借助 AI 提升效率？

本研究的目标并非直接寻找产品功能，而是深入理解用户的工作方式（Workflow）、行为模式（Behavior）以及决策过程（Decision Making），为后续产品设计原则（Design Principles）、产品需求（Product Requirements）以及 MVP 定义提供依据。

---

## 研究资料来源（Research Sources）

| 来源 | 研究重点 |
|------|---------|
| Thomson Reuters Institute《Evolving Risk in the Changing Landscape of Corporate Investigations》 | 企业调查工作流程的发展趋势 |
| Thomson Reuters《CLEAR Investigate》 | AI 在企业调查中的应用实践 |
| Deloitte《Conducting Remote Investigations》 | 数字证据收集与远程调查实践 |

---

# 关键发现一

## 企业调查并不是从搜索开始，而是从案件开始。

### Evidence（事实）

公开行业实践表明，企业调查通常由具体业务事件触发，而不是一次信息搜索。

常见触发场景包括：

- 欺诈预警（Fraud Alert）
- 举报（Whistleblower Report）
- 合规违规（Compliance Violation）
- AML 风险监测
- 监管调查
- HR 内部投诉

正式开展调查之前，调查员首先需要明确：

- 为什么启动本次调查？
- 调查目标是什么？
- 调查范围是什么？
- 涉及哪些部门和利益相关方？

信息搜索只是整个调查流程中的一个环节，而不是调查工作的起点。

### Insight（洞察）

企业调查本质上是一项**目标驱动（Goal-driven）**的工作，而不是一次信息检索任务。

真正驱动调查流程的是业务背景（Business Context），而非搜索行为本身。

### Design Principle（设计原则）

产品设计应首先帮助调查员理解案件，而不是立即开始搜索。

### Product Requirement（产品需求）

提供统一的 **Case Workspace（案件工作台）**，支持调查目标、调查范围、关键利益相关方及调查假设的管理，为后续调查建立统一的工作上下文（Context）。

---

# 关键发现二

## 调查员最大的成本来自证据收集，而不是证据分析。

### Evidence（事实）

现代企业调查需要从大量不同系统收集数字证据。

典型数据来源包括：

**结构化数据**

- ERP
- CRM
- 财务系统
- HR 系统

**非结构化数据**

- Email
- Microsoft Teams
- Slack
- PDF
- 云盘
- 手机设备

随着企业数字化程度不断提高，调查员需要频繁切换多个系统，完成证据定位、导出和整理，大量时间消耗在正式分析之前。

### Insight（洞察）

当前调查工作的主要瓶颈已经不是缺少数据，而是证据过于分散。

调查员真正消耗时间的不是分析，而是跨系统寻找、整理和统一证据。

### Design Principle（设计原则）

证据必须先统一，才能开始分析。

### Product Requirement（产品需求）

建立统一的 **Evidence Workspace（证据工作台）**，集中管理来自不同业务系统的调查证据，减少跨系统切换，提高调查效率。

---

# 关键发现三

## 在分析之前，调查员首先需要组织证据。

### Evidence（事实）

完成证据收集后，调查员需要进一步确认不同系统中的数据是否属于同一调查对象，以及这些对象之间存在怎样的关联关系。

典型工作包括：

- 身份核验（Identity Verification）
- 实体匹配（Entity Matching）
- 重复记录消除（Duplicate Resolution）
- 关系分析（Relationship Analysis）
- 交叉验证（Cross-reference Validation）

调查员很少直接分析单个文档，而是不断建立证据之间的联系，逐步还原事件全貌。

### Insight（洞察）

调查分析的前提不是拥有更多证据，而是建立可信的证据组织结构。

只有完成证据组织，调查员才能开展有效推理。

### Design Principle（设计原则）

证据必须先完成组织，再进行推理。

### Product Requirement（产品需求）

产品应支持统一的证据组织机制，将来自不同数据源的信息组织为相互关联的调查对象，为后续调查分析提供可靠基础。

---

# 关键发现四

## 企业调查最终输出的是基于证据的推理，而不是文档摘要。

### Evidence（事实）

完成证据组织后，调查员需要进一步分析案件，并形成最终调查结论。

典型分析内容包括：

- 时间线重建（Timeline Reconstruction）
- 行为模式分析（Behaviour Pattern Analysis）
- 关系解释（Relationship Interpretation）
- 矛盾证据验证（Contradictory Evidence Verification）
- 风险评估（Risk Assessment）

调查结束后，最终交付的是一份具有完整证据支撑的调查报告，包括：

- 调查结论
- 证据来源
- 审计记录
- 可追溯依据

这些成果需要能够接受法律、监管及企业内部审计。

### Insight（洞察）

企业调查的目标并不是生成一段 AI 回答，而是将分散证据转化为能够支撑业务决策的调查结论。

专业判断始终属于调查员，AI 的价值在于帮助调查员完成复杂推理，而不是替代调查员作出决策。

### Design Principle（设计原则）

AI 应增强调查推理能力，而不是替代专业判断。

### Product Requirement（产品需求）

产品应支持调查推理过程，帮助调查员完成事件重建、证据综合分析以及调查报告生成，同时确保所有 AI 输出均具备可解释性（Explainability）和可追溯性（Traceability）。

---

# 企业调查工作流总结（Investigation Workflow Summary）

综合公开行业实践资料，可以归纳出现代企业调查工作的典型流程：

```text
案件受理（Case Intake）
        ↓
证据收集（Evidence Collection）
        ↓
证据组织（Evidence Organisation）
        ↓
调查推理（Evidence Reasoning）
        ↓
调查报告（Investigation Report）
        ↓
决策支持（Decision Support）
```

虽然不同企业的调查场景存在差异，但整体工作流程具有高度一致性。

调查工作的核心并不是不断搜索信息，而是持续收集、组织、验证和推理证据，最终形成能够支撑业务决策的调查结论。

---

# 产品设计启示（Key Design Takeaways）

本次研究表明，企业调查本质上是一项以证据为中心（Evidence-centric）的工作，而不是以搜索为中心（Search-centric）的工作。

围绕真实调查流程，可以归纳出四项核心产品设计原则：

1. 调查应从案件背景开始，而不是从搜索开始。
2. 证据必须先统一，才能开展分析。
3. 证据必须先完成组织，才能进行推理。
4. AI 应增强调查员的专业判断，而不是替代调查员完成决策。

上述设计原则将作为后续 Product Discovery 的基础，并进一步推导出产品需求（Product Requirements）、MVP 定义以及最终的 **Evidence Intelligence Platform** 产品方案。


# 2. 为什么是现在？（Why Now）

## 研究目标（Research Objective）

第一章回答了：

> **调查员今天是如何完成企业调查工作的？**

而本章节希望进一步回答另一个关键问题：

> **为什么现在值得构建一款 AI 原生的企业调查产品？**

企业调查并不是一个新行业，但企业所面临的数据环境、AI 技术能力以及风险管理模式正在快速变化。

本次研究旨在理解这些行业变化如何共同推动下一代企业调查产品的发展，并判断当前是否已经具备产品落地的最佳时机（Product-Market Timing）。

重点关注四个问题：

- 企业调查行业正在发生哪些变化？
- 为什么传统调查工具开始无法满足需求？
- AI 为什么能够在当前阶段真正进入调查工作流？
- 新一代调查产品的市场机会来自哪里？

这些分析将帮助我们进一步定义产品定位（Product Positioning）和产品价值主张（Value Proposition）。

---

## 研究资料来源（Research Sources）

| 来源 | 研究重点 |
|------|---------|
| Gartner《How to Evaluate the Applicability of Knowledge Graphs for Your Use Cases》 | Knowledge Graph 在复杂关系发现中的价值 |
| Gartner《Bring Knowledge and Trust to Generative AI with GraphRAG》 | GraphRAG 如何提升 AI 的可信度与知识推理能力 |
| Thomson Reuters《Beyond Prevention: The Convergence of Detection, Investigation & Organizational Strategy》 | 企业调查的发展趋势 |
| Thomson Reuters《2026 AI in Professional Services Report》 | AI 在专业服务行业的发展趋势 |

---

# 关键变化一

## 企业风险管理正从"风险预防"走向"持续调查"。

### Evidence（事实）

过去，企业风险管理主要围绕风险预防（Prevention）展开，例如身份认证、黑名单管理和访问控制。

随着欺诈行为日益复杂，越来越多企业开始构建覆盖：

- Prevention（预防）
- Detection（检测）
- Investigation（调查）
- Response（响应）

的完整风险管理体系。

调查不再只是事后处理，而逐渐成为企业持续风险管理的重要组成部分。  [oai_citation:0‡Thomson Reuters](https://www.thomsonreuters.com/en-us/posts/corporates/beyond-prevention-fraud-investigation/?utm_source=chatgpt.com)

### Insight（洞察）

企业真正需要的不再是单点工具，而是一条贯穿风险发现、调查分析和决策支持的完整工作流。

调查能力正在成为企业风险管理体系中的核心能力，而不仅仅是支持功能。

### Design Principle（设计原则）

产品应围绕完整调查流程进行设计，而不是解决单一环节的问题。

### Product Requirement（产品需求）

产品定位应支持完整 Investigation Workflow，而不仅仅提供信息检索能力。

---

# 关键变化二

## 企业拥有越来越多的数据，却越来越难形成知识。

### Evidence（事实）

企业数字化不断推进，大量业务数据来自 CRM、ERP、协同办公平台、邮件系统以及第三方数据源。

与此同时，Gartner 指出，当业务场景涉及复杂实体关系和语义关联时，仅依赖传统数据库或关键词搜索已经难以满足需求，Knowledge Graph 更适用于知识整合、关系发现和复杂推理等场景。  [oai_citation:1‡Gartner](https://www.gartner.com/en/documents/5411463?utm_source=chatgpt.com)

Thomson Reuters 进一步提出，未来企业竞争优势来自于将数据（Data）转化为信息（Information），进一步形成知识（Knowledge），最终支撑业务决策。  [oai_citation:2‡Thomson Reuters](https://www.thomsonreuters.com/en-us/posts/corporates/beyond-prevention-fraud-investigation/?utm_source=chatgpt.com)

### Insight（洞察）

企业真正缺少的并不是数据，而是能够持续将分散证据组织成知识的能力。

未来企业调查产品竞争的重点，将从 **Search** 转向 **Knowledge**。

### Design Principle（设计原则）

产品应帮助用户构建知识，而不仅仅提供答案。

### Product Requirement（产品需求）

产品需要支持 Evidence → Knowledge 的持续转化过程，帮助调查员建立可复用、可积累的调查知识。

---

# 关键变化三

## 企业 AI 正从聊天工具走向专业工作流。

### Evidence（事实）

过去两年，生成式 AI 已快速进入企业应用。

与此同时，越来越多企业开始发现，通用聊天机器人虽然能够回答问题，却难以满足法律、金融、合规等高风险行业对于可信度、上下文、工作流管理以及审计要求。

AI 正逐渐从 Chatbot 演变为 Workflow AI，并进一步向 Agentic AI 发展，深度参与专业工作流程。  [oai_citation:3‡Thomson Reuters](https://www.thomsonreuters.com/content/dam/ewp-m/documents/thomsonreuters/en/pdf/reports/2026-ai-in-professional-services-report.pdf?utm_source=chatgpt.com)

### Insight（洞察）

企业采购 AI，不再只是购买一个能够回答问题的大模型。

真正创造价值的是能够参与专业工作流、理解业务上下文并持续协助完成复杂任务的 AI。

### Design Principle（设计原则）

产品应围绕 Workflow，而不是围绕 Chat Interface 设计。

### Product Requirement（产品需求）

产品需要深度嵌入企业调查流程，而不是作为独立聊天助手存在。

---

# 关键变化四

## 企业越来越重视可信 AI，而不仅仅关注模型能力。

### Evidence（事实）

随着 AI 被应用于法律、金融、监管等高风险行业，企业越来越关注：

- Explainability（可解释性）
- Traceability（可追溯性）
- Transparency（透明性）
- Governance（治理）

Thomson Reuters 提出的 **Fiduciary-Grade AI** 强调，高风险 AI 必须建立在权威数据、透明推理和可验证证据基础之上，而不仅仅追求生成速度或模型能力。  [oai_citation:4‡Thomson Reuters](https://www.thomsonreuters.com/en/press-releases/2026/may/thomson-reuters-standard-for-high-stakes-ai?utm_source=chatgpt.com)

### Insight（洞察）

未来企业采购 AI 产品时，信任将成为与模型能力同等重要的竞争因素。

尤其在调查场景中，AI 输出必须能够被验证、追溯和解释。

### Design Principle（设计原则）

可信性应成为产品架构的一部分，而不是后续增加的功能。

### Product Requirement（产品需求）

产品应支持完整的 Explainability、Traceability 与 Auditability，为调查结论提供可信依据。

---

# 市场机会总结（Market Opportunity Summary）

综合行业趋势可以发现，企业调查行业正在经历三个重要变化：

```text
Enterprise Risk
        ↓
Continuous Investigation
        ↓
Knowledge-driven Investigation
```

与此同时，企业 AI 产品的发展方向也在发生变化：

```text
Chatbot
      ↓
Copilot
      ↓
Workflow AI
      ↓
Agentic AI
      ↓
Domain-specific AI Platform
```

企业调查产品未来的竞争重点，将不再是谁能够提供更多搜索结果，而是谁能够帮助调查员持续将证据转化为知识，并最终支撑高质量业务决策。

---

# 产品机会（Product Opportunity）

结合第一章对用户工作流的分析以及本章节对行业趋势的研究，可以形成以下判断：

- 企业调查已从单次案件处理演变为持续性的风险管理能力。
- 企业拥有越来越多的数据，却缺少将数据持续沉淀为知识的能力。
- AI 正从通用问答工具走向深度参与专业工作流的智能协作者。
- 高风险行业对 AI 的要求已经从"会回答"升级为"可信、可解释、可审计"。

因此，我们认为下一代企业调查产品的核心价值，不应停留在 **AI Search**，而应进一步帮助调查员持续完成：

> **Evidence → Knowledge → Decision**

这也成为本项目提出 **Evidence Intelligence Platform** 的核心产品定位。

# 3. 现有产品如何解决这一问题？（How Existing Products Solve It）

## 研究目标（Research Objective）

前两章已经回答了两个问题：

> 用户今天如何完成企业调查？

以及：

> 为什么现在值得构建 AI 原生调查产品？

本章节进一步研究市场上的领先产品，希望回答第三个关键问题：

> **现有企业调查产品是如何解决这些问题的？**

相比传统竞品分析，本研究更加关注产品设计思路（Product Design Pattern），理解领先产品如何将 AI 引入调查工作流，以及哪些设计已经成为行业共识，哪些问题仍然没有得到有效解决。

重点关注四个问题：

- AI 如何融入调查工作流？
- 产品如何帮助调查员发现关系？
- AI 与调查员如何协同工作？
- 当前产品仍存在哪些产品机会？

这些分析将进一步帮助我们明确产品定位，并寻找差异化机会（Product Opportunity）。

---

## 研究资料来源（Research Sources）

| 来源 | 研究重点 |
|------|---------|
| Thomson Reuters CLEAR Investigate 产品官网 | Agentic AI 调查工作流与产品能力 |
| Thomson Reuters CLEAR Investigate Whitepaper | Agentic Investigation Workflow |
| Thomson Reuters《How to use Agentic AI Workflows in Professional Services》 | Agentic Workflow 设计思路 |

---

# 关键发现一

## AI 已经开始接管调查流程，而不仅仅负责回答问题。

### Evidence（事实）

最新一代调查产品已经从传统搜索工具演变为 Agentic AI Workflow。

以 CLEAR Investigate 为例，用户无需逐步搜索不同数据源，而是直接输入调查目标，AI 会自动：

- 制定调查计划
- 选择数据来源
- 搜索多个数据库
- 汇总调查结果
- 给出下一步建议

AI 不再只是回答问题，而是主动执行完整调查流程。 [oai_citation:0‡法律解决方案](https://legal.thomsonreuters.com/blog/clear-investigate-your-questions-answered/?utm_source=chatgpt.com)

### Insight（洞察）

企业调查产品正在从 Search Tool 演变为 Workflow Assistant。

真正创造价值的不再是搜索能力，而是 AI 对整个调查流程的自动编排能力。

### Design Principle（设计原则）

AI 应围绕完整工作流设计，而不是围绕聊天界面设计。

### Product Requirement（产品需求）

产品需要支持目标驱动（Goal-driven）的 Investigation Workflow，而不是单步问答。

---

# 关键发现二

## 关系发现（Relationship Discovery）已经成为调查产品的核心能力。

### Evidence（事实）

领先调查产品越来越强调自动发现人与人、人与企业、企业之间的关联关系。

例如：

- Associate Analytics
- Company Family Tree
- Connection Analysis
- Shortest Path Discovery

AI 可以自动识别隐藏关联，减少调查员跨系统交叉验证的工作量。 [oai_citation:1‡法律解决方案](https://legal.thomsonreuters.com/blog/how-agentic-tools-can-speed-up-your-investigative-workflow-in-clear/?utm_source=chatgpt.com)

### Insight（洞察）

调查员真正需要的不是更多搜索结果，而是自动发现证据之间的关系。

未来调查产品竞争的重点，将从 Document Search 转向 Relationship Intelligence。

### Design Principle（设计原则）

产品应帮助用户发现关系，而不仅仅提供数据。

### Product Requirement（产品需求）

产品应支持 Evidence Relationship Discovery，自动组织实体、事件与证据之间的关联关系。

---

# 关键发现三

## AI 正在增强调查员，而不是替代调查员。

### Evidence（事实）

领先产品普遍采用 Human-in-the-loop 模式。

AI 负责：

- 数据收集
- 信息整理
- 关系分析
- 初步总结

调查员负责：

- 判断调查方向
- 验证调查结果
- 最终业务决策

所有 AI 输出均保留完整来源和审计记录，确保调查过程透明、可信。 [oai_citation:2‡法律解决方案](https://legal.thomsonreuters.com/blog/clear-investigate-your-questions-answered/?utm_source=chatgpt.com)

### Insight（洞察）

企业调查属于高风险决策场景。

AI 的定位不是自动决策，而是增强调查员的专业能力。

### Design Principle（设计原则）

AI 应保持 Human-in-the-loop，而不是 Autonomous Decision。

### Product Requirement（产品需求）

产品需要支持人工确认、证据追溯和全过程审计，确保 AI 始终处于辅助角色。

---

# 关键发现四

## 现有产品提升了调查效率，但尚未沉淀组织知识。

### Evidence（事实）

现有调查平台大幅提升了：

- 数据搜索效率
- 多源信息整合
- 自动调查流程
- 调查报告生成

但调查结束后，大部分知识仍停留在单个案件。

案件之间缺乏知识复用，历史调查经验难以持续积累。

公开产品资料更多强调"更快完成调查"，较少涉及跨案件知识沉淀或持续学习能力。 [oai_citation:3‡法律解决方案](https://legal.thomsonreuters.com/en/products/clear-investigate?utm_source=chatgpt.com)

### Insight（洞察）

当前产品主要优化的是 Investigation Execution，而不是 Organizational Knowledge。

企业真正长期积累的资产并不是调查报告，而是调查知识。

### Design Principle（设计原则）

产品不仅应帮助完成调查，更应持续沉淀组织知识。

### Product Requirement（产品需求）

产品应支持 Evidence → Knowledge 的持续沉淀，构建可复用的企业调查知识体系。

---

# 产品设计总结（Product Design Summary）

领先企业调查产品已经形成四项共同设计模式：

```text
Workflow AI
        ↓
Relationship Discovery
        ↓
Human-AI Collaboration
        ↓
Trusted Investigation
```

这些设计共同推动企业调查从传统搜索工具演变为 AI 原生工作平台。

---

# 产品机会（Product Opportunity）

综合前三章研究可以发现：

- 第一章告诉我们：调查员如何工作。
- 第二章告诉我们：为什么现在值得做。
- 第三章告诉我们：领先产品已经验证了 Workflow AI 的方向。

然而，现有产品仍主要关注**调查执行效率（Execution）**。

对于企业而言，更大的长期价值来自于：

> **持续将案件证据沉淀为组织知识（Evidence → Knowledge）。**

因此，我们的产品定位不仅是一款 AI 调查工具，更希望构建一个能够持续积累调查经验、组织知识和推理能力的 **Evidence Intelligence Platform**。

# 4. 为什么这些能力可以实现？（Why Technically Feasible）

## 研究目标（Research Objective）

前面三个章节分别回答了：

- 用户今天如何完成企业调查？
- 为什么现在值得构建 AI 原生调查产品？
- 当前领先产品如何解决这一问题？

本章节进一步回答最后一个关键问题：

> **这些产品能力在今天是否具备工程可行性（Engineering Feasibility）？**

本研究并不关注具体模型的实现细节，而是从 AI Engineering 的角度分析：

- 每一项产品能力背后对应什么工程问题（Engineering Problem）？
- 当前学术界主要采用哪些研究方向进行解决？
- 这些研究是否已经具备成熟的工程基础，可以支撑企业级产品落地？

对于 AI Product Manager 而言，产品设计不需要发明新的模型，而需要理解：

> **每一个产品能力，本质对应 AI 工程团队正在解决的哪一个核心工程问题。**

---

## 研究资料来源（Research Sources）

| 来源 | 研究重点 |
|------|---------|
| Survey on Information Extraction | Information Extraction、NER、Relation Extraction、Event Extraction |
| A Survey on Knowledge Graphs: Representation, Acquisition and Applications | Knowledge Graph Construction 与 Knowledge Acquisition  [oai_citation:0‡Aalto University's research portal](https://research.aalto.fi/en/publications/a-survey-on-knowledge-graphs-representation-acquisition-and-appli/?utm_source=chatgpt.com) |
| A Survey of Knowledge Graph Reasoning | Graph Reasoning、Knowledge Graph Reasoning  [oai_citation:1‡DOI](https://doi.org/10.1109%2FTPAMI.2024.3417451?utm_source=chatgpt.com) |
| Temporal Knowledge Graph Completion: A Survey | Temporal Reasoning、Knowledge Graph Completion  [oai_citation:2‡ijcai.org](https://www.ijcai.org/proceedings/2023/734?utm_source=chatgpt.com) |

---

# 核心能力一

## Evidence Extraction & Mapping（证据抽取与映射）

### Engineering Problem（工程问题）

企业调查需要处理来自邮件、PDF、聊天记录、数据库、网页等大量异构数据。

这些数据天然缺乏统一结构，因此系统首先需要自动识别：

- 人（Person）
- 公司（Organization）
- 地点（Location）
- 时间（Time）
- 事件（Event）
- 实体之间的关系（Relation）

并将这些信息统一映射到标准化的数据表示。

这本质上属于 **Information Extraction（信息抽取）** 问题。

### Research Direction（研究方向）

学术界围绕 Information Extraction 已形成较成熟研究体系，主要包括：

- Named Entity Recognition（NER）
- Entity Linking（EL）
- Relation Extraction（RE）
- Event Extraction（EE）

近年来，大语言模型进一步提升了复杂文档、多源文本及开放领域信息抽取能力，使自动化证据抽取成为知识构建的重要基础。

### Representative Methods（代表方法）

- Transformer-based NER
- Relation Extraction
- Event Extraction
- Entity Linking

### Technical Feasibility（技术可行性）

Information Extraction 已成为 NLP 最成熟的研究方向之一。

目前已有大量成熟模型能够自动完成实体识别、关系抽取及事件抽取，为企业调查中的证据标准化提供稳定的工程基础。

### Product Implication（产品启示）

Evidence Workspace 可以建立在成熟的信息抽取能力之上，实现多源证据的自动解析与统一表示，而无需重新设计底层算法。

---

# 核心能力二

## Knowledge Graph Construction（知识图谱构建）

### Engineering Problem（工程问题）

完成证据抽取之后，系统仍然面对一个核心挑战：

> 如何将分散的证据组织为可持续推理的知识网络？

真正困难的并不是存储数据，而是建立实体之间的长期关联关系。

### Research Direction（研究方向）

对应的研究方向为：

Knowledge Graph Construction。

主要包括：

- Knowledge Acquisition
- Knowledge Fusion
- Knowledge Representation
- Knowledge Graph Completion

近年来，大语言模型进一步降低了知识图谱自动构建成本，使企业级知识组织成为现实。  [oai_citation:3‡Aalto University's research portal](https://research.aalto.fi/en/publications/a-survey-on-knowledge-graphs-representation-acquisition-and-appli/?utm_source=chatgpt.com)

### Representative Methods（代表方法）

- Knowledge Graph
- Graph Embedding
- Knowledge Fusion
- LLM-assisted Knowledge Graph Construction

### Technical Feasibility（技术可行性）

Knowledge Graph 已形成从知识获取、知识融合到知识演化的完整工程体系。

目前已有成熟方法能够自动构建跨文档、跨系统的知识网络，为复杂调查提供统一知识表示。

### Product Implication（产品启示）

Evidence Intelligence Platform 可以利用 Knowledge Graph 持续沉淀调查知识，而不仅仅保存单次调查结果。

---

# 核心能力三

## Timeline Reconstruction（事件时间线重建）

### Engineering Problem（工程问题）

调查过程中，大量事件来源于不同数据源，并具有不同时间粒度。

系统需要自动恢复：

- 什么时间发生了什么事件？
- 哪些事件存在因果关系？
- 哪些事件属于同一调查过程？

这属于 Temporal Reasoning（时间推理）问题。

### Research Direction（研究方向）

近年来，时间推理已成为知识图谱与事件理解的重要研究方向，包括：

- Temporal Knowledge Graph
- Temporal Reasoning
- Event Ordering
- Temporal Graph Learning

### Representative Methods（代表方法）

- Temporal Knowledge Graph
- Temporal Graph Network
- Event Ordering
- Sequence Modeling

### Technical Feasibility（技术可行性）

Temporal Reasoning 已广泛应用于法律分析、新闻事件追踪、医学事件分析等领域，能够自动恢复复杂事件的发展过程。  [oai_citation:4‡ijcai.org](https://www.ijcai.org/proceedings/2023/734?utm_source=chatgpt.com)

### Product Implication（产品启示）

Timeline Workspace 可以建立在成熟时间推理能力之上，帮助调查员快速重建案件全过程。

---

# 核心能力四

## Intelligent Correlation（智能关联分析）

### Engineering Problem（工程问题）

调查员真正关心的问题通常不是：

> "有哪些数据？"

而是：

> "这些证据之间隐藏着什么关系？"

系统需要自动发现跨实体、跨事件、跨案件之间的潜在关联。

这一问题本质属于 **Knowledge Graph Reasoning（知识图谱推理）**。

### Research Direction（研究方向）

目前主要研究方向包括：

- Graph Reasoning
- Multi-hop Reasoning
- Link Prediction
- Knowledge Graph Reasoning

### Representative Methods（代表方法）

- Graph Neural Network
- Multi-hop Reasoning
- Link Prediction
- Neural-symbolic Reasoning

### Technical Feasibility（技术可行性）

Knowledge Graph Reasoning 已成为知识图谱领域的重要研究方向，可支持复杂关系发现、多跳推理以及隐藏知识预测。  [oai_citation:5‡DOI](https://doi.org/10.1109%2FTPAMI.2024.3417451?utm_source=chatgpt.com)

### Product Implication（产品启示）

Relationship Discovery 可以建立在成熟图推理能力之上，实现跨案件、跨实体的智能关联分析。

---

# 核心能力五

## Evidence Gap Detection（证据缺口识别）

### Engineering Problem（工程问题）

调查过程中，系统不仅需要分析已有证据，还需要回答：

> 哪些关键证据仍然缺失？

如何自动识别调查中的信息缺口，并指导下一步调查方向，是企业调查中的重要工程问题。

### Research Direction（研究方向）

对应研究方向包括：

- Knowledge Graph Completion
- Missing Link Prediction
- Uncertainty Estimation
- Active Learning

近年来，大语言模型也逐渐参与复杂调查规划（Planning）和缺失信息推断任务。  [oai_citation:6‡ijcai.org](https://www.ijcai.org/proceedings/2023/734?utm_source=chatgpt.com)

### Representative Methods（代表方法）

- Knowledge Graph Completion
- Link Prediction
- Graph Completion
- LLM Planning

### Technical Feasibility（技术可行性）

Knowledge Graph Completion 已形成成熟研究体系，其核心目标就是预测知识图谱中的缺失实体和关系，为调查中的证据缺口识别提供了可靠工程基础。  [oai_citation:7‡ijcai.org](https://www.ijcai.org/proceedings/2023/734?utm_source=chatgpt.com)

### Product Implication（产品启示）

系统不仅能够帮助调查员分析已有证据，还能够主动提示调查缺口，辅助制定下一步调查计划。

---

# 工程成熟度总结（Engineering Readiness）

综合学术研究可以发现，Evidence Intelligence Platform 所需要的核心能力均建立在成熟 AI 工程方向之上：

```text
Evidence Extraction
        ↓
Knowledge Graph Construction
        ↓
Temporal Reasoning
        ↓
Knowledge Graph Reasoning
        ↓
Knowledge Graph Completion
```

这些能力分别对应 Information Extraction、Knowledge Graph、Temporal AI、Graph Reasoning 等成熟研究领域，并已形成较完善的方法体系和工程实践。

因此，本项目的技术创新重点并不在于发明新的 AI 模型，而在于：

> **将多个成熟 AI 能力整合为一条面向企业调查工作流的智能推理链路（Evidence → Knowledge → Reasoning → Decision）。**

这也进一步验证了 **Evidence Intelligence Platform** 在当前技术条件下具备较高的工程可行性（Engineering Feasibility）。