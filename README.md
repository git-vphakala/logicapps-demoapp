# logicapps-demoapp
Logic Apps demo app: POST HTTP Request {"name":"pekka"} - Response { "hello":"world" }

# Secrets in the repo
- AZURE_CREDENTIALS

## value
{
  "clientId": "azure spn id",
  "clientSecret": "passwd of the above",
  "subscriptionId": "subscription id",
  "tenantId": "tenant id",
  "activeDirectoryEndpointUrl": "https://login.microsoftonline.com",
  "resourceManagerEndpointUrl": "https://management.azure.com/",
  "activeDirectoryGraphResourceId": "https://graph.windows.net/",
  "sqlManagementEndpointUrl": "https://management.core.windows.net:8443/",
  "galleryEndpointUrl": "https://gallery.azure.com/",
  "managementEndpointUrl": "https://management.core.windows.net/"
}

Four first ones need correct values.

# Variables in the repo
- AZURE_LA_RG
- AZURE_LA_NAME
- AZURE_LA_APPFILES

# Required Azure resources
- Service principal
- [Logic Apps](https://github.com/git-vphakala/logicapps-iac)

# Local development
- local.settings.json is not in the repo. Add manually.
- add Stateles1/ host.json connections.json to the logicapp.zip (Right-click the selection → "Send to Compressed (zipped) folder")
- az functionapp deployment source config-zip --resource-group <rg-name> --name <logicapp-name> --src logicapp.zip
- 