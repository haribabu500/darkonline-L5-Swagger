# darkonline-L5-Swagger
multiple ui generation in swager

## Installation
php artisan vendor:publish --provider "L5Swagger\L5SwaggerServiceProvider"


## To get started, first publish L5-Swagger's config and view files into your own project:
php artisan vendor:publish --provider "L5Swagger\L5SwaggerServiceProvider"

##publish config if not available 
php artisan l5-swagger:publish-config
###Mobile and web documentation seperateion in config/l5-swagger.php



## Edited in files config/l5-swagger.php 
for web added default as it is and for mobile added mobile
       
         'api' => [
                /*
                |--------------------------------------------------------------------------
                | Edit to set the this group's title, will override global title
                |--------------------------------------------------------------------------
                */
               'separated_doc' => true
                ],
        'default' => [
            'api' => [
                /*
                |--------------------------------------------------------------------------
                | Edit to set the this group's title, will override global title
                |--------------------------------------------------------------------------
                */
                'title' => 'Laravel Web API Documentation UI',
            ],
            'routes' => [
                /*
                |--------------------------------------------------------------------------
                | Route for accessing this group api documentation interface
                |--------------------------------------------------------------------------
                */
                'api' => 'api/documentation',
            ],
            'paths' => [
                /*
                |--------------------------------------------------------------------------
                | Absolute path to location where parsed swagger annotations will be stored
                |--------------------------------------------------------------------------
                */
                'docs' => storage_path('api-docs'),
                /*
                |--------------------------------------------------------------------------
                | File name of the generated json documentation file
                |--------------------------------------------------------------------------
                */
                'docs_json' => 'default-api-docs.json',
                /*
                |--------------------------------------------------------------------------
                | Absolute path to directory containing the swagger annotations are stored.
                |--------------------------------------------------------------------------
                */
                'annotations' => base_path('app/'),
            ],
        ],
        'mobile' => [
            'api' => [
                /*
                |--------------------------------------------------------------------------
                | Edit to set the this group's title, will override global title
                |--------------------------------------------------------------------------
                */
                'title' => 'Laravel Mobile API Documentation UI',
            ],
            'routes' => [
                /*
                |--------------------------------------------------------------------------
                | Route for accessing this group api documentation interface
                |--------------------------------------------------------------------------
                */
                'api' => 'mobapi/documentation',
            ],
            'paths' => [
                /*
                |--------------------------------------------------------------------------
                | Absolute path to location where parsed swagger annotations will be stored
                |--------------------------------------------------------------------------
                */
                'docs' => storage_path('api-docs'),
                /*
                |--------------------------------------------------------------------------
                | File name of the generated json documentation file
                |--------------------------------------------------------------------------
                */
                'docs_json' => 'mobile-api-docs.json',
                /*
                |--------------------------------------------------------------------------
                | Absolute path to directory containing the swagger annotations are stored.
                |--------------------------------------------------------------------------
                */
                'annotations' => base_path('app/'),
            ],
        ],



## Generate the doucmentation
php artisan l5-swagger:generate

copy the vendor/darkonline
