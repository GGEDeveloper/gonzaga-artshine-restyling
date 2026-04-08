# SSL — Certbot / Let's Encrypt

## Instalação

```bash
apt install certbot python3-certbot-nginx
```

## Obter Certificado

```bash
certbot --nginx -d gonzagaartshine.com -d www.gonzagaartshine.com
```

## Renovação Automática

O Certbot cria automaticamente um timer systemd. Verificar:

```bash
systemctl status certbot.timer

# Testar renovação (dry-run)
certbot renew --dry-run
```

## Verificação

```bash
# Verificar certificado
certbot certificates

# Data de expiração
openssl s_client -connect gonzagaartshine.com:443 2>/dev/null | openssl x509 -noout -dates
```

---

← [Índice](../00-INDEX.md)
