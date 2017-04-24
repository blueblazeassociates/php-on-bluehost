# php-on-bluehost
Helper scripts for running PHP on Bluehost shared accounts.

This project has 3 components:
* Script launchers for PHP 5.4, 5.6, 7.0 (both php-cgi and php-cli) for Bluehost's shared hosting environement.
* php.ini files configured for php-cgi.
* php.ini files configured for php-cli.

## To install the project:
* Log into your Bluehost cPanel and be sure you are running your desired version of PHP.
* Log into your Bluehost cPanel and make sure SSH access is turned on.
* Log into your Bluehost account through SSH:
  * Create a directory where you want to install this project (recommendation is `~/opt/php`).
  * Navigate to the install directory.
  * Inside that directory, run (that last period is important): `git clone https://github.com/blueblazeassociates/php-on-bluehost .`
  * For your version of PHP, copy the correct .ini file as follows:
    * For CGI, copy `ini-cgi/phpXY.ini` into `~/public_html`, where `XY` are the version numbers of your PHP version. The copied file should be named `php.ini`.
    * For CLI, copy `ini-cli/phpXY.ini` into `~/.php`. You might need to create this directory. The copied file should be named `phpXY.ini`, where XY is replaced with your version, `php70.ini` for example.
  * At this point, the following things should be true:
    * You have downloaded the Git repository to `~/opt/php`.
    * You have copied `ini-cgi/phpXY.ini` (where XY = 54, 56, or 70) to `~/public_html/php.ini`.
    * You have copied `ini-cli/phpXY.ini` (where XY = 54, 56, or 70) to `~/.php/phpXY.ini`. This file doesn't actually have XY in the name, but XY is replaced with your version, `php70.ini` for example.
    * You have edited a few settings as indicated in an above step.
  
  
  
  * In each of the copied .ini files, adjust the following settings to match your environment.
    * error_log
    * mail.force_extra_parameters


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
