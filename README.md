# Redirect Old Links to New Domain
This is a basic .htaccess file which uses the rewrite engine of a webserver to redirect from an old Domain to the New domain keeping the original link intact.

This is used by <a href="http://mobogaming.com" />MoBogaming.com</a> to redirect all old links/files to the new domain <a href="https://hails.cc" />Hails.cc</a>

## Code
```
RewriteEngine On
RewriteCond %{HTTP_HOST} ^old-domain.tld$ [OR]
RewriteCond %{HTTP_HOST} ^www.old-domain.tld$
RewriteRule ^(.*)$ http://new-domain.tld/$1 [R=301,L]
```

## Usage
- Copy the code from above
- Create a file named `.htaccess` on your web server and paste the code
- Edit the Domains and TLD to match your use case
- Enjoy~

## Requirements
This requires ENABLING the Rewrite Engine for your web server.
