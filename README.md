# Distributed TensorFlow Example (O'Reilly Blog Post)

There are three pieces of example code here:
  
  * a Spark program to launch TensorFlow functions inside a Spark 'mapper' function. This is useful for hyperparameter optimization (parameter sweeps)
  
  * a TensorFlowOnSpark program that can be used with Hops Hadoop
  
  * a Horovod program that can be used with Hops Hadoop


Hyperparameter Optimization using Spark/TensorFlow
====

This has been tested on a Ubuntu 16.04 machine, but should work on other platforms.
We recommend that you do the following inside a new conda environment, but you may also run it without a virtual environment.


    # Download and install standalone Spark
    wget http://apache.mirrors.spacedump.net/spark/spark-2.2.1/spark-2.2.1-bin-hadoop2.7.tgz
    tar zxf spark-2.2.1-bin-hadoop2.7.tgz
    export SPARK_HOME=$(pwd)/spark-2.2.1-bin-hadoop2.7
    export PATH=$SPARK_HOME/bin:$PATH
    pip install pyspark
    pip install tensorflow==1.4.0
    pip install jupyter
    git clone https://github.com/hopshadoop/distributed-tf.git
    cd distributed-tf
    
    export PYSPARK_DRIVER_PYTHON=jupyter
    export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
    pyspark
    #The 'pyspark' command should start a Jupyter Notebook in your web browser. 
    #You can then create a new 'pyspark' notebook and test it using this code
    
    


TensorFlowOnSpark 
===================

You can get more details on [TensorFlowOnSpark at its github repo](https://github.com/yahoo/TensorFlowOnSpark).

Horovod
====================

More details on [Horovod at its github repo](https://github.com/uber/horovod).
    
    
Distributed TensorFlow on Hops
=====================

For details on how to install and setup Hops, so that you can run all three programs in a Tour, go to [hops.io](http://www.hops.io).

