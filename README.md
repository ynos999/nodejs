## --- Nodejs test ---
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
### docker tag show-ip-node:0.2 username/nodejsapp:0.2
### docker push username/nodejsapp:0.2
### image: username/nodejsapp:0.2
###
### --- Git ---
### git status
### git add .
### git commit -m "Last update"
### git push origin main
###