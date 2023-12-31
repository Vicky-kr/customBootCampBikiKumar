# customBootCampBikiKumar

> **Day 1**

  - Data : Any Information.

  - Database : Collection of Data.

  - E-R Diagram : Entity Relationship diagram to see the relationship between tables.

  - Normalisation : Conversion of single table into multiple table.

  - Denormalisation : Conversion of multiple table into single table.

  - Case study on E-R Diagram : Made an E-R diagram of Book.

  - Case study on Normalisation : Made 1NF table , 2NF....

  - Dimension modeling : Types of table fact table , Dimension Table , Types of schema SnowFlakes schema and Star Schema

  - Slowly Changing Dimension (Type 1,2,3) : SCD 1,SCD 2,SCD3

> **Day 2**
  - Data
  - Structure , Semi Structure, Unstructure,
  - Big Data
  - Batch and Stream data processing
  - Parallel & Sistributive processing
  - Framework of data : Hadoop, Spark
  - Data Warehouse, Data Lake, Lake House
  - Cloud Computing
  - Public Cloud,Private Cloud,Hybrid Cloud
  - Capex & Opex
  - IaaS,PaaS,SaaS
  - Azure fundamentals: Region Pairs ,Availability Zone,Azure resource Manager
  - Subscription,Resource Group,Resources

> **Day 3**
  - Database
  - Single & Elastic Database
  - Schemas
  - Views
  - DDL
  - DML
  - DCL
  - CRUD Operations
  - Constraints
  - WHERE clause
  - Group by
  - Having

> **Day 4**
  - Joins
  - Inner, Left Right,Self,Outer,Cross
  - Union
  - Stored Procedure
  - Functions
  - Scalar & Table view
  - Indexing
  - Cluster & Non Clustering Indexing
  - Columnar Indexing

> **Day 5**
  - Azure Storage
  - Data lake
  - Data warehouse
  - Data lakehouse
  - Blob Storage
  - Gen 2 storage Data lake
  - Storage account

> **Day 6**
  - Data Lake
  - Azure blob storage
  - Azure Data lake
  - File Share
  - Container
  - Upload the file to blob service
  - Table

> **Day 7**
  - Azure Data Factory
  - Access
  - Authentication
  - Creation of container in Data Lake
  - Uploading file into Azure Data Lake Gen2

> **Day 8**
  - Azure Data Factory
  - Source Transformation
  - Sink Transformation
  - API Integration
  - CDC

> **Day 9**
  - Azure Synapse Analytics
  - Creation of Azure Synapse Account
  - Synapse Studio
  - Pipeline
  - SQL Pool

> **Day 10**
  - Intro to Power BI. 
  - Data loading
  - Different data transformations – Removing duplicates, merge queries, slicers.
  - Parameters
  - DAX, Calculated columns, measures
  - Simple analysis charts

> **Day 11**
  - Power BI
  - Connection with Azure SQL
  - Univariate and Bivariate analysis
  - Exploring various analysis charts
  - Reports and dashboard

> **Day 12**
  - Intro to Python
  - Different data types and their syntaxes with examples
  - Different operators in python
  - Tuples, Dictionaries
  - User-defined functions
  - If-Else statements
  - Zip functions, Enumerate, Counter

> **Day 13**
  - Args
  - kwargs - keyword arguments
  - Keyword and positional parameters
  - Lambda Function
> **Day 14**
  - Big Data
  - Introduction to Spark
  - Architecture of Spark
  - Pyspark
  - Spark Session
  - Read File Using Spark

> **Day 15**
  - RDD
  - Data Transformation
  - SQL Query in PySpark
  - Filter Data 
  - Parquet 
  - Delta Table

> **Day 16**
  - Azure Data Bricks
  - Cluster
  - Caching
  - Persist and Unpersist
  - Data Cleaning 
  - Reading Data from uploaded file

> **Day 17**
  - Mounting and why mounting
  - Parameterization
  - Widgets
  - Azure Data Bricks Connection with another Services
  - Delta Table
  - Scheduling
  - Connection to Azure SQL DB through JDBC Connection

> **Day 18**

## Docker 

> Steps to Containerizing a Flask app

  - **app.py**
  - add **requirements.txt** file which contains all the libraries
  - add **Dockerfile** without any extension and add instructions in it
  - create image using command **`docker build -t app-name .`**
  - to check it use command **`docker images`**

> Steps to push to Azure Container Registry

  - Install Azure cli using command **` curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash`**
  - Login in Azure using command **`az login -u userName -p password`**
  - Create a Resource group in Azure using command **`az group create --name RG_Shell_IDA --location eastus`**
  - Create a Azure Container Registry using command **`az acr create --name cridashell --resource-group RG_Shell_IDA --sku Standard --admin-enabled true`**
  - Login in the Azure Container Registry using command **`az acr login --name acrName`**
  - Then enter the **username** and **password** (**from Azure Container Registry**)
  - name the container using command **`docker tag cridashell/flask-app:latest cridashell.azurecr.io/flask-app:latest`**
  - push the image into ACR using command **`docker push cridashell.azurecr.io/flask-app:latest`**

## Kubernetes

> Steps to Deploy the image using kubernetes

  - create a folder name **kubernetes** and add two files **service.yaml** and **deployment.yaml**
  - add necessary code in both the file
  - now run the command **`kubectl apply -f deployment.yaml`** and **`kubectl apply -f service.yaml`**
  - now run the command **`az aks get-credentials --resource-group RG_Shell_IDA --name K8S_Cluster`**
  - now run the command **`az aks update -n K8S_Cluster -g RG_Shell_IDA --attach-acr cridashell`**
  - now attach the container port to localhost port using command **`kubectl port-forward flask-app-deployment-658d6f6d66-djvm5 8000:8000`**

> **Day 19**
  - Intro to Azure DevOps
  - Azure Board
  - Epic,Feature,User Story,Tasks
  - Creating a simple project with proper naming
  - Creating Repos
  - Creating Pipelines
  - CI/CD

> **Day 20**
  - Machine Learning
  - Azure ML Service
  - ML Workspace
  - Pipeline
  - Dataset
  - Filter Data

> **Day 21**
  - Azure ML Service
  - Pipeline
  - Split Data
  - Train Model
  - ML Algorithm
  - Score
  - Evaluate Model
