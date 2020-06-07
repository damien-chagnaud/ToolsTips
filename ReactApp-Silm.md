### Structure:
```Bash
 .
 |-- .htaccess
 |-- /serv/[SLIM 'Public' Path]
 |-- /app/[APP 'Public' Path]
```
 
 
 ### HTACCESS:

````````
 <IfModule mod_rewrite.c>
  RewriteEngine on

  RewriteCond %{REQUEST_URI} /api
  RewriteRule ^ /serv/public/index.php [QSA]

  RewriteBase / 
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_URI} !/api
  RewriteRule ^ /index.html [QSA]

</IfModule>
````````
