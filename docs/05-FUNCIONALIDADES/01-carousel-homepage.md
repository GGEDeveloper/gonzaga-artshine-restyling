# Carousel Homepage — Swiper.js

## Conceito

Três banners por família de produto na homepage:
- **Prata** — joalharia prata 925
- **Latão** — peças em latão
- **Macramé** — artesanato têxtil

Cada banner com imagem full-width, nome da família e CTA para o catálogo filtrado.

## Implementação Swiper.js

```html
<!-- CDN gratuito -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css">
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>

<div class="swiper family-carousel">
  <div class="swiper-wrapper">
    <div class="swiper-slide" data-family="prata">...</div>
    <div class="swiper-slide" data-family="latao">...</div>
    <div class="swiper-slide" data-family="macrame">...</div>
  </div>
  <div class="swiper-pagination"></div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
</div>
```

```javascript
const familyCarousel = new Swiper('.family-carousel', {
  loop: true,
  autoplay: { delay: 5000, disableOnInteraction: false },
  effect: 'fade',
  pagination: { el: '.swiper-pagination', clickable: true },
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev'
  }
});
```

## A Definir

- [ ] Imagens de banner por família (dimensões: 1920×800px)
- [ ] Texto e CTA de cada slide
- [ ] Animação de entrada do texto sobre o banner

---

← [Índice](../00-INDEX.md)
