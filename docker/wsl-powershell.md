# Setting Up WSL in PowerShell

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

# Using WSL in PowerShell

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

[BACK Main](docker-main.md)
