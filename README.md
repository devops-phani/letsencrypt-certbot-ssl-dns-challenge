# letsencrypt-certbot-ssl-dns-challenge

Ref link:

https://www.bennadel.com/blog/3420-obtaining-a-wildcard-ssl-certificate-from-letsencrypt-using-the-dns-challenge.htm

```
docker run -it --rm --name letsencrypt \
	-v "/etc/letsencrypt:/etc/letsencrypt" \
	-v "/var/lib/letsencrypt:/var/lib/letsencrypt" \
	quay.io/letsencrypt/letsencrypt:latest \
		certonly \
		-d dailyprime.me \
		-d *.dailyprime.me \
		--manual \
		--preferred-challenges dns \
		--server https://acme-v02.api.letsencrypt.org/directory
 ```
