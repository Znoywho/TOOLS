> [!CAUTION]
> [tuorial video](https://youtu.be/GFgJkfScVNU?si=t3UM7jIV1T-zF9vv) 

> [!IMPORTANT]
> ***DOCKER = DEVELOPMENT + EXECUTION +  PACKAGING***
> Also include ***OS*** 


> [!HELP]
> INTEGRATION:
> - Developed
> - Tested
> - Deployed efficiently

## image

> [!NOTE]
> 1. lightweight
> 2. Stand alone
> 3. Executable package

## Container
> [!NOTE]
> ***Runnable Instance*** 

> [!HELP]
> 1. code 
> 2. runtime
> 3. library
> 4. System tools

## volumes
> [!NOTE]
> ***Persistent data storage mechanism***
> help data can be shared **Container** with **Whole machine**  

### DOCKER NETWORK
> Help container connect each other

> [!ATTENTION]
> # ***WORKFLOW*** 
> - Docker client(commandline)
> - Docker host(container + image )
> - Docker hub (the deepest)


## ***DOCKER FILE***
> [!IMPORTANT]
> ***WANNA CREATE YOUR OWN IMAGE***
> CREATE ***.yml** 

```Dockerfile
FROM image[:tag] [AS name]
# Example
FROM ubuntu:20.04
```
> [!NOTE]
> choose base image

### WORKDIR
```Dockerfile
WORKDIR /path/to/workdir
#Example
WORKDIR/app

```
> [!NOTE]
> Design place to hold container

### RUN 
```Dockerfile
run <command>
#Example
RUN npm run dev
```
> [!NOTE]
> SPECIFIC STEPS

### EXPOSE
```Dockerfile
EXPOSE <port> [<port>/<protocol>...]
# Example
EXPOSE 3000
```
> [!NOTE]
> SPECIFIC PORT 

### ENV
> [!NOTE]
> setting of System

### ARG
> [!NOTE]
> Arguments

### VOLUME 
```Dockerfile
VOLUME ["/data"]
# Example
VOLUME /myvol
```
> [!NOTE]
> Create an amount of points
### CMD 
```Dockerfile
CMD ["executable, param1","param2"]
```

### ENTRYPOINT
```Dockerfile
CMD npm run dev
```
> [!NOTE]
> 

| CMD | ENTRYPOINT |
| :--------------: | :---------------: |
| Flexible, can be overridden | cannot be overridden |
| Default executable | Fixed starting point |


## TERMINAL

```terminal 
docker pull [image]
```
> [!NOTE]
> Download specific image

```terminal
docker run -it [name of image]
```
> [!NOTE]
> run image

```terminal
docker build -t [name of directory] .
```
> [!NOTE]
> **"-t"** is task 

***TERMINAL***
![](../assets/docker%20run.png)
```Dockerfile
docker images
```
![](../assets/list%20all%20images.png)

```Dockerfile
docker run [name of image]
```
![](../assets/run%20file%20.png)

### Open OS 
```terminal
docker run -it docker_code sh
```
![Open os](../assets/open%20OS.png)

## Docker react







- [x] Keep going with video
- [-] write down the docker syntax
- [-] write down again the commandline









