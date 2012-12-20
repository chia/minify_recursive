minify_recursive
================

<p>Minify_recursive is a shell script that uses YUICOMPRESSOR to minify all css and js files recursively in a directory.</p>

<p>
<h3>Requirements</h3>
The only requirement is to install YUICOMPRESSOR https://github.com/yui/yuicompressor
</p>

<p>
<h3>Installation</h3>
<ol>
<li>Configure path to YUICOMPRESSOR_PATH by editing the minify_recursive.sh file</li>
<li>Create a soft link of minify_recursive script in /usr/local/bin <code>ln -s minify_recursive.sh /usr/local/bin/minify_recursive</code></li>
<li>Give execute permission to minify_recursive script <code>chmod +x minify_recursive.sh</code></li>
</ol>
</p>

<p>
<h3>Use case #1 (My usecase)</h3>
I had a project and wanted to create a git pre hook to recursively minify all files in my project. Hence this small script came into existence. It does 1 thing and does it pretty well for me. Minify all files in a directory and put it in minified directory.
</p>

<p>
<h3>Here how it works</h3>
I have throwed this shell script into /usr/local/bin
<ul>
  <li><code>minify_recursive css # This will recursively minify all css in your pwd (present directory)</code></li>
  <li><code>minify_recursive js # Recursively minify all js file in pwd</code></li>
  <li><code>minify_recursive js /var/www/html/myproject # This will recursively minify all js file in myproject directory.</code></li>
</ul>
</p>

<p>If your using drupal like me, you can use<br />
<ul><li>hook_js_alter($javascript)</li>
<li>hook_css_alter($css)</li>
</ul>
and point your css and js in your custom directory to minified folder created by this script<br />
