# Data Science in Production

__Applied Data Science__: Intersection of Data Science and Machine Learning Engineering. They are in charge of building a data product, a production system that provides predictive models.

## Cloud Environments

- __Databricks__ provide managed environments of Spark.
- __Dataflow__: GCP tool for building batch and streaming pipelines. Can connect __PubSub__ for messaging, __BigQuery__ for analytics, and __BigTable__ for application databases. It's __fully managed__. It's based on __Apache Beam Library__ which is portable.
- __BigQuery__ separate storage from compute and can scale to both __data lake__ and __data warehouse__ solutions.

## Coding Environments

- Google Colab and Databricks provide collaborative notebooks to work as a team.

## Automated Feature Engineering

- __Featuretools__
- __Framequery__: Allows to write SQL queries against a dataframe.

## General Notes

- One of the general strategies I take as a data scientist is to quickly deliver a proof of concept, and then iterate and improve a model once it is shown to provide value to an organization.

__To Study later:__

- Snowflake or Delta Lake
