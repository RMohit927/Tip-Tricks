## How to deploy Docker Image into Azure Container Registry:

Steps:
1. Prerequisites ready runnable docker container image
2. create Azure Container Registry from Azure
3. goto Access Key > Enabled the Admin Toggle
4. goto VS Code/Terminal
5. type this command and change approprietly "docker login Login_Server_Name"
6. Enter Username/Password
7. after successfully login
8. docker tag image_name:latest Server_Name/image_name
9. docker push  Server_Name/image_name
10. verify by checking on ACR > Repositories
11. Hurray! Done.
