FROM nginx:1.25-alpine

# Remove the default config and replace it with our own
RUN rm /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/nginx.conf

# Copy static files
COPY public/ /usr/share/nginx/html/

# Expose port 8080 for Cloud Run
EXPOSE 8080

# NGINX already uses CMD ["nginx", "-g", "daemon off;"]

