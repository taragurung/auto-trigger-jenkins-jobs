## Auto building the Jenkins jobs when the change is merged

Here we will trigger the jenkins job only when the changes are merged into TEST branch. So let's create one repository for the testing purpose. We will also add one branch TEST

#### Prerequisite:
Jenkins plugins:
    1. Not required
    
### setting up to be done in git 
You have to create a token on github and then use "Secret Text" and not "Username with password" when creating your login in Jenkins. There is a section called github in >>setting>global settings in jenkins. 

This is the url to create the secret key: 
create your own personal API tokens 

### Step-1 
-- setup webhook in github first, which is available in settings
   URL: set the url of jenkins which will be something like given bellow:
      http://jenkin-server-ip:<port>/github-webhook/

