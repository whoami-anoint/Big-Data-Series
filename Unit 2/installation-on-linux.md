# Installing Apache Hadoop on Linux:

[![Share on Twitter](https://img.shields.io/badge/-Share%20on%20Twitter-blue?logo=twitter&style=flat-square)](https://twitter.com/intent/tweet?text=https%3A%2F%2Fgithub.com%2Fwhoami-anoint%2FBig-Data-Series)
[![GitHub discussions](https://img.shields.io/github/discussions/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/discussions)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/pulls)

This guide will walk you through the process of installing Apache Hadoop on a Linux system. Hadoop is a powerful framework for distributed storage and processing of large datasets.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- **Java Installation:**
  - Install Java JDK (version 8 or later) if not already installed. You can usually install it using your package manager (e.g., `apt`, `yum`, or `brew`).

## Hadoop Installation

Follow these steps to install Hadoop:

1. **Download Hadoop:**
   - Visit the [Apache Hadoop Releases page](https://hadoop.apache.org/releases.html) and download the Hadoop binary distribution. Choose the version that suits your needs.

2. **Extract Hadoop Archive:**
   - Open your terminal and navigate to the directory where you downloaded the Hadoop binary.
   - Use the `tar` command to extract the downloaded archive:

     ```bash
     tar -zxvf hadoop-x.y.z.tar.gz
     ```

   Replace `x.y.z` with the version number you downloaded.

3. **Hadoop Configuration:**
   - Navigate to the Hadoop configuration directory:

     ```bash
     cd hadoop-x.y.z/etc/hadoop
     ```

   - Edit the `core-site.xml` and `hdfs-site.xml` files to configure Hadoop. Here are sample configurations:

     - `core-site.xml`:

       ```xml
       <configuration>
           <property>
               <name>fs.defaultFS</name>
               <value>hdfs://localhost:9000</value>
           </property>
       </configuration>
       ```

     - `hdfs-site.xml`:

       ```xml
       <configuration>
           <property>
               <name>dfs.replication</name>
               <value>1</value>
           </property>
       </configuration>
       ```

4. **Format HDFS:**
   - Format the Hadoop Distributed File System (HDFS) by running the following command:

     ```bash
     hadoop namenode -format
     ```

5. **Start Hadoop Services:**
   - Start the Hadoop services by running the following commands:

     ```bash
     start-dfs.sh
     start-yarn.sh
     ```

6. **Access Hadoop Web Interfaces:**
   - Open a web browser and access the following URLs to verify that the Hadoop services are running:
     - HDFS NameNode: [http://localhost:9870/](http://localhost:9870/)
     - ResourceManager: [http://localhost:8088/](http://localhost:8088/)

## Running Hadoop Jobs

With Hadoop successfully installed and running on your Linux system, you can now submit MapReduce or other Hadoop jobs using the `hadoop` command-line tools.

This concludes the installation of Hadoop on your Linux system.

For more advanced configurations and specific use cases, refer to the [Hadoop documentation](https://hadoop.apache.org/docs/current/).

[Back to Overview](/Unit%202/1.1_Hadoop_installation.md)
