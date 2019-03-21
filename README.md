STEPS:
git clone https://github.com/kanojia26/rubyrail-postgress.git

helm install --name postgres-ha stable/postgresql

Note:
export POSTGRES_PASSWORD=$(kubectl get secret postgres-ha-postgresql -o jsonpath="{.data.postgresql-password}" | base64 --decode)

Update in config/database.yaml

###
Deploy App

helm install --name rubyapp myrubyapp/

helm ls



