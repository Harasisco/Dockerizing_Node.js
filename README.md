# Dockerizing a Node.js Web App

Welcome to the Dockerizing a Node.js web app repository! In this project, we'll guide you through the process of containerizing a Node.js web application using Docker. Docker makes it easy to package your application and its dependencies into a single, portable container that can run consistently across different environments.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Clone the Repository](#clone-the-repository)
  - [Build the Docker Image](#build-the-docker-image)
  - [Run the Docker Container](#run-the-docker-container)
- [Accessing the Application](#accessing-the-application)
- [Customization](#customization)
- [Contributing](#contributing)

## Prerequisites

Before you get started, make sure you have the following prerequisites installed on your local machine:

- [Docker](https://www.docker.com/get-started)
- Git (optional, for cloning the repository)

## Getting Started

Follow these steps to build and run the Node.js web app using Docker on your local machine.

### Clone the Repository

If you haven't already, clone this repository to your local machine using Git:

```bash
git clone https://github.com/Harasisco/Dockerizing_Node.js.git
cd dockerizing-nodejs-web-app
```

### Build the Docker Image

To build the Docker image for the Node.js web app, run the following command in the project directory:

```bash
docker build . -t <your username>/node-web-app
```

This command will create a Docker image named nodejs-web-app based on the instructions defined in the Dockerfile.

Check the image using:

```bash
docker images
```

### Run the Docker Container

Now that you have built the Docker image, you can run the Node.js web app in a Docker container. Use the following command:

```bash
docker run -p 49160:8080 -d <your username>/node-web-app
```

This command will start a Docker container in detached mode, exposing port 8080 of the container to port 49160 on your local machine.

## Accessing the Application

Once the Docker container is running, you can access the Node.js web app in your web browser by navigating to http://localhost:49160.

Or you can call your app using ``` curl ``` (install if needed via: ``` sudo apt-get install curl ``` ):

```bash
curl -i localhost:49160
```
## Customization

Feel free to customize the Node.js web app and the Docker configuration to suit your needs. You can modify the source code in the ``` server.js ``` file and update the Dockerfile as necessary.

## Contributing

If you'd like to contribute to this project, please fork the repository and create a pull request. We welcome contributions from the community!
