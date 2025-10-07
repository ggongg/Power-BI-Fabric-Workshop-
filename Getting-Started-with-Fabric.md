# Getting Started with Microsoft Fabric

## Introduction

Microsoft Fabric is an all-in-one analytics solution for enterprises that covers everything from data movement to data science, real-time analytics, and business intelligence. It brings together new and existing components from Power BI, Azure Synapse, and Azure Data Factory into a single integrated environment.

## Table of Contents

1. [What is Microsoft Fabric?](#what-is-microsoft-fabric)
2. [Core Concepts](#core-concepts)
3. [Fabric Experiences](#fabric-experiences)
4. [Getting Started](#getting-started)
5. [Working with Fabric](#working-with-fabric)
6. [Integration with Power BI](#integration-with-power-bi)
7. [Best Practices](#best-practices)
8. [Resources](#resources)

## What is Microsoft Fabric?

Microsoft Fabric is a unified analytics platform that provides a comprehensive suite of services including:

- Data engineering
- Data integration
- Data warehousing
- Data science
- Real-time analytics
- Business intelligence

### Key Benefits

- **Unified Platform**: One platform for all analytics workloads
- **Integrated Experience**: Seamless movement between different analytics tasks
- **OneLake**: A single, unified data lake for all data
- **AI-Powered**: Built-in AI capabilities throughout
- **SaaS Foundation**: Fully managed Software-as-a-Service
- **Open and Governed**: Open data formats with built-in governance

## Core Concepts

### OneLake

OneLake is Microsoft Fabric's unified data lake that provides a single, unified storage system for all data in your organization. Think of it as "OneDrive for data."

**Key Features:**
- Automatically provisioned with every Fabric tenant
- Single copy of data for all analytics experiences
- Built on Azure Data Lake Storage (ADLS) Gen2
- Supports open data formats (Delta, Parquet)

### Workspaces

Workspaces are collaborative environments where teams can work together on projects. Each workspace contains items like notebooks, data pipelines, warehouses, and reports.

### Capacity

Fabric uses a capacity-based licensing model. Capacity represents the compute and storage resources available to your organization.

## Fabric Experiences

Microsoft Fabric provides several specialized experiences:

### 1. Data Factory

For data integration and orchestration:
- Data pipelines for ETL/ELT
- Dataflows for data transformation
- Over 150 connectors to various data sources

### 2. Synapse Data Engineering

For large-scale data processing:
- Lakehouses for storing and analyzing data
- Spark notebooks for data processing
- Spark job definitions for running Spark applications

### 3. Synapse Data Warehouse

For SQL-based analytics:
- Fully managed data warehouse
- T-SQL support
- Automatic indexing and optimization

### 4. Synapse Data Science

For machine learning and AI:
- Notebooks for data exploration
- Experiments for ML model training
- Models for deploying ML solutions

### 5. Synapse Real-Time Analytics

For streaming and time-series data:
- KQL databases for fast analytics
- Eventstreams for ingesting streaming data
- Real-time dashboards

### 6. Power BI

For business intelligence:
- Interactive reports and dashboards
- Natural language queries (Q&A)
- Integration with all Fabric data sources

## Getting Started

### Prerequisites

- A Microsoft account (work, school, or personal)
- Access to Microsoft Fabric (trial or paid capacity)

### Step 1: Enable Microsoft Fabric

1. Sign in to [Power BI Service](https://app.powerbi.com)
2. If you're an admin, go to Admin portal > Tenant settings
3. Enable Microsoft Fabric features for your organization
4. If you're not an admin, ask your administrator to enable it

### Step 2: Start a Fabric Trial (Optional)

1. Go to [Microsoft Fabric website](https://fabric.microsoft.com)
2. Click "Start free trial"
3. Follow the prompts to activate your 60-day trial
4. The trial includes Fabric capacity for testing

### Step 3: Create a Workspace

1. In Power BI Service, click "Workspaces" in the left navigation
2. Click "New workspace"
3. Give your workspace a name and description
4. Assign it to a Fabric capacity
5. Click "Apply"

### Step 4: Choose Your Experience

1. In your workspace, click the experience switcher in the bottom-left corner
2. Select the experience you want to start with:
   - Data Factory for data integration
   - Data Engineering for building lakehouses
   - Data Warehouse for SQL analytics
   - Data Science for ML workflows
   - Real-Time Analytics for streaming data
   - Power BI for business intelligence

## Working with Fabric

### Creating a Lakehouse

1. Switch to the Data Engineering experience
2. Click "New" > "Lakehouse"
3. Give your lakehouse a name
4. Start loading data using:
   - Upload files
   - Data pipelines
   - Notebooks
   - Dataflows

### Building a Data Pipeline

1. Switch to the Data Factory experience
2. Click "New" > "Data pipeline"
3. Use the visual designer to:
   - Add data sources
   - Configure transformations
   - Set destination
   - Schedule execution

### Creating a Data Warehouse

1. Switch to the Data Warehouse experience
2. Click "New" > "Warehouse"
3. Give your warehouse a name
4. Load data using:
   - COPY INTO statements
   - Data pipelines
   - SQL INSERT statements

### Running ML Experiments

1. Switch to the Data Science experience
2. Click "New" > "Notebook"
3. Write Python/R code for:
   - Data exploration
   - Feature engineering
   - Model training
   - Model evaluation

## Integration with Power BI

Microsoft Fabric and Power BI are deeply integrated:

### Direct Lake Mode

- Power BI can directly read from OneLake without data duplication
- Near real-time data refresh
- Better performance than Import or DirectQuery

### Unified Semantic Models

- Create semantic models from Fabric data sources
- Share models across the organization
- Single source of truth for business metrics

### Seamless Navigation

- Move between Power BI and other Fabric experiences
- Create reports from any Fabric data source
- Embedded analytics in Fabric notebooks

## Best Practices

### Data Organization

- Use lakehouses for raw and processed data
- Organize data in medallion architecture (Bronze, Silver, Gold)
- Use shortcuts to reference data without duplication
- Apply consistent naming conventions

### Performance Optimization

- Use Delta format for better performance
- Partition large tables appropriately
- Implement incremental data refresh
- Optimize Spark configurations for workloads

### Security and Governance

- Use workspace roles to control access
- Implement row-level security (RLS) where needed
- Tag and classify sensitive data
- Enable auditing and monitoring
- Use service principals for automation

### Development Workflow

- Use separate workspaces for dev, test, and production
- Implement CI/CD using deployment pipelines
- Version control notebooks and code using Git integration
- Document your data models and pipelines

### Cost Management

- Monitor capacity usage regularly
- Pause unused capacities
- Optimize queries and transformations
- Use appropriate file formats and compression

## Resources

### Official Documentation

- [Microsoft Fabric Documentation](https://docs.microsoft.com/fabric/)
- [Fabric Community](https://community.fabric.microsoft.com/)
- [Fabric Blog](https://blog.fabric.microsoft.com/)

### Learning Resources

- [Microsoft Learn - Fabric](https://learn.microsoft.com/training/browse/?products=fabric)
- [Fabric Adoption Roadmap](https://adoption.microsoft.com/fabric/)
- [Fabric YouTube Channel](https://www.youtube.com/@MicrosoftFabric)

### Sample Datasets

Check the `datasets/` folder in this repository for sample data you can use with Fabric.

## Common Use Cases

### End-to-End Analytics Pipeline

1. **Ingest**: Use Data Factory to bring in data from various sources
2. **Store**: Load raw data into a lakehouse (Bronze layer)
3. **Transform**: Use notebooks or dataflows to clean data (Silver layer)
4. **Model**: Create analytics-ready data (Gold layer)
5. **Analyze**: Build data warehouse or semantic models
6. **Visualize**: Create Power BI reports and dashboards
7. **Share**: Distribute insights to stakeholders

### Real-Time Analytics

1. **Stream**: Ingest streaming data with Eventstreams
2. **Process**: Transform data in real-time
3. **Store**: Load into KQL database
4. **Analyze**: Query with KQL (Kusto Query Language)
5. **Visualize**: Create real-time Power BI dashboards

### Machine Learning Workflow

1. **Prepare**: Load data into lakehouse
2. **Explore**: Use notebooks for data exploration
3. **Train**: Build ML models with MLflow integration
4. **Deploy**: Register and deploy models
5. **Score**: Apply models to new data
6. **Monitor**: Track model performance

## Next Steps

1. Enable Microsoft Fabric in your organization
2. Start a Fabric trial if you don't have a license
3. Create your first workspace
4. Explore the sample datasets in this repository
5. Build your first lakehouse or data pipeline
6. Create Power BI reports connected to Fabric data sources

---

**Want to learn more about Power BI?** Check out [Getting Started with Power BI](./Getting-Started-with-Power-BI.md) for detailed guidance on creating reports and dashboards.
