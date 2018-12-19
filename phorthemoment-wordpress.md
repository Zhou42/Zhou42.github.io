# Docoment for hosting www.phorthemoment.com website on wordpress
## Website Access
There are two addresses to access
  - website : 用户界面
    - http://204.152.201.82/
  - admin panel : 管理员后台，编辑页面
    - http://204.152.201.82/wp-admin
## Website setup
1. Host
  - Reserved instance at iozoom https://www.iozoom.com/
  - Memory Size	1024 MB
  - Disk Size	21 GB
  - IP Address	204.152.201.82
  - OS	CentOS 7.3 x64
  - $5 / mo

2. Http server
Install [Apache http server](https://www.linode.com/docs/web-servers/apache/install-and-configure-apache-on-centos-7/)
 
> sudo yum install httpd

3. MySQL instance
Install [mysql client and server](https://www.linode.com/docs/databases/mysql/how-to-install-mysql-on-centos-7/)
Create database and user for wordpress useage

4. PHP
Need to install PHP, because Wordpress is built with PHP for dynamic webpages

5. Wordpress setup
https://wordpress.org/
  - download and move wordpress files to Apache webserver root path `/var/www/html`
  - 
  - config database
  - run wp install script with web browser
  - permission 
    - chown apache:apache wp-content -R
    - chmod 755 wp-content -R
  - upload file size 
    - Default max upload file size is 2M, could be adjusted at /etc/php.ini follow [post](https://blog.gtwang.org/wordpress/how-to-increase-the-maximum-file-upload-size-in-wordpress/)
6. Domain name purchase and binding
  - godaddy etc
7. FTP
Do not setup FTP server for now follow [post](https://warptheme.com/wordpress-tutorials/update-wordpress-directly-without-using-ftp/)

## WordPress theme/plugin etc
1. `WooCommerce` 是WordPress的开源电子商务插件 (An eCommerce toolkit that helps you sell anything. Beautifully.)。它适用于使用WordPress的小型到大型在线商家 https://woocommerce.com/ 有很多有用的plugin

2. 在theme中 可以搜索 ecommerce 会找到很多template


## Security

## Website backup/recovery