# AI4DB Paper Sets [![666](https://awesome.re/badge.svg)](https://awesome.re)

[![Awesome AI4DB Paper](https://img.shields.io/static/v1?label=&message=Awesome+AI4DB+Paper&color=black&logo=awesomelists)](https://github.com/Wind-Gone/awesome-ai4db-paper)
![](https://img.shields.io/github/last-commit/Wind-Gone/awesome-ai4db-paper?color=green)
[![GitHub Repo stars](https://img.shields.io/github/stars/Wind-Gone/awesome-ai4db-paper?style=social)](https://github.com/Wind-Gone/awesome-ai4db-paper)

## Introduction

A curated paper list of awesome AI4DB <b> theory, frameworks, resources, tools</b> and other awesomeness, for data engineers.

## Contributing

The repository is under construction.  Welcome new PR, please conform to the committed rules: 

```bash
paperName(with pdf link) [MeetingName Year] Github link if it has open-sourced code (optional)
```
## Acknowledge
Thanks to all authors of the paper/repository I cite :D


## Table of Content

- [AI4DB Paper Sets ](#ai4db-paper-sets-)
  - [Introduction](#introduction)
  - [Contributing](#contributing)
  - [Acknowledge](#acknowledge)
  - [Table of Content](#table-of-content)
  - [Learning-based Query Optimization](#learning-based-query-optimization)
    - [Cardinality Estimation](#cardinality-estimation)
      - [Survey](#survey)
      - [Query-Driven](#query-driven)
        - [Single-Table](#single-table)
        - [Multi-Tables](#multi-tables)
      - [Data-Driven](#data-driven)
        - [Single-Table](#single-table-1)
        - [Multi-Tables](#multi-tables-1)
      - [Hybrid](#hybrid)
      - [Pretrain](#pretrain)
    - [Plan Hints](#plan-hints)
    - [Cost Model](#cost-model)
    - [SQL Embedding](#sql-embedding)
    - [Join Order](#join-order)
    - [Query Rewrite](#query-rewrite)
  - [Database Traditional Technology](#database-traditional-technology)
    - [Learning-based Index Design](#learning-based-index-design)
      - [Single-dimensional](#single-dimensional)
      - [Multi-dimensional](#multi-dimensional)
  - [Learning-based Configuration Advisor](#learning-based-configuration-advisor)
    - [Index Advisor](#index-advisor)
  - [Database Self-Tuning](#database-self-tuning)
  - [LLM](#llm)


## Learning-based Query Optimization
1. [LEON: A New Framework for ML-Aided Query Optimization](https://www.vldb.org/pvldb/vol16/p2261-chen.pdf) [VLDB 23]
2. [AutoSteer: Learned Query Optimization for Any SQL Database](https://db.in.tum.de/~anneser/autosteer-paper.pdf) [VLDB 24]

### Cardinality Estimation

#### Survey

1. [Cardinality Estimation: An Experimental Survey](https://www.vldb.org/VLDB/vol11/p499-harmouch.pdf) [VLDB 17]
2. [Are We Ready For Learned Cardinality Estimation?](https://arxiv.org/pdf/2012.06743.pdf) [VLDB 21]
3. [Cardinality Estimation in DBMS: A Comprehensive Benchmark Evaluation](https://kai-zeng.github.io/papers/benchmark_vldb_2021.pdf) [VLDB 21]
4. [Learned cardinality estimation: A design space exploration and a comparative evaluation](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/vldb22-card-exp.pdf) [VLDB 22]
5. [Learned Cardinality Estimation: An In-depth Study](https://dl.acm.org/doi/10.1145/3514221.3526154) [SIGMOD 22]
6. [A Comparative Study and Component Analysis of Query Plan Representation Techniques in ML4DB Studies](https://www.vldb.org/pvldb/vol17/p823-zhao.pdf) [VLDB 24]

#### Query-Driven

##### Single-Table

1. [Selectivity estimation for range predicates using lightweight models](http://www.vldb.org/pvldb/vol12/p1044-dutt.pdf) [VLDB 19]
2. [Deep learning models for selectivity estimation of multiattribute queries](https://dl.acm.org/doi/abs/10.1145/3318464.3389741) [SIGMOD 20]

##### Multi-Tables

1. [Learned Cardinalities: Estimating Correlated Joins with Deep Learning](https://arxiv.org/pdf/1809.00677.pdf) [CIDR 2019]
2. [An End-to-End Learning-based Cost Estimator](http://www.vldb.org/VLDB/vol13/p307-sun.pdf) [VLDB 19] [![](https://img.shields.io/github/stars/greatji/Learning-based-cost-estimator?style=social&label=Code+Stars)](https://github.com/greatji/Learning-based-cost-estimator)
3. [Flow-Loss: Learning Cardinality Estimates That Matter](https://people.csail.mit.edu/tatbul/publications/flowloss_vldb21.pdf) [VLDB 21]
4. [Speeding Up End-to-end Query Execution via Learning-based Progressive Cardinality Estimation](https://www.fangwang.online/_files/ugd/5d2324_ddbbd368d939421e9f2b7295b919d90d.pdf) [SIGMOD 23] [![](https://img.shields.io/github/stars/Eilowangfang/LPCE?style=social&label=Code+Stars)](https://github.com/Eilowangfang/LPCE)
5. [Robust Query Driven Cardinality Estimation under Changing Workloads](https://www.vldb.org/pvldb/vol16/p1520-negi.pdf)[[VLDB 23](https://github.com/learnedsystems/CEB)]
6. [AutoCE: An Accurate and Efficient Model Advisor for Learned Cardinality Estimation](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/AutoCE_camera_ready_ICDE2023.pdf) [ICDE 23]
7. [Asm: Harmonizing autoregressive model, sampling, and multi-dimensional statistics merging for cardinality estimation](https://dl.acm.org/doi/pdf/10.1145/3639300) [SIGMOD 24]

#### Data-Driven

##### Single-Table

1. [Self-tuning, gpu-accelerated kernel density models for multidimensional selectivity estimation](https://dl.acm.org/doi/10.1145/2723372.2749438) [SIGMOD 15]
2. [Deep Unsupervised Cardinality Estimation](http://www.vldb.org/VLDB/vol13/p279-yang.pdf) [VLDB 19] [![](https://img.shields.io/github/stars/naru-project/naru?style=social&label=Code+Stars)](https://github.com/naru-project/naru)
3. [Quicksel: Quick selectivity learning with mixture models](https://arxiv.org/pdf/1812.10568.pdf) [SIGMOD 20]  [![](https://img.shields.io/github/stars/illinoisdata/quicksel?style=social&label=Code+Stars)](https://github.com/illinoisdata/quicksel) 
4. [Pre-training Summarization Models of Structured Datasets for Cardinality Estimation](http://yao.lu/iris.pdf) [VLDB 22] [![](https://img.shields.io/github/stars/tjluyao/iris_demo?style=social&label=Code+Stars)]( https://github.com/tjluyao/iris_demo) 

##### Multi-Tables

1. [DeepDB: Learn from Data, not from Queries!](http://www.vldb.org/VLDB/vol13/p992-hilprecht.pdf) [VLDB 20] [![](https://img.shields.io/github/stars/DataManagementLab/deepdb-public?style=social&label=Code+Stars)](https://github.com/DataManagementLab/deepdb-public) 
2. [NeuroCard: One Cardinality Estimator for All Tables](https://vldb.org/VLDB/vol14/p61-yang.pdf) [VLDB 21]  [![](https://img.shields.io/github/stars/neurocard/neurocard?style=social&label=Code+Stars)](https://github.com/neurocard/neurocard) 
3. [FLAT: Fast, Lightweight and Accurate Method for Cardinality Estimation](http://www.vldb.org/VLDB/vol14/p1489-zhu.pdf) [VLDB 21]
4. [BayesCard: Revitilizing Bayesian Frameworks for Cardinality Estimation](https://arxiv.org/pdf/2012.14743.pdf) [aiXiv 21] [![](https://img.shields.io/github/stars/wuziniu/BayesCard?style=social&label=Code+Stars)](https://github.com/wuziniu/BayesCard) 
5. [Glue: Adaptively Merging Single Table Cardinality to Estimate Join Query Size](https://arxiv.org/pdf/2112.03458.pdf)  [aiXiv 21]
6. [Fauce: fast and accurate deep ensembles with uncertainty for cardinality estimation](http://vldb.org/pvldb/vol14/p1950-liu.pdf) [VLDB 21]
7. [FACE: a normalizing flow based cardinality estimator](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/vldb22-flow-card.pdf) [VLDB 22]  [![](https://img.shields.io/github/stars/for0nething/FACE-A-Normalizing-Flow-based-Cardinality-Estimator?style=social&label=Code+Stars)](https://github.com/for0nething/FACE-A-Normalizing-Flow-based-Cardinality-Estimator/) 
8. [FactorJoin: A New Cardinality Estimation Framework for Join Queries](https://arxiv.org/pdf/2212.05526.pdf) [SIGMOD 22] (Bounded)

#### Hybrid

1. [A Unified Deep Model of Learning from both Data and Queries for Cardinality Estimation](https://arxiv.org/pdf/2107.12295.pdf) [SIGMOD 21]  [![](https://img.shields.io/github/stars/pagegitss/UAE?style=social&label=Code+Stars)](https://github.com/pagegitss/UAE) 

#### Pretrain
1. [PRICE: A Pretrained Model for Cross-Database Cardinality Estimation](https://arxiv.org/pdf/2406.01027#page=1.22) [arXiv 24]

### Plan Hints

1. [Bao: Making Learned Query Optimization Practical](https://dl.acm.org/doi/pdf/10.1145/3448016.3452838) [SIMOD 21]

### Cost Model

1. [Cost-based or Learning-based? A Hybrid Query Optimizer for Query Plan Selection](https://www.vldb.org/pvldb/vol15/p3924-li.pdf) [VLDB 22]  [![](https://img.shields.io/github/stars/yxfish13/HyperQO?style=social&label=Code+Stars)](https://github.com/yxfish13/HyperQO) 
1. [Lero: A Learning-to-Rank Qery Optimizer](https://www.vldb.org/pvldb/vol16/p1466-zhu.pdf) [VLDB 23]

### SQL Embedding

1. [PreQR: Pre-training Representation for SQL Understanding](https://dl.acm.org/doi/abs/10.1145/3514221.3517878) [SIGMOD 22]
2. [LearnedSQLGen: Constraint-aware SQL Generation using Reinforcement Learning](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/sigmod2022-sqlgen.pdf) (SIGMOD 2022)

### Join Order

1. [Learning to Optimize Join queries With Deep Reinforcement Learning](https://arxiv.org/pdf/1808.03196.pdf) [SIGMOD 16]
2. [Deep Reinforcement Learning for Join Order Enumeration](https://arxiv.org/pdf/1803.00055.pdf)[arXiv 18]
3. [Reinforcement Learning with Tree-LSTM for Join Order Selection](https://qcai.qcri.org/ntang/pubs/icde20jos.pdf) [ICDE 20]

### Query Rewrite

1. [A Learned Query Rewrite System using Monte Carlo Tree Search](http://dbgroup.cs.tsinghua.edu.cn/ligl/papers/vldb22-query-rewrite.pdf) [VLDB 22] [![](https://img.shields.io/github/stars/zhouxh19/LearnedRewrite?style=social&label=Code+Stars)](https://github.com/zhouxh19/LearnedRewrite) 

## Database Traditional Technology

### Learning-based Index Design

#### Single-dimensional

1. [The Case for Learned Index Structures](https://dl.acm.org/doi/pdf/10.1145/3183713.3196909) [SIGMOD 18]
2. [FITing-Tree: A Data-aware Index Structure](https://arxiv.org/pdf/1801.10207.pdf) [SIGMOD 19]
3. [ALEX: An Updatable Adaptive Learned Index](https://arxiv.org/pdf/1905.08898.pdf)  [aiXiv 20]
4. [The PGM-index: a fully-dynamic compressed learned index with provable worst-case bounds](http://www.vldb.org/VLDB/vol13/p1162-ferragina.pdf)  [VLDB 20]
5. [RadixSpline: a single-pass learned index](https://dl.acm.org/doi/pdf/10.1145/3401071.3401659) [aiDM 20]
6. [Why Are Learned Indexes So Effective?](http://proceedings.mlr.press/v119/ferragina20a/ferragina20a.pdf) [ICML 20]
7. [A Pluggable Learned Index Method via Sampling and Gap Insertion](https://arxiv.org/pdf/2101.00808.pdf) [aiXiv 21]
8. [Updatable Learned Index with Precise Positions](https://arxiv.org/pdf/2104.05520.pdf) [VLDB 21]
9. [The next 50 years in database indexing or: the case for automatically generated index structures](https://dl.acm.org/doi/10.14778/3494124.3494136) [VLDB 21]
10. [Tuning Hierarchical Learned Indexes on Disk and Beyond](https://dl.acm.org/doi/abs/10.1145/3514221.3520255) [SIGMOD 22]
11. [APEX: A High-Performance Learned Index on Persistent Memory](https://arxiv.org/pdf/2105.00683.pdf) [VLDB 22]
12. [FINEdex: A Fine-grained Learned Index Scheme for Scalable and Concurrent Memory Systems](http://www.vldb.org/VLDB/vol15/p321-hua.pdf) [VLDB 22]
13. [Are Updatable Learned Indexes Ready?](https://arxiv.org/pdf/2207.02900.pdf) [VLDB 22]
14. [CARMI: A Cache-Aware Learned Index with a Cost-based Construction Algorithm](https://www.vldb.org/VLDB/vol15/p2679-gao.pdf) [VLDB 22]
15. [NFL: Robust Learned Index via Distribution Transformation](https://www.vldb.org/VLDB/vol15/p2188-wu.pdf) [VLDB 22]
16. [Cutting Learned Index into Pieces: An In-depth Inquiry into Updatable Learned Indexes]() [ICDE 23]


#### Multi-dimensional

1. [Learning Multi-dimensional Indexes](https://dl.acm.org/doi/pdf/10.1145/3318464.3380579) [SIGMOD 20]
2. [LISA: A Learned Index Structure for Spatial Data](https://dl.acm.org/doi/abs/10.1145/3318464.3389703) [SIGMOD 20]
3. [Effectively Learning Spatial Indices](https://vbn.aau.dk/ws/files/391644098/p2341_qi.pdf) [VLDB 20]
4. [The ML-Index: A Multidimensional, Learned Index for Point, Range, and Nearest-Neighbor Queries](https://dbis.informatik.uni-kl.de/files/papers/ml-index-edbt2020.pdf) [EDBT 20]
5. [Tsunami: A Learned Multi-dimensional Index for Correlated Data and Skewed Workloads](http://vldb.org/VLDB/vol14/p74-ding.pdf) [VLDB 21]
6. [NEIST: a Neural-Enhanced Index for Spatio-Temporal Queries](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8861025) [TKDE 21]
7. [RW-Tree: A Learned Workload-aware Framework for R-tree Construction](https://ieeexplore.ieee.org/abstract/document/9835605/) [ICDE 22]

## Learning-based Configuration Advisor

### Index Advisor

1. [The Case for Automatic Database Administration using Deep Reinforcement Learning](https://arxiv.org/abs/1801.05643) [arXiv 18]
2. [AI Meets AI: Leveraging Query Executions to Improve Index Recommendations](https://pages.cs.wisc.edu/~wentaowu/papers/sigmod19-auto-indexing.pdf) [SIGMOD 19]
3. [Online Index Selection Using Deep Reinforcement Learning for a Cluster Database](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9094124) [ICDEW 20] 
4. [SMARTIX: A database indexing agent based on reinforcement learning](https://link.springer.com/article/10.1007/s10489-020-01674-8) [Applied Intelligence 20]
5.  [Magic mirror in my hand, which is the best in the land? An Experimental Evaluation of Index Selection Algorithms](http://www.vldb.org/VLDB/vol13/p2382-kossmann.pdf) [VLDB 20]  [![](https://img.shields.io/github/stars/hyrise/index_selection_evaluation?style=social&label=Code+Stars)](https://github.com/hyrise/index_selection_evaluation/tree/rl_index_selection) 
6. [An Index Advisor Using Deep Reinforcement Learning](https://baozhifeng.net/papers/cikm20-IndexRec.pdf) [CIKM 20]
7. [Automated Database Indexing Using Model-Free Reinforcement Learning](https://icaps20subpages.icaps-conference.org/wp-content/uploads/2020/10/SPARK-2020_paper_4.pdf) [ICAPS 20]
8. [DBA bandits: Self-driving index tuning under ad-hoc, analytical workloads with safety guarantees ](https://arxiv.org/pdf/2010.09208) [ICDE 21]
9. [Index selection for NoSQL database with deep reinforcement learning](https://www.sciencedirect.com/science/article/pii/S0020025521000049) [Information Sciences 21]
10. [MANTIS: Multiple Type and Attribute Index Selection using Deep Reinforcement Learning](https://dl.acm.org/doi/10.1145/3472163.3472176) [IDEAS 21]
11. [AutoIndex: An Incremental Index Management System for Dynamic Workloads](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/icde2022-autoindex.pdf) [ICDE 22]
12. [SWIRL: Selection of Workload-aware Indexes using Reinforcement Learning ](https://openproceedings.org/2022/conf/edbt/paper-37.pdf) [EDBT 22]
13. [Indexer++: Workload-Aware Online Index Tuning with Transformers and Reinforcement Learning](https://dl.acm.org/doi/abs/10.1145/3477314.3507691) [SAC 22]
14. [Budget-aware Index Tuning with Reinforcement Learning ](https://www.microsoft.com/en-us/research/uploads/prod/2022/06/mcts-full.pdf) [SIGMOD 22] 
15. [ISUM: Efficiently Compressing Large and Complex Workloads for Scalable Index Tuning](https://dl.acm.org/doi/10.1145/3514221.3526152) [SIGMOD 22]
16. [DISTILL: low-overhead data-driven techniques for filtering and costing indexes for scalable index tuning](https://www.microsoft.com/en-us/research/uploads/prod/2022/06/DISTILL.pdf) [VLDB 22]
17. [HMAB: Self-Driving Hierarchy of Bandits for Integrated Physical Database Design Tuning](https://www.vldb.org/pvldb/vol16/p216-perera.pdf) [VLDB 22]  [![](https://img.shields.io/github/stars/malingaperera/HMAB?style=social&label=Code+Stars)](https://github.com/malingaperera/HMAB) 
18. [SmartIndex: An Index Advisor with Learned Cost Estimator](https://dl.acm.org/doi/abs/10.1145/3511808.3557163) [CIKM 22]
19. [Learned Index Benefits: Machine Learning Based Index Performance Estimation](https://www.vldb.org/pvldb/vol15/p3950-shi.pdf) [VLDB 23] [![](https://img.shields.io/github/stars/JC-Shi/Learned-Index-Benefits?style=social&label=Code+Stars)](https://github.com/JC-Shi/Learned-Index-Benefits) 

## Database Self-Tuning

1. [Automatic Database Management System Tuning Through Large-scale Machine Learning](https://www.cs.cmu.edu/~ggordon/van-aken-etal-parameters.pdf) [SIGMOD 17]
2. [Deploying a Steered Query Optimizer in Production at Microsof](https://arxiv.org/pdf/2210.13625.pdf) [SIGMOD 22]
3. [Detect, Distill and Update: Learned DB Systems Facing Out of Distribution Data](https://arxiv.org/pdf/2210.05508.pdf) [SIGMOD 23]
4. [AutoSteer: Learned Query Optimization for Any SQL Database](https://files.zotero.net/eyJleHBpcmVzIjoxNjkzOTEyOTM1LCJoYXNoIjoiNzZiM2Y1NDE5OGI3NzBjOTI0NTBkZmQ4MTRhMjU2MDIiLCJjb250ZW50VHlwZSI6ImFwcGxpY2F0aW9uXC9wZGYiLCJjaGFyc2V0IjoiIiwiZmlsZW5hbWUiOiJBbm5lc2VyIGV0IGFsLiAtIDIwMjMgLSBBdXRvU3RlZXIgTGVhcm5lZCBRdWVyeSBPcHRpbWl6YXRpb24gZm9yIEFueSBTUUwgLnBkZiJ9/14317cdbbbbe22f7074b637d497dfc63100a1c33ac4df53fe8dd8e9a0cbbad02/Anneser%20et%20al.%20-%202023%20-%20AutoSteer%20Learned%20Query%20Optimization%20for%20Any%20SQL%20.pdf) [SIGMOD 23]
5. [Auto-WLM: Machine Learning Enhanced Workload Management in Amazon Redshif](https://files.zotero.net/eyJleHBpcmVzIjoxNjkzOTEzMDc2LCJoYXNoIjoiNWIzODAwNDAxNDkwNzI5NDdkMWU2OGI1MTE1MWU2YTIiLCJjb250ZW50VHlwZSI6ImFwcGxpY2F0aW9uXC9wZGYiLCJjaGFyc2V0IjoiIiwiZmlsZW5hbWUiOiJHYXVyYXYgU2F4ZW5hIGV0IGFsLiAtIDIwMjMgLSBBdXRvLVdMTSBNYWNoaW5lIExlYXJuaW5nIEVuaGFuY2VkIFdvcmtsb2FkIE1hbmFnLnBkZiJ9/09cfdb42a31ac864d182519dccc997cd40c0900c8c9d0e8b41043b8629ebd58b/Gaurav%20Saxena%20et%20al.%20-%202023%20-%20Auto-WLM%20Machine%20Learning%20Enhanced%20Workload%20Manag.pdf) [SIGMOD 23]


## LLM
1. [GPTuner: A Manual-Reading Database Tuning System via GPT-Guided Bayesian Optimization](https://www.vldb.org/pvldb/vol17/p1939-tang.pdf) [VLDB 24]
2. [D-Bot: Database Diagnosis System using Large Language Models](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/dbot_vldb_camera_ready_v1.pdf) [VLDB 24]
3. [LLMTune: Accelerate Database Knob Tuning with Large Language Models](https://arxiv.org/pdf/2404.11581) [VLDB 24]c
4. [ArcheType: A Novel Framework for Open-Source Column Type Annotation using Large Language Models](https://www.vldb.org/pvldb/vol17/p2279-freire.pdf) [VLDB 24]


<a href="https://star-history.com/#Wind-Gone/awesome-ai4db-paper&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Wind-Gone/awesome-ai4db-paper&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Wind-Gone/awesome-ai4db-paper&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Wind-Gone/awesome-ai4db-paper&type=Date" />
  </picture>
</a>