# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The application listens on port 8000, returns a plain-text greeting and health status, and can be reached at http://localhost:8080 when run with Docker.

## Verification

The running application should be verified using an HTTP request to port 8000.

## Usage

Build the image:

    docker build -t git-docker-app:test .

Run the container and map host port 8080 to application port 8000:

    docker run -d --name app-test -p 8080:8000 git-docker-app:test

Check that the application responds:

    curl localhost:8080

Stop and remove the container when finished:

    docker stop app-test
    docker rm app-test
