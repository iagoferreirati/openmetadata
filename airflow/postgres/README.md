
helm repo add postgres https://raw.githubusercontent.com/hansehe/postgres-helm/master/helm/charts/postgres

helm install my-postgres postgres/postgres --version 0.1.0 -f values.yml --create-namespace --namespace postgres
