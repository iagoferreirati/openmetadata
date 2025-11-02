 helm install my-airflow apache-airflow/airflow --version 1.18.0 -f values.yaml --create-namespace --namespace airflow


  helm upgrade my-airflow apache-airflow/airflow --version 1.18.0 -f values.yaml --namespace airflow


---------------


## add this helm repository
helm repo add airflow-stable https://airflow-helm.github.io/charts

## update your helm repo cache
helm repo update
helm upgrade -i my-airflow airflow-stable/airflow --create-namespace  --namespace airflow --values values-new.yaml

https://pypi.org/project/openmetadata-ingestion/
