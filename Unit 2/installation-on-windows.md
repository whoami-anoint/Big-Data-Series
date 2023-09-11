# Installing Apache Hadoop on Windows:

[![Share on Twitter](https://img.shields.io/badge/-Share%20on%20Twitter-blue?logo=twitter&style=flat-square)](https://twitter.com/intent/tweet?text=https%3A%2F%2Fgithub.com%2Fwhoami-anoint%2FBig-Data-Series)
[![GitHub discussions](https://img.shields.io/github/discussions/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/discussions)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/pulls)

## In Windows: 
Installing Apache Hadoop on Windows can be a bit more challenging compared to other operating systems like Linux or macOS. However, it is possible to set up Hadoop on a Windows machine. Below is a step-by-step guide in Markdown (md) script format for installing Hadoop on Windows:

## Prerequisites
1. **Java Installation:**
   - Download and install Java JDK 8 or later from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).

2. **Hadoop Binary:**
   - Download the Hadoop binary distribution from the official Apache Hadoop website (https://hadoop.apache.org/releases.html).

3. **Hadoop Environment Variables:**
   - Create environment variables for Hadoop in your Windows system.
     - Right-click on "This PC" or "My Computer" and select "Properties."
     - Click on "Advanced system settings" on the left.
     - Click the "Environment Variables" button.
     - Under "System Variables," click "New" and add the following variables:
       - Variable Name: `HADOOP_HOME`
       - Variable Value: The path to your Hadoop installation directory (e.g., `C:\hadoop`)
       - Variable Name: `JAVA_HOME`
       - Variable Value: The path to your Java JDK installation directory (e.g., `C:\Program Files\Java\jdk-14.0.2`)
     - Add the following to the "Path" variable:
       - `%HADOOP_HOME%\bin`
       - `%JAVA_HOME%\bin`

## Hadoop Installation

1. **Extract Hadoop Archive:**
   - Extract the Hadoop binary distribution (e.g., `hadoop-x.y.z.tar.gz`) to a directory (e.g., `C:\hadoop`).

2. **Hadoop Configuration:**
   - Navigate to the `C:\hadoop\etc\hadoop` directory and configure Hadoop by editing the `core-site.xml` and `hdfs-site.xml` files.
   - Sample `core-site.xml`:
     ```xml
     <configuration>
         <property>
             <name>fs.defaultFS</name>
             <value>hdfs://localhost:9000</value>
         </property>
     </configuration>
     ```
   - Sample `hdfs-site.xml`:
     ```xml
     <configuration>
         <property>
             <name>dfs.replication</name>
             <value>1</value>
         </property>
     </configuration>
     ```

3. **Format HDFS:**
   - Open a command prompt and run the following command to format the Hadoop Distributed File System (HDFS):
     ```
     hdfs namenode -format
     ```

4. **Start Hadoop Services:**
   - Start the Hadoop services using the following commands:
     ```
     start-dfs.sh
     start-yarn.sh
     ```

5. **Access Hadoop Web Interfaces:**
   - Open a web browser and access the following URLs to verify Hadoop services are running:
     - HDFS NameNode: http://localhost:9870/
     - ResourceManager: http://localhost:8088/

## Running Hadoop Jobs

Now that Hadoop is installed and running, you can submit MapReduce or other Hadoop jobs using the `hadoop` command.

Remember that running Hadoop on Windows may have limitations and performance differences compared to running it on Unix-like systems. Consider using a virtual machine or Windows Subsystem for Linux (WSL) for a more seamless experience if you encounter issues.

[Back to Overview](/Unit%202/1.1_Hadoop_installation.md)