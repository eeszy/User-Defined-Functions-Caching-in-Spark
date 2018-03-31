# User-Defined-Functions-Caching-in-Spark
- Implemented in-memory UDF caching to ensure that the UDF is only called once per distinct input value
- Optimized the UDF caching via external hashing to solve the problem of performance degradation when there were too many distinct values to fit in memory
- Implemented disk-based hash partitioning, used coarse grained hash function to stream an input into multiple partition relations on disk
- Implemented out-of-core UDF caching which can handle large datasets based on the optimization above
