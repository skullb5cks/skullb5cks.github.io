
1. install Docker  
https://hub.docker.com/editions/community/docker-ce-desktop-mac  
  
2. clone docket-node-app  
git clone https://github.com/arvindr21/docker-node-app


cd docker-node-app

Dockerfile 수정  
```
# A node.js v8 box
FROM node:8

# Who(m) to blame if nothing works
MAINTAINER arvind.ravulavaru@gmail.com

# Create a working directory 
RUN mkdir -p /usr/src/app

# Switch to working directory
WORKDIR /usr/src/app

# Copy contents of local folder to `WORKDIR`
# You can pick individual files based on your need
COPY . .

# Install nodemon globally
RUN npm install -g nodemon

# Install dependencies (if any) in package.json
RUN npm install

# Expose port from container so host can access $PORT
EXPOSE $PORT

# Start the Node.js app on load
CMD [ "npm", "start" ]
```

heroku create 실행  
heroku container:push web 실행  
> no basic auth credentials ▸ Error: docker push exited with Error: 1 에러가 난다면  
> heroku container:login 실행  

