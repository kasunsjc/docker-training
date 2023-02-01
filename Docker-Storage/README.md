# Docker Storage

Docker Storage is a Docker plugin that provides a unified interface for managing storage for containers and images. It supports multiple storage drivers, including `devicemapper`, `overlay`, `overlay2`, `btrfs`, `zfs`, and `vfs`.


## Docker Storage Drivers

Docker supports multiple storage drivers. The following table lists the supported drivers and their capabilities.

| Driver | Linux | Windows | Mac | Description |
| --- | --- | --- | --- | --- |
| `devicemapper` | Yes | No | No | It uses a block device to store container images and layers. |
| `overlay` | Yes | No | No | It uses a file system to store container images and layers. |
| `overlay2` | Yes | No | No | It uses a file system to store container images and layers. |
| `btrfs` | Yes | No | No | It uses a file system to store container images and layers. |
| `zfs` | Yes | No | No | It uses a file system to store container images and layers. |
| `vfs` | Yes | Yes | Yes | It uses a file system to store container images and layers. |

## Docker Volume Commands

The following table lists the Docker storage commands.

| Command | Description |
| --- | --- |
| `docker volume create` | It creates a volume. |
| `docker volume inspect` | It displays detailed information on one or more volumes. |
| `docker volume ls` | It lists the volumes. |
| `docker volume prune` | It removes all unused volumes. |
| `docker volume rm` | It removes one or more volumes. |

## Docker Volume Examples

The following examples show how to use Docker volumes.

### Create a Volume

The following command creates a volume named `my-volume`.

```bash
docker volume create my-volume
```

### Inspect a Volume

The following command displays detailed information on a volume named `my-volume`.

```bash
docker volume inspect my-volume
```

### List Volumes

The following command lists the volumes.

```bash
docker volume ls
```

### Remove a Volume

The following command removes a volume named `my-volume`.

```bash
docker volume rm my-volume
```

### Remove Unused Volumes

The following command removes all unused volumes.

```bash
docker volume prune
```

### Mount a Volume

The following command mounts a volume named `my-volume` to a container named `my-container`.

```bash
docker container run -d --name my-container -v my-volume:/data ubuntu sleep infinity
```

### Unmount a Volume

The following command unmounts a volume named `my-volume` from a container named `my-container`.

```bash
docker container run -d --name my-container -v my-volume:/data ubuntu sleep infinity
```

### Mount a Host Directory

The following command mounts a host directory named `/data` to a container named `my-container`.

```bash
docker container run -d --name my-container -v /data:/data ubuntu sleep infinity
```

### Unmount a Host Directory

The following command unmounts a host directory named `/data` from a container named `my-container`.

```bash
docker container run -d --name my-container -v /data:/data ubuntu sleep infinity
```

### Mount a Host File

The following command mounts a host file named `/data/file.txt` to a container named `my-container`.

```bash
docker container run -d --name my-container -v /data/file.txt:/data/file.txt ubuntu sleep infinity
```