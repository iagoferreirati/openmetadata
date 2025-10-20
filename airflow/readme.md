 helm install my-airflow apache-airflow/airflow --version 1.18.0 -f values.yaml --create-namespace --namespace airflow


  helm upgrade my-airflow apache-airflow/airflow --version 1.18.0 -f values.yaml --namespace airflow