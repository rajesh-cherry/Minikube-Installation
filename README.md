# Minikube-Installation

# How to install Minikube in Ubuntu 18.04 LTS in AWS EC2 Machine 

##  Pre-Requesties

1. Ubuntu 18.04 LTS with 2CPU and 8Gb RAM (t2.Medium)
2. Allow All Traffic in security Group


lets see 

1. Install Ubuntu 18.04 Lts 

2. Install Kubectl: and use the below command 
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod 700 kubectl
sudo mv kubectl /usr/local/bin

3. Install Docker: Minikube Required Docker use the below command
sudo apt-get update && \
sudo apt-get install docker.io -y

4. Install Minikube: 
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin
 
5. check Minikube version
minikube version

6. Kubernetes 1.20.7 requires conntrack to be installed in root's path
sudo apt-get install -y conntrack

7. start Minikube 
minikube start --vm-driver=none

* check the status of minikube
minikube status
 
8. Excute the kubectl commands
kubectl get pods 
kubectl get all          

