### To create the docker image
``` $ docker build -t <image_name> .```

- .  refers that docker image is build in current working directory


### To see the existing images
``` $ docker images```

### To run docker container from existing images
```$ docker run -d -p 8080:80 <existing_image_name>```

- -d : run container in background/detached mode
- -p : publish container's ports to the host
- 8080 port of local machine is mapped to 80 port of docker

### To list all the docker containers
```$ docker ps -a```

### To list only the containers which are running
``` $ docker ps ```

### To stop the running docker container
```$ docker stop <CONTAINER_ID>```

### To restart the container
``` $ docker start <CONTAINER_ID>```

### To remove the container
``` $ docker rm <CONTAINER_ID>```


### To remove the container and volume associated with it
``` $ docker rm -v <CONTAINER_ID>```

### To remove the docker image
``` $ docker image rm <IMAGE_ID> ```
- Note : -f tag is used to remove the running container forcefully

