# Instructions for installing wordpress on Ubuntu 18.04

To get wordpress working, you need php and mysql

Run the code in terminal application.

Install php dependencies:

```sudo apt install php-curl php-gd php-mbstring php-xml php-xmlrpc```

Install mysql:

```sudo apt install mysql-server```

Set the mysql root password (note in the code, dog is the password, change that to anything you want):

``` sudo mysql -u root ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'dog'; ```

