# FontAwesome Bundle for Symfony2

## Current Version

Font Awesome v3.2.1

## Installation

### Add bundle to your composer.json file

``` js
// composer.json

{
    "require": {
		// ...
        "bmatzner/fontawesome-bundle": "*"
    }
}
```

### Add bundle to your application kernel

``` php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Bmatzner\FontAwesomeBundle\BmatznerFontAwesomeBundle(),
        // ...
    );
}
```

### Download the bundle using Composer

``` bash
$ php composer.phar update bmatzner/fontawesome-bundle
```

### Install assets

Given your server's public directory is named "web", install the public vendor resources

``` bash
$ php app/console assets:install web
```

Optionally, use the --symlink attribute to create links rather than copies of the resources 

``` bash
$ php app/console assets:install --symlink web
```

## Usage

Refer to the desired files in your HTML template, e.g.

``` html
<link rel="stylesheet" type="text/css" href="{{ asset('bundles/bmatznerfontawesome/css/font-awesome.min.css') }}" />
```

For IE7 support, add the following conditional comment to the head of your HTML.
``` html
<!--[if IE 7]>
  <link rel="stylesheet" href="{{ asset('bundles/bmatznerfontawesome/css/font-awesome-ie7.min.css') }}">
<![endif]-->
```

## Notes

The relative path of the fonts has been changed to an absolute path in the web/bundles folder, allowing for CSS rewriting.

# Licenses

Refer to the source code of the included files for license information

# References

1. http://fortawesome.github.com/Font-Awesome/
2. http://symfony.com
