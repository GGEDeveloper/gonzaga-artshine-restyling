# Stack Técnica

## Servidor de Aplicação

| Camada | Tecnologia | Versão |
|---|---|---|
| Runtime | Node.js | 20 LTS |
| Framework | Express | 4.x |
| Templates | EJS | latest |
| Process Manager | PM2 | latest |

## Base de Dados

| Componente | Tecnologia |
|---|---|
| SGBD | MySQL 8 |
| ORM/Query | mysql2 (driver directo) |

## Servidor / Infraestrutura

| Componente | Tecnologia |
|---|---|
| OS | Ubuntu LTS (VPS) |
| Web server / Proxy | Nginx |
| SSL | Certbot (Let's Encrypt) |
| CI/CD | GitHub Actions → SSH deploy |

## Serviços Externos (únicos custos aceites)

| Serviço | Uso | Custo |
|---|---|---|
| Stripe | Pagamentos | % por transacção |
| Resend.com | Emails transaccionais | Grátis até 3000/mês |
| Google Fonts | Tipografia | Gratuito |

## Frontend (sem framework JS)

| Componente | Tecnologia |
|---|---|
| Carousel | Swiper.js (gratuito) |
| Auth clientes | Passport.js (local strategy) |
| Sessões | express-session + MySQL store |

## Regras de Stack

- **Nunca** sugerir WordPress, Shopify ou SaaS
- O servidor é nosso — free-first
- Sem React, Vue ou frameworks JS pesados no frontend

---

← [Índice](../00-INDEX.md)
