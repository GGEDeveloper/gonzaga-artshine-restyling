# Área de Cliente — Passport.js

## Fluxo de Autenticação

```
Registo → Email confirmação (Resend) → Login → Dashboard cliente
```

## Passport.js Local Strategy

```javascript
passport.use(new LocalStrategy(
  { usernameField: 'email' },
  async (email, password, done) => {
    const user = await db.query('SELECT * FROM customers WHERE email = ?', [email]);
    if (!user) return done(null, false, { message: 'Email não encontrado' });
    const valid = await bcrypt.compare(password, user.password_hash);
    if (!valid) return done(null, false, { message: 'Password incorrecta' });
    return done(null, user);
  }
));
```

## Rotas Necessárias

| Rota | Método | Descrição |
|---|---|---|
| `/cliente/registo` | GET/POST | Formulário de registo |
| `/cliente/login` | GET/POST | Formulário de login |
| `/cliente/logout` | POST | Terminar sessão |
| `/cliente/dashboard` | GET | Área privada |
| `/cliente/encomendas` | GET | Histórico de encomendas |

## Middleware de Protecção

```javascript
const requireAuth = (req, res, next) => {
  if (req.isAuthenticated()) return next();
  res.redirect('/cliente/login');
};
```

---

← [Índice](../00-INDEX.md)
