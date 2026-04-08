# Paleta de Cores — Dark Nature

> ⚠️ **IMUTÁVEL** — Nunca alterar sem aprovação explícita de Hugo Gonzaga.

## Tokens

| Token | Nome | Hex | Uso |
|---|---|---|---|
| `--color-base` | Preto Base | `#0B0D0C` | Fundo principal |
| `--color-gold` | Dourado Antigo | `#B08D57` | Acentos, CTAs, títulos decorativos |
| `--color-silver` | Prata Fosca | `#C7CACE` | Texto corpo, elementos UI |
| `--color-moss` | Verde Musgo | `#0F2E20` | Fundos secundários, cards |
| `--color-earth` | Terra | `#3A2C22` | Bordas, separadores, texturas |
| `--color-forest` | Floresta | `#123524` | Hover states, gradientes |

## Regra de Equilíbrio UI

> **50% prata / 50% dourado** nos elementos de interface.

- Botões primários: dourado (`#B08D57`)
- Texto e ícones: prata (`#C7CACE`)
- Nunca usar os dois no mesmo elemento de forma competitiva

## Gradientes Permitidos

```css
/* Fundo hero */
background: linear-gradient(180deg, #0B0D0C 0%, #0F2E20 100%);

/* Overlay cards */
background: linear-gradient(180deg, transparent 40%, #0B0D0C 100%);
```

## CSS Variables (tokens-dark-nature.css)

Fonte única de verdade — nunca duplicar valores hardcoded fora deste ficheiro.

---

← [Índice](../00-INDEX.md)
