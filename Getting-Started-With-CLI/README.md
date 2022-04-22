
# Working with Docker Container Life Cycle

```
docker container run hello-world
```

### List the running containers

```
docker container ls
docker container ls -a
```

### List the images

```
docker image ls
```

### Managing Life-Cycle of a Container

Download the Image of ubuntu 18.04 and list available images

```
docker image pull ubuntu:18.04
docker image ls 
```

### Inspect the container

```
docker inspect <imageID>
```

### Running the container with ubuntu 18.04

We can run the container from the image with the following command. -d is for detached mode.

```
docker container run -d ubuntu:18.04
docker container ls
```

We can run the containers with interactive mode.
- -i is for interactive mode.
- -t is for tty mode.
- -d is for detached mode.
- --name is for naming the container.

```
docker run -i -t -d --name ubuntu1 ubuntu:18.04
```

We can use exec to run the command inside the container.

```
docker exec -it ubuntu1 /bin/bash
```

Run commands inside the container

```
echo "Hello world from ubuntu1" > hello-world.txt
```

insteard of exec in to container we can run the command directly in the container with the following command.

```
docker exec -it ubuntu1 cat hello-world.txt
```

Stop & start running container

```
docker stop ubuntu1 
docker start ubuntu1
```

Remove a container. if the container is running docker will not allow to remove the container. To force the remove the container we need to use -f flag.

```
docker stop ubuntu1 
docker rm ubuntu1
```

To remove the image from local enviornment we can use the following command.

```
docker image rm <ImageName/ImageID>
```

## Attach to a container

Run a container with the following command.

```
docker run -itd --name attach-example1 ubuntu:latest
```

Run the docker attach command to attach to the primary process inside this container, (/bin/bash). Use docker attach followed by the name or ID of the container instance.

```
docker attach attach-example1
```

Use the keyboard combinations **Ctrl + P** and then **Ctrl + Q** to detach from this session gracefully. Otherwise container will stop when you exit from the container

Use the following command to clean up the stopped container instances

```
docker system prune -fa
```

## Activity 1

You can find the required documentation for postgresql from the following link.

https://hub.docker.com/_/postgres

1. Create a Postgres database container instance that will serve as the data tier of our application stack.

2. Use environment variables to configure the container at runtime to use the following database credentials
```
username: root
password: trekking
```

3. Verify whether the container is running and healthy.

After container is running, run the following command to verify the postgresql container is running and healthy.

1. Log in to the Postgres database container using the PSQL command-line utility.
Once logged in to the database, return a list of databases in Postgres by default.

**Note**

- If you are not familiar with the PSQL CLI, the following is a list of reference commands to assist you with this activity:

1. Logging in: **psql --username username --password**

2. Listing the database: \l

3. Quitting the PSQL shell: \q


---
## Answer - Activity 1

<details><summary>CLICK ME</summary>
<p>

Running the Postgresql server container with the following command.

    docker container run -d --name postgres01 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=trekking postgres:12

    docker exec -it postgres01 psql -U root  --password

Expected output:

```
root=# \l
                             List of databases
   Name    | Owner | Encoding |  Collate   |   Ctype    | Access privileges 
-----------+-------+----------+------------+------------+-------------------
 postgres  | root  | UTF8     | en_US.utf8 | en_US.utf8 | 
 root      | root  | UTF8     | en_US.utf8 | en_US.utf8 | 
 template0 | root  | UTF8     | en_US.utf8 | en_US.utf8 | =c/root          +
           |       |          |            |            | root=CTc/root
 template1 | root  | UTF8     | en_US.utf8 | en_US.utf8 | =c/root          +
           |       |          |            |            | root=CTc/root
(4 rows)

```
</p>
</details>