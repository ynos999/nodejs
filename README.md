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