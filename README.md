## Introduction
This benchmark provides a ground truth for evaluating table union search algorithms. All tables are synthesized from Open Data tables. For more details, please refer to: 

F. Nargesian, E. Zhu, K. Pu, R. J. Miller, [*Table Union Search on Open Data*](http://www.vldb.org/pvldb/vol11/p813-nargesian.pdf)

## Resources

This suite consists of two benchmarks of size ~1,300 and ~5,000 tables. 
These benchmarks are available in sqlite databases:

Small:
* [base.sqlite](https://storage.googleapis.com/table-union-benchmark/small/base.sqlite) (96 MB)
* [benchmark.sqlite](https://storage.googleapis.com/table-union-benchmark/small/benchmark.sqlite) (1.3 GB) 
* [groundtruth.sqlite](https://storage.googleapis.com/table-union-benchmark/small/groundtruth.sqlite) (196 MB)

Large:
* [benchmark.sqlite](https://storage.googleapis.com/table-union-benchmark/large/benchmark.sqlite) (1.59 GB)
* [groundtruth.sqlite](https://storage.googleapis.com/table-union-benchmark/large/groundtruth.sqlite) (3.5 GB)

The "base.sqlite" databases contain the base tables used for generating the benchmark 
and "benchmark.sqlite" databases contain unionable tables. 
For each benchmark, we provided a ground truth database in "groundtruth.sqlite". 
These databases contain three tables. 
Table "att_groundtruth" provides all mappings between unionable attributes. 
Table "alignment_groundtruth" provides the size of the max-alignment (c) between two tables. 
Finally, table "recall_groundtruth" provides the number of tables that are unionable with a benchmark table. 

We also included a script in the benchmark that converts benchmark tables to csv files. 
