# Create a alpine docker image  and pushing it to the Docker Hub

Add the Docker Hub Credentials to Jenkins
You could use your password for your Docker Hub credentials, but it’s better to create an access token to login into Docker Hub. The Jenkins pipeline will use your Docker Hub username and access token when pushing the Docker image to the Docker Hub repository. To create the Docker Hub access token, follow the steps below:

First Step: Log into your Docker Hub account
Second Step: Click `Account Settings`

Third Step: Click `Security`

Fourth Step: Click `New Access Token`

Fifth Step: Add Access Token Description  ex: jenkins

After adding the access token description, click `Generate`. Copy and save the generated access token. You will go back to the Jenkins `Manage Credentials` and add the new credentials 

Our two credentials are now ready to use. The next step is to create the Project files.

Creating Project Files
In your PC, create a new folder named `jenkins-docker`. In the folder, create a file named `Dockerfile` without any extension and add the following Docker command:

FROM alpine:3.13.5

This command will instruct Docker to build an Alpine-based Docker image. We have a very simple Dockerfile with only a single instruction/command. Next, create a file named `Jenkinsfile`. Please find the Jenkinsfile in the repository.

Then call this as jenkins pipeline.

After succesful run you can then login into your Docker Hub account to see the pushed Docker image:





