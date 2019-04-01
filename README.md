## Auto building the Jenkins jobs when the change is merged.
.
Here we will trigger the jenkins job only when the changes are merged into TEST branch. So let's create one repository for the testing purpose. We will also add one branch TEST

#### Prerequisite:
Jenkins plugins:
    1. Not required
    
### setting up to be done in git to get the credentials
You have to create a token on github and then use "Secret Text" and not "Username with password" when creating your login in Jenkins. There is a section called github in >>setting>global settings in jenkins. 

This is the url to create the secret key: 
create your own personal API tokens 

### Step-1 
-- setup webhook in github first, which is available in settings
   URL: set the url of jenkins which will be something like given bellow:
      http://jenkin-server-ip:<port>/github-webhook/

## Step-2
Let's do the necessary setup required in the Jenkins

First setup the git credentials as mentioned above. To be done in >> settings > global. We can also test if the connection is ok or now prior to heading to jenkins job setup.

Check the image for the normal setup done.
1. Added the giturl 
2. Checked the option *GitHub hook trigger for GITScm polling*

## Some important variables to access from jenkins
Once the hook start working than we can start accessing so many cool variables directly from the jenkins environment. Few of my favorites being.

**GIT_COMMITTER_NAME:** To know who made the commit but this doesnot work in jenkins

**GIT_COMMIT:** To know what was the exact commit being made

## Getting some more details from the github Payload


## To get who made the commiter details in bash

` git show -s --format='%ce','%cn','%H' `

This will privide us commiter email, name and the commit-id

