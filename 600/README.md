# 600 - Saving Images via Docker Save Image

Perhaps you want to save a Docker image rather than a container. If so, go with the ```docker save image``` command instead. Unlike the ```docker export``` command, the ```docker save``` command lets save one or more images to a tar archive directly and share it with anyone.

**Note**: you can only save and load Docker images, not containers.

1. Run the command below to save a Docker image (```arithmetic```) to your preferred *.tar* archive (```arm_image.tar```). You can now share the *.tar* archive with other developers so they can load the image.

```
$ cd containers/app/arithmetic
$ docker save arithmetic > arm_image.tar
```

```
$ cd containers/app/arithmetic
$ ls -la
...
arm_image.tar
...
```

2. Now, run the command below to create a directory with the name of your choice (```mkdir arm```). But for this demo, the directory is named ```arm```. The command then extracts the image from the *.tar* archive (```-xf arm_image.tar```) to the new directory (```arm```).

Extracting the contents of the *.tar* archive lets you confirm if the image you saved in the *.tar* archive exists.

```
$ cd containers/app/arithmetic
$ mkdir arm && tar -xf arm_image.tar -C arm
```

3. Finally, run the ```tree``` command below to view the directory tree of the image you extracted in the ```~/arm``` directory. ```tree ~/arm```

Below you can see the files and subdirectories inside the directory where you extracted the Docker image.

```
$ cd containers/app/arithmetic
$ tree ~/arm

```
