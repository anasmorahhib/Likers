![likers logo](http://www.morahhib.com/img/likers-logo.jpg)
# Likers (arabic version)
*This script is in Arabic, and for now there is only the RTL version.*  
This script is for managing advertising campaigns for social networks. to see the content of this script watch this [video](https://www.youtube.com/watch?v=ZAOk2-0pDRs&index=3&list=PLQJjtF_jDk3vImSt72cwwh5uV0o7vyx2m).  
سكريبت لإدارة الحملات الإعلانية للمواقع الإجتماعية 
### The technologies used:
> PHP 5.6  
CakePHP 2.2.x  
Twitter bootstrap 2.3  
Paypal API  
Instagram API  
### The necessary modifications before host the code:
* Import the database `db-likers.sql`. 
* Configure your database file:  
`app\Config\database.php` 
```php
	public $default = array(
		'datasource' => 'Database/Mysql',
		'persistent' => false,
		'host' => 'localhost',
		'login' => '',
		'password' => '',
		'database' => 'likers',
		'prefix' => '',
		'encoding' => 'utf8',
	);
```
* Configure the mail client settings:
you can use your webmail as you can use GMAIL.  
` app\Config\email.php`
```php
    public $gmail = array(
		'host' => 'mail.exemple.com',
		'port' => 587,
		'username' => '',
		'password' => '',
		'transport' => 'Smtp',
		'from' => ''
    );
```

### The necessary modifications after hosting the code:
* Setup your PayPal API
 With an admin account, go to url `www.yourdomain.com/users/profile_admin`, and change the paypal information requested, or directly from `\app\Lib\Paypale.php`.
![config paypal](http://www.morahhib.com/img/likers-paypal.png)
* Setup your Instagram API
Directly from `\app\Lib\Instagram.php` change `$client_id` to your client id.
```php
class Instagram{
    public $url ='http://';
    public $user_name='';
    public $img='';
    public $followd_by;
    private $client_id="your-client-id";
```
Made by [Anas MORAHHIB](http://www.morahhib.com) and [Mouad MAHFOUD](https://github.com/mouad-mahfoud)

Last updated: December 2015
