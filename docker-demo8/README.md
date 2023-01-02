# Node app on Container

### Description
- This is a sample node app for getting feedback
- This container uses volumes to store the persistent data
- The Docker run command is in provided.
- This Dockerfile uses env variable and build arg .

### Usage
- only learning purposes 

### how to use it
- clone the repo
- build the image using the Dockerfile
- Run the container based on the image created.
- if you use the build arg and change the default port number to 8000 make sure to expose the port in the docker run command.

### Commands to run 

```
git clone https://github.com/Saintmori/Docker-learning.git
```
```
cd docker-demo7
```
```
docker build -t node:dev --build-arg DEFAULT_PORT=8000 .
```
```
docker run -p 3000:8000 --env-file ./.env --rm -d --name any_name -v /app/node_modules -v feedback:/app/feedback -v "$(pwd):/app:ro" -v /app/temp Image_name
```
- make sure the docker is running and then visit localhost on port 3000
