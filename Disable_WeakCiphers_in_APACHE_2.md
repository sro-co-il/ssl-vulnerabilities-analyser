# Disable WeakCiphers in APACHE 2 #

  * Add this line (or edit if it's exists) to the httpd.conf or ssl.conf file:
```
SSLCipherSuite ALL:!aNULL:!ADH:!eNULL:!LOW:!EXP:RC4+RSA:+HIGH:+MEDIUM
```
  * Restart APACHE
```
/etc/init.d/apache2 restart
```