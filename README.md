# Atlas Softy Pinko Docker Project
![docker-desktop](https://github.com/LJThao/atlas-softy-pinko-docker/assets/155511159/67f03371-7570-4d5d-a1ca-e255f2a790fe)

## Description 
We will use Docker to create a scalable application infrastructure in this project. Docker containers will package our applications into portable environments, ensuring smooth transitions between different systems without dependency issues.

Our setup includes a single entry-point server that acts as a reverse proxy and load balancer. This server will direct traffic to either the front-end static-content server or one of the two API servers. We will implement a round-robin load-balancing algorithm to evenly distribute requests across the API servers, ensuring efficient and balanced traffic management.

This project will demonstrate the use of Docker to build and manage a robust, scalable application infrastructure.

## Installation
Install Docker Desktop on your local computer:
* [Install Docker](https://www.docker.com/)
* [Docker Tutorial](https://docs.docker.com/guides/getting-started/)

## Task 0 - Create Your First Docker Image
* When you build this `Dockerfile` into a Docker image and run a container from that image, the container will perform the update and upgrade steps during the build process. When you run the container, it will execute the echo `"Hello, World!"` command and display the message in the terminal.

## Task 1 - Back-end
* To test this setup, save the `Dockerfile` and `api.py` in your task1 directory, build the Docker image using docker build -t flask-app ., and then run the container using docker run -p 5252:5252 flask-app. You should be able to access your Flask app at http://localhost:5252/ and see "Hello, World!" displayed in your browser.
  
## Task 2 - Front-end
* Reorganized project structure with a `back-end` and `front-end` directory. The front-end directory will contain a Dockerfile for Nginx to serve the static content of the cloned `softy-pinko-front-end repository`, ensuring that the site is accessible when visited in a browser.

## Task 3 - Connecting the Front-end and Back-end
* Involves connecting a `front-end` to a `back-end` in separate `Docker` containers. The front-end will request the back-end to retrieve dynamic data, which will be displayed on the front-end. Therefore, you can establish communication between your front-end and back-end Docker containers, allowing your front-end to display dynamic data fetched from the back-end.

## Task 4 - Making it Simpler with Docker Compose
* You will use `Docker Compose` to manage multiple Docker containers for your application components. Docker Compose allows you to define and run multi-container Docker applications with ease. With Docker Compose, you can manage the lifecycle of your application's containers, ensuring they are started and stopped together, making it easier to develop and deploy complex applications with multiple components.

## Task 5 - Proxy Server
* Setting up a `proxy server` using `Nginx` to act as an intermediary between your front-end, back-end, and clients. This proxy server will simplify your architecture by allowing clients to interact with your application through a single endpoint, regardless of the actual locations of your front-end and back-end services. With these changes, the proxy server will route requests from the front-end to the back-end, allowing your application to function as if the front-end and back-end were directly connected while simplifying the client-side setup.

## Task 6 - Scale Horizontally
* Setting up multiple `API servers` and configuring Nginx to load balance requests between them using the `Round-Robin` algorithm. This setup helps distribute incoming traffic evenly across the API servers, improving performance and reliability in handling high-traffic loads. By load-balancing requests between multiple API servers, you can improve the scalability and resilience of your application, ensuring that it can handle increased traffic without being overwhelmed by any single server.

## Authors and Acknowledgments
* `LJ Thao`

<p align="center">
  <img src="https://github.com/LJThao/atlas-softy-pinko-docker/assets/155511159/f6333099-8e92-4e8d-b9ca-e4401fb7140b" alt="docker windows">
</p>
