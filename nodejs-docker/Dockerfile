#Santosh
FROM  node:buster
RUN apt-get update 
RUN apt install docker.io -y
RUN docker --version
ENTRYPOINT nohup dockerd >/dev/null 2>&1 & sleep 10 && node /app/app.js
