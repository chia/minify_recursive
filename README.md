minify_recursive
================

Use case #1 (My usecase)
I had a project and wanted to create a git pre hook to recursively minify all files in my project. Hence this small script came into existence. It does 1 thing and does it pretty well for me. Minify all files in a directory and put it in minified directory.

Minify all css or js in a folder recursively using YUIcompressor

Here how it works:
I have throwed this shell script into /usr/local/bin

* minify_recursive css # This will recursively minify all css in your pwd (present directory)
* minify_recursive js
* minify_recursive js /var/www/html/myproject # This will recursively minify all js file in myproject directory.


If your using drupal like me, you can use 
hook_js_alter($javascript)
hook_css_alter($css)
and point your css and js in your custom directory to minified folder created by this script
