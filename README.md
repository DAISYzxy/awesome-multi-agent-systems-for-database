<h1 align="center">🗃️ Awesome Multi-Agent Systems for Database Papers</h1>

<p align="center">
  <strong>Multi-agent systems for data management, data preparation, and data analysis.</strong>
</p>

<p align="center">
  <a href="#data-management"><img src="https://img.shields.io/badge/Data_Management-6266A4?style=flat-square" alt="Data Management"></a>
  <a href="#data-preparation"><img src="https://img.shields.io/badge/Data_Preparation-258866?style=flat-square" alt="Data Preparation"></a>
  <a href="#data-analysis"><img src="https://img.shields.io/badge/Data_Analysis-B23C89?style=flat-square" alt="Data Analysis"></a>
</p>

> [!NOTE]
> A topic guide and paper list on **Multi-Agent Systems for Database (MAS for DB)**: using collaborating agents to perform data management, data preparation, and data analysis tasks.
>
> For the complementary direction, see [**Database for Multi-Agent Systems (DB for MAS)**](https://github.com/DAISYzxy/awesome-database-for-multi-agent-systems): how database and data-system techniques support efficient, correct, and reliable multi-agent collaboration.

## 📑 Contents

- [Introduction](#introduction)
- [Database Task Taxonomy](#task-taxonomy)
- [Paper List](#paper-list)
  - [Data Management](#data-management)
  - [Data Preparation](#data-preparation)
  - [Data Analysis](#data-analysis)
- [Related Foundations](#related-foundations)
- [Citation](#citation)

<a id="introduction"></a>

## 🎯 Introduction

**Multi-Agent Systems for Database** studies how collaborating agents perform database and data-system tasks across relational databases, data lakes, knowledge graphs, documents, and multimodal data.

**Current collection:** **52 distinct primary papers** across **27 populated task categories**, plus **3 related foundation papers**. Research and demonstration publications are counted separately; cross-task placements are counted once. The [per-paper review](SCREENING.md) records inclusion decisions, classification changes, sources, and evidence limits.

<a id="task-taxonomy"></a>

## 🧭 Database Task Taxonomy

The taxonomy builds on [Awesome Data Agents](https://github.com/HKUSTDial/awesome-data-agents) and expands it across the database lifecycle. Categories with no confirmed qualifying paper remain in this table.

| Perspective | Database task | Scope | Papers |
| --- | --- | --- | ---: |
| **Data Management** | **[M1. Configuration and Resource Tuning](#m1)** | Knob selection, configuration search, workload adaptation, resource sizing, deployment and cost tuning. | 3 |
| **Data Management** | **[M2. Physical Database Design](#m2)** | Index selection, materialized views, partitioning, clustering, storage layout and compression. | 2 |
| **Data Management** | **[M3. Query Rewriting and Plan Optimization](#m3)** | Equivalent SQL rewriting, rule discovery, join ordering, hint selection, plan search, cardinality and cost estimation. | 1 |
| **Data Management** | **[M4. Semantic and Multimodal Query Processing](#m4)** | Semantic maps, filters, joins and aggregates; operator decomposition; model selection, ensembles and cascades. | 4 |
| **Data Management** | **[M5. Execution, Scheduling and Caching](#m5)** | Query and workflow scheduling, batching, parallel execution, intermediate-result reuse and semantic caching. | 1 |
| **Data Management** | **[M6. Diagnosis, Observability and Remediation](#m6)** | Log and metric interpretation, performance debugging, incident knowledge extraction, root-cause diagnosis and repair advice. | 2 |
| **Data Management** | **[M7. Database Testing and Verification](#m7)** | Test generation, SQL equivalence, test oracles, bug reproduction, reduction, deduplication and regression testing. | 1 |
| **Data Management** | **M8. Schema Evolution, Dialect Translation and Migration** | Schema changes, cross-dialect translation, compatibility checking, migration planning and maintenance. | 0 |
| **Data Management** | **[M9. Database Code and Engine Generation](#m9)** | UDF and native-function synthesis, query execution code, database kernel development and workload-specific engines. | 1 |
| **Data Management** | **M10. Transactions, Concurrency and Recovery** | Isolation and concurrency control, transaction coordination, commit/rollback, recovery, replication and availability. | 0 |
| **Data Management** | **[M11. Security, Privacy, Governance and Provenance](#m11)** | Access control, policy enforcement, privacy-preserving data release, auditing, lineage and attack investigation. | 1 |
| **Data Management** | **[M12. Cross-Source and Federated Data Access](#m12)** | Coordinated access to multiple databases and data lakes; source selection, federated planning and distributed data access. | 2 |
| **Data Preparation** | **[P1. Data Discovery and Collection](#p1)** | Dataset and table search, relevance assessment, web collection, source selection and acquisition. | 4 |
| **Data Preparation** | **P2. Data Profiling, Metadata and Cataloging** | Schema and column annotation, dataset descriptions, business semantics, catalog construction and metadata maintenance. | 0 |
| **Data Preparation** | **[P3. Data Cleaning and Repair](#p3)** | Error detection, correction, missing-value imputation, normalization, standardization and integrity repair. | 2 |
| **Data Preparation** | **[P4. Data Transformation and ETL Pipelines](#p4)** | Table transformations, joins and reshaping; ETL/ELT construction, pipeline validation and optimization. | 2 |
| **Data Preparation** | **[P5. Schema and Ontology Matching](#p5)** | Column, schema, vocabulary and ontology alignment across heterogeneous sources. | 1 |
| **Data Preparation** | **[P6. Entity Resolution and Data Fusion](#p6)** | Entity matching, deduplication, knowledge-graph alignment and completion, record linking and fusion. | 1 |
| **Data Preparation** | **[P7. Information Extraction and Database Construction](#p7)** | Document/table extraction, document-to-database conversion, relation extraction and knowledge-graph construction. | 4 |
| **Data Preparation** | **[P8. Feature Engineering](#p8)** | Feature discovery, generation, selection and validation; SQL/UDF features and relational learning inputs. | 3 |
| **Data Preparation** | **[P9. Synthetic Data and Workload Generation](#p9)** | Synthetic tables, graphs, queries, dialogues and agent trajectories; realistic workloads and private data synthesis. | 3 |
| **Data Preparation** | **P10. Data Labeling and Training-Data Curation** | Automatic annotation, weak supervision, label refinement, data filtering and preparation for model training. | 0 |
| **Data Preparation** | **[P11. Benchmark Construction and Evaluation](#p11)** | Task and test-set construction, coverage/diversity control, agent evaluation and NL-to-query benchmarking. | 3 |
| **Data Analysis** | **[A1. Natural Language to SQL](#a1)** | Schema/value linking, question decomposition, SQL generation, candidate selection, query refinement and repair. | 6 |
| **Data Analysis** | **[A2. Graph, NoSQL and Spatial Querying](#a2)** | Natural-language interfaces to knowledge graphs, SPARQL, Cypher, document stores and spatial databases. | 3 |
| **Data Analysis** | **[A3. Table Question Answering](#a3)** | Reasoning over single or multiple tables, spreadsheets and semi-structured tables to return grounded answers. | 4 |
| **Data Analysis** | **[A4. Document, Multimodal and Unstructured Analytics](#a4)** | Question answering and analytics over documents, text, images, videos and logs; retrieval-augmented analysis. | 4 |
| **Data Analysis** | **[A5. Exploratory Analysis and Business Intelligence](#a5)** | Interactive exploration, end-to-end analysis planning, business metrics, SQL/Python analysis and analytical workflows. | 8 |
| **Data Analysis** | **[A6. Data Visualization and Visual Analytics](#a6)** | NL-to-chart generation, chart/code verification, interactive visual exploration and multimodal visualization. | 6 |
| **Data Analysis** | **[A7. Report Generation and Data Storytelling](#a7)** | Grounded reports, analytical narratives, explanations, text-chart reports and animated data stories. | 5 |
| **Data Analysis** | **[A8. Statistical Analysis, Prediction and Data Mining](#a8)** | Hypothesis generation/testing, modeling, forecasting, classification, anomaly detection and in-database prediction. | 3 |
| **Data Analysis** | **A9. Answer Verification and Fact Checking** | SQL/answer auditing, evidence checking, reasoning criticism, uncertainty estimation and selective answering. | 0 |

<a id="paper-list"></a>

## 📚 Paper List

Within each category, papers are ordered by **year descending**, then **SIGMOD → VLDB → ICDE → other venues**. Ties use venue/title alphabetical order. Badges use the recorded conference cycle, which can differ from the journal publication year; arXiv badges use the initial submission year. A paper appears in multiple categories only when its documented task contributions support those placements.

<a id="data-management"></a>

### Data Management

<a id="m1"></a>

#### M1. Configuration and Resource Tuning

1. **AgentTune: An Agent-Based Large Language Model Framework for Database Knob Tuning.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3769758)
2. **Why Database Manuals Are Not Enough: Efficient and Reliable Configuration Tuning for DBMSs via Code-Driven LLM Agents.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3797919.3797940)
3. **Rabbit: Retrieval-Augmented Generation Enables Better Automatic Database Knob Tuning.** [![ICDE '25](https://img.shields.io/badge/ICDE%20%2725-green)](https://doi.org/10.1109/icde65448.2025.00284)

<a id="m2"></a>

#### M2. Physical Database Design

1. **Hyper: Hybrid Physical Design Advisor with Multi-agent Reinforcement Learning.** [![ICDE '25](https://img.shields.io/badge/ICDE%20%2725-green)](https://doi.org/10.1109/icde65448.2025.00121)
2. **AMAZe: A Multi-Agent Zero-shot Index Advisor for Relational Databases.** [![arXiv '25](https://img.shields.io/badge/arXiv%20%2725-purple)](https://arxiv.org/abs/2508.16044)

<a id="m3"></a>

#### M3. Query Rewriting and Plan Optimization

1. **QUITE: A Query Rewrite System Beyond Rules with LLM Agents.** [![arXiv '25](https://img.shields.io/badge/arXiv%20%2725-purple)](https://arxiv.org/abs/2506.07675)

<a id="m4"></a>

#### M4. Semantic and Multimodal Query Processing

1. **Carnot: Interpretable, Interactive, and Optimized Execution of Deep Research Queries.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828086)
2. **Multi-Objective Agentic Rewrites for Unstructured Data Processing.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3836663.3836673)
3. **DocETL: Agentic Query Rewriting and Evaluation for Complex Document Processing.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3746405.3746426)
4. **AgenticData: An Agentic Data Analytics System for Heterogeneous Data.** [![arXiv '25](https://img.shields.io/badge/arXiv%20%2725-purple)](https://arxiv.org/abs/2508.05002)

<a id="m5"></a>

#### M5. Execution, Scheduling and Caching

1. **Semantic Caching and Intent-Driven Context Optimization for Multi-Agent Natural Language to Code Systems.** [![arXiv '26](https://img.shields.io/badge/arXiv%20%2726-purple)](https://arxiv.org/abs/2601.11687)

<a id="m6"></a>

#### M6. Diagnosis, Observability and Remediation

1. **SuperDRI: Graph-Guided Autonomous Troubleshooting for Cloud Databases.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828095)
2. **D-Bot: Database Diagnosis System using Large Language Models.** [![VLDB '24](https://img.shields.io/badge/VLDB%20%2724-blue)](https://doi.org/10.14778/3675034.3675043)

<a id="m7"></a>

#### M7. Database Testing and Verification

1. **Pisco: An Isolation Bug Case Reduction and Deduplication Framework.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3797919.3797944)

<a id="m9"></a>

#### M9. Database Code and Engine Generation

1. **Demonstrating GenDB: Instance-Optimized and Customized Query Processing Code Generation via LLM Agents.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828076)

<a id="m11"></a>

#### M11. Security, Privacy, Governance and Provenance

1. **ANTEATER: A Filter-then-Scrutinize Architecture for End-to-End Attack Investigation.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3802012)

<a id="m12"></a>

#### M12. Cross-Source and Federated Data Access

1. **UNITQA: A Unified Automated Tabular Question Answering System with Multi-Agent Large Language Models.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3722212.3725140)
2. **AutoTQA: Towards Autonomous Tabular Question Answering through Multi-Agent Large Language Models.** [![VLDB '24](https://img.shields.io/badge/VLDB%20%2724-blue)](https://doi.org/10.14778/3685800.3685816)

<a id="data-preparation"></a>

### Data Preparation

<a id="p1"></a>

#### P1. Data Discovery and Collection

1. **Drama: Unifying Data Retrieval and Analysis for Open-Domain Analytic Queries.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3769781)
2. **A Demo of Interactive Thematic Data Collection on the Live Web.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828064)
3. **Revisiting Task-Oriented Dataset Search in the Era of Large Language Models: Challenges, Benchmark, and Solution.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3796195.3796209)
4. **Sentence to Model: Cost-Effective Data Collection LLM Agent.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3722212.3725134)

<a id="p3"></a>

#### P3. Data Cleaning and Repair

1. **AutoPrep: Natural Language Question-Aware Data Preparation with a Multi-Agent Framework.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3748191.3748211)
2. **CleanAgent: Automating Data Standardization with LLM-based Agents.** [![VLDB Workshop '25](https://img.shields.io/badge/VLDB%20Workshop%20%2725-5588bb)](https://www.vldb.org/2025/Workshops/VLDB-Workshops-2025/DATAI/DATAI25_8.pdf)

<a id="p4"></a>

#### P4. Data Transformation and ETL Pipelines

1. **AutoPrep: Natural Language Question-Aware Data Preparation with a Multi-Agent Framework.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3748191.3748211)
2. **DataLab: A Unified Platform for LLM-Powered Business Intelligence.** [![ICDE '25](https://img.shields.io/badge/ICDE%20%2725-green)](https://doi.org/10.1109/icde65448.2025.00326)

<a id="p5"></a>

#### P5. Schema and Ontology Matching

1. **Agent-OM: Leveraging LLM Agents for Ontology Matching.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3712221.3712222)

<a id="p6"></a>

#### P6. Entity Resolution and Data Fusion

1. **Towards Unsupervised Entity Alignment for Highly Heterogeneous Knowledge Graphs.** [![ICDE '25](https://img.shields.io/badge/ICDE%20%2725-green)](https://doi.org/10.1109/icde65448.2025.00283)

<a id="p7"></a>

#### P7. Information Extraction and Database Construction

1. **Drama: Unifying Data Retrieval and Analysis for Open-Domain Analytic Queries.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3769781)
2. **Revisiting Task-Oriented Dataset Search in the Era of Large Language Models: Challenges, Benchmark, and Solution.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3796195.3796209)
3. **DocETL: Agentic Query Rewriting and Evaluation for Complex Document Processing.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3746405.3746426)
4. **TabAgent: A Multi-Agent Table Extraction Framework for Unstructured Documents.** [![VLDB Workshop '25](https://img.shields.io/badge/VLDB%20Workshop%20%2725-5588bb)](https://www.vldb.org/2025/Workshops/VLDB-Workshops-2025/DATAI/DATAI25_6.pdf)

<a id="p8"></a>

#### P8. Feature Engineering

1. **Adda: An Agent-Driven in-Database Feature Generation System.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3801606)
2. **FELA: A Multi-Agent Evolutionary System for Feature Engineering of Industrial Event Log Data.** [![ICDE '26](https://img.shields.io/badge/ICDE%20%2726-green)](https://doi.org/10.1109/icde65706.2026.00292)
3. **Adda: Towards Efficient in-Database Feature Generation via LLM-based Agents.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3725262)

<a id="p9"></a>

#### P9. Synthetic Data and Workload Generation

1. **ConDABench: Interactive Evaluation of Language Models for Data Analysis.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3803099)
2. **SAGA: Synthetic Agentic Graph Architecture for Temporal Benchmark Generation.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828134)
3. **SQL-Factory: A Multi-Agent Framework for High-Quality and Large-Scale SQL Generation.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3778092.3778093)

<a id="p11"></a>

#### P11. Benchmark Construction and Evaluation

1. **ConDABench: Interactive Evaluation of Language Models for Data Analysis.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3803099)
2. **NL2SQLBench: A Modular Benchmarking Framework for LLM-Enabled NL2SQL Solutions.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3796195.3796211)
3. **SAGA: Synthetic Agentic Graph Architecture for Temporal Benchmark Generation.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828134)

<a id="data-analysis"></a>

### Data Analysis

<a id="a1"></a>

#### A1. Natural Language to SQL

1. **Bridging NL2SQL for CAN Signal Analytics at NIO: From Externalized Schemas to CTE Pipelines.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828036)
2. **CoeusBI: A Comprehensive Interactive Business Intelligence System Powered by LLMs at Baidu.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828017)
3. **LEAF-SQL: Level-Wise Exploration with Adaptive Fine-Graining for Text-to-SQL Skeleton Prediction.** [![ICDE '26](https://img.shields.io/badge/ICDE%20%2726-green)](https://doi.org/10.1109/icde65706.2026.00181)
4. **OmniTune: A Universal Framework for Query Refinement via LLMs.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3722212.3725121)
5. **OpenSearch-SQL: Enhancing Text-to-SQL with Dynamic Few-shot and Consistency Alignment.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3725331)
6. **Demonstration of DB-GPT: Next Generation Data Interaction System Empowered by Large Language Models.** [![VLDB '24](https://img.shields.io/badge/VLDB%20%2724-blue)](https://doi.org/10.14778/3685800.3685876)

<a id="a2"></a>

#### A2. Graph, NoSQL and Spatial Querying

1. **Chatty-KG: A Multi-Agent AI System for On-Demand Conversational Question Answering over Knowledge Graphs.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3786632)
2. **SpatialSQL: A Multi-Agent System for Interactive and Observable Spatial Text-to-SQL.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828055)
3. **Graph Query Generation with Constraint-Guided Large Language Agents.** [![ICDE '26](https://img.shields.io/badge/ICDE%20%2726-green)](https://doi.org/10.1109/icde65706.2026.00283)

<a id="a3"></a>

#### A3. Table Question Answering

1. **Accurate Table Question Answering with Accessible LLMs.** [![ICDE '26](https://img.shields.io/badge/ICDE%20%2726-green)](https://doi.org/10.1109/icde65706.2026.00020)
2. **A Vision for Autonomous Data Agent Collaboration: From Query-by-Integration to Query-by-Collaboration.** [![CIDR '26](https://img.shields.io/badge/CIDR%20%2726-yellow)](https://www.vldb.org/cidrdb/papers/2026/p19-eckmann.pdf)
3. **UNITQA: A Unified Automated Tabular Question Answering System with Multi-Agent Large Language Models.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3722212.3725140)
4. **AutoTQA: Towards Autonomous Tabular Question Answering through Multi-Agent Large Language Models.** [![VLDB '24](https://img.shields.io/badge/VLDB%20%2724-blue)](https://doi.org/10.14778/3685800.3685816)

<a id="a4"></a>

#### A4. Document, Multimodal and Unstructured Analytics

1. **ANTEATER: A Filter-then-Scrutinize Architecture for End-to-End Attack Investigation.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3802012)
2. **Carnot: Interpretable, Interactive, and Optimized Execution of Deep Research Queries.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828086)
3. **DocETL: Agentic Query Rewriting and Evaluation for Complex Document Processing.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3746405.3746426)
4. **AgenticData: An Agentic Data Analytics System for Heterogeneous Data.** [![arXiv '25](https://img.shields.io/badge/arXiv%20%2725-purple)](https://arxiv.org/abs/2508.05002)

<a id="a5"></a>

#### A5. Exploratory Analysis and Business Intelligence

1. **DeepEye: A Steerable Self-driving Data Agent System.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3801612)
2. **Drama: Unifying Data Retrieval and Analysis for Open-Domain Analytic Queries.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3769781)
3. **CoeusBI: A Comprehensive Interactive Business Intelligence System Powered by LLMs at Baidu.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828017)
4. **Semantic Caching and Intent-Driven Context Optimization for Multi-Agent Natural Language to Code Systems.** [![arXiv '26](https://img.shields.io/badge/arXiv%20%2726-purple)](https://arxiv.org/abs/2601.11687)
5. **A Demonstration of QueryArtisan: Real-Time Data Lake Analysis via Dynamically Generated Data Manipulation Code.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3750601.3750647)
6. **DataLab: A Unified Platform for LLM-Powered Business Intelligence.** [![ICDE '25](https://img.shields.io/badge/ICDE%20%2725-green)](https://doi.org/10.1109/icde65448.2025.00326)
7. **AgenticData: An Agentic Data Analytics System for Heterogeneous Data.** [![arXiv '25](https://img.shields.io/badge/arXiv%20%2725-purple)](https://arxiv.org/abs/2508.05002)
8. **Demonstration of DB-GPT: Next Generation Data Interaction System Empowered by Large Language Models.** [![VLDB '24](https://img.shields.io/badge/VLDB%20%2724-blue)](https://doi.org/10.14778/3685800.3685876)

<a id="a6"></a>

#### A6. Data Visualization and Visual Analytics

1. **DeepEye: A Steerable Self-driving Data Agent System.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3801612)
2. **Demonstration of MultiVis-Agent: Interactively Generating Reliable Visualizations via Logic-Rule Agents.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3801584)
3. **MultiVis-Agent: A Multi-Agent Framework with Logic Rules for Reliable and Comprehensive Cross-Modal Data Visualization.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3786670)
4. **DataMagic: Transforming Tabular Data into Data Insight Video.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828057)
5. **Hypothesis Exploration with LLM-driven Intelligent Orchestration System.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828129)
6. **DataLab: A Unified Platform for LLM-Powered Business Intelligence.** [![ICDE '25](https://img.shields.io/badge/ICDE%20%2725-green)](https://doi.org/10.1109/icde65448.2025.00326)

<a id="a7"></a>

#### A7. Report Generation and Data Storytelling

1. **ANTEATER: A Filter-then-Scrutinize Architecture for End-to-End Attack Investigation.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3802012)
2. **DeepEye: A Steerable Self-driving Data Agent System.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3788853.3801612)
3. **DataMagic: Transforming Tabular Data into Data Insight Video.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828057)
4. **Hypothesis Exploration with LLM-driven Intelligent Orchestration System.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828129)
5. **NeurIDA: Dynamic Modeling for Effective In-Database Analytics.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3819518.3819563)

<a id="a8"></a>

#### A8. Statistical Analysis, Prediction and Data Mining

1. **Hypothesis Exploration with LLM-driven Intelligent Orchestration System.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3827998.3828129)
2. **NeurIDA: Dynamic Modeling for Effective In-Database Analytics.** [![VLDB '26](https://img.shields.io/badge/VLDB%20%2726-blue)](https://doi.org/10.14778/3819518.3819563)
3. **Sentence to Model: Cost-Effective Data Collection LLM Agent.** [![SIGMOD '25](https://img.shields.io/badge/SIGMOD%20%2725-red)](https://doi.org/10.1145/3722212.3725134)

<a id="related-foundations"></a>

## 🔗 Related Foundations

Database systems supporting multi-agent workflows (DB for MAS); counted separately from the task-solving papers above.

1. **Rethinking Query Optimization for Multi-Agent Systems.** [![VLDB '27](https://img.shields.io/badge/VLDB%20%2727-blue)](https://www.vldb.org/pvldb/vol20/p46-kaoudi.pdf)
2. **Efficient LLM Serving for Agentic Workflows: A Data Systems Perspective.** [![SIGMOD '26](https://img.shields.io/badge/SIGMOD%20%2726-red)](https://doi.org/10.1145/3802046)
3. **SagaLLM: Context Management, Validation, and Transaction Guarantees for Multi-Agent LLM Planning.** [![VLDB '25](https://img.shields.io/badge/VLDB%20%2725-blue)](https://doi.org/10.14778/3750601.3750611)

Last reviewed: **2026-10-29**. [Review and evidence](SCREENING.md) · [Historical catalogue](WORKS.md)

## Citation

If you find this resource useful in your research, please cite it as follows:

**BibTeX:**

```bibtex
@misc{zhu2026multiagent4database,
  author       = {Zhu, Xinyi},
  title        = {{Awesome Multi-Agent System for Database Papers}},
  year         = {2026},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/DAISYzxy/awesome-multi-agent-systems-for-database}},
  note         = {Maintained by DAISYzxy}
}
```
