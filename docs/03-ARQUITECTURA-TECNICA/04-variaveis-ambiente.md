# Variáveis de Ambiente — Template

> ⚠️ **Nunca commitar o `.env` real.** Este ficheiro é apenas o template de referência.

## .env.example

```env
# ── Aplicação ──────────────────────────────
NODE_ENV=production
PORT=3000
APP_URL=https://gonzagaartshine.com
SESSION_SECRET=change_me_to_a_random_string_min_32_chars

# ── Base de Dados ───────────────────────────
DB_HOST=localhost
DB_PORT=3306
DB_NAME=gonzaga_artshine
DB_USER=db_user
DB_PASSWORD=db_password

# ── Stripe ──────────────────────────────────
STRIPE_PUBLIC_KEY=pk_live_...
STRIPE_SECRET_KEY=sk_live_...
STRIPE_WEBHOOK_SECRET=whsec_...

# ── Resend (email) ───────────────────────────
RESEND_API_KEY=re_...
EMAIL_FROM=noreply@gonzagaartshine.com

# ── Admin ────────────────────────────────────
ADMIN_EMAIL=admin@gonzagaartshine.com
```

## Notas

- `SESSION_SECRET` deve ser gerado com `openssl rand -hex 32`
- Stripe: usar chaves `test_` em desenvolvimento, `live_` em produção
- O `.env` real vive apenas no servidor VPS e nunca no Git

---

← [Índice](../00-INDEX.md)
