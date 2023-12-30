# Hello-world-docker Module

It is a web application web application exposing REST API that send a message.

## Functionality

1. Start a web server

## Installation

This application requires: 

1. [Install NodeJS](https://nodejs.org/en/download/)

2. [Install Docker](https://docs.docker.com/desktop/)

3. Install application

Go to the hello-docker directory 

```shell
docker build -t hello-docker .
```

## Usage

1. Start a web server

From the hello-docker directory of the project, run:

```shell
docker run -p 12345:8080 -d hello-docker
```

It will start a web server available in your browser at <http://localhost:12345>



















# Hello-world-docker-compose Module

It is a web application web application exposing REST API that count how many times an user visit the web page and stores it in Redis database

## Functionality

1. Start a web server
2. Count how many times the page is visited

## Installation

This application requires: 

1. [Install NodeJS](https://nodejs.org/en/download/)

2. [Install Redis](https://redis.io/download)

3. [Install Docker](https://docs.docker.com/desktop/)

4. Install application

Go to the hello-world-docker-compose directory

```shell
docker build -t hello-world-docker-compose .
```

## Usage

1. Start a web server

From the hello-world-docker-compose directory of the project, run:

```shell
docker-compose up
```

It will start a web server available in your browser at <http://localhost:5000>






# Kubernetes / Storage-Kubernetes Module

It is a web application web application exposing REST API that count how many times an user visit the web page and stores it in Redis database

## Functionality

1. Start a web server
2. Count how many times the page is visited

## Installation

This application requires: 

1. [Install NodeJS](https://nodejs.org/en/download/)

2. [Install Redis](https://redis.io/download)

3. [Install Docker](https://docs.docker.com/desktop/)

3. [Install Minikube](https://minikube.sigs.k8s.io/docs/start/)

3. [Install Kubernetes](https://kubernetes.io/docs/tasks/tools/)


## Usage

1. Start a web server

From the kubernetes directory of the project, run:

```shell
minikube start --driver=docker
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
Retrieve the URL of the web page by running:

```shell
minikube service kubernetes-bootcamp-service
``` 
It will start a web server available in your browser at the URL you retrieve.







# User API web application

It is a basic NodeJS web application exposing REST API that creates and stores user parameters in [Redis database](https://redis.io/).

## Functionality

1. Start a web server
2. Create a user
3. Get a user

## Installation

This application is written on NodeJS and it uses Redis database.

1. [Install NodeJS](https://nodejs.org/en/download/)

2. [Install Redis](https://redis.io/download)

3. Install application

Go to the root directory of the application (where `package.json` file located) and run:

```shell
npm install 
```

## Usage

1. Start a web server

From the root directory of the project, run:

```shell
npm start
```

It will start a web server available in your browser at <http://localhost:3000>

2. Create a user

Send a POST (REST protocol) request using terminal:

```bash
curl --header "Content-Type: application/json" \
  --request POST \
  --data '{"username":"sergkudinov","firstname":"sergei","lastname":"kudinov"}' \
  http://localhost:3000/user
```

It will output:

```shell
{"status":"success","msg":"OK"}
```

Another way to test your REST API is to use [Postman](https://www.postman.com/).

## Testing

From the root directory of the project, run:

```shell
npm test
```
