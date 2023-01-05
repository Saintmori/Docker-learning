# 3 tier node app

## description 

- This app contains a frontend, backend and a mongodb database
- These tiers are all containerized and are used for learning purposes
- The backend is to fetch the goals from the database 
- The node react app talks to the backend and then the database
- The more efficient version of this code is not commited yet.

## Usage

- for learning purposes
- used with docker to containerize the whole application

## How to use this

- First clone the repo
```
git clone https://github.com/Saintmori/Docker-learning.git
```
- Then navigate to the docker-demo10 folder
```
cd demo-docker10
```
- Build the images in the right frontend and backend folder.
```
cd backend 
docker build -t backend-goals .
```
```
cd frontend
docker build -t frontend-goals .
```
- Now we need to create a network in order to launch the containers in the same network.
```
docker network create goal-net
```
- After building the images with the Dockerfiles now run them.

```
docker run --name mongodb --rm -d --network goal-net mongo 
```
- Now launch the backend and publish port 80: NOTE; normally we should not publish any port since we are launching the containers in the same network but because the react app needs to talk to the backend and its charecteristics is to run in the browser , we can't launch that in the network same as the containers. but still we need to put the backend in the network cause it needs to communicate with the mongodb.
```
docker run --name backend-goal --rm -d -p 80:80 --network goal-net backend-goals
```
- Now we run the react app
```
docker run --name frontend-goal --rm -it -p 3000:3000 frontend-goals 
```
