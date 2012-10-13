ShellWrap
==================

DISCLAIMER: This isn't ready to use yet.

What is it?
------------------

It's a way to use powerful underlying Unix tools while feeling slightly less dirty.

Features (TBC)
------------------

* Exceptions are thrown if the executable returns an error.
* Paths to binaries are automatically resolved
* Easy logging of command line options

Examples
------------------

// Get a list of files in the current directory, and list them biggest first

```php
<?php 
require 'ShellWrap.php';
use \MrRio\ShellWrap as sh;

echo sh:ls('*');

echo sh::sort(sh::du(sh::glob("*"), "-sb"), "-rn");

echo sh::curl('http://snapshotmedia.co.uk', array(
	'o' => 'page.html',
	'silent' => true
));
?>
```

Acknowledgements
--------------------

Inspired by the Python project [sh by Andrew Moffat](http://pypi.python.org/pypi/sh)