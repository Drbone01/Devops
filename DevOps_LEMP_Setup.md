# GitHub Link
[https://github.com/Drbone01/Devops](https://github.com/Drbone01/Devops)

# LinkedIn Post

```bash
sudo apt update
sudo apt install nginx
sudo systemctl status nginx
curl http://localhost:80

sudo apt install mysql-server
sudo mysql

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1'

sudo mysql -p

mysql>exit

sudo apt install php-fpm php-mysql

sudo mkdir /var/www/projectLEMP

sudo chown -R $USER:$USER /var/www/projectlamp

sudo nano /etc/nginx/sites-available/projectLEMP

#/etc/nginx/sites-available/projectLEMP

server {
    listen 80;
    server_name projectLEMP www.projectLEMP;
    root /var/www/projectLEMP;

    index index.html index.htm index.php;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php8.3-fpm.sock;
    }

    location ~ /\.ht {
        deny all;
    }
}

sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/

sudo nginx -t

sudo unlink /etc/nginx/sites-available/default

sudo systemctl reload nginx


sudo echo 'Hello LEMP from hostname! ' $(TOKEN=`curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600"` && curl -H "X-aws-ec2-metadata-token: $TOKEN" -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP ' $(TOKEN=`curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600"` && curl -H "X-aws-ec2-metadata-token: $TOKEN" -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectLEMP/index.html

nano /var/www/projectLEMP/info.php

<?php
phpinfo();
?>

sudo mysql
mysql> CREATE DATABASE 'example_database'

CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'PassWord.1'

GRANT ALL ON example_database.* TO 'example_user'@'%'

exit

-u example_user -p
```
