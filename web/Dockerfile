FROM nginx:stable

RUN apt update -yq && apt upgrade -yq && apt install -yq python3 python3-venv libaugeas0
RUN python3 -m venv /opt/certbot/ && /opt/certbot/bin/pip install --upgrade pip
RUN /opt/certbot/bin/pip install certbot certbot-nginx && ln -s /opt/certbot/bin/certbot /usr/bin/certbot

VOLUME [ "/etc/letsencrypt" ]
VOLUME [ "/etc/nginx/conf.d" ]

EXPOSE 80
EXPOSE 443