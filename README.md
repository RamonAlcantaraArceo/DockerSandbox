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

Syntax?
Remember that the syntax maters and helps you name things the right way.
Once you have multiple images you might want to jump back and forth.
    'imagename:tag'
The suggested convention by docker is:
    'username/repository:tag'



Ready to swarm and scale?
remember to run:
    $ docker swarm init

and then deploy:
    $ docker stack deploy -c docker-compose.yml getstartedlab

Ready to abandon the swarm?
Remember to stop the stack:
    $ docker stack rm getstartedlab

and leave the swarm:
    $ docker swarm leave --force

To monitor what I did?

    $ docker service ls
    $ docker service ps getstartedlab_web
    $ docker container ls -q
