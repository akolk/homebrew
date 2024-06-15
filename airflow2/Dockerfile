FROM apache/airflow:2.9.2
USER root
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
         libgdal-dev \
  && apt-get autoremove -yqq --purge \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
USER airflow

#RUN pip install GeoAlchemy2 tuspy lxml retry geopandas oracledb apache-airflow-providers-oracle[common.sql]  apache-airflow-providers-databricks[common.sql]
RUN pip install  tuspy lxml retry oracledb apache-airflow-providers-oracle[common.sql]  apache-airflow-providers-databricks[common.sql]
