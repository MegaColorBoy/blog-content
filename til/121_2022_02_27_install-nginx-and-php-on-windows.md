title: Install NGINX and PHP on Windows
date: February 27th, 2022
slug: install-nginx-and-php-on-windows
category: Tutorial
summary: Write your summary here.
status: inactive

Thought of writing a small tutorial on how to install NGINX and PHP on Windows. You can also use this as a reference if you wanted to install them on Windows Server too.

<div class="post-notification warning">
	<h3>Tip</h3>
	<p>Try not to copy-paste every piece of the examples provided.</p>
</div>

## Setting up NGINX

1. Download [NGINX for Windows](http://nginx.org/en/docs/windows.html)
2. Go to `C:/` directory and create a folder named `C:/nginx`.
3. Unzip the downloaded `.zip` file in `C:/nginx` directory.
4. Go to `C:/nginx` and create two new folders named `sites-available` and `sites-enabled`.
5. To test, if it's working, double-click on `C:/nginx/nginx.exe` and type `localhost` in the browser. You should be able to see a Welcome page.
6. Kill the NGINX process from Task Manager.

## Setting up PHP

1. Download [PHP 8.1 for Windows](https://windows.php.net/downloads/releases/php-8.1.1-nts-Win32-vs16-x64.zip).
2. Go to `C:/` directory and create a folder named `C:/php` or if you wanted to have multiple versions, `C:/php8.1`.
3. Unzip the downloaded `.zip` file in `C:/php` directory.
4. Add PHP to your system environment variables by adding the path `C:/php`
5. Open Command Prompt and type `php -v`. You see should be able to see the version if it's installed correctly.

## Run NGINX and PHP as separate services

### Install NSSM Service Manager

1. Download [NSSM Service Manager](https://nssm.cc/download)
2. Go to `C:/` directory and create a folder named `C:/nssm`.
3. Unzip the downloaded `.zip` file in `C:/nssm` directory.

### Install NGINX as a service

1. Open Command Prompt as an Administrator.
2. Go to `C:/nssm/win64/` directory.
3. Type `nssm install nginx`
4. Define the path of the `nginx.exe` file.
5. Click on `Install Service`.
6. Press `Win+R` and type `services.msc`.
7. Look for `nginx` and start the service.
8. Open your browser and type `localhost` to see if it's working correctly.

### Install PHP as a service

1. Open Command Prompt as an Administrator.
2. Go to `C:/nssm/win64/` directory.
3. Type `nssm install php`
4. Define the path of the `php-cgi.exe` file.
5. Add the arguments: `-b 127.0.0.1:9000`
6. Click on `Install Service`.
7. Press `Win+R` and type `services.msc`.
8. Look for `php` and start the service.

### Useful commands while using NSSM


## Conclusion
