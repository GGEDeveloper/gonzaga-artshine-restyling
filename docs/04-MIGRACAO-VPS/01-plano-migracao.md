# Plano de Migração — Ubuntu VPS

## Pré-Requisitos

- [ ] Acesso SSH ao VPS com sudo
- [ ] Domínio apontado para o IP do VPS
- [ ] Backup completo do gartnshine (código + DB)
- [ ] Credenciais: MySQL root, Stripe, Resend

## Checklist de Migração

### 1. Preparação do Servidor
- [ ] Ubuntu LTS actualizado (`apt update && apt upgrade`)
- [ ] Node.js 20 LTS instalado (via NodeSource)
- [ ] PM2 instalado globalmente
- [ ] MySQL 8 instalado e seguro (`mysql_secure_installation`)
- [ ] Nginx instalado
- [ ] Certbot instalado

### 2. Base de Dados
- [ ] Criar DB e utilizador MySQL dedicado
- [ ] Importar dump do gartnshine
- [ ] Verificar integridade dos dados

### 3. Aplicação
- [ ] Clone do repo gartnshine no servidor
- [ ] `npm install --production`
- [ ] `.env` configurado no servidor
- [ ] PM2 ecosystem.config.js criado
- [ ] `pm2 start` e `pm2 save`
- [ ] `pm2 startup` para auto-restart

### 4. Nginx + SSL
- [ ] Virtual host configurado
- [ ] Reverse proxy para Node (porta 3000)
- [ ] Certbot: `certbot --nginx -d gonzagaartshine.com`
- [ ] Renovação automática testada

### 5. CI/CD
- [ ] SSH key gerada no servidor
- [ ] GitHub Secret `VPS_SSH_KEY` adicionado
- [ ] GitHub Actions workflow configurado
- [ ] Deploy de teste executado com sucesso

### 6. Validação Final
- [ ] Site acessível via HTTPS
- [ ] Admin panel funcional
- [ ] Catálogo a carregar
- [ ] Formulários a funcionar

---

← [Índice](../00-INDEX.md)
