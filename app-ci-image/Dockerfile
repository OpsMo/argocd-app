FROM nginx:alpine

# Default value
ENV ENV=prod

RUN printf '#!/bin/sh\n\
mkdir -p /usr/share/nginx/html/$ENV && \n\
echo \"<!DOCTYPE html><html><head><title>ArgoCD-Nginx Demo</title></head><body><h1>Welcome to the $ENV environment - ArgoCD-Nginx Demo</h1></body></html>\" > /usr/share/nginx/html/$ENV/index.html && \n\
nginx -g \"daemon off;\"' > /entrypoint.sh && \
chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]

# FROM nginx:alpine
# RUN mkdir -p /usr/share/nginx/html/prod

# RUN echo "Version #1 - ArgoCD-Nginx Production Demo" > /usr/share/nginx/html/prod/index.html