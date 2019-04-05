# darkonline-L5-Swagger
multiple ui generation in swager

Installation
php artisan vendor:publish --provider "L5Swagger\L5SwaggerServiceProvider"


To get started, first publish L5-Swagger's config and view files into your own project:
php artisan vendor:publish --provider "L5Swagger\L5SwaggerServiceProvider"

publish config if not available 
php artisan l5-swagger:publish-config

Edit the files config/l5-swagger.php 

Add the vendor files

Generate the doucmentation
l5-swagger:generate
