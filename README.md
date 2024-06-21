### Getting started
- Clone project.
- Install Docker.
- Create a file for port 80 (http) only for generate certs (test.relyjs.com.conf.ssl).
- Create a file for port 80 and 443, for use new certs (test.relyjs.com.http.conf).
- docker compose run --rm web certbot certonly --nginx
- docker compose run --rm web certbot renew --dry-run
