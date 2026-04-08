# Estrutura dos Repositórios

## Repositório de Produção

**[GGEDeveloper/gartnshine](https://github.com/GGEDeveloper/gartnshine)**

> ⚠️ **Tocar com cuidado** — é o site live.

- Deploy automático via GitHub Actions
- Nunca fazer force push
- Qualquer alteração deve passar primeiro pelo repo de restyling

## Repositório de Trabalho

**[GGEDeveloper/gonzaga-artshine-restyling](https://github.com/GGEDeveloper/gonzaga-artshine-restyling)**

- Repo activo de desenvolvimento e planeamento
- Toda a documentação e novos ficheiros aqui primeiro
- Quando validado → merge/port para gartnshine

## Fluxo de Trabalho

```
restyling (dev) → validação → gartnshine (prod)
      ↑                              ↓
   GitHub                      Ubuntu VPS
   Actions                   (via SSH deploy)
```

## Convenção de Branches

| Branch | Uso |
|---|---|
| `main` | Estável, documentação e código validado |
| `feature/*` | Novas funcionalidades |
| `fix/*` | Correcções |
| `design/*` | Experiências visuais / protótipos CSS |

---

← [Índice](../00-INDEX.md)
