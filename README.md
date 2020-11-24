# Como-ver-los-hash-de-integridad-de-un-archivo-SHELL

```
cat FILENAME.js | openssl dgst -sha384 -binary | openssl base64 -A
```

O

```
shasum -b -a 384 FILENAME.js | awk '{ print $1 }' | xxd -r -p | base64
```

Fuente: https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity
