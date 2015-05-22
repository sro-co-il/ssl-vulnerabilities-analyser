# Disable SSLv2 in IIS 6 #

  * Add\Modify the following keys in the Registry:
```
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\PCT 1.0\Server]
“Enabled”=dword:00000000
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\SSL 2.0\Server]
“Enabled”=dword:00000000
```
  * Restart IIS (If needed, also restart using OpenSSL)
```
iisreset /restart
```