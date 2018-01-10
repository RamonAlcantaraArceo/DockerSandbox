# DockerSandbox
Learning Docker Sandbox


https://docs.docker.com/get-started/part2/#apppy

To create my image based on what I have on the path
$ docker build -t firendlyhello .
...
Successfully built c9a3da5a9c7e
Successfully tagged friendlyhello:latest

Where did it go?
$ docker images
REPOSITORY                              TAG                 IMAGE ID            CREATED             SIZE
friendlyhello                           latest              c9a3da5a9c7e        6 seconds ago       148MB

Run it?
$ docker run -p 4000:80 friendlyhello

remember '-p 4000:80' LocalHost port 4000 is mapped to port 80 in the container. Remember how we expose that already in the Dockerfile?


