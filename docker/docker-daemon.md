# Docker Daemon Connection Problem

```
Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?
```

## Solution A: Use Docker Desktop Socket

```
export DOCKER_HOST=unix:///mnt/wsl/docker-desktop/docker.sock
```

## Solution B: Start Docker Service in WSL

```
sudo service docker start
```

## Ensure your user has access to the docker socket

```
sudo usermod -aG docker $USER

```

[BACK Docker](wsl-powershell.md)
