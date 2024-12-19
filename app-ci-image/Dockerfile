FROM nginx:alpine

# Define an environment variable with a default value
ENV ENVIRONMENT=prod

# Create the HTML file dynamically at container runtime
CMD sh -c "echo '<!DOCTYPE html><html><head><title>ArgoCD-Nginx Demo</title></head><body><h1>Welcome to the $ENV environment - ArgoCD-Nginx Demo</h1></body></html>' > /usr/share/nginx/html/index.html && nginx -g 'daemon off;'"

# FROM nginx:alpine
# RUN mkdir -p /usr/share/nginx/html/prod

# RUN echo "Version #1 - ArgoCD-Nginx Production Demo" > /usr/share/nginx/html/prod/index.html