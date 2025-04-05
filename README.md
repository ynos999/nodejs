## --- Nodejs app show Your IP ---
###
## --- Local Test ---
###
### npm install
### npm start app.js
### http://0.0.0.0:3000
###
## --- Docker Build ---
###
### docker build -t show-ip-node:0.2 .
### docker run -p 3000:3000 show-ip-node:0.2
### curl http://localhost:3000
### docker ps -a
### docker exec -it docker_name sh
###
### --- Push to Docker Hub ---
### docker login
### docker image ls
### docker tag show-ip-node:0.2 dockerhub_username/nodejsapp:0.2
### docker push dockerhub_username/nodejsapp:0.2
### image: dockerhub_username/nodejsapp:0.2
###
### --- Git push ---
###
### git status
### git add .
### git commit -m "Last update Nodejs App"
### git push origin main
###
###
###
## K3s + Argocd + Nodejs
### 
### --- Install K3s to Ubuntu 22.04 ---
###
### sudo apt update && sudo apt upgrade -y
### sudo su
### vi /etc/fstab
### swapoff -a
### free -m
### curl -sfL https://get.k3s.io | sh -
### sudo systemctl enable k3s
###
### --- Argocd install ---
###
### sudo kubectl create namespace argocd
### wget https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
### mv install.yaml argocd.yaml
### sudo kubectl apply -n argocd -f argocd.yaml
### sudo kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "NodePort"}}'
### sudo kubectl get svc -n argocd
### sudo kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
### 
### sudo kubectl delete -n argocd -f argocd.yaml
### sudo kubectl delete namespace argocd
###
### --- Kubectl commands ---
###
### kubectl apply -f *.yaml
### kubectl get deployment
### kubectl get pods -o wide
### kubectl get svc
### kubectl get ingress
### kubectl get namespace
### kubectl get secret
### kubectl describe ingress nodejsapp-ingress
### kubectl get pods -n default
### 
### --- Add git to Argocd ---
### Settings / Repositories
### Add Repositories
### Create Aplication
### --- Add to host file Domain Name ---
### sudo nano /etc/hosts
### your_server_IP  nodejs.db.local