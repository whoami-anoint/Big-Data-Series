# Hadoop Installation on AWS EC2

[![Share on Twitter](https://img.shields.io/badge/-Share%20on%20Twitter-blue?logo=twitter&style=flat-square)](https://twitter.com/intent/tweet?text=https%3A%2F%2Fgithub.com%2Fwhoami-anoint%2FBig-Data-Series)
[![GitHub discussions](https://img.shields.io/github/discussions/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/discussions)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/pulls)

This guide will walk you through the process of installing Apache Hadoop on an Amazon Web Services (AWS) EC2 instance. Hadoop is a powerful framework for distributed storage and processing of large datasets.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- **AWS Account:**
  - You need an AWS account to create and manage EC2 instances.

- **EC2 Instance:**
  - Launch an EC2 instance using your preferred Linux distribution (e.g., Amazon Linux, Ubuntu).
  - Ensure that you have SSH access to your EC2 instance.

- **Java Installation:**
  - Install Java JDK (version 8 or later) on your EC2 instance. You can usually install it using your package manager (e.g., `apt`, `yum`, or `brew`).

## Hadoop Installation on AWS EC2

Follow these steps to install Hadoop on your AWS EC2 instance:

1. **SSH into Your EC2 Instance:**
   - Open your terminal and SSH into your EC2 instance using the public IP address or DNS name:

     ```bash
     ssh -i your-key-pair.pem ec2-user@your-ec2-public-ip
     ```

   Replace `your-key-pair.pem` with the path to your AWS key pair and `your-ec2-public-ip` with your EC2 instance's public IP address or DNS name.

2. **Download Hadoop:**
   - Inside your EC2 instance, download the Hadoop binary distribution by visiting the [Apache Hadoop Releases page](https://hadoop.apache.org/releases.html). Choose the version that suits your needs.

3. **Extract Hadoop Archive:**
   - Use the `tar` command to extract the downloaded archive:

     ```bash
     tar -zxvf hadoop-x.y.z.tar.gz
     ```

   Replace `x.y.z` with the version number you downloaded.

4. **Hadoop Configuration:**
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

5. **Format HDFS:**
   - Format the Hadoop Distributed File System (HDFS) by running the following command:

     ```bash
     hdfs namenode -format
     ```

6. **Start Hadoop Services:**
   - Start the Hadoop services by running the following commands:

     ```bash
     start-dfs.sh
     start-yarn.sh
     ```

7. **Access Hadoop Web Interfaces:**
   - Open a web browser and access the following URLs to verify that the Hadoop services are running:
     - HDFS NameNode: `http://your-ec2-public-ip:9870/`
     - ResourceManager: `http://your-ec2-public-ip:8088/`

## Running Hadoop Jobs

With Hadoop successfully installed and running on your AWS EC2 instance, you can now submit MapReduce or other Hadoop jobs using the `hadoop` command-line tools.

This concludes the installation of Hadoop on your AWS EC2 instance.

For more advanced configurations and specific use cases, refer to the [Hadoop documentation](https://hadoop.apache.org/docs/current/).

[Back to Overview](/Unit%202/1.1_Hadoop_installation.md)
