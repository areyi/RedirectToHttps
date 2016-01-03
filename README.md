# RedirectToHttps
Middleware for Laravel 5, to redirect a HTTP to HTTPS, and a non-WWW to WWW

### Features
* Redirect HTTP to HTTPS
* Redirect non-WWW to WWW
* Compatible with Cloudflare

### How to Use?
* Copy Secure.php to /home/nexus/public_html/app/Http/Middleware/
* Add this to /home/nexus/public_html/app/Http/Kernel.php under the $middleware array: 

```php
protected $middleware = [
    ...
    \App\Http\Middleware\Secure::class,
];

```
* Edit YOURSITEHERE to your own site, e.g: www.studionexus.co
```php
...
$request->headers->set('host', 'www.studionexus.co');
...
```
