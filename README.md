Cache Helper
===

Wrapper for 10up's [Async Transients](https://github.com/10up/Async-Transients) library.

*NOTE*: run composer install before running, put this in your plugins directory and enable it

Rudimentary sample usage:

```
$function = function ($value){
	sleep( 2 );
	// long running API call
	return $value . time();

};

$async = new Cache( 'mycachekey123', 'bar', 20, $function, array('prefix') );

$before = microtime(true);
$val = $async->get();
var_dump($val);
echo '<BR>';
echo microtime(true)-$before;
```