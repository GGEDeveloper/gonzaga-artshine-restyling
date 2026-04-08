# PM2 — Setup

## ecosystem.config.js

```javascript
module.exports = {
  apps: [{
    name: 'gonzaga-artshine',
    script: './src/app.js',   // ajustar ao entry point real
    instances: 1,
    autorestart: true,
    watch: false,
    max_memory_restart: '512M',
    env: {
      NODE_ENV: 'production',
      PORT: 3000
    },
    error_file: './logs/pm2-error.log',
    out_file: './logs/pm2-out.log',
    log_date_format: 'YYYY-MM-DD HH:mm:ss'
  }]
};
```

## Comandos Essenciais

```bash
# Iniciar
pm2 start ecosystem.config.js

# Guardar configuração (sobrevive a reboot)
pm2 save

# Auto-start no boot
pm2 startup

# Monitorização
pm2 status
pm2 logs gonzaga-artshine
pm2 monit

# Restart gracioso (zero-downtime)
pm2 reload gonzaga-artshine
```

---

← [Índice](../00-INDEX.md)
