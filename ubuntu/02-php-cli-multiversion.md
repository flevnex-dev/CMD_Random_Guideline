### PHP Multi-PHP

- Install required php
  ```
  sudo apt update
  sudo apt-add-repository ppa:ondrej/php
  sudo apt update
  sudo apt install php7.4-fpm
  sudo apt install php7.4-common php7.4-mysql php7.4-xml php7.4-xmlrpc php7.4-curl php7.4-gd php7.4-imagick php7.4-cli php7.4-dev php7.4-imap php7.4-mbstring php7.4-opcache php7.4-soap php7.4-zip php7.4-intl
  ```
- Install MultiPHP Manager `sudo apt install ea-php-cli`
- List Available PHP Versions: `sudo update-alternatives --list php`
- Switch PHP Version `sudo update-alternatives --set php /usr/bin/php7.4`
- Check Current PHP Version `php -v`

#### Service Restart

- Nginx `sudo systemctl restart nginx`
- Apache2 `sudo service apache2 restart`

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
