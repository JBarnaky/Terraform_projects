HelloWorld.zip - passwd:123456

ASP.NET Application ready for publishing in Docker Hub or Azure Container Registry (!!! Switch Solution Configuration to: Release !!!)
Dockerfile
docker-compose.yml
.dockerignore

Program.cs - sections of the code under the comments "// Forwarded Headers Middleware order" responsible for work with proxy servers and load balancers

TF.zip - Terraform Infrastructure files

First terraform apply will generate a kubeconfig file which after moving in C:\Users\*User*\.kube or ~/.kube/config can be used to access the kubernetes nodes and deploy app using .yaml files

To achive HA i used multiple availability_zones | enable_auto_scaling = true | load balancing | create_before_destroy = true

Login to registry
az login
az acr login --name myregistry

https://docs.microsoft.com/en-us/azure/container-registry/container-registry-get-started-docker-cli?tabs=azure-cli

To attach acr to aks use the following command
az aks update -n HelloWorld2022 -g aks_tf_rg --attach-acr "acr name"



what i used 
https://docs.microsoft.com/en-us/azure/aks/
