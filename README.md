CodeIgniter-PHPMustache
=======================

Integrating PHP Mustache Engine (bobthecow) into Code Igniter


======================


The integration is done via the use of helper loader.

-Navigate to application/helper.  cd application/helper
-Use composer to get all the dependencies by calling composer install
-(Optional) :  look at application/helper/composer.json for the version of php mustache in case you need to download some new stuffs.

application/helper/composer.json
<pre>
{
    "require": {
        "mustache/mustache": "2.1.*"
    }
}
</pre>

By default this code autoload vendor helper
application/config/autoload.php - line 55
<pre>
$autoload['libraries'] = array('vendor');
</pre>



Then rendering the mustache template is as easy as 
application/controller/welcome.php - line 22
<pre>
$m = new Mustache_Engine;
echo $m->render('Hello {{planet}}', array('planet' => 'World!')); // "Hello World!"
</pre>

For more information, please visit


-Code Igniter : http://ellislab.com/codeigniter
-Bobthecow PHP Mustache : https://github.com/bobthecow/mustache.php
