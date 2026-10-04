# Databricks Bootcamp 2026

A comprehensive hands-on bootcamp for building modern data lakehouses using Databricks, Apache Spark, and the Medallion Architecture. Learn enterprise-grade data engineering patterns with real-world bike-sharing dataset.

## 🎯 Project Overview

This bootcamp provides a complete learning path for mastering Databricks and data lakehouse concepts through a practical bike-sharing analytics project. Using the Medallion Architecture (Bronze-Silver-Gold), you'll build a scalable data platform while learning Spark SQL, Delta Lake, and Databricks features.

**Learning Outcomes:**
- Master Databricks platform and features
- Implement Medallion Architecture patterns
- Develop production-grade data pipelines
- Apply PySpark and Spark SQL for transformations
- Build analytics-ready data models
- Work with Delta Lake and Unity Catalog

## 🏗️ Medallion Architecture

```
┌─────────────────────────────────────────────────────┐
│           MEDALLION ARCHITECTURE                    │
├─────────────────────────────────────────────────────┤
│                                                     │
│  GOLD LAYER (Analytics-Ready)                      │
│  ├─ dim_customers                                  │
│  ├─ dim_trips                                      │
│  ├─ fct_rentals                                    │
│  └─ agg_daily_metrics                              │
│           ↑                                         │
│  ┌────────┴────────┐                               │
│  │                 │                               │
│  SILVER LAYER (Cleaned & Transformed)              │
│  ├─ trips_cleaned                                  │
│  ├─ stations_validated                             │
│  ├─ users_enriched                                 │
│  └─ weather_normalized                             │
│           ↑                                         │
│  ┌────────┴────────┐                               │
│  │                 │                               │
│  BRONZE LAYER (Raw Data)                           │
│  ├─ trips_raw                                      │
│  ├─ stations_raw                                   │
│  ├─ users_raw                                      │
│  └─ weather_raw                                    │
│           ↑                                         │
│  ┌────────┴────────┐                               │
│  │   Data Sources  │                               │
│  ├─ CSV files      │                               │
│  ├─ APIs           │                               │
│  └─ Databases      │                               │
│                                                     │
└─────────────────────────────────────────────────────┘
```

## 🛠️ Tech Stack

- **Primary Platform:** Databricks
- **Compute Engine:** Apache Spark 3.x
- **Languages:** PySpark, Spark SQL
- **Storage:** Delta Lake (ACID transactions)
- **Governance:** Unity Catalog
- **Notebooks:** Databricks Notebooks
- **Languages Supported:** Python, Scala, SQL

## 📚 Curriculum

### Module 1: Foundations (Days 1-3)
- **Topics:**
  - Databricks workspace overview
  - Notebook basics and shortcuts
  - Cluster management
  - Introduction to Spark
- **Skills:** Navigate Databricks, create notebooks, manage clusters
- **Hands-on:** Create first notebook, explore sample data

### Module 2: Delta Lake & Data Ingestion (Days 4-6)
- **Topics:**
  - Delta Lake fundamentals
  - ACID properties
  - Data ingestion patterns
  - Handling schema evolution
- **Skills:** Create Delta tables, handle updates, manage data quality
- **Hands-on:** Build Bronze layer, ingest bike trip data

### Module 3: Data Transformation (Days 7-10)
- **Topics:**
  - PySpark fundamentals
  - DataFrame operations
  - Window functions
  - Performance optimization
- **Skills:** Write efficient Spark code, handle big data transformations
- **Hands-on:** Build Silver layer, implement data cleaning

### Module 4: Analytics & Aggregations (Days 11-14)
- **Topics:**
  - Dimensional modeling
  - Fact and dimension tables
  - Star schema design
  - Complex aggregations
- **Skills:** Design analytics schemas, build reporting layers
- **Hands-on:** Build Gold layer, create analytics tables

### Module 5: Unity Catalog & Governance (Days 15-16)
- **Topics:**
  - Unity Catalog overview
  - Metadata management
  - Access control
  - Data lineage
- **Skills:** Implement governance, secure data, track lineage
- **Hands-on:** Set up UC, implement access policies

### Module 6: Advanced Topics (Days 17-20)
- **Topics:**
  - Incremental processing
  - Real-time streaming
  - Performance tuning
  - Production deployment
- **Skills:** Build production pipelines, handle streaming data
- **Hands-on:** Implement incremental loads, set up jobs

## 📁 Project Structure

```
Databricks_bootcamp_2026/
├── 01_foundations/
│   ├── 01_notebook_basics.py
│   ├── 02_cluster_setup.py
│   └── 03_spark_intro.py
├── 02_delta_lake/
│   ├── 01_create_bronze_layer.py
│   ├── 02_data_ingestion.py
│   └── 03_schema_evolution.py
├── 03_transformations/
│   ├── 01_dataframe_operations.py
│   ├── 02_pyspark_sql.py
│   ├── 03_window_functions.py
│   └── 04_performance_tuning.py
├── 04_analytics/
│   ├── 01_create_silver_layer.py
│   ├── 02_dimensional_modeling.py
│   ├── 03_create_gold_layer.py
│   └── 04_business_metrics.py
├── 05_governance/
│   ├── 01_unity_catalog_setup.py
│   ├── 02_access_control.py
│   └── 03_data_lineage.py
├── 06_advanced/
│   ├── 01_incremental_processing.py
│   ├── 02_streaming_processing.py
│   ├── 03_optimization_techniques.py
│   └── 04_production_pipelines.py
├── data/
│   ├── trips.csv
│   ├── stations.csv
│   ├── users.csv
│   └── weather.csv
├── solutions/
│   └── [Complete solutions for all exercises]
├── docs/
│   ├── architecture.md
│   ├── data_dictionary.md
│   └── best_practices.md
└── README.md
```

## 🎯 Learning Path

### Prerequisites
- Basic SQL knowledge
- Python familiarity (preferred but not required)
- No prior Databricks experience required
- Access to Databricks workspace

### Recommended Learning Approach

```
Week 1: Learn Concepts + Theory
Week 2: Build Bronze Layer (Data Ingestion)
Week 3: Build Silver Layer (Data Transformation)
Week 4: Build Gold Layer (Analytics)
Final: Deploy Production Pipeline
```

## 🚀 Getting Started

### Prerequisites Setup

1. **Create Databricks Workspace:**
   - Free tier available at databricks.com
   - Or use existing workspace

2. **Create Cluster:**
   ```
   - Cluster Mode: All-purpose
   - Databricks Runtime: 14.0+
   - Python: 3.11
   - Spark: 3.5.0+
   ```

3. **Import Datasets:**
   - Download bike-sharing data from `data/` folder
   - Upload to Databricks File System (DBFS)

### Quick Start

1. **Access Workspace:**
   - Navigate to your Databricks workspace
   - Create new folder: `bootcamp_2026`

2. **Create First Notebook:**
   ```python
   # Notebook: 01_foundations/01_notebook_basics.py
   
   # Test Spark
   print("Spark version:", spark.version)
   
   # Create simple DataFrame
   df = spark.createDataFrame(
       [(1, "Alice"), (2, "Bob")],
       ["id", "name"]
   )
   df.display()
   ```

3. **Run Your First Cell:**
   - Shift + Enter to execute
   - Should display a table

## 📊 Bike-Sharing Dataset

### Dataset Overview

**Data Scale:**
- Records: 500K+ trip records
- Time Period: 2023-2024
- Stations: 100+ bike stations
- Users: 50K+ unique riders

### Tables

**trips_raw** (Bronze Layer)
- trip_id, start_time, end_time
- start_station_id, end_station_id
- user_id, bike_id
- trip_duration, distance

**stations_raw** (Bronze Layer)
- station_id, station_name
- latitude, longitude
- capacity, available_bikes

**users_raw** (Bronze Layer)
- user_id, age, membership_type
- registration_date, location

### Transformations in Bootcamp

```
Raw Data (Bronze)
    ↓
[Cleaning & Validation]
    ↓
Processed Data (Silver)
    ↓
[Aggregations & Modeling]
    ↓
Analytics Data (Gold)
    ├─ Daily trip summaries
    ├─ Station performance metrics
    ├─ User behavior analysis
    └─ Revenue insights
```

## 💻 Example: Building Silver Layer

```python
# Notebook: 03_transformations/01_dataframe_operations.py

from pyspark.sql.functions import col, when, round, datediff

# Read Bronze Data
trips_bronze = spark.table("bronze.trips_raw")
stations_bronze = spark.table("bronze.stations_raw")

# Clean and transform
trips_silver = trips_bronze \
    .filter(col("trip_duration") > 0) \
    .filter(col("start_station_id").isNotNull()) \
    .withColumn(
        "trip_duration_minutes",
        round(col("trip_duration") / 60, 2)
    ) \
    .withColumn(
        "user_type",
        when(col("membership_type") == "annual", "member")
        .when(col("membership_type") == "daily", "casual")
        .otherwise("unknown")
    ) \
    .select(
        "trip_id",
        "start_time",
        "end_time",
        "trip_duration_minutes",
        "start_station_id",
        "end_station_id",
        "user_id",
        "user_type"
    )

# Write to Silver
trips_silver.write \
    .mode("overwrite") \
    .option("mergeSchema", "true") \
    .saveAsTable("silver.trips_cleaned")
```

## 📈 Example: Building Gold Layer

```python
# Notebook: 04_analytics/04_business_metrics.py

from pyspark.sql.functions import col, count, avg, max, min, date_format

# Aggregate by day
daily_metrics = spark.table("silver.trips_cleaned") \
    .withColumn("trip_date", date_format(col("start_time"), "yyyy-MM-dd")) \
    .groupBy("trip_date", "start_station_id") \
    .agg(
        count("trip_id").alias("total_trips"),
        avg("trip_duration_minutes").alias("avg_duration_minutes"),
        count(when(col("user_type") == "member", 1)).alias("member_trips"),
        count(when(col("user_type") == "casual", 1)).alias("casual_trips")
    ) \
    .orderBy("trip_date", "start_station_id")

# Write to Gold
daily_metrics.write \
    .mode("overwrite") \
    .saveAsTable("gold.daily_station_metrics")

# Show results
daily_metrics.display()
```

## 🧪 Exercises

Each module includes hands-on exercises:

1. **Exercise: Ingest Data**
   - Load CSV data into Bronze table
   - Handle schema errors
   - Validate data

2. **Exercise: Clean Data**
   - Remove duplicates
   - Handle nulls
   - Validate data types

3. **Exercise: Aggregate Metrics**
   - Calculate daily summaries
   - Compute user statistics
   - Create performance metrics

4. **Exercise: Build Dashboard**
   - Create SQL queries for insights
   - Design visualizations
   - Build executive dashboard

## 📚 Resources

### Databricks Documentation
- [Official Databricks Docs](https://docs.databricks.com/)
- [Spark SQL Reference](https://spark.apache.org/docs/latest/sql-ref.html)
- [Delta Lake Guide](https://docs.delta.io/)
- [Unity Catalog Docs](https://docs.databricks.com/data-governance/unity-catalog/)

### Video Series
- Check Notion roadmap for YouTube links
- Live coding sessions available
- Q&A recordings

### Additional Learning
- Databricks Academy (free courses)
- Apache Spark documentation
- Delta Lake tutorials

## 🤝 Self-Study Tips

✅ **Recommended Approach:**
1. Read module overview
2. Watch video tutorials (if available)
3. Code along with examples
4. Complete exercises independently
5. Compare with provided solutions
6. Experiment and extend

❌ **Don't:**
- Just read without coding
- Copy-paste solutions without understanding
- Skip exercises
- Rush through concepts

## 🐛 Common Issues

### Issue: "Table Not Found"
**Solution:** Ensure data is loaded in correct catalog/schema:
```python
# Use full path
spark.table("catalog.schema.table_name")
```

### Issue: "Memory Issues"
**Solution:** 
- Partition large datasets
- Use `coalesce()` or `repartition()`
- Filter early in pipeline

### Issue: "Slow Queries"
**Solution:**
- Check query plan with `explain()`
- Add appropriate indexes
- Optimize join order

## 📊 Bootcamp Projects

**Final Project:** Build Complete Lakehouse
- Ingest bike-sharing data
- Transform through Bronze → Silver → Gold
- Create analytics models
- Build reporting layer
- Implement governance

**Extensions:**
- Real-time streaming pipeline
- ML predictions
- Cost optimization
- Performance tuning

## 🎓 Certification

Upon completion:
- Certificate of completion
- Portfolio project
- Reference materials
- Community access

## 🤝 Support

- Peer discussion forums
- Instructor Q&A sessions
- Office hours
- Slack community channel

## 📄 License

This bootcamp material is provided for educational purposes.

## 🔗 Related Projects

- [AI_Data_Agent](https://github.com/vinayshetty777/AI_Data_Agent)
- [SQL-DataWareHouse-Project](https://github.com/vinayshetty777/SQL-DataWareHouse-Project)
- [customer_service_app](https://github.com/vinayshetty777/customer_service_app)

---

**Bootcamp Status:** Active  
**Last Updated:** 2026-03-02  
**Duration:** 20 Days (Full-time) / 10 Weeks (Part-time)  
**Difficulty:** Beginner to Intermediate
