# ADR 005: Building Farmacy Data Platform for business analytics
We want "Farmacy family" to have robust Event Bus for different services streaming from differenrt sources, and a Data Platform for business analytics.

# Status
Proposed

# Rationale
Farmacy Family systems needs to build the analytics that provides recommendations on the types of food for engaged customers as well as the view about what type of food Farmacy Food SMart fridges should fill in so that customers find right type of food based in a given geographical region. The systems needs an event streaming fucntionality to be built and fucntionality that provides platform for models to be built and rely on those models to recommend/suggest based on teh insights and user/request context.
In order to react to changes in customer behavior and their medical issues in a timely and flexible way, in order to better predict demand and optimal fridge contents, the system should gather data from data lake, analyze, learn and save the model that will be used to predict customer/gegraphical chnages nmeeded from food perspective. 

# Decision
We will use [Amazon Data Lake](https://aws.amazon.com/big-data/datalakes-and-analytics/) platform as it simplify every step of the ML workflow fully managed service that empowers developers and data scientists to build, train, and deploy ML models at scale and across use cases. It also has tools to run analytics reports, run SQL type queries to view data etc. AWS provides from data movement, data storage, data lakes, big data analytics, and machine learning (ML) to anything in between, AWS offers purpose-built services that provide the best price performance, scalability, and lowest cost.

We will be using Domain Events that will be sourced by all source systems and will be ingested into Farmacy Data Platform.

We need to build farmacy Data Lake platform with following key modules.
- Event Bus
    - Use Kafka
        - build real-time streaming data pipelines and applications that adapt to the data streams.
        - It combines messaging, storage, and stream processing to allow storage and analysis of both historical and real-time data.
- Streaming Ingestion
    - Kafka is great for durable and scalable ingestion of streams of events coming from many producers to many consumers.
    - Spark is great for processing large amounts of data, including real-time and near-real-time streams of events.
- Farmacy Data Lake
    - Data Lake for raw data collection.
    - Data comes from many types of sources. In fact, businesses rarely come to a data-driven decision with just one source. Instead, it takes numerous inputs, and much of that can be unstructured.
    - Data Lakes place these all in a single repository, saving time, effort, and cost
    - Data Lakes create a single repository for both structured and unstructured data, making it easy for data scientists to pull exactly what they need for analysis.
- Analytics Processor
    - Analytics and processing module for data analysis.
        - ML Training
        - ML Model
        - Analytics Processor

# Architectural Style
 - Event based architecture
 - Data Lake

# Consequences
 - Learn to Build this Platform
 - Need to maintain Business Analytics infrastructure.
