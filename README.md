Introduction:

From last many years it has been a debatable topic that why there exists a different SQL based ecosystem? Which one is best suited in what condition? We thought why not do a performance based project related to all these 3 ecosystem (HIVE vs IMPALA vs SPARK SQL). Performance analysis can be done on various metrics like CPU, I/O, Impacted CPU, Query response time etc.
but due to time constraint we could perform analysis only at query response time parameter.

Performed performance bench marking based on query response time by executing same set of queries on Hive, Impala and Spark-SQL execution engines.
We took complex queries like "Window Function - RANK(), Aggregate Function - COUNT(), Multi-Level Join, Computing Duplicate row count" into consideration.
We optimized Hive ecosystem using methods like Partitioning,ORC storage format and setting parameter to force "MAP JOIN".
Concluded by creating visualization performance comparison chart using Tableau.


Conclusion:

•	Many customers who wants to do analysis on large data uses Hive for data preparation.
•	Hive is still recommended for batch processing as it is also fault tolerant.
•	Impala is a best solution now to use BI tools directly with HDFS.
•	It is better to use it for small queries as it doesn't provide fault tolerant behavior.
•	Whereas, Spark SQL is a best solution for application development as it mixes procedural spark and SQL jobs using Java, Scala and Python.
•	It all depends upon what kind of operation customer wants, Nature of data and cost of operations to be performed.

Challenges:

•	Complex queries could not be executed due to container size restriction – As we performed the execution on Virtual Machine so were running short of Task Container size.
•	Queries were getting hanged, so we had to restart the cloudera Manager
