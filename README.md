# Udagram Image Filtering Application

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:

1. The Simple Frontend A basic Ionic client web application which consumes the RestAPI Backend.
2. The RestAPI Feed Backend, a Node-Express feed microservice.
3. The RestAPI User Backend, a Node-Express user microservice.

## Getting Started
> _tip_: it's recommended that you start with getting the backend API running since the frontend web application depends on the API.

### Installing Node and NPM
This project depends on Nodejs and Node Package Manager (NPM). Before continuing, you must download and install Node (NPM is included) from https://nodejs.com/en/download.

### Installing Ionic Cli
The Ionic Command Line Interface is required to serve and build the frontend. Instructions for installing the CLI can be found in the Ionic Framework Docs.

### Installing project dependencies
This project uses NPM to manage software dependencies. NPM Relies on the package.json file located at the root directory of a Node.js project.

1. Clone this repository
2. Open your terminal
3. Run npm install for the frontend and backend projects.
tip: npm i is shorthand for npm install

Example:
> cd ./udacity-c3-restapi-feed
>
> npm install

### Configure The Backend Endpoint
Ionic uses enviornment files located in ./src/enviornments/enviornment.*.ts to load configuration variables at runtime. By default environment.ts is used for development and enviornment.prod.ts is used for produciton. The apiHost variable should be set to your server url either locally or in the cloud.

### Running the Development Server
Ionic CLI provides an easy to use development server to run and autoreload the frontend. This allows you to make quick changes and see them in real time in your browser. To run the development server, open terminal and run:

> ionic serve

### Building the Static Frontend Files
Ionic CLI can build the frontend into static HTML/CSS/JavaScript files. These files can be uploaded to a host to be consumed by users on the web. Build artifacts are located in ./www. To build from source, open terminal and run:

> ionic build

## Setup Docker Environment 
You'll need to install docker https://docs.docker.com/install/. Open a new terminal within the udacity-c3-deployment/docker directory and run:

1. Build the images: docker-compose -f docker-compose-build.yaml build --parallel
2. Push the images: docker-compose -f docker-compose-build.yaml push
3. Run the container: docker-compose up

## Deploy on Kubernetes
Docker Desktop includes a standalone Kubernetes server and client, as well as Docker CLI integration. See Docker Desktop for Windows or Mac > Getting started to enable Kubernetes.

1. Navigate to the udacity-deployment/k8s directory
2. Set AWS credentials and configs
3. Run: docker-compose up
> kubectl apply -f ./config

> kubectl apply -f ./service

> kubectl apply -f ./deployment

