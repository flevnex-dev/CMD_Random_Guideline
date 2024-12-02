### File Permission

#### Add User

```
sudo adduser username
```

#### Give permission to user use sudo

```
sudo visudo
```

--------------Open edit file with nano also
This will open the sudoers file in a text editor. Look for a line that includes the phrase %sudo ALL=(ALL:ALL) ALL.
Add a new line below that line and enter: username ALL=(ALL:ALL) ALL
Save the file and exit the text editor.

```
username ALL=(ALL) ALL
```

#### Add under group any user

```
sudo usermod -aG sudo username
```

// www-data - group name, $USER - get automatic current user, also can use username like `$ sudo usermod -aG www-data asifulmamun`, here usermod user adding under the www-data group
// Check - also you can check how many groups using the user username with this comman `$ grep -i --color 'username' /etc/group`

```
sudo usermod -aG www-data $USER
```

// $USER change also with username like as `su mostafizur`

```
su $USER
```

#### Show all users in ubuntu

```
cut -d: -f1 /etc/passwd
```

or

```
compgen -u
```

or

```
getent passwd
```

#### Show all Groups in ubuntu

```
compgen -g
```

or

```
getent group
```

#### Show User info - mostafizur user replace with your username

```
getent passwd mostafizur
```

#### Show group info user - mostafizur user replace with your username

```
grep -i --color 'mostafizur' /etc/group
```

#### Add user mostafizur and group www-data - mostafizur can access file like as owner also www-data because mostafizur also www-data group member

```
sudo chown -R $USER:www-data filename.txt/foldername
```

1. $USER - also change with asifulmamun but need write permission to group
2. Permission to grop `$ sudo chmod -R g+w html`

### Describe

`ls -l` - show file permission

```
ls -l
```

[04.1-describe.txt](04.1-describe.txt)

Where: - : Means No Permission
r : Means No Read
w : Means No Write
x : Means No Execution

### Command

```
sudo chown asifulmamun:asifulmamun filename.txt
```

or

```
sudo chown asifulmamun: filename.txt


```

Where:
sudo - Command Permission as super user
chown - Command type for make owner of this file
asifulmamun:asifulmamun - First part is username and after ':' colon second part is group name
filename.txt - File or Folder name

```
sudo chown asifulmamun filename.txt
```

Where only change user as asifulmamun

```
sudo chown :root filename.txt
```

Where only change group as root

```
sudo chmod -R 777 filename.txt
```

Where:
chmod - Permission type
-R - All file and folder and sub folder targated
777 - Set permission read, write and execution (rwx)
755 - Set permission read and execution only (r-x)

# Here we can use:

u = User
g = Group
o = Others
a = 'ugo' / all

```
sudo chmod u+x filename.txt
```

Where set execution permission to this file, can multiple (u+rwx), also single (u+r)

```
sudo chmod u-x filename.txt
```

Where remove execution permission to this file only user, can multiple (u-rwx), also single (u-r)

```
sudo chmod g+x filename.txt
```

Where set execution permission to this file only group, can multiple (g+rwx), also single (g+r)

```
sudo chmod g-x filename.txt
```

Where remove execution permission to this file only from group, can multiple (g-rwx), also single (g-r)

```
sudo chmod u-x *.txt
```

Where remove execution permission to this file only from user all txt files

```
sudo chmod ug-r filename.txt
```

Where set execution permission to this file, can multiple (u+rwx), also single (u+r)

Where we can use: - ugo+rwx / ugo-rwx / ug+rwx / ug-urx - So any user, group or others can be possible remove or set any permission just need to mention (ugo or a for all or single, and permission any rwx / rw / r / x / w etc)

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
