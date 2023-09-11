# Unit 2: Introduction to Hadoop
## Chapter: Introduction to Hadoop
### **What is Hadoop:**
  - Hadoop is a robust open-source framework designed for the distributed storage and processing of massive and diverse datasets.
  - It was initially developed by Apache Software Foundation and is now widely adopted for big data analytics.

### **Why Hadoop:**
  - **Scalability:** Hadoop can easily scale horizontally by adding more commodity hardware to accommodate growing data volumes and computational needs.
  - **Fault Tolerance:** One of Hadoop's key strengths is its ability to handle hardware failures gracefully. It does this through data replication, ensuring that data is stored redundantly across multiple nodes.
  - **Cost-Effective:** By utilizing low-cost commodity hardware, Hadoop offers a cost-effective solution for storing and analyzing vast amounts of data.

### Hadoop and its Ecosystem
- **Hadoop Ecosystem:**
  - The Hadoop ecosystem comprises a rich collection of tools and frameworks that complement Hadoop's core functionality.
  - These tools extend Hadoop's capabilities and cater to various aspects of data processing, ingestion, and analysis.

- **Examples:**
  - **HBase:** HBase is a NoSQL database that runs on top of Hadoop and provides real-time, random read/write access to large datasets. It's suitable for applications requiring high-speed data retrieval.
  - **Hive:** Hive is a data warehousing and SQL-like querying tool that simplifies data analysis in Hadoop. It allows users to write SQL queries to extract insights from structured data.
  - **Pig:** Pig is a high-level scripting language used for data flow scripting in Hadoop. It's particularly useful for transforming and processing large datasets.

### Hadoop Distributed File System (HDFS)
- **HDFS Overview:**
  - HDFS is the primary storage system in Hadoop, designed to store and manage enormous datasets efficiently.
  - It achieves this by breaking data into blocks, typically 128MB or 256MB in size, and storing multiple replicas of these blocks across the Hadoop cluster.

- **Key Features:**
  - **Fault Tolerance:** HDFS ensures data durability by replicating data blocks across multiple nodes. Even if some nodes fail, data remains accessible.
  - **High Throughput:** HDFS is optimized for streaming data access, making it well-suited for applications that require high-speed data ingestion and retrieval.

### MapReduce Framework and Programming Model
- **MapReduce:**
  - MapReduce is a programming model and processing framework used for distributed data processing within Hadoop.
  - It divides data processing into two main phases: the Map phase and the Reduce phase.

- **Map and Reduce Functions:**
  - **Mappers:** Mappers are responsible for processing and transforming input data into key-value pairs. They distribute data across the cluster.
  - **Reducers:** Reducers aggregate and summarize the results produced by the mappers, producing the final output.

- **Scalability:**
  - MapReduce is inherently scalable. It can process vast datasets by distributing the workload across numerous nodes in a Hadoop cluster, which allows for parallel processing.

### Hadoop Yarn (Yet Another Resource Negotiator)
- **Yarn Overview:**
  - Yarn is the resource management layer in Hadoop that efficiently manages and allocates resources for running various applications on a Hadoop cluster.

- **Benefits:**
  - **Resource Utilization:** Yarn optimizes resource allocation, ensuring efficient usage of cluster resources. It enables multiple applications to coexist and run simultaneously.
  - **Multi-Tenancy:** Yarn supports multi-tenancy, allowing different workloads, including batch processing and real-time analytics, to share the same cluster resources.

### Hadoop Ecosystem Tools
- **Various Tools:**
  - The Hadoop ecosystem offers a vast array of tools and libraries to cater to a wide range of big data use cases.

- **Examples:**
  - **Apache Spark:** Apache Spark is a high-speed, in-memory data processing framework that complements Hadoop's batch processing capabilities. It's well-suited for iterative and real-time analytics.
  - **Sqoop:** Sqoop is a tool designed for efficiently importing and exporting data between Hadoop and relational databases. It simplifies data transfer tasks.
  - **Kafka:** Kafka is a distributed event streaming platform that handles real-time data feeds and supports stream processing. It's crucial for building real-time data pipelines.
