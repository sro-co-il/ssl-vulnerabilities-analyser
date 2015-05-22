# Disable SSL v2 in APACHE 2 #

  * Add this line (or edit if it's exists) to the httpd.conf or ssl.conf file:
```
SSLProtocol -ALL +SSLv3 +TLSv1
```
  * Restart APACHE
```
/etc/init.d/apache2 restart
```