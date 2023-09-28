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
