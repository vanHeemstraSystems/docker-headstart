# 300 - Building a Base Docker Application

Before jumping to exporting or saving Docker containers and images, you first need to build an application you’ll use for sharing purposes. You’ll build a basic arithmetic solution as a sample Docker application via a command-line environment.

1. Create a file for your project named Dockerfile, and paste the code below into the newly created Dockerfile.

```
$ cd containers/app/arithmetic
$ touch Dockerfile.dev
```

The code below performs a basic arithmetic operation that results in a value of 10.

```
# busybox provides Unix utilities in a single executable file, 
# which enables you to do some arithmetic.
FROM busybox
# Performs a basic arithmetic operation that results in a value of 10.
CMD echo $(((20*5)/10))
```
containers/app/arithmetic/Dockerfile.dev

2. Next, open your terminal, and run the docker build command below to build the application named (arithmetic) in the working location (.).

```
$ cd containers/app/arithmetic
$ docker build -f Dockerfile.dev --tag arithmetic .
```
