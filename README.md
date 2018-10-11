## Auto building the Jenkins jobs when the change is merged

Here we will trigger the jenkins job only when the changes are merged into TEST branch. So let's create one repository for the testing purpose. We will also add one branch TEST.

####Prerequisite:
Jenkins plugins:
    1. Not required

### Step-1 
-- setup webhook in github first
   URL: set the url of jenkins which will be something like given bellow:
      http://<jenkin-server-ip>:<port>/github-webhook/

