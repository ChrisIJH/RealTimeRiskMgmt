Real Time Risk Management
================
Introduction
------------
This is the project of Big Data Analytics Course at Columbia University.
This project consists of 2 different jobs to implement of risk management by finding **_Value-At-Risk(VaR)_** using 5-minute-tick-data with [Apache Spark][1]. One is data collecting job which is coded in _Java_. The other is compuation job for finding VaR coded in _Python_ with [**Spark Python API**][2]. This project will give an example of implementing VaR by utlizing not only [**Hadoop ditributed file system**][4] and spark cluster computing platform but also its computing algorithm with iPython's interactive analytic functionality. We used [*Google Cloud Service*][3].

[1]: http://spark.apache.org
[2]: http://spark.apache.org/docs/1.0.2/api/python/index.html
[3]: https://cloud.google.com
[4]: https://hadoop.apache.org


System
------
- Google Cloud Service: 
  - Master node and workers for Apache Spark.
  - Name/Secondary node, Data nodes
- iPython : For interactive analytics
  - Setup with Pyspark module
  - Setup for remote access to server
- Apache Hadoop
- Apache Spark


Software Packages
-----------------
- Data Collecting Module
  - TickDataReadWrite.java : Jave file for data collecting and write them to Apache Hadoop Ditributed File System.
  - ReadTickData.jar : Jar package from TickDataReadWrite.java
    - Usage:

    `hadoop jar com.cijhwang.hadoop.TickDataReadWrite [ 0: 10 day 5 min data, 1: intra day 1 min data]`
  - You may want to create crontab for automatic operations for data collecting.
- Computing Module
  - GetVar.py : Python file for computing Value-At-Risk of Portfolio using Apache Spark Python API.
- sample file
  - sp500: Ticker list






