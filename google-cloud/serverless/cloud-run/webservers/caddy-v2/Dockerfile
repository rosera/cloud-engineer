FROM caddy:2.7.6-alpine

# Copy static files (optional: only for static sites)
COPY ./public /srv

# Copy the Caddyfile config
COPY Caddyfile /etc/caddy/Caddyfile

# Expose port 8080 (required by Cloud Run)
EXPOSE 8080

# Entrypoint is already `caddy run --config /etc/caddy/Caddyfile` in the base image

