FROM nginx:alpine

LABEL maintainer="<sapunidze@ya.ru>"

ENV NGINX_USER=1001
ENV NGINX_PORT=8000

COPY nginx.conf /etc/nginx/nginx.conf

RUN touch /var/run/nginx.pid && \
  chown -R ${NGINX_PORT} /var/run/nginx.pid && \
  chown -R ${NGINX_PORT} /var/cache/nginx

EXPOSE ${NGINX_PORT}

USER ${NGINX_USER}