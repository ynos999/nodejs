## --- Nodejs test ---
###
### npm install
### http://0.0.0.0:3000
### npm start app.js
###
## --- Docker Build ---
###
### docker build -t show-ip-node .
### docker run -p 3000:3000 show-ip-node
### curl http://localhost:3000
###
### --- Push to Docker Hub ---
### docker login
### docker image ls
### docker tag show-ip-node:latest username/nodejsapp:0.1
### docker push username/nodejsapp:0.1
### image: username/nodejsapp:0.1
###
### --- Git ---
### git status
### git add .
### git commit -m "Last update Chatbot"
### git push origin main
###