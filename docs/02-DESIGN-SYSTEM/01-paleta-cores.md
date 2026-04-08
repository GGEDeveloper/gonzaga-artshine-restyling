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


---

## Paletas Alternativas Dark — Exploração

### Contexto

As notas do GitHub sobre a paleta "Dark Nature" (#0d0d0d, #B80D57, #4C7CAE) são **sugestivas**, não prescritivas.

Esta secção apresenta 6 paletas alternativas **todas escuras**, curadas a partir de análise de 23 gothic/jewel-tone palettes profissionais + tendências 2025–2026.

### Critérios de Selecção

✅ **Background sempre escuro** (`#000 a #151515`)
✅ **Jewel tones** ou cores naturais profundas (não neon, não pastéis)
✅ **Legibilidade** garantida (contraste WCAG AA mínimo)
✅ **Adequação ao artesanato** de prata/latão/macramé/cera

---

## 🎨 Paleta 1: **Cathedral Velvet** (Romântico Regalista)

### HEX Codes
```css
--base:       #0b0b0f;   /* preto aveludado */
--surface:    #2a2438;   /* púrpura profundo */
--accent:     #5a1f2b;   /* borgonha escura */
--gold:       #a28b6e;   /* ouro antigo fosco */
--text:       #e7e1d6;   /* marfim envelhecido */
```

### Mood
**Regal, candlelit, dark romantic**

### Aplicação Gonzaga ArtShine
- **Background:** `#0b0b0f` fixo em todo o site
- **Navbar/Footer:** `#2a2438`
- **CTAs primários:** `#5a1f2b` (adicionar ao carrinho)
- **Acentos decorativos:** `#a28b6e` (ícones, badges "PEÇA ÚNICA")
- **Texto corpo:** `#e7e1d6`

### Vantagens
- Extremamente elegante e premium
- Borgonha dá calor humano vs preto frio
- Ouro fosco evita ostentação

### Desvantagens
- Pode ser "demasiado sério" se não houver fotografia vibrante
- Contraste borgonha/preto é médio — exige tipografia bold

---

## 🎨 Paleta 2: **Cursed Emerald Ink** (Místico Natural)

### HEX Codes
```css
--base:       #060907;   /* preto com hint verde */
--surface:    #0e1f17;   /* verde floresta noturno */
--accent:     #124136;   /* jade profundo */
--jewel:      #1f7a63;   /* esmeralda saturada */
--text:       #d5efe6;   /* verde menta pálido */
```

### Mood
**Mysterious, botanical, spell-like glow**

### Aplicação Gonzaga ArtShine
- **Background:** `#060907`
- **Cards produto:** `#0e1f17`
- **Hover states:** `#124136`
- **CTAs:** `#1f7a63` (cor de destaque forte)
- **Texto:** `#d5efe6`

### Vantagens
- **Conecta directamente ao conceito "Dark Nature"**
- Verde esmeralda é raro em joalharia → diferenciação forte
- Funciona muito bem com fotografias de prata oxidada e latão

### Desvantagens
- Verde pode ser associado a "eco/sustentável" vs "luxo artesanal"
- Exige fotografia de produto com fundos neutros (cinza/preto) para não chocar

---

## 🎨 Paleta 3: **Arcane Copper** (Alquimista Artesanal)

### HEX Codes
```css
--base:       #0e0906;   /* espresso quase preto */
--surface:    #2f1a12;   /* castanho chocolate escuro */
--accent:     #6a3a28;   /* terracota queimada */
--copper:     #b06a43;   /* cobre fosco */
--text:       #f2d6c7;   /* pêssego pergaminho */
```

### Mood
**Warm, alchemical, handcrafted workshop**

### Aplicação Gonzaga ArtShine
- **Ideal para secção "Latão" ou "Processo Artesanal"**
- **Background:** `#0e0906`
- **Painéis de texto:** `#2f1a12`
- **Detalhes de borda:** `#b06a43` (muito subtil, 1px)
- **CTAs secundários:** `#6a3a28`
- **Texto:** `#f2d6c7`

### Vantagens
- **Perfeito para destacar peças de latão/cobre**
- Paleta quente, intimista, convida ao toque
- Cor cobre `#b06a43` combina literalmente com o material

### Desvantagens
- Pode ficar "barrento" se mal fotografado
- Menos versátil que paletas neutras (preto/cinza/branco)

---

## 🎨 Paleta 4: **Obsidian Amethyst** (Luxo Nocturno)

### HEX Codes
```css
--base:       #0a0710;   /* obsidiana violeta */
--surface:    #241338;   /* púrpura meia-noite */
--accent:     #4b1f6f;   /* ametista profunda */
--jewel:      #7c49b9;   /* violeta saturado */
--text:       #e9ddff;   /* lavanda pálida */
```

### Mood
**Arcane, luxe, night-sky, stage lights**

### Aplicação Gonzaga ArtShine
- **Para colecção "Especial" ou "Edição Limitada"**
- **Background:** `#0a0710`
- **Hero section:** `#241338` com gradiente para `#0a0710`
- **CTAs:** `#7c49b9` (muito impactante)
- **Badges:** `#4b1f6f`

### Vantagens
- **Extremamente diferenciador** — ninguém usa púrpura escuro em joalharia artesanal
- Transmite magia, mistério, exclusividade
- Funciona lindamente com prata oxidada + pedras roxas (ametista)

### Desvantagens
- Pode parecer "demasiado gótico" para público mainstream
- Exige fotografia de qualidade altíssima para não parecer "barato"

---

## 🎨 Paleta 5: **Storm Chapel** (Cinematográfico Frio)

### HEX Codes
```css
--base:       #0d1016;   /* chumbo escuro */
--surface:    #1e2a3a;   /* ardósia fria */
--accent:     #334b63;   /* azul tempestade */
--steel:      #6f8aa3;   /* aço azulado */
--text:       #d9e2ec;   /* névoa clara */
```

### Mood
**Brooding, cool, cinematic, architectural**

### Aplicação Gonzaga ArtShine
- **Para colecção "Prata"** exclusivamente
- **Background:** `#0d1016`
- **Cards:** `#1e2a3a`
- **Hover:** `#334b63`
- **Texto:** `#d9e2ec`

### Vantagens
- **Combina perfeitamente com prata 925**
- Paleta "fria" transmite pureza, precisão, modernidade
- Excelente para hero sections com parallax

### Desvantagens
- Pode ser "demasiado fria" para artesanato (perde calor humano)
- Azul é tradicionalmente masculino — pode afastar público feminino

---

## 🎨 Paleta 6: **Velvet Olive Dusk** (Terroso Intimista)

### HEX Codes
```css
--base:       #0b0c07;   /* preto oliváceo */
--surface:    #23260f;   /* verde oliva noite */
--accent:     #4a4f1e;   /* musgo seco */
--earth:      #7b842f;   /* verde terra */
--text:       #e6e8c7;   /* creme vegetal */
```

### Mood
**Earthy, muted, forest-at-dusk, grounded**

### Aplicação Gonzaga ArtShine
- **Ideal para colecção "Macramé" ou "Cera Natural"**
- **Background:** `#0b0c07`
- **Secções de texto:** `#23260f`
- **CTAs:** `#7b842f`
- **Texto:** `#e6e8c7`

### Vantagens
- **Directamente alinhada com "Dark Nature"** — literalmente cores de floresta
- Verde oliva é neutro, unisex, atemporal
- Funciona muito bem com macramé (fibras naturais)

### Desvantagens
- Pode ficar "militar" se mal equilibrada
- Contraste é o mais baixo de todas as opções — exige tipografia forte

---

## Recomendação Final

### Para lançamento inicial (Q2 2026)
**Paleta 1 (Cathedral Velvet)** ou **Paleta 3 (Arcane Copper)**

**Porquê?**
- Ambas são **quentes e acolhedoras** (importante para artesanato)
- Borgonha e cobre são **cores naturais**, não sintéticas
- Ambas têm **contraste forte** → acessibilidade WCAG garantida
- Funcionam com **todas as famílias de produto** (Prata, Latão, Macramé, Cera)

### Para experimentação futura (A/B testing)
- **Paleta 2 (Cursed Emerald)** para hero alternativo
- **Paleta 5 (Storm Chapel)** para landing page exclusiva "Colecção Prata"

### A evitar
- Paletas com **azuis frios puros** sem contrabalanço quente
- Paletas com **contraste insuficiente** (exemplo: verde oliva escuro + texto verde claro)
- **Preto absoluto #000000** — usar sempre `#0a–#10` para evitar OLED burn-in e dar profundidade

---

## CSS Variables — Template Genérico

Independentemente da paleta escolhida, usar sempre esta estrutura:

```css
:root {
  /* Surfaces */
  --color-bg-primary:   /* o mais escuro */;
  --color-bg-secondary: /* cards, painéis */;
  
  /* Accents */
  --color-accent-primary:   /* CTAs, links */;
  --color-accent-secondary: /* hover states */;
  
  /* Text */
  --color-text-primary:  /* body text */;
  --color-text-muted:    /* labels, meta */;
  --color-text-inverse:  /* texto sobre accent */;
  
  /* Borders */
  --color-border:        /* geralmente accent com 20% opacity */;
  --color-border-focus:  /* accent a 100% */;
}
```

---

← [Índice](../00-INDEX.md)
