Install OpenMetadata
Assuming kubectl context points to the correct kubernetes cluster, first create kubernetes secrets that contain MySQL and Airflow passwords as secrets.

kubectl create secret generic mysql-secrets --from-literal=openmetadata-mysql-password=openmetadata_password
kubectl create secret generic airflow-secrets --from-literal=openmetadata-airflow-password=admin
The above commands sets the passwords as an example. Change to any password of choice.

Run the following command to install openmetadata with default configuration.

helm repo add open-metadata https://helm.open-metadata.org
helm install openmetadata open-metadata/openmetadata
If the default configuration is not applicable, you can update the values listed below in a values.yaml file and run

helm upgrade -i openmetadata open-metadata/openmetadata --values values.yaml --namespace openmetadata --create-namespace


Username - admin@open-metadata.org
Password - admin



https://docs.open-metadata.org/latest/connectors/search/elasticsearch/yaml



https://github.com/open-metadata/openmetadata-helm-charts/blob/main/charts/openmetadata/values.yaml