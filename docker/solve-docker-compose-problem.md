# Solve docker/docker-compose problem

---

## Step 1: Update Packages List

```
sudo apt-get update
```

## Step 2: Install Docker

```
sudo apt install docker-compose
```

## Step 3: Verify Docker Installation

```
docker-compose --version

```

Output:

```
docker-compose version 2.21.0
```

Note : [Fix Docker Daemon](docker-daemon.md) Connection Problem

## Step 4: Install Docker Dependencies

```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

## Step 5: Add Docker’s Official GPG Key

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

## Step 6: Add Docker APT Repository

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

## Step 7: Update Packages List

```
sudo apt-get update
```

## Step 8: Install Docker Engine

```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

## Step 9: Start Docker Service

```
sudo service docker start
```

## Step 10: Check Docker Status

```
sudo service docker status
```

Output:

```
docker.service - Docker Application Container Engine
```

## Step 11: Add User to Docker Group

```
sudo usermod -aG docker $USER
```

## Step 12: Verify Docker Group Membership

```
groups $USER
```

Output:

```
docker
```

## Step 13: Verify Docker Installation

```
docker run hello-world
```

## Step 14: Restart WSL

```
wsl --shutdown
```

[BACK Docker](docker-main.md)
