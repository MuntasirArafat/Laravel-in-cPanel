# Laravel-in-cPanel
How do I upload a laravel project on cPanel shared hosting?


You don't need to make changes to the structure of Laravel. Just copy below htaccess code and paste in <b>.htaccess</b> file at the root of your laravel project.
```
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteBase /
    RewriteRule ^$ public/index.php [L]
    RewriteRule ^((?!public/).*)$ public/$1 [L,NC]
</IfModule>```
