# Docker Task 1

## Part 1

### Create a new Alpine container

Create a detached container named `alpine_sleeper` that sleeps for 1000 seconds.

```bash
docker run -d --name alpine_sleeper alpine sleep 1000
```

### List all containers

Display all running and stopped containers.

```bash
docker ps -a
```

### Stop the container

```bash
docker stop alpine_sleeper
```

### Remove the container

```bash
docker rm alpine_sleeper
```

### Remove the Alpine image

```bash
docker rmi alpine
```

---

## Part 2

### Create an interactive Ubuntu container

Run an Ubuntu container that repeatedly asks for a website, waits one second, and then fetches its contents using `curl`.

```bash
docker run -it --name ubuntu-server ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
```

### Open a shell inside the running container

```bash
docker exec -it ubuntu-server bash
```

### Update package lists

```bash
apt update
```

### Install curl

```bash
apt install curl -y
```
