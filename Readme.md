#Spark on Mac Feb 2017

##Impatient Guide

This will take aprox 10 mins from beginning to end.

You then have Spark installed on a Mac

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install scala
#If you are using IntelliJ
export SCALA_HOME=/usr/local/opt/scala/idea   #Note you need to do this when you next login
wget -nc http://d3kbcqa49mib13.cloudfront.net/spark-2.1.0-bin-hadoop2.7.tgz
tar -xvzf spark-2.1.0-bin-hadoop2.7.tgz # to extract the contents of the archive
mv spark-2.1.0-bin-hadoop2.7 /usr/local/spark # moves the folder from Downloads to local
#Setup my env file for spark
echo "export SCALA_HOME=/usr/local/opt/scala/idea" > myspark.env
echo "alias spark=/usr/local/spark/bin/pyspark" >> myspark.env
echo "export JAVA_HOME=$(/usr/libexec/java_home)" >> myspark.env
#use your env file
source myspark.env
#Now run Spark
spark
```

