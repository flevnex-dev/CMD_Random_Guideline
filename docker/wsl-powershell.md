# Setting Up WSL in PowerShell

---

## Step 1: Check WSL Version

```
wsl -l -v
```

or

```
wsl --list --verbose
```

## Step 2: Install WSL

```
wsl --install
```

## Step 3: Install a specific Linux distribution

```
wsl --install -d <distro-name>
```

Example:

```
wsl --install -d Ubuntu
```

## Step 4: Set Default WSL Version

```
wsl --set-default-version 2
```

---

# Using WSL in PowerShell

---

## Step 1: Launch WSL:

```
wsl
```

## Step 2: Run a Single Linux Command:

```
wsl <command>
```

Example:

```
wsl ls
```

Executes ls (list files) in the default WSL distribution.

## Step 3: Specify a Distribution

```
wsl -d <distro-name>
```

Example:

```
wsl -d Ubuntu
```

## Step 4: List Installed Distributions:

```
wsl --list --verbose
```

Output:

```
NAME                   VERSION                   STATE   SHARE   USER    VM ID
Ubuntu                22.04                      Running   None    user    -

```

## Step 5: Set Default Distribution:

```
wsl --set-default <distro-name>
```

Example:

```
wsl --set-default Ubuntu
```

## Step 6: Terminate a WSL Session:

```
wsl --terminate <distro-name>
```

Example:

```
wsl --terminate Ubuntu
```

## Step 7: Uninstall a Linux Distribution:

```
wsl --unregister <distro-name>
```

Example:

```
wsl --unregister Ubuntu
```

## Step 8: Check WSL Status:

```
wsl --status
```

---

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

[BACK Main](docker-main.md)
