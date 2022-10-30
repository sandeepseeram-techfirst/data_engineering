# data_engineering - workshop notes 


Task1 - Run a Google Cloud Dataflow batch pipeline to import the data into BigQuery, and push errors to another dead-letter table for analysis.  

# Learning Points - Retry Mechanism 

If your application attempts to connect to the database and does not succeed, the database could be temporarily unavailable. In this case, sending too many simultaneous connection requests might waste additional database resources and increase the time needed to recover. Using exponential backoff prevents your application from sending an unresponsive number of connection requests when it can't connect to the database.

# Dataflow 
There are 3 windowing concepts in dataflow and each can be used for below use cases

1) Fixed window
2) Sliding window and
3) Session window.

Fixed window = any aggregation use cases, any batch analysis of data, relatively simple use cases.
Sliding window = Moving averages of data
Session window = user session data, click data and real time gaming analysis.


Task2 - Create a Cloud Dataproc cluster that uses the Google Cloud Storage connector

Dataproc is used to migrate Hadoop and Spark jobs on GCP. Dataproc with GCS connected through Google Cloud Storage connector helps store data after the life of the cluster. When the job is high I/O intensive, then we need to create a small persistent disk.

 # Partition Skew aka Data Skew 
 Partition skew, sometimes called data skew, is when data is partitioned into very unequally sized partitions. This creates an imbalance in the amount of data sent between slots. You can't share partitions between slots, so if one partition is especially large, it can slow down, or even crash the slot that processes the oversized partition.

 # Scenario 
 Have each application server write the bid events to Google Cloud Pub/Sub as they occur. Use a pull subscription to pull the bid events using Google Cloud Dataflow. Give the bid for each item to the user in the bid event that is processed first.

 The need is to collate the messages in real-time. We need to de-dupe the messages based on timestamp of when the event occurred. This can be done by publishing ot Pub-Sub and consuming via Dataflow.