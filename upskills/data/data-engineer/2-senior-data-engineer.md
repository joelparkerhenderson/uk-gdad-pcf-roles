# Senior data engineer - upskill resources

This page focuses on learning and growth resources for the work role of senior data engineer.

- The resources include links to online courses, blogs, research articles, videos, and books.

- These help with job upskilling, work training, professional development, and career advancement.

- These are intended to be good starting points, not a comprehensive catalogue.

At this role level you take responsibility for more complex data engineering work, design for reliability and observability, and guide less experienced engineers. The resources below emphasise pipeline reliability, data contracts and platform design.

We welcome constructive feedback to improve this page and these lists.

- GitHub issues and/or pull requests are welcome.

- The resources are found via AI searches then go through human-in-the-loop proofing.

- For more contact Joel Henderson <joel@joelparkerhenderson.com>

## Coursera courses

- [IBM Data Engineering Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-engineer): A multi-course programme covering relational databases, SQL, Python, ETL and data pipelines, big data with Hadoop and Spark, and data warehousing.

- [Open source Data Engineering with Spark, dbt and Airflow Professional Certificate](https://www.coursera.org/professional-certificates/open-source-data-engineering-with-spark-dbt-and-airflow): Covers building modular ETL pipelines into a cloud data warehouse, authoring Airflow DAGs with retry logic and SLA monitoring, and diagnosing Spark performance bottlenecks.

- [ETL and Data Pipelines with Shell, Airflow and Kafka](https://www.coursera.org/learn/etl-and-data-pipelines-shell-airflow-kafka): Teaches building batch pipelines with Airflow and streaming pipelines with Kafka, and when each approach is appropriate.

## Udemy courses

- [Data Engineering Bootcamp: SQL, ETL, PySpark and AWS](https://www.udemy.com/course/data-engineering-bootcamp-series-1/): Builds real pipelines with Airflow, AWS, Spark and Python, including an Airflow DAG that provisions a cluster, submits a PySpark job and tears the cluster down.

- [The Complete Data Engineering Bootcamp with PySpark](https://www.udemy.com/course/data-engineering-projects-with-pyspark-2025/): Sets up a full stack with Docker, Spark, Airflow and HDFS, writes production-ready PySpark ETL jobs, and schedules them with Airflow DAGs.

- [Data Engineering: Apache Airflow](https://www.udemy.com/course/data-engineering-apache-airflow/): Focuses on orchestrating ETL pipelines in Airflow DAGs, with worked examples using Spark, Elasticsearch and Snowflake.

## Skillsoft courses

- [Courses for Data Engineer](https://www.skillsoft.com/journey/data-engineer-73684d02-760d-4220-ab9a-52e417966178): A career path covering Python and SQL fundamentals for data engineers, an introduction to big data with PySpark, and a data pipeline portfolio project.

- [Data Engineering Getting Started](https://www.skillsoft.com/course/data-engineering-getting-started-df850c00-2f92-11e9-9f0a-4d6965a87299): A twelve-video course covering distributed systems, batch versus in-memory processing, NoSQL stores and their uses, and the ETL process and its tooling.

- [Data Engineering on Microsoft Azure: Data Lake Storage](https://www.skillsoft.com/course/data-engineering-on-microsoft-azure-data-lake-storage-68aff9a6-040c-463d-9b00-952474b210d0): Covers lake storage design on Azure, relevant where departments have standardised on the Microsoft stack.

## edX courses

- [Data Engineering Professional Certificate (IBM)](https://www.edx.org/professional-certificate/ibm-data-engineering): Covers big data practitioner knowledge with Hadoop and Spark alongside practical skills to build and manage pipelines and ETL processes with shell scripts, Airflow and Kafka.

- [Spark, Hadoop, and Snowflake for Data Engineering](https://www.edx.org/learn/computer-science/pragmatic-ai-labs-spark-hadoop-and-snowflake-for-data-engineering): Teaches building efficient and scalable pipelines across the three platforms and optimising them with Python, PySpark and MLflow.

- [Apache Spark for Data Engineering and Machine Learning (IBM)](https://www.edx.org/learn/apache-spark/ibm-apache-spark-for-data-engineering-and-machine-learning): Covers Spark Structured Streaming, ETL for machine learning pipelines and Spark ML.

## MIT OpenCourseWare courses

- [6.830 Database Systems](https://ocw.mit.edu/courses/6-830-database-systems-fall-2010/): Covers the relational model, schema normalisation, query optimisation and transactions. Understanding how a query planner works is what separates fast pipelines from slow ones.

- [1.264J Database, Internet, and Systems Integration Technologies](https://ocw.mit.edu/courses/1-264j-database-internet-and-systems-integration-technologies-fall-2013/): Covers data modelling, UML, relational databases and SQL alongside integration technologies including web services and service-oriented architectures.

- [6.005 Elements of Software Construction](https://ocw.mit.edu/courses/6-005-elements-of-software-construction-fall-2008/): Covers specification, abstraction and testing, which are exactly the disciplines that separate maintainable pipelines from fragile ones.

## Blog posts

- [Building reliable data pipelines: a foundational approach](https://www.getdbt.com/blog/building-reliable-data-pipelines): From dbt Labs, covering why transformation after loading suits modern warehouses and what reliability requires in practice.

- [Data Contracts for Data Engineers: Stop Breaking Downstream Pipelines](https://dataskew.io/blog/data-contracts-for-data-engineers/): Argues that a data contract is schema plus semantics, quality expectations, ownership, service levels and a change policy, and that engineering is about creating reliable interfaces between teams.

- [Data Contracts: The Backbone of Modern Data Architecture with dbt and BigQuery](https://medium.com/dbt-for-analytics/data-contracts-the-backbone-of-modern-data-architecture-with-dbt-and-bigquery-8a027fd924b4): Shows how contracts formalise the agreement between producers and consumers so that guarantees become enforceable, versioned and testable.

- [dbt Contracts: Enforcing Schema in Data Pipelines](https://blog.pmunhoz.com/blog/dbt/dbt-contracts-schema-enforcement-guide/): A practical guide to implementing executable specifications that verify data matches expected patterns at each pipeline stage.

- [Implementing Data Contracts in Modern Pipelines](https://www.cloudthat.com/resources/blog/implementing-data-contracts-in-modern-pipelines): Covers using schema tests, documentation and version-controlled models to enforce quality and consistency.

- [Understanding dbt: basics and best practices](https://www.datadoghq.com/blog/understanding-dbt/): An accessible introduction to dbt and where it fits in a modern pipeline, including its testing and documentation features.

- [What Data Engineers Really Do: Guarantees, Contracts, and Cost-Aware Systems](https://idatamax.com/blog/real-data-engineering): Notes that most practitioners spend more time fixing broken pipelines and chasing upstream issues than building new functionality, and what to do about it.

- [Data Engineering for Streaming Data: how to ensure data quality](https://crosser.io/blog/data-engineering-for-streaming-data-how-to-ensure-data-quality/): Covers quality assurance where there is no batch boundary to validate against.

- [Data governance on the Government Data Architecture blog](https://dataarchitecture.blog.gov.uk/category/data-architecture/data-governance/): Covers the governance environment UK government data engineering operates within.

- [Data Standards on the Data in Government blog](https://dataingovernment.blog.gov.uk/category/data-standards/): Posts on cross-government data standards, which shape what pipelines must produce and accept.

## Research articles

- [Data pipeline quality: Influencing factors, root causes of data-related issues, and processing problem areas for developers](https://www.sciencedirect.com/science/article/pii/S0164121223002509): An empirical study introducing a taxonomy of 41 factors influencing pipeline quality, validated through literature review and eight expert interviews, across data, infrastructure, life cycle management, development and deployment, and processing.

- [Data Pipeline Quality (preprint)](https://arxiv.org/abs/2309.07067): The open-access version of the above, including the full taxonomy and the finding that debugging and maintaining pipelines is the most pressing issue data engineers report.

- [An Overview and Critical Analysis of Recent Advances in Challenges Faced in Building Data Engineering Pipelines for Streaming Media](https://www.researchgate.net/publication/372338809_An_Overview_and_Critical_Analysis_of_Recent_Advances_in_Challenges_Faced_in_Building_Data_Engineering_Pipelines_for_Streaming_Media): Covers quality, consistency, completeness, format adherence, scalability, latency and security in streaming pipelines.

- [Designing a Data Pipeline Architecture for Intelligent Analysis of Streaming Data](https://link.springer.com/chapter/10.1007/978-3-031-72284-4_22): A worked architecture using Kafka for ingestion, a time-series store and real-time visualisation.

- [Architecting Data-Intensive Applications: From Data Architecture Design to Its Quality Assurance](https://arxiv.org/pdf/2401.12011): Examines how architecture practice determines data quality outcomes in data-intensive systems.

- [Evaluating Data Quality: Comparative Insights on Standards, Methodologies, and Modern Software Tools](https://www.mdpi.com/2079-9292/14/15/3038): Compares data quality standards, methodologies and the tools that implement them.

- [Exploration and Evaluation of Congestion Control Algorithms for Data Center Networks](https://link.springer.com/article/10.1007/s42979-023-02016-4): Relevant background for engineers whose pipelines are limited by network behaviour rather than compute.

- [Enterprise Data Modelling Methodologies: A Comparative Analysis of Inmon, Kimball, and Data Vault](https://arxiv.org/pdf/2606.29355): Compares the dominant warehouse modelling methodologies and the situations that favour each.

- [Improving Data Quality and Data Governance Using Master Data Management: A Review](https://www.researchgate.net/publication/354967542_Improving_Data_Quality_and_Data_Governance_Using_Master_Data_Management_A_Review): Reviews how master data management addresses quality problems by standardising and profiling data from diverse sources.

- [Data Mesh: A Systematic Gray Literature Review](https://dl.acm.org/doi/10.1145/3687301): An ACM Computing Surveys review of data mesh design principles, architectural components and organisational roles, separating substance from hype.

## Videos

- [Data Engineer Project: An end-to-end Airflow data pipeline with BigQuery, dbt and Soda](https://www.youtube.com/watch?v=DzxtCxi4YaA): A complete project build including orchestration, transformation and data quality checks.

- [dbt core and Airflow 101: Building data pipelines demystified](https://www.youtube.com/watch?v=d0wXnimEMUk): From Airflow Summit, covering how the two tools fit together without duplicating responsibilities.

- [Building robust data pipelines with dbt, Airflow, and Great Expectations](https://www.youtube.com/watch?v=yJFHgNWmoMg): Sam Bail on embedding data quality checks into a pipeline rather than bolting them on afterwards.

- [Code along: build an ELT Pipeline in 1 Hour with dbt, Snowflake and Airflow](https://www.youtube.com/watch?v=OLXkGB7krGo): A live build that shows the whole shape of a modern ELT pipeline quickly.

- [Data Engineer's Lunch: Airflow and Spark](https://www.youtube.com/watch?v=V-Ux18que6A): Covers using Airflow to manage Spark jobs, including the failure modes that combination introduces.

- [End-to-End Data Engineering Project with Airflow, dbt and Databricks](https://www.youtube.com/watch?v=ZEE-jNAthB0): A larger project build across an orchestration, transformation and compute stack.

- [Snowflake Data Engineering with dbt and Airflow](https://www.youtube.com/watch?v=vYthwG9PrLI): A guide to building scalable pipelines on a cloud warehouse.

- [Databricks tutorial: an intro to the medallion architecture](https://www.youtube.com/watch?v=u3MSka3WLpE): Explains organising lakehouse data through layered refinement stages.

- [The Medallion Data Architecture: Pros and Cons](https://www.youtube.com/watch?v=8p77fOWp5F4): A critical assessment of the pattern, including where it creates more work than it saves.

- [Demystifying the Medallion and Lakehouse Architectures](https://www.youtube.com/watch?v=iLgDKVlPN1w): Compares lakehouse and medallion approaches and the conditions favouring each.

## Books on Amazon

- [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable-ebook/dp/B0GNTX59CY): By Martin Kleppmann and Chris Riccomini. Examines the trade-offs between technologies for processing and storing data, and explains the fundamentals of distributed systems. The single most useful book for a data engineer.

- [The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling](https://www.amazon.com/Data-Warehouse-Toolkit-Definitive-Dimensional-ebook/dp/B00DRZX6XS): Kimball and Ross. The reference for dimensional modelling, conformed dimensions and the bus architecture that most analytical schemas still follow.

- [Building the Data Lakehouse](https://www.amazon.com/Building-Data-Lakehouse-Bill-Inmon-ebook/dp/B09GRZ9KP3): Inmon, Levins and Srivastava on the lakehouse pattern and its relationship to warehouse and lake architectures.

- [Building the Data Warehouse](https://www.amazon.com/Building-Data-Warehouse-W-Inmon/dp/0764599445): Inmon's foundational text on the Corporate Information Factory and relational warehousing.

- [Mastering Data Warehouse Design: Relational and Dimensional Techniques](https://www.amazon.com/Mastering-Data-Warehouse-Design-Dimensional/dp/0471324213): Imhoff, Galemmo and Geiger on combining relational and dimensional approaches into a sustainable design.

- [The DAMA Guide to the Data Management Body of Knowledge](https://www.skillsoft.com/book/the-dama-guide-to-the-data-management-body-of-knowledge-dama-dmbok-guide-first-edition-cc095fa0-f038-11e6-87f4-0242c0a80606): The reference across data management knowledge areas including integration, metadata and quality.

- [Python Data Science Handbook: Essential Tools for Working with Data](https://www.amazon.com/Python-Data-Science-Handbook-Essential/dp/1098121228): By Jake VanderPlas. Strong coverage of pandas and NumPy, which remain central to much pipeline work.

- [Fundamentals of Software Architecture: A Modern Engineering Approach](https://www.amazon.com/Fundamentals-Software-Architecture-Engineering-Approach-ebook/dp/B0F1BWQGYZ): Richards and Ford. Covers architecture characteristics and trade-offs that apply directly to pipeline design.

- [Threat Modeling: Designing for Security](https://www.amazon.com/Threat-Modeling-Designing-Adam-Shostack-ebook/dp/B00IG71FAS): Adam Shostack. Pipelines move sensitive data; this is the standard reference for reasoning about that risk during design.

- [The Chief Data Officer's Playbook](https://www.amazon.com/Chief-Data-Officers-Playbook/dp/1783302577): Carruthers and Jackson. Useful context on how data functions are organised, funded and held to account.

## Professional development tips

- Treat your outputs as interfaces with contracts, not as files that happen to appear
- Design for observability from the start, so that failures are detected before consumers notice
- Learn the cost profile of the platforms you use, since inefficient pipelines get expensive quickly
- Automate quality checks rather than relying on downstream users to spot problems
- Understand the security and privacy obligations attached to the data you move
- Document schemas and lineage where consumers can actually find them
- Review other engineers' pipelines, since design habits spread faster through review than through documents
