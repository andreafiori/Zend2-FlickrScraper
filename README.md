[![Build Status](https://travis-ci.org/andreafiori/zend2-flickr-web-scraper.svg?branch=master)](https://travis-ci.org/andreafiori/zend2-flickr-web-scraper)

Zend2 Flickr Scraper
=======================

Introduction
------------

Zend framework 2 application to scrape a Flickr page and store images properties on a database.
I've used Doctrine 2 ORM to map entities and handle data from a MySQL database.
The Frontend get the result of a GET call made with AngularJS using $http. 
The call will return a JSON response and if there will be a result, the HTML table will be populated.

Installation Using Composer
----------------------------

Clone the repository and manually invoke `composer` using the shipped
`composer.phar`:

    cd /
	git clone https://github.com/andreafiori/Zend2-FlickrScraper.git
    mv Zend2-FlickrScraper zf2-flickrscraper
    cd zf2-flickrscraper
    php composer.phar self-update
    php composer.phar install

(The `self-update` directive is to ensure you have an up-to-date `composer.phar`
available.)

NOTE: the basic URL on my localhost is actually http://localhost/zf2-flickrscraper/public/
I've not set a Virtual Host on my XAMPP.

HTACCESS
----------------

You can create your virtual host on your web server. I've renamed the .htaccess file on public dir 
to use it on my Windows 7, so rename it or the URL rewriting will not work.

FLICKR API Key
----------------

I've stored the API Key on the main Application module. Replace the key on the module.config.php file.

RESTful CALL on Frontend 
----------------

You can edit the link that gives the JSON response on module\Application\module.config.php

MySQL Database Setup
----------------

You have to change parameter on ./config/doctrine.global.php
and ./config/doctrine.local.php

The database dump is on the sql directory.

### PHP CLI URLs

View images:
	http://localhost/zf2-flickrscraper/public/flickr-backend

Scrape the page and store images on db:
	http://localhost/zf2-flickrscraper/public/flickr-scraper

Screenshot
----------------

Frontend screenshot:

![Alt text](/img/screenshot.jpg)