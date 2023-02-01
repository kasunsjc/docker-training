# Docker Troubleshooting 

## Docker Troubleshooting Commands

Following is a list of Docker troubleshooting commands.

| Command | Description |
| --- | --- |
| `docker container logs` | It displays the logs of a container. |
| `docker container top` | It displays the running processes of a container. |
| `docker container stats` | It displays a live stream of container(s) resource usage statistics. |
| `docker container inspect` | It displays detailed information on one or more containers. |
| `docker container port` | It lists port mappings or a specific mapping for the container. |
| `docker container diff` | It displays changes on a container's filesystem. |
| `docker container exec` | It runs a command in a running container. |
| `docker container cp` | It copies files/folders between a container and the local filesystem. |
| `docker container commit` | It creates a new image from a container's changes. |
| `docker container wait` | It blocks until one or more containers stop, then print their exit codes. |
| `docker container export` | It exports a container's filesystem as a tar archive. |
| `docker container kill` | It kills one or more running containers. |
| `docker container pause` | It pauses all processes within one or more containers. |
| `docker container rename` | It renames a container. |
| `docker container restart` | It restarts one or more containers. |
| `docker container rm` | It removes one or more containers. |

## Docker Troubleshooting Examples

The following examples show how to use Docker troubleshooting commands.

### Display the Logs of a Container

The following command displays the logs of a container named `my-container`.

```bash
docker container logs my-container
```

### Display the Running Processes of a Container

The following command displays the running processes of a container named `my-container`.

```bash
docker container top my-container
```

### Display a Live Stream of Container(s) Resource Usage Statistics

The following command displays a live stream of container(s) resource usage statistics.

```bash
docker container stats
```

### Display Detailed Information on a Container

The following command displays detailed information on a container named `my-container`.

```bash
docker container inspect my-container
```

### List Port Mappings or a Specific Mapping for the Container

The following command lists port mappings or a specific mapping for the container named `my-container`.

```bash
docker container port my-container
```

### Display Changes on a Container's Filesystem

The following command displays changes on a container's filesystem.

```bash
docker container diff my-container
```

### Run a Command in a Running Container

The following command runs a command in a running container named `my-container`.

```bash
docker container exec my-container
```

### Docker interactive mode

The following command runs a command in a running container named `my-container` in interactive mode.

```bash
docker container exec -it my-container /bin/bash
```

### Copy Files/Folders Between a Container and the Local Filesystem

The following command copies files/folders between a container and the local filesystem.

```bash
docker container cp my-container
```

### Create a New Image from a Container's Changes

The following command creates a new image from a container's changes.

```bash
docker container commit my-container
```

### Block Until One or More Containers Stop, Then Print Their Exit Codes

The following command blocks until one or more containers stop, then print their exit codes.

```bash
docker container wait my-container
```
