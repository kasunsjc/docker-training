# Docker Networking 

Docker Networking is a feature that allows you to connect containers to each other and to the outside world. It is a powerful feature that allows you to create complex topologies and to connect containers to each other and to the outside world.

## Docker Networking Drivers

Docker supports multiple networking drivers. The default driver is `bridge` which is a simple network that connects containers to each other and to the outside world. The `bridge` driver is the only driver that is supported on Windows. The other drivers are supported on Linux only.

The following table lists the supported drivers and their capabilities.

| Driver | Linux | Windows | Mac | Description |
| --- | --- | --- | --- | --- |
| `bridge` | Yes | Yes | Yes | The default driver. It creates a network that connects containers to each other and to the outside world. |
| `host` | Yes | No | No | It removes the network isolation between the container and the Docker host. |
| `overlay` | Yes | No | No | It creates a network that spans multiple Docker hosts. |
| `macvlan` | Yes | No | No | It creates a network that uses the MAC address of the container. |
| `none` | Yes | No | No | It removes the network isolation between the container and the Docker host. |

## Docker Networking Commands

The following table lists the Docker networking commands.

| Command | Description |
| --- | --- |
| `docker network create` | It creates a network. |
| `docker network connect` | It connects a container to a network. |
| `docker network disconnect` | It disconnects a container from a network. |
| `docker network inspect` | It displays detailed information on one or more networks. |
| `docker network ls` | It lists the networks. |
| `docker network prune` | It removes all unused networks. |
| `docker network rm` | It removes one or more networks. |

## Docker Networking Examples

The following examples show how to use Docker networking.

### Create a Network

The following command creates a network named `my-network`.

```bash
docker network create my-network
```

### Connect a Container to a Network

The following command connects a container named `my-container` to a network named `my-network`.

```bash
docker container run -d --name my-container ubuntu sleep infinity

docker network connect my-network my-container

docker container inspect my-container
```

### Disconnect a Container from a Network

The following command disconnects a container named `my-container` from a network named `my-network`.

```bash
docker network disconnect my-network my-container
```

### Inspect a Network

The following command displays detailed information on a network named `my-network`.

```bash
docker network inspect my-network
```

### List Networks

The following command lists the networks.

```bash
docker network ls
```

### Remove a Network

The following command removes a network named `my-network`.

```bash
docker network rm my-network
```

### Remove Unused Networks

The following command removes all unused networks.

```bash
docker network prune
```

