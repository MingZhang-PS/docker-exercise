FROM nginx:alpine
COPY resources/* /usr/share/nginx/html/
COPY ssl.conf /etc/nginx/conf.d/ssl.conf
COPY cert/* /etc/nginx/ssl/
EXPOSE 443 80

