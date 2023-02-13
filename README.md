# Kubernetes-Dashboard
To Deploy the Kubernetes Dashboard in docker desktop for windows follw the below steps.
1. Download the recommended.yaml file from this repo and navigate the folder
2. Execute this command either in Bash/Powershell/CMD
kubectl apply -f recommended.yaml
3. If you want to bypass the login page add this command  - --enable-skip-login in the below

spec:
      containers:
        - name: kubernetes-dashboard
          image: kubernetesui/dashboard:v2.2.0
          imagePullPolicy: Always
          ports:
            - containerPort: 8443
              protocol: TCP
          args:
            - --auto-generate-certificates
            - --namespace=kubernetes-dashboard
             - --enable-skip-login              #add this command
            # Uncomment the following line to manually specify Kubernetes API server Host
