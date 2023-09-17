# .htaccess File
This is a basic .htaccess file used to use the rewrite engine of a web server to redirect from one domain link to the new domain location.

This is used by <a href="http://mobogaming.com" />MoBogaming.com</a> to redirect all old links/files to the new domain <a href="https://hails.cc" />Hails.cc</a>

<code>RewriteEngine On
RewriteCond %{HTTP_HOST} ^old-domain.tld$ [OR]
RewriteCond %{HTTP_HOST} ^www.old-domain.tld$
RewriteRule ^(.*)$ http://new-domain.tld/$1 [R=301,L]</code>

This requires ENABLING the Rewrite Engine for your web server.
