# Referências Visuais & Moodboard

## Referência Principal: lulamaiz.com

**URL:** https://lulamaiz.com  
**Análise realizada:** 2026-04-08

---

## 1. Estrutura de Layout — Homepage

### Anatomia da Página (de cima para baixo)

| # | Secção | Descrição |
|---|--------|-----------|
| 1 | **Announcement Bar** | Faixa topo escura, texto centrado branco — promoção envios grátis |
| 2 | **Navbar** | Logo esquerda (dourado em fundo preto), nav central (JOYAS / HISTORIA), ícones search+cart direita. Fundo: preto total `#0a0a0a`. Altura ~70px. |
| 3 | **Hero Carousel** | Full-width, sem texto sobreposto. Fotografias macro em fundo escuro dramático. 3–4 slides. Dots indicadores em baixo. Setas laterais minimalistas. |
| 4 | **Intro Marca** | Layout 3 colunas: imagem esq | texto centrado | imagem dir. Fundo preto. Corpo texto branco ~16px. CTA "VER COLECCIÓN" outline + seta. |
| 5 | **Grid Categorias** | Fundo fotográfico full-bleed (modelo, tons laranja/terra). Grid 3x2 tiles com texto branco canto inf-esq, bordas 1px branco. |
| 6 | **Feed Instagram** | Carrossel horizontal @lulamaiz. Título em dourado. Fotos quadradas. |
| 7 | **Footer** | 4 colunas: Logo+email | JOYAS | LULA MÁIZ | MÁS INFORMACIÓN. Fundo `#0d0d0d`. |

---

## 2. Tokens Visuais Extraídos

### Cores

```css
--color-bg-primary:   #0a0a0a;   /* preto quente — background principal */
--color-bg-secondary: #111111;   /* navbar, footer */
--color-text-primary: #ffffff;   /* texto principal */
--color-text-muted:   #cccccc;   /* texto secundário */
--color-gold-brand:   #b8973a;   /* logo, super-labels, detalhes */
--color-gold-hover:   #d4a843;   /* CTA hover */
--color-border:       rgba(255,255,255,0.15); /* bordas tiles/cards */
--color-cta-solid-bg: #c9a227;   /* botão primário (add to cart) */
--color-cta-solid-text: #000000;
```

### Tipografia

| Elemento | Família | Peso | Tamanho | Notas |
|----------|---------|------|---------|-------|
| Super-label | Sans caps tracked | 400 | ~11px | Letter-spacing 0.18em, cor dourada |
| H3 Secção | Serif light (Cormorant/Playfair style) | 300 | ~44px | Peso light, espaçado |
| Corpo texto | Sans-serif limpa | 400 | ~16px | Line-height 1.7, centrado |
| Nav links | Sans caps | 600 | ~13px | Letter-spacing 0.05em |
| Labels tiles | Serif light | 300 | ~30px | Branco, canto inf-esq |
| Nome produto | Serif/Sans | 400 | ~15px | Centrado abaixo da imagem |
| Preço produto | Sans | 400 | ~14px | Centrado, branco |
| H1 produto | Serif | 500 | ~32px | Página de detalhe |

### Hierarquia Tipográfica Padrão
```
SUPER-LABEL  → dourado, caps, track alto        "PIEZAS ÚNICAS"
H3 PRINCIPAL → serif light, 44px               "by Lula Máiz"
BODY         → sans, 16px, branco, centrado    parágrafo descritivo
CTA OUTLINE  → sans caps, border 1px branco    "VER COLECCIÓN →"
```

---

## 3. Linguagem Visual

### Fotografia de Produto
- Fundos escuros exclusivamente: preto, castanho, tecido texturado
- Macro/close-up do detalhe do material como protagonista
- Contexto humano mínimo: mão, pescoço, dedo — nunca rosto dominante
- Paleta fotográfica quente: âmbar, turquesa, laranja, prata, ouro sobre fundo neutro escuro
- Sem texto sobreposto no hero — imagem fala por si

### Cards de Produto (catálogo)
- Fundo escuro do card (`#111`)
- Imagem centrada com margem de respiração
- Nome produto + preço abaixo, sem botão no card
- Hover: cursor pointer implícito
- Grid: **4 colunas desktop**, 2 mobile

### Página de Produto
- Layout 2 colunas: galeria esquerda + info direita
- Thumbs em coluna vertical esquerda, imagem principal ao centro-esq
- H1 nome (serif 32px) → preço → seletor qtd → CTA sólido dourado
- Descrição em texto corrido, atributos em linhas separadas

### CTAs
```
Primário  (ação direta): bg #c9a227 sólido | texto preto | sem border-radius (sharp)
Secundário (navegação):  bg transparent  | border 1px #fff | texto branco | sharp
```

---

## 4. UX & Navegação

- Navbar: 2 itens de conteúdo + ícones utilitários — extremamente minimalista
- Sem mega-menu
- Scroll suave sem animações excessivas
- Announcement bar com X para fechar
- Feed Instagram integrado como prova social na homepage
- Footer 4 colunas com links organizados por tema

---

## 5. Aplicação ao Gonzaga ArtShine

### Adoptar directamente

| Padrão Lulamaiz | Tradução Gonzaga ArtShine |
|----------------|---------------------------|
| Background `#0a0a0a` | Base Dark Nature `#0d0d0d` |
| Super-label dourado + H serif light | Label família + título colecção |
| Hero full-width sem texto | Hero fotográfico das peças artesanais |
| Grid 3x2 tiles categorias sobre foto | Grid famílias: Prata / Latão / Macramé / Cera |
| CTA outline branco (nav) | Botão "Ver Catálogo" / "Explorar" |
| CTA sólido dourado (ação) | Botão "Adicionar ao Carrinho" |
| Cards 4 col, fundo escuro, sem botão | Cards produto: imagem + nome + preço |
| Galeria thumbs vertical + principal | Detalhe produto múltiplos ângulos |
| Footer 4 colunas | Footer: Logo | Catálogo | Empresa | Legal |

### Diferenciar / Elevar

| O que fazer diferente no Gonzaga ArtShine |
|-------------------------------------------|
| Tipografia: **Cinzel** (mais gótico/medieval) em vez de serif neutral |
| Paleta: adicionar verde musgo `#3d4a2e` e cobre `#b87333` |
| Animações: parallax subtil no hero (lulamaiz é estático) |
| Badges de material nas cards (Prata 925 / Latão / Macramé) |
| Secção "processo de fabrico" na homepage — diferenciação artesanal |

---

## 6. Decisões de Design Fixadas

1. **Navbar:** Logo esquerda | nav centrada (máx 4 items) | ícones direita
2. **Hero:** Full-width, 3 slides, macro-foto, sem texto sobreposto, CTA após carousel
3. **Cores CTA:** dourado `#b8973a` para ação | outline `1px solid #fff` para navegação
4. **Grid catálogo:** 4 colunas desktop / 2 mobile | sem botão no card | hover scale subtil
5. **Produto:** thumbs vertical esq + imagem principal + info direita
6. **Fundo:** `#0d0d0d` fixo — nunca branco em nenhum template
7. **Super-label:** Cinzel caps + letter-spacing 0.15em + cor `#b8973a`

---

## 7. Referências Adicionais Analisadas

### 7.1 RegalRose — regalrose.co.uk

**Perfil:** Gothic alt-fashion UK | Shopify | Coleções temáticas sazonais

#### Layout & Estética
- Background **branco creme/bege** (`#f5f0eb`) no body principal — contraste com o hero escuro
- Hero: layout editorial full-width com **3 paineis** (esq+centro+dir) tipo frames vintage com bordas decorativas
- Coleções nomeadas como histórias: "THE FRAMES COLLECTION", "BELOVED", "DEATH..."
- Fotografia: mãos com unhas vermelhas segurando peças, tons escarlate e preto
- Grid produtos: 4 colunas, fundo branco/cinza claro, badge "NEW IN" / "SEMI-PRECIOUS" no canto
- Secção "ADORED BY YOU": 2 filas de 6 fotos de clientes (UGC) — mosaico full-bleed
- Secção tabbed: "THE VAULT" | "RINGS" — tabs com underline dourado no activo

#### Tipografia RegalRose
```
Logo:        Sans-serif geométrico bold, caps, tracking largo — "REGALROSE"
Nav links:   Sans caps, 600, ~13px
Labels coleção: Serifada decorativa, 300, ~11px — "THE FRAMES COLLECTION"
H Hero:      Serifada display grande, ~60–70px — "BELOVED"
CTA:         Sans caps, outline rectangular, ~12px — "NEW COLLECTION >"
```

#### Paleta RegalRose
```css
--rr-bg:          #f5f0eb;   /* creme/bege — body */
--rr-dark:        #1a1a1a;   /* navbar, footer, hero */
--rr-scarlet:     #8b0000;   /* acento rubim/escarlate */
--rr-gold:        #c9a84c;   /* detalhes dourados, tabs activos */
--rr-text:        #222222;
--rr-badge-bg:    #1a1a1a;
--rr-badge-text:  #ffffff;
```

#### O que adaptar para Gonzaga ArtShine
- **Tabbed sections** para navegar famílias (ex: PRATA | LATÃO | MACRAMÉ)
- **Badge de categoria** no canto sup-esq dos cards ("PEÇA ÚNICA", "PRATA 925")
- **Mosaico UGC** de fotos de clientes como prova social
- **Coleções com nome narrativo** em vez de apenas categoria técnica

---

### 7.2 Shop Dixi — shopdixi.com

**Perfil:** Witchy / Gothic / Autumnal UK | Shopify | Foco em prata esterlina

#### Layout & Estética
- Background: fundo **quente âmbar/terra** nas fotos do hero (tons de outono, velas, cogumelos)
- Navbar: branca/clara com logo script cursive elegante ("Dixi")
- Hero: full-width close-up de mão com vários anéis empilhados, tons warm
- Secção testimonials: 3 colunas, fundo branco, texto preto, aspas grandes em cinzento
- Layout 50/50: imagem esq (mão com anéis empilhados) + texto+CTA dir
- Product cards: fundo branco, imagem centrada, sem borda, hover subtil
- CTA: botao outline rectangular com texto caps espaçado — "SHOP WITCHY JEWELLERY"
- Badges de colecção no header: "50% OFF RING SETS", "SHOP BY AESTHETIC"
- Trustbar com 3 pilares: icone + título + descrição (Secure / Simple checkout / Get in touch)

#### O que adaptar para Gonzaga ArtShine
- **Trustbar de 3 pilares** abaixo do hero ou no footer: "Artesanato Autoral | Materiais Naturais | Envio Seguro"
- **Layout 50/50** para secção de processo de fabrico
- **Navegação por estética** ("SHOP BY AESTHETIC") → adaptar para "POR MATERIAL" ou "POR OCASIÃO"
- **Empilhamento de anéis/peças** na fotografia — mostrar variedade numa única imagem

---

### 7.3 Black Feather Design — blackfeatherdesign.co.uk

**Perfil:** Rock/Macabre/Gothic UK | Artesanato a pedido | Bespoke

#### Layout & Estética
- Background: **preto total `#000000`** sem qualquer excepção — mais escuro que lulamaiz
- Logo: ilustrado, manuscrito cursive, cor **dourado âmbar** `#c8821a`
- Nav links: cor **dourado âmbar**, sem caps, serifada leve
- Hero: full-width dramático, **texto sobreposto** em tipografia gótica display: "CONQUEROR'S SWORD" em branco, sub-label "OUT NOW" em dourado
- Grid coleções: 4 tiles, fundo escuro, foto produto + categoria em branco abaixo
- Secção "What's New": produtos recentes em grid 4 colunas
- Review bar Trustpilot no topo ("262 reviews")
- Botão "BESPOKE" na nav — destaca personalização artesanal como proposta de valor

#### Tipografia Black Feather
```
Logo:         Script cursive, dourado âmbar
Nav links:    Serifada, 400, ~14px, dourado
Hero title:   Gótica display, bold, branco, ~50-60px
Hero sub:     Gótica display, dourado, ~36px
Bod texto:    Serifada, 400, branco/cinzento
```

#### Paleta Black Feather
```css
--bfd-bg:       #000000;   /* preto absoluto */
--bfd-gold:     #c8821a;   /* dourado âmbar — logo, nav, destaques */
--bfd-text:     #ffffff;
--bfd-muted:    #aaaaaa;
--bfd-red:      #8b0000;   /* acento esârlate nas joias */
```

#### O que adaptar para Gonzaga ArtShine
- **Tipografia gótica display** para títulos de coleção no hero (Cinzel fills this role)
- **Texto sobreposto no hero** com nome da coleção em destaque — mais impactante que hero só fotográfico
- **Botão "Bespoke"** ou "Encomenda Especial" na nav — diferenciar o artesanato a pedido
- **Trustpilot / Google Reviews bar** no topo como prova social imediata
- **Dourado `#c8821a`** como cor accent mais quente e artesanal vs dourado frió do lulamaiz

---

## 8. Matriz Comparativa de Referências

| Atributo | Lula Maiz | RegalRose | Shop Dixi | Black Feather | **Gonzaga ArtShine** |
|----------|-----------|-----------|-----------|---------------|----------------------|
| **Background** | Preto `#0a0a0a` | Creme `#f5f0eb` | Claro/quente | Preto `#000000` | **Preto `#0d0d0d`** |
| **Acento** | Dourado `#b8973a` | Dourado `#c9a84c` | Neutro | Dourado âmbar `#c8821a` | **Dourado+Cobre** |
| **Tipografia logo** | SVG ornamental | Sans bold caps | Script cursive | Script cursive dourada | **Cinzel serifada** |
| **Hero** | Só imagem, sem texto | Editorial 3 paineis | Close-up macro | Imagem + texto gótico sobreposto | **Imagem + super-label** |
| **Grid produtos** | 4 col, fundo escuro | 4 col, fundo claro | 4 col, fundo branco | 4 col, fundo escuro | **4 col, fundo escuro** |
| **Badges cards** | Nenhum | "NEW IN" / tipo | Nenhum | Nenhum | **Material + "PEÇA ÚNICA"** |
| **Trustbar** | Não | Não | 3 pilares | Trustpilot barra | **3 pilares + reviews** |
| **Bespoke/encomenda** | Não | Não | Não | Sim (nav item) | **Sim (Área cliente)** |
| **UGC/social** | Feed Instagram | Mosaico clientes | Testimonials | Trustpilot | **Feed + testimonials** |
| **Coleções nomeadas** | Por tipo de jóia | Por tema narrativo | Por estética | Por peça | **Por material** |

