# Instructions for installing wordpress on Ubuntu 18.04

To get wordpress working, you need php and mysql

Run the code in terminal application.

Install php dependencies:

```sudo apt install php php-curl php-gd php-mbstring php-xml php-xmlrpc```

Install mysql:

```sudo apt install mysql-server```

Set the mysql root password (note in the code, dog is the password, change that to anything you want):

``` sudo mysql -u root ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'dog'; ```

Download the latest version of wordpress:

```wget https://wordpress.org/latest.tar.gz```

Untar the wordpress file that is called latest.tar.gz:

```tar -xvf latest.tar.gz```

This will create a new folder called wordpress

Copy this wordpress folder to anywhere you want, or leave it where it is, remember the location.

Inside the wordpress folder, copy wp-config-sample.php and make a file called wp-config.php

Your file should look like this:

```// ** MySQL settings - You can get this info from your web host ** //
   /** The name of the database for WordPress */
   define('DB_NAME', 'database_name_here');
   
   /** MySQL database username */
   define('DB_USER', 'username_here');
   
   /** MySQL database password */
   define('DB_PASSWORD', 'password_here');
   
   /** MySQL hostname */
   define('DB_HOST', 'localhost');
   
   /** Database Charset to use in creating database tables. */
   define('DB_CHARSET', 'utf8');
   
   /** The Database Collate type. Don't change this if in doubt. */
   define('DB_COLLATE', '');
```

Change the 'database_name_here' to 'wordpress'

Change 'username_here' to 'root'

Change 'password_here' to 'dog' (your password)

Save the file.

We will add the wordpress site into PHPStorm. 

Open up PHPStorm

Go to File > New Project and set the location to the wordpress folder that was created.

On the right of PHPStorm there should be a button called "Add Configuration" click it.

Press the + symbol and select "PHP Built-in-web Server"

Change the host to 8080

Set the "Document Root" to the wordpress folder location.

Then press apply and okay.

Now, we will create and add the MySQL database using PHPStorm

Go to View > Tool Windows > Database 

A window will appear on the right side of the screen press the + symbol

Hover over "Data Source" and select "MySQL"

A window will appear and you need to edit the user and password boxes

Enter root for the user and your password (in the example it was dog) for password

You can then press the button "Test connection". If this does not say "success" re-run the password command in the beginning, make sure your user is correct or try runing "systemctl start mysql"

If test connection was successful, hit apply and okay and then a new window will appear where you can type queries.

Create the wordpress database by copying/pasting the following lines: 

```
   CREATE DATABASE wordpress;
   CREATE USER "wordpress"@"localhost" IDENTIFIED WITH mysql_native_password BY 'dog';
   GRANT ALL PRIVILEGES ON wordpress.* TO "wordpress"@"localhost";
   
   FLUSH PRIVILEGES;
```

Click on the beginning of each line and press the green play button. A little window will appear called "Statements", click on the first statement.

Now we can start the PHP built in webserver and visit the website.

Look for the "Add configuration" button, to the right of that will be a green play button. Pres that, a window will appear and if there aren't any errors, open up a web browser and type in ```localhost:8080``` into your web browser.

You will be brought to a wordpress signup page with a logo

Name your website, pick a username such as "admin" and a password "dog" as an example and enter your email

Click install wordpress and wordpress will be installed.