# Node app on Container

### Description
- This is a sample node app for getting feedback
- This container uses volumes to store the persistent data
- The Docker run command is in provided.

### Usage
- only learning purposes 

### how to use it
- clone the repo
- build the image using the Dockerfile
- Run the container based on the image created.

### Commands to run 

```
git clone https://github.com/Saintmori/Docker-learning.git
```
```
cd docker-demo7
```
```
docker build . 
```
```
docker run -p 3000:80 --rm -d --name any_name -v /app/node_modules -v feedback:/app/feedback -v "$(pwd):/app:ro" -v /app/temp Image_name
```
- make sure the docker is running and then visit localhost on port 3000
