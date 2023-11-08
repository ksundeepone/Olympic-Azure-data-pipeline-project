# Olympic-Azure-data-pipeline-project



## To create connection from Azure Databricks to Azure Data Factory

```sh
configs = {"fs.azure.account.auth.type": "OAuth",
"fs.azure.account.oauth.provider.type": "org.apache.hadoop.fs.azurebfs.oauth2.ClientCredsTokenProvider",
"fs.azure.account.oauth2.client.id": "35ec14f4-8d57-4c00-9e9f-ab5cbbe8ffb4",
"fs.azure.account.oauth2.client.secret": 'hEo8Q~B2kkZOR4WIyDYVzQdHxu5f1LEChQ~81c11',
"fs.azure.account.oauth2.client.endpoint": "https://login.microsoftonline.com/873b06a8-4913-4d25-8fd6-905dfacbfecf/oauth2/token"}


dbutils.fs.mount(
source = "abfss://olympic-data@olympicdata97.dfs.core.windows.net", # contrainer@storageacc
mount_point = "/mnt/olympicmount",
extra_configs = configs)
```

## TO check if the connection is successful 

```sh
%fs
ls "/mnt/olympicmount"
```
