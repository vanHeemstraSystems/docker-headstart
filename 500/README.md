# 500 - Importing Docker Containers

Instead of exporting, perhaps you need to import a Docker container that a teammate shared with you. If so, the [docker import](https://docs.docker.com/engine/reference/commandline/import/) command is what you need. The ```docker import``` command takes the exported filesystem and converts it into an image filesystem you can run on your machine.

1. Run the following ```docker``` command to ```import``` a container (```arithmetic.tar```) and convert it to an image. When importing, you must attach a tag (```latest```) and name the image (```put_any_name_here```), as shown below.

```
$ cd containers/app/arithmetic
$ docker import arithmetic.tar put_any_name_here:latest
sha256:579843543543u543uto43t0uerp094386i3t436096363
```

2. Next, run the below command to list all existing Docker images, so you can verify if a new image exists.

```
$ docker images
REPOSITORY          TAG    IMAGE ID       CREATED              SIZE
put_any_name_here   latest  7ce909a4e1d8  About a minute ago   1.24MB
```

3. Now execute the ```docker run``` command below to open the shell (```sh```) for the imported image. The container runs interactively and is attached to your terminal (```-i``` and ```-t``` flags).

```
$ docker run -i -t put_any_name_here:latest sh
```

