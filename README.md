# ingress-azure
App Gateway Ingress Helm Chart


helm install ingress-azure \
     ingress-azure \
     --namespace default \
     --debug \
     --set appgw.resourceGroup=<resource group name> \
     --set appgw.environment=AZUREPUBLICCLOUD \
     --set appgw.subscriptionId=<WXYZ-9876> \
     --set appgw.tenantId=<WXYZ-9876> \
     --set appgw.shared=false \
     --set appgw.name=myApplicationGateway \
     --set appgw.usePrivateIP=true \
     --set armAuth.type=aadPodIdentity \
     --set armAuth.identityClientID=<User Managed Identity Client ID> \
     --set rbac.enabled=true \
     --set verbosityLevel=3 \
     --set aksClusterConfiguration.apiServerAddress=<guid>.hcp.<location>.azmk8s.io