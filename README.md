# Kubernetes
Connect to a shared EKS cluster

Install Kubernetes:
Download the latest kubectl binary
`curl -LO "https://dl.k8s.io/release/$(curl -sL https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`


Make the binary executable
`chmod +x kubectl`

Move it to your PATH
`sudo mv kubectl /usr/local/bin/`

Verify installation
`kubectl version --client`

Install eksctl in WSL (Ubuntu)
`curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp`
`sudo mv /tmp/eksctl /usr/local/bin`

![alt text](image.png)


Cluster created in AWS console:
shared-eks-cluster

Region:
us-east-1

`aws eks update-kubeconfig --name shared-eks-cluster --region us-east-1`

`kubectl create namespace ws-eks-activity`

`kubectl get namespaces`

`kubectl apply -f nginx-deployment.yaml`

`kubectl get pods -n ws-eks-activity`

Check Pod running:
`kubectl get svc -n ws-eks-activity`

`kubectl get deployment -o yaml -n ws-eks-activity | grep serviceAccount`

`kubectl get svc -n ws-eks-activity`

![alt text](image-3.png)   
![alt text](image-4.png)   
![alt text](image-5.png)   
![S](image-2.png)   
![alt text](image-6.png)   
![alt text](image-1.png)   
![alt text](image-7.png)   
![alt text](image-8.png)     
![alt text](image-14.png)      
![alt text](image-13.png)   

Deployment:   
![alt text](image-9.png)   
![alt text](image-16.png)  
![alt text](image-17.png)   


Pod:   
![alt text](image-10.png)   
![alt text](image-15.png)   


Replica:   
![alt text](image-11.png)   

Node:   
![alt text](image-12.png)   

Services:
![alt text](image-18.png)   
![alt text](image-19.png)   
Load Balancer URL:   
![alt text](image-20.png)   



`kubectl get pods`
