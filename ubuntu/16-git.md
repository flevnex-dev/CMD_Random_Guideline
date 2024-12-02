# Git

## Step 1: Setup Git

### Install Git

```
sudo apt update
sudo apt install -y git
```

### Check Git Version

```
git --version
```

### Example Output

```
git version 2.34.1
```

## Step 2: Configure Git

```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list
```

## Step 3: Basic Git Commands

### Clone Repository

```
git clone <repository-url>

```

Example

```
git clone https://github.com/username/repo.git
```

### Initialize Git Repository

```
git init
git add .
git commit -m "Initial commit"
git status

git push origin <branch-name>


```

### Git pull

```
git pull origin <branch-name>
```

### Git log

```
git log
```

## Step 4: Generate SSH Key (Optional)

```
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
```

### Add SSH Key to SSH Agent

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa

```

### Copy SSH Key

```
cat ~/.ssh/id_rsa.pub
```

### Test SSH Connection

```
ssh -T git@github.com
```

## Step 5: Undo Changes (Optional)

### Unstage a File

```
git reset HEAD <file>
```

### Undo the Last Commit

```
git reset --soft HEAD~1


```

### Discard All Local Changes

```
git checkout .
```

## Resources

[Git Resources Atlassian](https://www.atlassian.com/git/tutorials)
[Git Resources](https://git-scm.com/doc)

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
