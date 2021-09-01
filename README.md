# GitHub Advanced Security Webinar
This repo demonstrates how to combine multiple code scanning tools using Github Actions and Github Advanced Security.

# Steps to test
1. Fork this repository into your account
2. You will need to enable Actions in this repository. Go to `Actions` tab and click on `I understand my workflows, go ahead and enabled them` button.
3. Even though each workflow exists, you will need to approve it for your repo. On the next screen, select each workflow.
4. You should see `This scheduled workflow is disabled because scheduled workflows are disabled by default in forks.` warning. Click on `Enable workflow` button next to it.
5. Configure the following secrets for your environment
    - AZURE_LOGIN_SECRET -> output from `az ad sp create-for-rbac --sdk-auth`
    - AZURE_SERVICE_PRINCIPAL_CLIENT_ID -> Client ID from above
    - AZURE_SERVICE_PRINCIPAL_CLIENT_SECRET -> Client Secret from above
    - AZ_APPINSIGHTS_CONNECTION_STRING -> As per setup instructions from [Microsoft](https://docs.microsoft.com/en-gb/azure/security-center/defender-for-container-registries-cicd).
    - AZ_SUBSCRIPTION_TOKEN -> As per setup instructions from [Microsoft](https://docs.microsoft.com/en-gb/azure/security-center/defender-for-container-registries-cicd).
6. Configure an environment titled `production_environment` 
7. Each of the workflows have been configured for manual dispatch, select these as you require and execute.

# Credits
The following repos are leveraged for examples:
- [terragoat](https://github.com/bridgecrewio/terragoat)
- [dvna](https://github.com/appsecco/dvna)
- [h3kz-security](https://github.com/h3kz-security)# Github-Advanced-Security-Demo
