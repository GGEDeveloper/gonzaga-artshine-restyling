# Animações CSS

> A detalhar durante a fase de redesign do hero.

## Princípios

- Animações **subtis e lentas** — nunca agressivas ou distractoras
- Duração base: `0.6s–1.2s` ease-in-out
- Usar `will-change: transform` apenas onde necessário
- Respeitar `prefers-reduced-motion`

## Hero Slogan — "Elegância que nasce da terra"

Conceito cinematográfico proposto:

```css
/* Fade + rise suave */
@keyframes heroReveal {
  from {
    opacity: 0;
    transform: translateY(24px);
    letter-spacing: 0.2em;
  }
  to {
    opacity: 1;
    transform: translateY(0);
    letter-spacing: 0.08em;
  }
}

.hero-slogan {
  animation: heroReveal 1.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}
```

## Transitions Globais

```css
/* Hover padrão em elementos interactivos */
transition: all 0.3s ease;

/* Cards */
transition: transform 0.4s ease, box-shadow 0.4s ease;
```

## A Definir

- [ ] Animação de entrada do carousel
- [ ] Parallax no hero (se aplicável)
- [ ] Loading states
- [ ] Page transitions

---

← [Índice](../00-INDEX.md)
