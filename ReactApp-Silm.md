Structure:
 /
 |-> /
 
 

 .htaccess :````````
 <IfModule mod_rewrite.c>
  RewriteEngine on

  RewriteCond %{REQUEST_URI} /api
  RewriteRule ^ /serv/public/index.php [QSA]

  RewriteBase / 
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_URI} !/api
  RewriteRule ^ /aic_app/index.html [QSA]

</IfModule>
````
