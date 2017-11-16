RSA key pair generation
-----------------------
```bash
$ sudo apt-get install openssl

$ openssl
  OpenSSL> genrsa -out rsa_private_key.pem 1024 ##generating  private key
  OpenSSL> pkcs8 -topk8 -inform PEM -in rsa_private_key.pem  -outform PEM -nocrypt ##transform private key into PKCS8 format
  OpenSSL> rsa -in rsa_private_key.pem -pubout -out  rsa_public_key.pem ##Generate public key
  OpenSSL> exit
```

