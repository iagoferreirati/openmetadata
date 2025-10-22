helm repo add apache-airflow https://airflow.apache.org/


  helm upgrade my-airflow apache-airflow/airflow --version 1.18.0 -f values.yaml --namespace airflow
