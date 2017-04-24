# php-on-bluehost
Helper scripts for running PHP on Bluehost shared accounts.

This project has 3 components:
* Script launchers for PHP 5.4, 5.6, 7.0 (both php and php-cli) for Bluehost's shared hosting environement.
* php.ini files configured for php-cgi.
* php.ini files configured for php-cli.

## To install the project:
* Log into your Bluehost cPanel and be sure you are running your desired version of PHP.
* Log into your Bluehost cPanel and make sure SSH access is turned on.
* Log into your Bluehost account through SSH.
 * Create a directory where you want to install this project (recommendation is ~/opt/php).
 * Navigate to the install directory.
 * Inside that directory, run (that last period is important): `git clone https://github.com/blueblazeassociates/php-on-bluehost .`
 * Copy each 


* If on Windows, be sure to be using a Bash shell.
* Make sure php-cli is available on your system path.
* Make sure Git is available on your system path.
* Create a directory where you want to install Composer.
* Inside that directory, run (that last period is important): `git clone https://github.com/blueblazeassociates/composer-installer.git .`
* If not on Windows, make the scripts executable:
 * `chmod 744 composer-install.bash`
 * `chmod 744 composer`
* Run the installer: `composer-install.bash`
* Add the composer to your system path, either by:
 * Add the install directory to the system path.
 * Symlink the `composer` script into your `bin` directory.
 
## What is inside this project?
* Installer script: `composer-installer.bash`
* Execution script with preset PHP options: `composer`

## Why?
* I have to run these commands for every project I work on, so I placed them here for easy use.
