Copy of official Alipay SDK

RSA key pair generation
-----------------------
```bash
$ sudo apt-get install openssl

$ openssl
  OpenSSL> genrsa -out rsa_private_key.pem 2048 ##generating  private key
  OpenSSL> pkcs8 -topk8 -inform PEM -in rsa_private_key.pem  -outform PEM -nocrypt ##transform private key into PKCS8 format
  OpenSSL> rsa -in rsa_private_key.pem -pubout -out  rsa_public_key.pem ##Generate public key
  OpenSSL> exit
```

After generate keys, you need delete first and last line (keys must be without "-----BEGIN RSA PRIVATE KEY-----", "-----END RSA PRIVATE KEY----- and whitespaces)
