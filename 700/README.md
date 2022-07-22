# 700 - Loading Docker Images 

Assuming you already saved an image for backup or sharing purposes, how would you load it to a machine? No worries, the [docker load](https://docs.docker.com/engine/reference/commandline/load/) command can help. The ```docker load``` command lets you load an image or repository to your machine, restoring both images and tags.

To better see how the ```docker load``` command works, delete all the Docker images you created previously.

1. Run the command below to list all Docker ```images``` in your machine.

```
$ docker images
```

Below, you can see that there are two available images. Note each of the images’ ```IMAGE ID``` as you’ll delete those images in the next step.

```
REPOSITORY          TAG      IMAGE ID       CREATED            SIZE
put_any_name_here   latest   7ce909a4e1d8   about 1 hour ago   1.24 MB
arithmetic          latest   930e9171d304   about 1 hour ago   1.24 MB
```

2. Run the below command to delete (```rm```) Docker images by the image IDs you specify. Replace ```imageID1``` and ```imageID2``` with the image IDs you noted in step one.

```
$ docker image rm imageID1 imageID2
```

