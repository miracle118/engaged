Engaged
=======

LIVE DEMO: http://www.mtkocak.net/engaged
DOWNLOAD: https://github.com/mtkocak/engaged

Engaged is an open source software that lets you create your own Pinterest like applications. With Engaged - You can share your interests (of course) - You can create hierarchical interest categories - You can change app's look & feel using settings - You can add new users thanks to Authake plugin

Features
----------------

- A Flexible user interface that you can almost change everything. Background images, Header & Pin colors can be changed using color picker.
- Easy to use control panel
- Hierarchical Categories like a tree
- Multiple language support (For now English & Turkish)
- Authake User Management (https://github.com/mtkocak/authake)

Requirements
----------------

- PHP installed webserver 5.3+
- MySQL database

Installation
----------------

1. Copy the all files to your server. For general xampp or mamp there is a htdocs folder. Create a folder named 'engaged' and copy all files there. If you install to your local webserver, at the end you should access to you Engaged app from http://127.0.0.1/engaged. Don't try to access it now. Installation is not finished yet :)
2. You have to first change permissions of App/tmp folder and it's subfolders. If you receive App/tmp/cache/persistent error, just create that folder. Also change the permissions for App/webroot/img folders. (Unix: Chmod 777) (Windows: I don't know). You have to do samething to the App/webroot/img folder.
3. On your MySQL database, create a database called engaged. Import engaged.sql file in the db folder.
4. Change App/Config/database.php like:

    public $default = array(
    	'datasource' => 'Database/Mysql',
    	'persistent' => false,
    	'host' => 'YOURHOSTNAME',
    	'login' => 'YOURUSERNAME',
    	'password' => 'DATABASEPASSWORD',
    	'database' => 'engaged',
    	'prefix' => '',
    	//'encoding' => 'utf8',
    );

    public $authake = array(
    	'datasource' => 'Database/Mysql',
    	'persistent' => false,
    	'host' => 'YOURHOSTNAME',
    	'login' => 'YOURUSERNAME',
    	'password' => 'DATABASEPASSWORD',
    	'database' => 'engaged',
    	'prefix' => '',
    	//'encoding' => 'utf8',
    );
    
5. After you change the database config, you can access http://127.0.0.1/engaged. A wild installation form will appear. Simply change that as you want and you are ready!

Author
----------------

Mutlu Tevfik Kocak (a.k.a Midori)
http://www.mtkocak.net

For questions and everything:
mtkocak@gmail.com






