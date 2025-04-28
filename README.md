# Movie API with Flask and Docker

This project provides a simple Flask API that serves movie data (ID, Title, Image URL) from a CSV file. The application is containerized using Docker for easy setup and deployment.

## Prerequisites

* [Docker](https://docs.docker.com/get-docker/) installed on your system.

## Project Structure

your_project/├── Dockerfile           # Docker instructions├── requirements.txt     # Python dependencies├── app.py               # Flask API script└── tmdb_subset_300.csv  # Movie data CSV
## Usage

Follow these steps to build the Docker image and run the containerized application.

**1. Build the Docker Image**

   Navigate to the project directory in your terminal and run the build command. This will create a Docker image named `my-movie-api`.

   ```bash
   docker build -t my-movie-api .
2. Run the Docker ContainerYou can run the container in two ways:Detached Mode (Runs in the background):This command starts the container and maps port 5000 on your host machine to port 5000 inside the container.docker run -d -p 5000:5000 --name movie-api-container my-movie-api
Interactive Mode (Shows logs in the terminal):Use this command if you want to see the application logs directly in your current terminal window. Press Ctrl+C to stop the container.docker run -p 5000:5000 --name movie-api-container my-movie-api
3. Access the APIOnce the container is running, you can access the API endpoints through your browser or an API tool like Postman or curl:http://localhost:5000/movieshttp://localhost:5000/movies?page=2&per_page=20Basic Docker Commands for ManagementHere are some useful commands to manage your Docker container and image:List running containers:docker ps
List all containers (including stopped ones):docker ps -a
Stop the container:docker stop movie-api-container
Start a stopped container:docker start movie-api-container
View container logs (if running in detached mode):docker logs movie-api-container
Remove the container (must be stopped first):docker rm movie-api-container
Remove the Docker image:docker rmi my-movie-api
