FROM nginx:alpine
# Use a volume is more efficient and speed that filesystem
VOLUME /tmp
RUN rm -rf /usr/share/nginx/html/*
COPY nginx.conf /etc/nginx/nginx.conf
COPY billingApp_prep /usr/share/nginx/html/billingApp_prep
COPY billingApp_prod /usr/share/nginx/html/billingApp_prod
# Expose app and 80 for nginx app
EXPOSE 80 81
CMD [ "nginx", "-g", "daemon off;" ]