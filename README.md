# Big Data Engineering test

The goal of this test is to evaluate your technical knowledge, asses yourself and open a path to a clear and concise technical interview. The technical interview is not going to be a whiteboard-let's-talk-about-binary-tree-data-sorting but an explanation about the steps you took, why you did so and what was your line of thinking.

Remember, you already went through our screening and first interview; this is the beginning and preparation for a mutual technical conversation.

## Where to run

So, while you are developing I expect that you are capable of setting up a localstack with the tools you select. You will need Spark, HBase, Kafka, Hive and S3/Azure Blob Storage/HDFS... feel free to change these components if you want to use different tools.

> You must use Scala overall plus Spark and Kafka on the assignments that require it.

> You do not need to use HBase... you can change to another column-store DB or cloud databases, as long you show you understand the concepts.

> You do not need to use Hive... you can use just Athena on S3, BigTable on GCP or whatever that gets it done and can easily create tables from S3/HDFS.

> I say S3/HDFS because it is up to you to use a cloud object storage or create a Hadoop cluster with HDFS or just use Azure Blob Storage.

> Yup, we use cloud a lot.

## 1. Basic HDFS & Hive on Spark

Build a Scala application using Spark and execute against Hive & Spark to do the following:
- upload the `.csv` files on <a href="data-spark/">`data-spark`</a> to HDFS
- create tables on Hive for each `.csv` file
- output a dataframe on Spark that contains `DRIVERID, NAME, HOURS_LOGGED, MILES_LOGGED` so you can have aggregated information about the driver.

Besides the code on a repo, explain you steps and impression in <a href="`MyExperience.md">`MyExperience.md`</a>.

## 2. HBase

Build a Scala application using Spark to do the following: 
- create a table `dangerous_driving` on HBase
- load <a href="data-hbase/dangerous-driver.csv">`dangerous-driver.csv`</a>
- add a 4th element to the table from `extra-driver.csv`
- Update `id = 4` to display `routeName` as `Los Angeles to Santa Clara` instead of `Santa Clara to San Diego`
- Outputs to console the Name of the driver, the type of event and the event Time if the origin or destination is `Los Angeles`.

Same thing here, besides the code on a repo, explain you steps and impression in <a href="`MyExperience.md">`MyExperience.md`</a>.

## 3. Kafka Ingestion

Setup a Kafka cluster and create a third application that ingests the raw stream from Kafka with the following:
- Ingest `raw` stream into HDFS. How? Choose your preferred tool - Kafka (Streaming or Connect), Spark (Regular or Streaming), Flink, Storm, NiFi... up to you. 
- Choose if you want to do in batches or real-streaming.
<br> I expect you to have issues on the connectivity and make it work here, so do not worry... put your learnings and explain your steps in <a href="`MyExperience.md">`MyExperience.md`</a>.

## Extra Points
You get extra points if you (3) using Spark Structured Streaming.

## Doubts &/Or Submission

Clone this repository and create your own version of it. In the end, commit and push your solution and send us your GitHub repo link.
<br> Feel free to reach out to [Alyona Galyeva](mailto:alyona.galyeva@linkit.nl).
