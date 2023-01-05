# 3 Tier Node app using docker compose

## description 

- This app contains a frontend, backend and a mongodb database
- These tiers are all containerized and are used for learning purposes
- The backend is to fetch the goals from the database 
- The node react app talks to the backend and then the database
- This version uses docker-compose file .

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
cd demo-docker11
```
- run the docker-compose command which will pull node and mongo image and build 3 containers out of them to run the backend and frontend containers as well as mongodb container.
```
docker-compose up
```
- use docker compose down command to automatically stop and remove the containers.
```
docker-compose down
```

