# Hardening APACHE SSL #

**Disable SSLv2**
  * Add this line (or edit if it's exists) to the httpd.conf or ssl.conf file:
```
SSLProtocol -ALL +SSLv3 +TLSv1
```

**Disable Null Cipher and Weak Ciphers**
  * Add this line (or edit if it's exists) to the httpd.conf or ssl.conf file:
```
SSLCipherSuite ALL:!aNULL:!ADH:!eNULL:!LOW:!EXP:RC4+RSA:+HIGH:+MEDIUM
```

**Restart APACHE**
  * Run the command:
```
/etc/init.d/apache2 restart
```