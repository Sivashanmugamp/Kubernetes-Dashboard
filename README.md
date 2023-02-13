# Kubernetes-Dashboard
To Deploy the Kubernetes Dashboard in docker desktop for windows follw the below steps.
1. Download the recommended.yaml file from this repo and navigate the folder
2. Execute this command either in Bash/Powershell/CMD
kubectl apply -f recommended.yaml
3. If you want to bypass the login page add this command  - --enable-skip-login in the below

![image](https://user-images.githubusercontent.com/93910728/218376977-c5fca10e-1fe7-4302-b974-4fe772196170.png)


4. To Launch the dashboared use the below command
5. kubectl proxy
6. Then launch this URL http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/error?namespace=default

WITH SAMPLE USER
1. We need Service account and cluster role binding
2. Download the dashboard-adminuser.yaml file and execute using below command

##### kubectl apply -f dashboard-adminuser.yaml

And then execute the below command to get the token

##### kubectl -n kubernetes-dashboard create token admin-user

3. Use the generated token to access the dashboard
For more details refer the below url
https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/
