# Stream-with-Pulsar
pipeline for stream processing.
Project Overview: Real-time Sales Data Processing and Analysis with Docker, Minio, Apache Pulsar, and PySpark

In this dynamic data stream project, the objective is to process and analyze real-time sales data within the Docker environment, utilizing tools such as Apache Pulsar for streaming, Minio for storage, and PySpark for data processing. The primary dataset consists of a sales table featuring essential details like product information, transaction amounts, user IDs, and localizations.

The entire project is encapsulated within a Jupyter/All-Spark-Notebook running on Docker, providing an interactive and collaborative environment for seamless development and execution.

Data Generation:
The project kicks off by generating a static dataset with a date-time column using PySpark. This dataset captures transactional details, including sender, receiver, and transaction amounts, setting the stage for subsequent analysis.

Data Enrichment:
A complementary dataset for data enrichment is created to augment the analysis. This dataset includes additional user information, such as bank-emitter details and location codes, enhancing the depth of the overall analysis.

Data Streaming with Pulsar:
A robust Python code, executed within the Jupyter/All-Spark-Notebook environment, is developed to read data from the static datasets and push it seamlessly into Apache Pulsar. This establishes a real-time streaming environment for continuous data ingestion and processing.

Real-time Filtering and Enrichment:
Within the Apache Pulsar environment, data is dynamically filtered based on specified conditions, ensuring the quality of the incoming stream. Subsequently, the streaming data is enriched with additional user details from the static dataset, creating a comprehensive dataset for further analysis.

Window Functions and Aggregation with PySpark:
PySpark's capabilities are harnessed to apply window functions to the enriched stream. For example, the project computes the average transaction value per bank-emitter using PySpark's advanced analytics functionalities. This step ensures a nuanced understanding of sales patterns and user behavior over specified time intervals.

Storage in Minio via Delta Lake:
The final processed and enriched data is securely stored in Minio, a high-performance object storage service, using Delta Lake. This combination ensures data integrity, scalability, and efficient retrieval for future analyses or reporting.

In summary, this end-to-end data stream project harnesses the power of Docker, Minio, Apache Pulsar, and PySpark within a Jupyter/All-Spark-Notebook environment. It seamlessly processes real-time sales data, enriches it with additional information, applies advanced analytics, and securely stores the results, providing a robust foundation for ongoing data-driven insights.
