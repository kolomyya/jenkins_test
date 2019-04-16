# jenkins_test
# Deploy the Jenkins on  Kubernetes Cluster

This repo deploy a Jenkins on Kubernetes cluster. Jenkins is a distributed automation server, generally associated with Continuous Integration (CI) and Continuous Delivery (CD). A Jenkins cluster typically involves one or more master instance(s) coupled with one or more slave instance(s)

![](https://github.com/kolomyya/jenkins_test/blob/master/Picture/JenkinsK8sOpenEBS.jpg)
 

We have created files to deploy code:
```
jenkins-deployment.yaml
```
Run kubectl create -f jenkins-deployment.yaml

If a code looks good, it create you:
```
 - namespaces=tools
 ```
Under this namespase you will have:
```
 - persisten volume
 - persistem volume claim
 - servise(LoadBalancer)
 - deployment(replicas(jenkins))
```
When it created, it'll output the domain name of your server. Head over to that URL and you'll be prompted to login to Jenkins.

Login to Jenkins
When you first load Jenkins, it will ask you to enter the initial admin password to unlock it. This password is located on the Jenkins server itself and the initial login page will show you the path (typically,``` /jenkins/secrets/initialAdminPassword```). You'll need to SSH to the server to get the passwor
