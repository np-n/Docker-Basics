### To create the docker image
``` $ docker build -t <image_name> <Dockerfile_relative_path>```

e.g ``` $ docker build -t <image_name> .```

Where:
- Run all commands with `sudo` permissions
- `.`  refers that relative path of the Dockerfile is same as the current working directory relative path

### To see the existing images
``` $ docker images```

### To run docker container from existing images
```$ docker run -d -p 8080:80 <existing_image_name>```

- `-d `: run container in background/detached mode
- `-p` : publish container's ports to the host
- `8080` port of local machine is mapped to `80` port of docker container
- It doesn't create the container name.


``` $docker run --name <docker_container_name> -d -p <local_machine_port>:<container_exposed_port> <existing_image_name>```

where:
- `--name` refers the custom name of the docker container, by container name is similar to the docker image name

### To run the docker container which is already created but stopped/exited
```$docker start <container_name>```

### To list all the docker containers
```$ docker ps -a```

where:
- ```ps``` refers to the porcess, where container is the process/ runnable instance of the image
- `-a` refers to all the processes

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
- `-f` tag is used to remove the running container forcefully

#### Note: Sometimes the `CONTAINER_ID` and `CONTAINER_NAME`  are used interchangeably.