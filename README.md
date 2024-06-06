INTRODUCTION:

This ETL pipeline leverages a combination of robust technologies—API, Python, Kafka, Spark, and PostgreSQL—to handle high-throughput data streams and ensure seamless data extraction, transformation, and storage.Data extraction and streaming to processing and storage, making it an integral solution for handling large-scale data efficient


ARCHITECTURE:

![Screenshot 2024-06-05 113149(1)](https://github.com/Athiravk19/Real-Time-ETL-Pipeline/assets/161004016/8f6c9006-af90-4f04-8a3a-0965adf31a3d)




Dataset/api:This api contains personal information of random individuals-Random User generator "https://randomuser.me/api/" 


COMPONENTS:

API:  The source of data, which is accessed via an API.
Python: Used to extract data from the API. Python scripts can handle data extraction and   initial processing.

Kafka: A distributed streaming platform that handles the data stream from Python. Kafka can manage high-throughput data streams and ensures reliable data transfer.
Zookeeper: A centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services. It is used by Kafka to manage brokers.
Spark: A unified analytics engine for big data processing, with built-in modules for streaming, SQL, machine learning, and graph processing. Spark processes the data streamed by Kafka.
PostgreSQL: A relational database where the processed data is stored. It provides robust data storage and querying capabilities.




WORKFLOW:

Extract: Data is extracted from the API using Python.

Transform: The extracted data is streamed to Kafka for further processing.

Load: Kafka streams the data to Spark for transformation and processing.

Store: The processed data is streamed back from Spark and loaded into PostgreSQL.

