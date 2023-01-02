# Node app

## Description
- This is a node app that sends api request to get movies names
- The node app is containerized and will be able to communicate to the world because containers give out of the box WWW connection
- It also connects to a mongodb container 
- we should create a network for the containers to be able to communicate

## Usage 
- only personal learning purposes

## how to use this.
- clone the repo
- run mongo container with the official mongo image with the name mongodb
- use postman to send api request to the app and check if the post request are saved in the mondgodb container

## commands
```
git clone https://github.com/Saintmori/Docker-learning.git
```
```
cd docker-demo9
```
```
docker build .
```
```
docker network create test
```
```
docker run --name any_name -d --network test -p 3000:3000 name_of_built_image
```
```
docker run --name mongodb --network test mongo
```
