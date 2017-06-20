Cache Helper
===

Wrapper for 10up's [Async Transients](https://github.com/10up/Async-Transients) library.

Run composer install before running

Sample usage:

```
$function = function ($foo){
	sleep( 2 );
	return $foo . time();

};

$async = new Cache( 'cachekey123', 'bar', 20, $function, array('prefix') );

$before = microtime(true);
$val = $async->get();
var_dump($val);
echo '<BR>';
echo microtime(true)-$before;
```