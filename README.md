# ALY6110_DATA-MANAGEMENT-AND-BIG-DATA

#Install Java: 
#Following command will install necessary JAVA JDK to run Spark Cluster:
$ sudo apt update && upgrade
$sudo apt-get install openjdk-11-jre
$ sudo apt-get install openjdk-11-jdk

#Check your Java version:
$java -version

#Install Python3: 
#The following commands will install necessary dependencies and packages for Python3
$sudo apt update && sudo apt upgrade
$sudo apt install python3 python3-pip ipython3
$sudo apt install python3-pip
$pip3 install jupyter py4j pyspark

#Set Alias for Jupyter Notebook:
$nano ~/.bashrc

#Add these lines in the end of the files or your preferred location:

alias jupyter-notebook="~/.local/bin/jupyter-notebook --no-browser"

$source ~/.bashrc


#Install Scala: 
Download Scale and Unzip Sclala:
$wget https://downloads.lightbend.com/scala/2.13.3/scala-2.13.3.tgz
$tar xvf scala-2.13.3.tgz

#add Scala on bashrc:
$nano ~/.bashrc
#Please add these lines in the end of the files

export SCALA_HOME="/home/aitmsi/scala-2.13.3"
export PATH=$PATH:$SCALA_HOME/bin

#Please save close and Source the file
$source ~/.bashrc

#Check the Scala Version:
$scala -version

#Install Spark with Hadoop 
#Install Spark with Hadoop using following Steps:

#Download and Unzip Spark with Hadoop:
$wget https://archive.apache.org/dist/spark/spark-3.1.1/spark-3.1.1-bin-hadoop3.2.tgz
$tar xvf spark-3.1.1-bin-hadoop3.2.tgz

#Open bashrc:
$nano ~/.bashrc

#Add following lines in the bashrc file
export SPARK_HOME="/home/username/spark-3.1.1-bin-hadoop3.2"
export PATH=$PATH:$SPARK_HOME/bin

#Save, close and source the file 
$source ~/.bashrc

#Activate Spark
#Run the following commands to activate the cluster
$cd $SPARK_HOME
$./sbin/start-master.sh
$./sbin/start-worker.sh spark://ubuntu1:7077

#test spark
$spark-shell

$jupyter-notebook

#stop cluster
$./sbin/stop-master.sh
$./sbin/stop-worker.sh


#notebook jupyter link 
http://127.0.0.1:8888/notebooks/DIGHE_Jupyter_Notebook.ipynb#
