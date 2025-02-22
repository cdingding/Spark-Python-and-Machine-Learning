# Spark Python Notebooks  

This is a collection of [IPython notebook](http://ipython.org/notebook.html)/[Jupyter](https://jupyter.org/) 
notebooks intended to train the reader on different [Apache Spark](http://spark.apache.org/) concepts, from 
basic to advanced, by using the **Python** language.  

## Installation on Mac
Reference: 
https://towardsdatascience.com/how-to-get-started-with-pyspark-1adc142456ec 

Verified compatibility for new version of relevant packages:    
Pyspark: spark-2.4.3-bin-hadoop2.s7.tgz
Form terminal to unzip the spark: 
tar -xzf spark-2.4.3-bin-hadoop2.7.tgz
mv spark-2.4.3-bin-hadoop2.7 ~/spark243

Java: Regist on Oracel and download and install Java version 1.8

Add lines below to ~/.bash_profile:
ln -s ~/spark243 ~/spark
export JAVA_HOME=$(/usr/libexec/java_home)
export SPARK_HOME=~/spark
export PATH=$SPARK_HOME/bin:$PATH
export PYSPARK_PYTHON=python3

export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS=‘notebook'
From terminal to launch Jupyter notebook with PySpark:
	$> pypark

## Instructions  

A good way of using these notebooks is by first cloning the repo, and then 
starting your own [IPython notebook](http://ipython.org/notebook.html)/[Jupyter](https://jupyter.org/) in 
**pySpark mode**. For example, if we have a *standalone* Spark installation
running in our `localhost` with a maximum of 6Gb per node assigned to IPython:  

    MASTER="spark://127.0.0.1:7077" SPARK_EXECUTOR_MEMORY="6G" ~/spark-2.4.3-bin-hadoop2.7/bin/pyspark

Notice that the path to the `pyspark` command will depend on your specific 
installation. So as requirement, you need to have
[Spark installed](https://spark.apache.org/docs/latest/index.html) in 
the same machine you are going to start the `IPython notebook` server.     

For more Spark options see [here](https://spark.apache.org/docs/latest/spark-standalone.html). In general it works the rule of passing options
described in the form `spark.executor.memory` as `SPARK_EXECUTOR_MEMORY` when
calling IPython/pySpark.   
 
## Datasets  

We will be using datasets from the [KDD Cup 1999](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html). The results 
of this competition can be found [here](http://cseweb.ucsd.edu/~elkan/clresults.html).  

## References

The reference book for these and other Spark related topics is:  

- https://github.com/jadianes/spark-py-notebooks

- *Learning Spark* by Holden Karau, Andy Konwinski, Patrick Wendell, and Matei Zaharia.  

