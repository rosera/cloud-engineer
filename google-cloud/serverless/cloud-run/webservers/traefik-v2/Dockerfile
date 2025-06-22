FROM alpine:3.20

# Install traefik and caddy
RUN apk add --no-cache traefik caddy

# Copy configs and static files
COPY traefik.yml /etc/traefik/traefik.yml
COPY dynamic.yml /etc/traefik/dynamic.yml
COPY public/ /public/

# Cloud Run uses port 8080
EXPOSE 8080

# Run static server (on 8000) and Traefik (on 8080)
CMD sh -c "caddy file-server --listen :8000 --root /public & traefik"

