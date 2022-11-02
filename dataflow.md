After messages have been captured from the streaming input sources you need a way to pipe that data into a data warehouse for analysis. This is where Dataflow comes in.

Dataflow creates a pipeline to process both streaming data and batch data. 
“Process” in this case refers to the steps to extract, transform, and load data, or ETL. 

When building a data pipeline, data engineers often encounter challenges related to
coding the pipeline design and implementing and serving the pipeline at scale. During the pipeline design phase, there are a few questions to consider: Will the pipeline code be compatible with both batch and streaming data, or will it
need to be refactored? Will the pipeline code software development kit, or SDK, being used have all the transformations, mid-flight aggregations and windowing and be able to handle late data?


Are there existing templates or solutions that should be referenced? 
A popular solution for pipeline design is Apache Beam. 

It’s an open source, unified programming model to define and execute data processing pipelines, including ETL, batch, and stream processing. Apache Beam is unified, which means it uses a single programming model for both batch and streaming data. It’s portable, which means it can work on multiple execution environments, like Dataflow and Apache Spark, among others. And it’s extensible, which means it allows you to write and share your own connectors and transformation libraries. Apache Beam provides pipeline templates, so you don’t need to build a pipeline from nothing. And it can write pipelines in Java, Python, or Go. The Apache Beam software development kit, or SDK, is a collection of software development tools in one installable package.

It provides a variety of libraries for transformations and data connectors to sources and sinks. Apache Beam creates a model representation from your code that is portable across many runners. Runners pass off your model for execution on a variety of different possible engines, with Dataflow being a popular choice.