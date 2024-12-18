### Update and Upgrade

```
$ sudo apt update && sudo apt upgrade
```

If need to upgrade then upgrade 'Y' for yes.

<br/>
If need to remove unused or non-requre package or depencies then need to remove with below command.

```
$ sudo apt autoremove
```

Press 'Y' for yes to remove

### Install Preload

```
$ sudo apt-get install preload
```

Preload is a tool that runs in the background and keeps track of the user’s most frequently used applications. And using this data, it tries to predict what applications the user might run next and ensures that they’re the first to load on login, which reduces your start-up time significantly.

### Using Apt-fast Instead of Apt-get

```
$ sudo add-apt-repository ppa:apt-fast/stable
$ sudo apt-get update
$ sudo apt-get install apt-fast
```

Apt-get is one of the most important Ubuntu commands. It is basically a command line tool for installing or updating any packages in your system. Apt-fast is something of a packet that attaches itself to apt-get and accelerates the upgrade of the system and downloading of packages from the network. For installation of apt-fast, we run the following commands:

### Reducing Overheating of the System

```
$ sudo add-apt-repository ppa:linrunner/tlp
$ sudo apt-get update
$ sudo apt-get install tlp tlp-rdw
$ sudo tlp start
```

One of the major problems that systems have to face is the overheating problem. When your system gets hot, it runs slower and gives a poor performance. A very effective tool in the Ubuntu repository for this problem is TLP which helps in cooling down your system and making it run faster and smoother.<br/>
Show tlp status `$ sudo tlp-stat -s` or `$ sudo systemctl status tlp` if tlp not start automatic just add this command for startup `$ sudo tlp start`

### Cleaning Up Apt-Cache

```
$ sudo apt-get clean
$ du -sh ~/.cache/thumbnails
$ rm -r ~/.cache/thumbnails
```

There `$ sudo apt-get clean` cache clean, `$ du -sh ~/.cache/thumbnails` thumbnail cache size check and `$ rm -r ~/.cache/thumbnails` delete the thumnail cache.<br/>
Ubuntu uses Apt for installing, managing & removing software’s on the system which results in cache of previously downloaded and installed packages being stored, even after their uninstallation. This package cache can quickly become large and eat up your space. Also remove the thumnail cache.

### Configure Startup command

```
$ sudo apt-get clean
$ rm -r ~/.cache/thumbnails
```

For cleaning cache from ubuntun

### Install Bangla Keyboard

Open Bangla Keyboard:<br/>
Go to Open Bangla Keyboard Website then install keyboard with their documentation. Then go to setting and add keyboard input source/method Open Bangla Keyboard for bangla suupport, now can possible to write bangla `super key+space bar`.

<br/>Avro:<br/>If chose avro command `sudo apt-get install ibus-avro` then go to setting and add keyboard input source/method as Bangla (Avro Phonetic) for bangla suupport, now can possible to write bangla `super key+space bar`.

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
