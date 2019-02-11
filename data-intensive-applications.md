[https://learning.oreilly.com/library/view/spark-for-python/9781784399696/ch01.html](https://learning.oreilly.com/library/view/spark-for-python/9781784399696/ch01.html)

In order to understand the architecture of data-intensive applications, the following conceptual framework is used. The is architecture is designed on the following five layers:

* Infrastructure layer
* Persistence layer
* Integration layer
* Analytics layer
* Engagement layer

![](/assets/import.png)



## Infrastructure layer

The infrastructure layer is primarily concerned with virtualization, scalability, and continuous integration. In practical terms, and in terms of virtualization, we will go through building our own development environment in a VirtualBox and virtual machine powered by Spark and the Anaconda distribution of Python. If we wish to scale from there, we can create a similar environment in the cloud. The practice of creating a segregated development environment and moving into test and production deployment can be automated and can be part of a continuous integration cycle powered by DevOps tools such as **Vagrant**, **Chef**, **Puppet**, and **Docker**. Docker is a very popular open source project that eases the installation and deployment of new environments. The book will be limited to building the virtual machine using VirtualBox. From a data-intensive app architecture point of view, we are describing the essential steps of the infrastructure layer by mentioning scalability and continuous integration beyond just virtualization.

## Persistence layer

The persistence layer manages the various repositories in accordance with data needs and shapes. It ensures the set up and management of the polyglot data stores. It includes relational database management systems such as **MySQL** and **PostgreSQL**; key-value data stores such as **Hadoop**, **Riak**, and **Redis**; columnar databases such as **HBase** and **Cassandra**; document databases such as **MongoDB** and **Couchbase**; and graph databases such as **Neo4j**. The persistence layer manages various filesystems such as Hadoop's HDFS. It interacts with various storage systems from native hard drives to Amazon S3. It manages various file storage formats such as `csv`, `json`, and `parquet`, which is a column-oriented format.

## Integration layer

The integration layer focuses on data acquisition, transformation, quality, persistence, consumption, and governance. It is essentially driven by the following five Cs: _connect_, _collect_, _correct_, _compose_, and _consume_.

The five steps describe the lifecycle of data. They are focused on how to acquire the dataset of interest, explore it, iteratively refine and enrich the collected information, and get it ready for consumption. So, the steps perform the following operations:

* **Connect**
  : Targets the best way to acquire data from the various data sources, APIs

   offered by these sources, the input format, input schemas if they exist, the rate of data collection, and limitations from providers
* **Correct**
  : Focuses

   on transforming data for further processing and also ensures that the quality and consistency of the data received are maintained
* **Collect**
  : Looks

   at which data to store where and in what format, to ease data composition and consumption at later stages
* **Compose**
  : Concentrates

   its attention on how to mash up the various data sets collected, and enrich the information in order to build a compelling data-driven product
* **Consume**
  : Takes

   care of data provisioning and rendering and how the right data reaches the right individual at the right time
* **Control**
  : This sixth 
  _additional_
   step will sooner or later be required as the data, the

   organization, and the participants grow and it is about ensuring data governance

The following diagram depicts the iterative process of data acquisition and refinement for consumption:

![](https://learning.oreilly.com/library/view/spark-for-python/9781784399696/graphics/B03968_01_02.jpg "Integration layer")

## Analytics layer

The analytics layer is where Spark processes data with the various models, algorithms, and machine learning pipelines in order to derive insights. For our purpose, in this book, the analytics layer is powered by Spark. We will delve deeper in subsequent chapters into the merits of Spark. In a nutshell, what makes it so powerful is that it allows multiple paradigms of analytics processing in a single unified platform. It allows batch, streaming, and interactive analytics. Batch processing on large datasets with longer latency periods allows us to extract patterns and insights that can feed into real-time events in streaming mode. Interactive and iterative analytics are more suited for data exploration. Spark offers bindings and APIs in Python and R. With its **SparkSQL** module and the Spark Dataframe, it offers a very familiar analytics interface.

## Engagement layer

The engagement layer interacts with the end user and provides dashboards, interactive visualizations, and alerts. We will focus here on the tools provided by the PyData ecosystem such as Matplotlib, Seaborn, and Bokeh.

