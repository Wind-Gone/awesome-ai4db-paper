# AI4DB Paper Sets

Welcom new PR, please conform to the commited rules:  paperName(with link) [MeetingName Year]

If the paper has the open-souce code, please supply its github links in Meeting

- [AI4DB Paper Sets](#ai4db-paper-sets)
  - [Learning-based Query Optimization](#learning-based-query-optimization)
    - [Cardinality Estimation](#learning-based-cardinality-estimation)
      - [Survey](#survey)
      - [Query-Driven](#query-driven)
        - [Single-Table](#single-table)
        - [Multi-Tables](#multi-tables)
      - [Data-Driven](#data-driven)
        - [Single-Table](#single-table-1)
        - [Multi-Tables](#multi-tables-1)
      - [Hybrid](#hybrid)
    - [Plan Hints](#learning-based-plan-hints)
  - [Database Traditional Technology](#database-traditional-technology)
    - [Learning-based Index Design](#learning-based-index-design)
      - [Single-dimensional](#single-dimensional)
      - [Multi-dimensional](#multi-dimensional)
  - [Learning-based Configuration Advisor](#learning-based-configuration-advisor)
    - [Index Advisor](#index-advisor)


## Learning-based Query Optimization

### Cardinality Estimation

#### Survey

1. [Cardinality Estimation: An Experimental Survey](https://www.vldb.org/VLDB/vol11/p499-harmouch.pdf) [VLDB 17]
2. [Are We Ready For Learned Cardinality Estimation?](https://arxiv.org/pdf/2012.06743.pdf) [VLDB 21]
3. [Cardinality Estimation in DBMS: A Comprehensive Benchmark Evaluation](https://kai-zeng.github.io/papers/benchmark_vldb_2021.pdf) [VLDB 21]
4. [Learned cardinality estimation: A design space exploration and a comparative evaluation](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/vldb22-card-exp.pdf) [VLDB 22]
5. [Learned Cardinality Estimation: An In-depth Study](https://dl.acm.org/doi/10.1145/3514221.3526154) [SIGMOD 22]

#### Query-Driven

##### Single-Table

1. [Selectivity estimation for range predicates using lightweight models](http://www.vldb.org/pvldb/vol12/p1044-dutt.pdf) [VLDB 19]
2. [Deep learning models for selectivity estimation of multiattribute queries](https://dl.acm.org/doi/abs/10.1145/3318464.3389741) [SIGMOD 20]

##### Multi-Tables

1. [Learned Cardinalities: Estimating Correlated Joins with Deep Learning](https://arxiv.org/pdf/1809.00677.pdf) [[CIDR 2019](https://github.com/andreaskipf/learnedcardinalities)]
2. [An End-to-End Learning-based Cost Estimator](http://www.vldb.org/VLDB/vol13/p307-sun.pdf) [[VLDB 19](https://github.com/greatji/Learning-based-cost-estimator)]
3. [Flow-Loss: Learning Cardinality Estimates That Matter](https://people.csail.mit.edu/tatbul/publications/flowloss_vldb21.pdf) [VLDB 21]
4. [Speeding Up End-to-end Query Execution via Learning-based Progressive Cardinality Estimation](https://www.fangwang.online/_files/ugd/5d2324_ddbbd368d939421e9f2b7295b919d90d.pdf) [[SIGMOD 22](https://github.com/Eilowangfang/LPCE)]

#### Data-Driven

##### Single-Table

1. [Self-tuning, gpu-accelerated kernel density models for multidimensional selectivity estimation](https://dl.acm.org/doi/10.1145/2723372.2749438) [SIGMOD 15]
2. [Deep Unsupervised Cardinality Estimation](http://www.vldb.org/VLDB/vol13/p279-yang.pdf) [[VLDB 19](https://github.com/naru-project/naru)]
3. [Quicksel: Quick selectivity learning with mixture models](https://arxiv.org/pdf/1812.10568.pdf) [[SIGMOD 20](https://github.com/illinoisdata/quicksel)]
4. [Pre-training Summarization Models of Structured Datasets for Cardinality Estimation](http://yao.lu/iris.pdf) [[VLDB 22](https://github.com/tjluyao/iris_demo)]

##### Multi-Tables

1. [DeepDB: Learn from Data, not from Queries!](http://www.vldb.org/VLDB/vol13/p992-hilprecht.pdf) [[VLDB 20](https://github.com/DataManagementLab/deepdb-public)]
2. [NeuroCard: One Cardinality Estimator for All Tables](https://vldb.org/VLDB/vol14/p61-yang.pdf) [[VLDB 21](https://github.com/neurocard/neurocard)]
3. [FLAT: Fast, Lightweight and Accurate Method for Cardinality Estimation](http://www.vldb.org/VLDB/vol14/p1489-zhu.pdf) [VLDB 21]
4. [BayesCard: Revitilizing Bayesian Frameworks for Cardinality Estimation](https://arxiv.org/pdf/2012.14743.pdf) [[aiXiv 21](https://github.com/wuziniu/BayesCard)]
5. [Glue: Adaptively Merging Single Table Cardinality to Estimate Join Query Size](https://arxiv.org/pdf/2112.03458.pdf)  [aiXiv 21]
6. [Fauce: fast and accurate deep ensembles with uncertainty for cardinality estimation](http://vldb.org/pvldb/vol14/p1950-liu.pdf) [VLDB 21]
7. [FACE: a normalizing flow based cardinality estimator](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/vldb22-flow-card.pdf) [[VLDB 22](https://github.com/for0nething/FACE-A-Normalizing-Flow-based-Cardinality-Estimator)]

#### Hybrid

1. [A Unified Deep Model of Learning from both Data and Queries for Cardinality Estimation](https://arxiv.org/pdf/2107.12295.pdf) [[SIGMOD 21](https://github.com/pagegitss/UAE)]

### Plan Hints

1. [Bao: Making Learned Query Optimization Practical](https://dl.acm.org/doi/pdf/10.1145/3448016.3452838) [SIMOD 21]

## Database Traditional Technology

### Learning-based Index Design

#### Single-dimensional

1. [FITing-Tree: A Data-aware Index Structure](https://arxiv.org/pdf/1801.10207.pdf) [SIGMOD 19]
2. [ALEX: An Updatable Adaptive Learned Index](https://arxiv.org/pdf/1905.08898.pdf)  [aiXiv 20]
3. [The PGM-index: a fully-dynamic compressed learned index with provable worst-case bounds](http://www.vldb.org/VLDB/vol13/p1162-ferragina.pdf)  [VLDB 20]
4. [RadixSpline: a single-pass learned index](https://dl.acm.org/doi/pdf/10.1145/3401071.3401659) [aiDM 20]
5. [A Pluggable Learned Index Method via Sampling and Gap Insertion](https://arxiv.org/pdf/2101.00808.pdf) [aiXiv 21]
6. [The Case for Learned Index Structures](https://dl.acm.org/doi/pdf/10.1145/3183713.3196909) [SIGMOD 18]
7. [APEX: A High-Performance Learned Index on Persistent Memory](https://arxiv.org/pdf/2105.00683.pdf) [VLDB 22]
8. [Updatable Learned Index with Precise Positions](https://arxiv.org/pdf/2104.05520.pdf) [VLDB 21]
9. [Why Are Learned Indexes So Effective?](http://proceedings.mlr.press/v119/ferragina20a/ferragina20a.pdf) [ICML 20]
10. [Tuning Hierarchical Learned Indexes on Disk and Beyond](https://dl.acm.org/doi/abs/10.1145/3514221.3520255) [SIGMOD 22]
11. [FINEdex: A Fine-grained Learned Index Scheme for Scalable and Concurrent Memory Systems](http://www.vldb.org/VLDB/vol15/p321-hua.pdf) [VLDB 22]
12. [Are Updatable Learned Indexes Ready?](https://arxiv.org/pdf/2207.02900.pdf) [VLDB 22]
13. [CARMI: A Cache-Aware Learned Index with a Cost-based Construction Algorithm](https://www.vldb.org/VLDB/vol15/p2679-gao.pdf) [VLDB 22]
14. [NFL: Robust Learned Index via Distribution Transformation](https://www.vldb.org/VLDB/vol15/p2188-wu.pdf) [VLDB 22]
15. [The next 50 years in database indexing or: the case for automatically generated index structures](https://dl.acm.org/doi/10.14778/3494124.3494136) [VLDB 21]


#### Multi-dimensional

1. [Learning Multi-dimensional Indexes](https://dl.acm.org/doi/pdf/10.1145/3318464.3380579) [SIGMOD 20]
2. [LISA: A Learned Index Structure for Spatial Data](https://dl.acm.org/doi/abs/10.1145/3318464.3389703) [SIGMOD 20]
3. [Tsunami: A Learned Multi-dimensional Index for Correlated Data and Skewed Workloads](http://vldb.org/VLDB/vol14/p74-ding.pdf) [VLDB 21]
4. [NEIST: a Neural-Enhanced Index for Spatio-Temporal Queries](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8861025) [TKDE 21]
5. [Effectively Learning Spatial Indices](https://vbn.aau.dk/ws/files/391644098/p2341_qi.pdf) [VLDB 20]
6. [The ML-Index: A Multidimensional, Learned Index for Point, Range, and Nearest-Neighbor Queries](https://dbis.informatik.uni-kl.de/files/papers/ml-index-edbt2020.pdf) [EDBT 20]
7. [RW-Tree: A Learned Workload-aware Framework for R-tree Construction](https://ieeexplore.ieee.org/abstract/document/9835605/) [ICDE 22]

## Learning-based Configuration Advisor

### Index Advisor

1. [AI Meets AI: Leveraging Query Executions to Improve Index Recommendations](https://pages.cs.wisc.edu/~wentaowu/papers/sigmod19-auto-indexing.pdf) [SIGMOD 19]
2. [Magic mirror in my hand, which is the best in the land? An Experimental Evaluation of Index Selection Algorithms](http://www.vldb.org/VLDB/vol13/p2382-kossmann.pdf) [VLDB 20]
3. [An Index Advisor Using Deep Reinforcement Learning](https://baozhifeng.net/papers/cikm20-IndexRec.pdf) [CIKM 20]
4. [DBA bandits: Self-driving index tuning under ad-hoc, analytical workloads with safety guarantees ](https://arxiv.org/pdf/2010.09208) [ICDE 21]
5. [AutoIndex: An Incremental Index Management System for Dynamic Workloads](https://dbgroup.cs.tsinghua.edu.cn/ligl/papers/icde2022-autoindex.pdf) [ICDE 22] 
6. [SWIRL: Selection of Workload-aware Indexes using Reinforcement Learning ](https://openproceedings.org/2022/conf/edbt/paper-37.pdf) [EDBT 22]
7. [Budget-aware Index Tuning with Reinforcement Learning ](https://www.microsoft.com/en-us/research/uploads/prod/2022/06/mcts-full.pdf) [SIGMOD 22] 
8. [DISTILL: low-overhead data-driven techniques for filtering and costing indexes for scalable index tuning](https://www.microsoft.com/en-us/research/uploads/prod/2022/06/DISTILL.pdf) [VLDB 22]
9. [SmartIndex: An Index Advisor with Learned Cost Estimator](https://dl.acm.org/doi/abs/10.1145/3511808.3557163) [CIKM 22]
