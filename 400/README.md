# 400 - Exporting Docker Containers

Now that you have a base Docker application it’s time to cover how to export a Docker container. Building a huge application takes a long time and can be a drag if you just want to share the container with your team. So is there a quicker way to share the container? Yes!

Instead of building the application directly from a Dockerfile, export the Docker container.

1. Run the ```docker``` command below to list all (```ls --all```) ```containers``` available on your machine. Note the ```CONTAINER ID``` of the container you want to share as you’ll need it to export the container in the next step.

**Note**: you can only export containers, not images.

```
$ docker container ls --all
CONTAINER ID   IMAGE        COMMAND                   CREATED        STATUS                    PORTS     NAMES
3bb38d370535   arithmetic   "/bin/sh -c 'echo $(..."  6 minutes ago  Exited (0) 6 minutes ago            epic-yalow
```

