# Ficheiros a Eliminar — Legado dominios.pt

> Ficheiros criados durante a tentativa de alojamento no dominios.pt / CloudLinux. Não têm utilidade no VPS Ubuntu.

## Lista de Ficheiros a Remover

```
COMANDOS_*DOMINIOS*.md      # Todos os ficheiros com este padrão
CLOUDLINUX_*.md             # Todos os ficheiros com este padrão
.cpanel.yml                 # Ficheiro de config cPanel
```

## Procedimento

```bash
# Listar antes de apagar
ls COMANDOS_*DOMINIOS*.md CLOUDLINUX_*.md .cpanel.yml 2>/dev/null

# Remover e commitar
git rm COMANDOS_*DOMINIOS*.md CLOUDLINUX_*.md .cpanel.yml
git commit -m "chore: remover ficheiros legados dominios.pt / cPanel"
git push
```

## Verificação

Após limpeza, confirmar que o repo gartnshine não contém referências a:
- `CLOUDLINUX`
- `cPanel`
- `dominios.pt`
- Paths do tipo `/home/username/public_html`

---

← [Índice](../00-INDEX.md)
