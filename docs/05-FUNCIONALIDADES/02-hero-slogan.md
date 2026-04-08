# Hero Slogan — "Elegância que nasce da terra"

## Conceito Cinematográfico

Entrada lenta e dramática do slogan sobre fundo full-screen escuro.
Inspiraçao: títulos de abertura de filmes de autor europeus.

## Estrutura HTML

```html
<section class="hero">
  <div class="hero__bg"></div>
  <div class="hero__content">
    <p class="hero__pretext">Gonzaga Art & Shine</p>
    <h1 class="hero__slogan">
      <span class="hero__slogan-line">Elegância que</span>
      <span class="hero__slogan-line">nasce da terra</span>
    </h1>
    <a href="/catalogo" class="hero__cta">Explorar Colecção</a>
  </div>
</section>
```

## CSS

```css
.hero {
  position: relative;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.hero__slogan-line {
  display: block;
  opacity: 0;
  animation: heroLineReveal 1.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

.hero__slogan-line:nth-child(2) {
  animation-delay: 0.3s;
}

@keyframes heroLineReveal {
  from { opacity: 0; transform: translateY(32px); }
  to   { opacity: 1; transform: translateY(0); }
}
```

## A Definir

- [ ] Imagem / vídeo de fundo do hero
- [ ] Versão mobile (texto menor, padding ajustado)
- [ ] Partículas ou overlay animado (opcional)

---

← [Índice](../00-INDEX.md)
