# CI/CD — GitHub Actions

## Workflow de Deploy

```yaml
# .github/workflows/deploy.yml

name: Deploy para VPS

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Deploy via SSH
        uses: appleboy/ssh-action@v1
        with:
          host: ${{ secrets.VPS_HOST }}
          username: ${{ secrets.VPS_USER }}
          key: ${{ secrets.VPS_SSH_KEY }}
          script: |
            cd /var/www/gonzagaartshine
            git pull origin main
            npm install --production
            pm2 reload gonzaga-artshine
```

## GitHub Secrets Necessários

| Secret | Valor |
|---|---|
| `VPS_HOST` | IP ou domínio do VPS |
| `VPS_USER` | Utilizador SSH (ex: `deploy`) |
| `VPS_SSH_KEY` | Chave privada SSH (conteúdo do `id_rsa`) |

## Gerar SSH Key para Deploy

```bash
# No VPS
ssh-keygen -t ed25519 -C "github-deploy" -f ~/.ssh/github_deploy
cat ~/.ssh/github_deploy.pub >> ~/.ssh/authorized_keys

# Copiar a chave privada para o GitHub Secret
cat ~/.ssh/github_deploy
```

---

← [Índice](../00-INDEX.md)
