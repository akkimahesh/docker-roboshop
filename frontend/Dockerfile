FROM nginx:1.24.0
RUN rm -f /usr/share/nginx/html/index.html
RUN rm -f /etc/nginx/nginx.conf
RUN rm -f /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/nginx.conf
#here actually copying only file inside the static directory, not copied the directory
COPY static /usr/share/nginx/html/