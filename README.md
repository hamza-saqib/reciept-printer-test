Simple Laravel App that uses charlieuki/receiptprinter package to integrate ESC/POS/Thermal Print Driver for PHP.
this project uses Laravel 8, php 8 but you can install your on invirement for this 
## Installation 
run following commands
``` bash
composer install
composer require charlieuki/receiptprinter
```
## Config
if you want to see config file run following command
``` bash
php artisan vendor:publish --tag=receiptprinter.config
```
now you will see file recieptprinter.php in config folder. <br>
Edit the config file located at `config/receiptprinter.php` as follows:

1. Set `connector_type` to:
    - `windows` if you are using Windows as your web server.
    - `cups` if you are using Linux or Mac as your web server.
    - `network` if you are using a network printer.
2. Set `connector_descriptor` to:
    - the printer name if your `connector_type` is either `windows` or `cups`
    - the IP address or Samba URI, e.g: `smb://192.168.0.5/PrinterName` if your `connector_type` is `network`
3. Set `connector_port` to the open port for the printer, only if your `connector_type` is `network`

## Run
when everything config run follwing commad
``` bash
php artisan config:cache
php artisan serve
composer require charlieuki/receiptprinter
```
run follwing link to test a sample print
http://baseURL/print or http://127.0.0.1:8000/print


## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting). 
