# Nginx — Configuração

## Virtual Host

```nginx
# /etc/nginx/sites-available/gonzagaartshine

server {
    listen 80;
    server_name gonzagaartshine.com www.gonzagaartshine.com;
    return 301 https://$server_name$request_uri;
}

server {
    listen 443 ssl;
    server_name gonzagaartshine.com www.gonzagaartshine.com;

    ssl_certificate /etc/letsencrypt/live/gonzagaartshine.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/gonzagaartshine.com/privkey.pem;

    # Gzip
    gzip on;
    gzip_types text/plain text/css application/json application/javascript;

    # Static files servidos directamente pelo Nginx
    location /public/ {
        alias /var/www/gonzagaartshine/public/;
        expires 30d;
        add_header Cache-Control "public, immutable";
    }

    # Uploads / media
    location /uploads/ {
        alias /var/www/gonzagaartshine/uploads/;
        expires 7d;
    }

    # Proxy para Node.js
    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_cache_bypass $http_upgrade;
    }
}
```

## Activar e Testar

```bash
ln -s /etc/nginx/sites-available/gonzagaartshine /etc/nginx/sites-enabled/
nginx -t
systemctl reload nginx
```

---

← [Índice](../00-INDEX.md)
