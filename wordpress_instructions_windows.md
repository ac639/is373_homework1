To get wordpress working, you need php and mysql


Install php:

	Go to: http://php.net/downloads.php
  
	Select the 'Windows downloads' option in the 'Current Stable PHP' section at the top
  
	Select the best option for your computer (x64 or x86) and download the Zip file
  
	Once the download is complete, right click on the downloaded file and 'Extract All'
  

Install mysql:

	Go to: https://dev.mysql.com/downloads/installer/
  
	Select 'Microsoft Windows' as your operating system
  
	Select the first download option and download the installer.
  
		Note: there is no need to create an account to download,
    
			scroll down and select 'No thanks, just start my download.'
      
	Follow the steps shown, selecting MySQL Server
  
	At the password portion, be sure to set a password that you will remember
  

Set Up WordPress:

	Go to: https://wordpress.org/download/
  
	Download the zip file
  
	When complete, right click and 'Extract All'
  
	Copy the unzipped wordpress folder to anywhere you want, or leave it where it is, remember the location.
  
	Inside the wordpress folder, copy wp-config-sample.php and name the copy wp-config.php
  
	Open wp-config.php
  
	
    Your file should look like this:
  
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
    
    Change the 'database_name_here' to 'wordpress'

    Change 'username_here' to 'root'

    Change 'password_here' to (your password)

    Save the file.


Add the WordPress site into PHPStorm:

	Open up PHPStorm
  
	Go to File > New Project and set the location to the wordpress folder that was created.
  
	On the right of PHPStorm there should be a button called "Add Configuration" click it.
  
	Press the + symbol and select "PHP Built-in-web Server"
  
	Change the host to 8080
  
	Set the "Document Root" to the wordpress folder location.
  
	Then press apply and okay.
  

Create and add the MySQL database using PHPStorm:

	Go to View > Tool Windows > Database
  
	A window will appear on the right side of the screen 
  
		Press the + symbol
    
	Hover over "Data Source" and select "MySQL"
  
	A window will appear and you need to edit the user and password boxes
  
		Enter 'root' for the user and (your password) for password
    
	Press the button "Test connection". 
  
	Hit apply and okay and then a new window will appear where you can type queries.
  

    Create the wordpress database by copying/pasting the following lines:

      CREATE DATABASE wordpress;

      CREATE USER "wordpress"@"localhost" IDENTIFIED WITH mysql_native_password BY '(your password)';

      GRANT ALL PRIVILEGES ON wordpress.* TO "wordpress"@"localhost";


      FLUSH PRIVILEGES;
    

    Click on the beginning of each line and press the green play button. 

    A little window will appear called "Statements", click on the first statement.



Start the PHP built in webserver and visit the website:

    Look for the "Add configuration" button, to the right of that will be a green play button. 

      Press that, a window will appear

    If there aren't any errors, open up a web browser

      Type in localhost:8080 into your web browser.



You will be brought to a wordpress signup page with a logo

Name your website, pick a username and password, and enter your email

Click install wordpress and wordpress will be installed.
