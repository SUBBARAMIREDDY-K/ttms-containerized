CI/CD for the timetable management System using Jenkins


prerequisites

TTMS Repository view

Jenkins master - Agent setup

Open the AWS management console, search for the ec2 and click on it. Click on the Launch instance Launch the instance with the name Jenkins-master. ...

devops-voyager.hashnode.dev

Open Jenkins using the Jenkins master IP with port 8080.Login with Admin credentials.



After logging into Jenkins, we can see the dashboard.



Enter the item name as ttms-pipeline. select the Pipeline option and click on OK.



In the configure page select the required things as follows. Jenkinsfile



ttms-pipeline has been created click on the Build Now option for Continuous Integration and Continuous Delivery.



we can view the List of Stages in the CI/CD.



Open the ttms application using the public IP of the Jenkins-agent address with port 80.



To set up the Continuous Deployment open the GitHub repository of ttms and click on settings.



In the Code and automation select the Webhooks.



In the Webhooks click on the Add webhook.



Copy the public IP address of the Jenkins-master node and append the URL with the /github-webhook/. select the Content type as application/json and select just the push event. Enable the Active and click on Add webhook.



In the webhooks, we can view the added webhook status.



Modify the code in the ttms repo and push it. Automatically the GitHub hook will trigger the changes to the Jenkins-agent.



we can view the pipeline process status. Which is automatically triggered by the GitHub webhook.



Open the ttms application with Jenkins-agent IP. we can see the changes in the application.




