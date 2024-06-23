### Getting started
- Install Docker.
- Docker Compose (Container Optimized: curl -s https://gist.githubusercontent.com/kurokobo/25e41503eb060fee8d8bec1dd859eff3/raw/0d7cd29472f0eaa26ce424071456ad84b24fb318/installer.sh | bash)
- Clone/Copy project (wget https://github.com/superrandres/nginx-certbot/archive/master.tar.gz).
- Descompress file project (tar -xvzf master.tar.gz).
- cd nginx-certbot-main/
- Create / Edit a file for port 80 (http) only for generate certs (test.relyjs.com.conf.ssl).
- Create / Edit a file for port 80 and 443, for use new certs (test.relyjs.com.http.conf).
- docker compose run --rm web certbot certonly --nginx
- docker compose run --rm web certbot renew --dry-run
