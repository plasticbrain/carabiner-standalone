Carabiner Standalone
====================

[Carabiner](https://github.com/tonydewan/Carabiner) is a great, lightweight asset manager for CodeIgniter. I like and use it so much that I decided to port it to a standalone version, so it can be used outside of CodeIgniter projects.

Basic Usage
-----------

1. Clone this repository `$ git clone https://github.com/plasticbrain/carabiner-standalone carabiner`
2. Open config.php and set `script_dir`, `style_dir`, `cache_dir`, and `base_uri` in 
3. Make sure your cache directory (defined in config.php) exists and is writable (chmod to 775 or 777)
4. Instantiate Carabiner and load your assets

```php
//------------------------------------------------------------------------------
// Require and instantiate Carabiner
//------------------------------------------------------------------------------
require('carabiner/carabiner.php');
$carabiner = new $Carabiner();


//------------------------------------------------------------------------------
// CSS Stylesheets
//------------------------------------------------------------------------------

// Define our stylesheets
$css_files = array(
	array('stylesheet1.css'),
	array('stylesheet2.css'),
	array('stylesheet3.css')
);

// Load the stylesheets into Carabiner
$carabiner->css($css_files);

// Render the  stylesheets
$carabiner->display('css');


//------------------------------------------------------------------------------
// Javascripts
//------------------------------------------------------------------------------

// Define our Javascript files
// Note that you can use URLs as well
$css_files = array(
	array( '//ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.js'),
	array('file1.js'),
	array('file2.js'),
	array('file3.js')
);

// Load our JS files into Carabiner
$carabiner->js($js_files);

// Render our JS
$carabiner->display('css');
```


License
-------
Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
