# https on gitpod

https://nodejs.org/en/knowledge/HTTP/servers/how-to-create-a-HTTPS-server/

```sh
openssl genrsa -out key.pem
openssl req -new -key key.pem -out csr.pem
openssl x509 -req -days 9999 -in csr.pem -signkey key.pem -out cert.pem
rm csr.pem
```

`curl -k https://localhost:9761`

`gp url 9761` not working
