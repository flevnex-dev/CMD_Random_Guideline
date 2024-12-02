# Nodejs

## Step 1 : Update the System

```
sudo apt update
sudo apt upgrade -y
sudo apt install -y curl
```

## Step 2: Install Node.js Using NodeSource (Recommended)

### Add the NodeSource repository:

1. For the latest LTS version (e.g., Node.js 18):

```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -

```

2. For the latest Current version:

```
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
```

### Install Node.js:

```
sudo apt install -y nodejs
```

### Verify the installation:

```
node -v
npm -v

```

## Step 3: (Optional) Install Node.js Using nvm (Node Version Manager)

### Install nvm:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

### Activate nvm:

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

### Run the following command to make nvm available in your current shell session:

```
source ~/.bashrc
```

### Install Node.js Using nvm:

```
nvm install --lts
nvm install node  # For the latest version
```

### Switch Between Versions:

```
nvm use <version>
nvm use 18  # Example: Use Node.js 18

```

### Check Installed Version:

```
node -v
```

## Step 4: Install npm Packages (Optional)

### Install popular global packages like npm, yarn, or pm2:

```
npm install -g yarn pm2
```

## Common Issues and Solutions

### Node.js Command Not Found:

```
sudo apt install -y nodejs
```

### Old npm Version:

```
sudo npm install -g npm
```

### Permission Issues with npm:

```
sudo chown -R $USER:$USER ~/.npm


```

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
