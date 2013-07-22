Snaphax: a PHP library to use APIs
==============================================

This library allows you to communicate with an app's servers using their
undocumented HTTP API. It has been tested with SnapChat and works perfectly (but breaks their TOS). It's possible that it works with other APIs too.

How to use
----------

Pretty simple:

```
	require_once('snaphax/snaphax.php');

	$opts = array();
	$opts['url'] = 'https://example.com' // We totally don't suggest you put "https://feelinsonice.appspot.com" (SnapChat's API endpoint) because that'd break their TOS
	$opts['username'] = 'username';
	$opts['password'] = 'password';
	$opts['debug'] = 1; 

	$s = new Snaphax($opts);
	$result = $s->login();
	var_dump($result);
```

Limitations
-----------

Only login (with list of new media) and fetching of image/video snaps is
implemented.  This is obviously a huge failing which I am to correct when I
have more time.

License
-------

MIT

Credits
-------

Made by Thomas Lackner <[@tlack](http://twitter.com/tlack)> with a lot of help
from [@adamcaudill](http://twitter.com/adamcaudill).  And of course none of
this would be possible without the inventiveness of the
[Snapchat](http://snapchat.com) team

