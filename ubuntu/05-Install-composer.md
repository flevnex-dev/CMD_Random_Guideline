# Install Composer on Ubuntu

## Step 1: Update the System

```
sudo apt update
sudo apt upgrade -y


```

## Step 2: Install Required Packages

```
sudo apt install php-cli unzip curl -y
```

## Step 3: Download Composer Installer

```
curl -sS https://getcomposer.org/installer | php
```

## Step 4: Move Composer to Global Location

```
sudo mv composer.phar /usr/local/bin/composer
```

## Step 5: Verify Composer Installation

```
composer --version
```

You should see output like this:

```
Composer version 2.10.0 2024-01-19 15:24:17
```

---

# Optional: Install Specific PHP Extensions

---

## Step 1: Install PHP Extensions

```
sudo apt install php-mbstring php-xml php-curl -y
```

## Step 2: Verify PHP Extensions

```
php -m | grep mbstring
php -m | grep xml
php -m | grep curl
```

## Step 3: Common Issues and Solutions

- If you encounter any issues during the installation process, you can try the following solutions:

1. **Missing PHP CLI**: Ensure PHP CLI is installed on your system.
2. **Missing `unzip` and `curl`**: Install these packages using `sudo apt install unzip curl -y`.

### Ensure PHP is installed

```
sudo apt install php-cli
```

### Set proper permissions

```
sudo chown -R $USER:$USER ~/.composer
```

### Permission Issues with Composer

Run commands with sudo or ensure your user has proper rights.

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
