# swaggervel
appointer/swaggervel backup

## Installation
- Execute `composer require kakuilan/swaggervel --dev` within your laravel root directory
- Add `Appointer\Swaggervel\SwaggervelServiceProvider::class` to your providers array in `app/config/app.php` above your route provider, to avoid any catch-all routes
- Run `php artisan vendor:publish --tag=public` to push swagger-ui to your public folder (can be found in public/vendor/swaggervel).
- Optionally run `php artisan vendor:publish --tag=config` to push the swaggervel default config into your application's config directory.
- Optionally run `php artisan vendor:publish --tag=views` to push the swaggervel index view file into `resources/views/vendor/swaggervel`.

## Examples (when using the default configuration)
- www.example.com/docs  <- You may find your automatically generated Swagger .json-File there
- www.example.com/api/docs <- Access to your Swagger UI

## Options
All options are well commented within the swaggervel.php config file.

## How to Use Swagger-php
The actual Swagger spec is beyond the scope of this package. All Swaggervel does is package up swagger-php and swagger-ui in a Laravel-friendly fashion, and tries to make it easy to serve. For info on how to use swagger-php [look here](http://zircote.com/swagger-php/). For good examples of swagger-php in action [look here](https://github.com/zircote/swagger-php/tree/master/Examples).
