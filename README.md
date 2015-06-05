# Plugin-Q2A-Overrides-all-standard-pages
Plugin Name: Overrides all standard Q2A pages
My freelancer job ask for change page or form in page or function like login/register ... of Q2A(question2answer).

I go to search and read manual how to overrides function of Q2A [1]

Plugin overrides (requires Q2A 1.5+) can replace or wrap over 150 functions defined within the Q2A core. Overrides can be very powerful, but they run a risk of incompatibility with future versions of Q2A. If possible, it is recommended to use modules or layers instead. Nonetheless, some things can only be done via overrides, and future versions of Q2A will try not to break them.

Not all functions in Q2A can be overridden. To check a particular function, see whether its definition begins with:

if (qa_to_override(__FUNCTION__)) ...

Functions are overridden by redefining them in a PHP file in your plugin directory, then calling qa_register_plugin_overrides() with the name of that file in qa-plugin.php. Here is a simple example of a PHP file which overrides qa_retrieve_url():

<?php

	function qa_retrieve_url($url)
	{
		// implement some specialized code for retrieving a URL's contents
	}
and our code look like:

qa_register_plugin_overrides('pages-override.php');

Then i search in code of Q2A 1.7 and we found in qa-pages.php [2]:

function qa_page_routing()
/*
Return an array of the default Q2A requests and which qa-page-*.php file implements them
If the key of an element ends in /, it should be used for any request with that key as its prefix
*/

Verry simple we only need change path of there page in our plugin.

We done.

See our code in github Plugin Name: Overrides all standard Q2A pages [3]

Download the plugin : Plugin Overrides all standard Q2A pages [4]

Support: http://gg.edu.vn/plugin-q2a-overrides-all-standard-q2a-pages/[5]

Referent:

[1]http://www.question2answer.org/overrides.php

[2]question2answer-1.7\qa-include\qa-page.php

[3]https://github.com/hscale/Plugin-Q2A-Overrides-all-standard-pages/

[4]https://github.com/hscale/Plugin-Q2A-Overrides-all-standard-pages/releases

[5]http://gg.edu.vn/plugin-q2a-overrides-all-standard-q2a-pages/



