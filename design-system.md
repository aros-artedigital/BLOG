# Blog_Aros — Design System v1.0
> Base visual extraída da identidade da marca. Referência para desenvolvimento front-end.

---

## 1. CORES

### 1.1 Paleta Principal

Cores de maior hierarquia visual. Usadas em elementos de destaque, CTAs e identidade da marca.

| Token                  | Nome          | Hex       | Uso principal                                      |
|------------------------|---------------|-----------|----------------------------------------------------|
| `--color-brand-blue`   | Brand Blue    | `#2D5AB0` | Cor do logotipo. Cabeçalho, nav ativa, links.      |
| `--color-orange`       | Orange        | `#F08900` | CTA primário, badges de categoria, destaques.      |
| `--color-navy`         | Navy          | `#0D2550` | Fundo de header/footer, textos sobre fundo claro.  |
| `--color-sky`          | Sky Blue      | `#0099D6` | Links, hover states, ícones informativos.          |

### 1.2 Paleta Secundária

Cores de suporte à composição, usadas em fundos, bordas e variações de estado.

| Token                  | Nome          | Hex       | Uso                                                |
|------------------------|---------------|-----------|----------------------------------------------------|
| `--color-gold`         | Golden Yellow | `#FFC107` | Alertas, badge de "Urgente", estrelas, destaques.  |
| `--color-orange-logo`  | Orange Accent | `#D4630E` | Ponto do logotipo. Micro-detalhes, separadores.    |

### 1.3 Paleta de Suporte (Neutros)

| Token                  | Nome          | Hex       | Uso                                                |
|------------------------|---------------|-----------|----------------------------------------------------|
| `--color-black`        | Black         | `#000000` | Texto principal sobre fundo branco.                |
| `--color-steel`        | Steel         | `#2C3E55` | Fundo de sidebar, seções alternadas, nav dark.     |
| `--color-charcoal`     | Charcoal      | `#3A3D45` | Texto secundário, metadados (autor, data).         |
| `--color-gray`         | Gray          | `#6E6E6E` | Texto de apoio, placeholders, bordas sutis.        |
| `--color-gray-light`   | Light Gray    | `#F4F5F7` | Fundo de página, fundo de cards inativos.          |
| `--color-white`        | White         | `#FFFFFF` | Fundo de cards, formulários, áreas de leitura.     |

### 1.4 Cores Semânticas

| Token                  | Nome          | Hex       | Uso                                                |
|------------------------|---------------|-----------|----------------------------------------------------|
| `--color-success`      | Success       | `#1DB954` | Confirmações, formulários válidos.                 |
| `--color-error`        | Error         | `#E53935` | Erros de formulário, alertas críticos.             |
| `--color-warning`      | Warning       | `#FFC107` | Avisos (reutiliza Gold).                           |
| `--color-info`         | Info          | `#0099D6` | Informativos (reutiliza Sky Blue).                 |

---

## 2. TIPOGRAFIA

### 2.1 Fontes do Projeto

| Papel          | Fonte        | Tipo        | Uso                                                  |
|----------------|--------------|-------------|------------------------------------------------------|
| Display/Brand  | **Crasus**   | Local (.ttf/.otf) | Logotipo, manchetes especiais, títulos de seção de impacto. |
| Heading        | **Barlow Condensed** | Google Fonts | H1 a H3. Compacta, leitora, jornalística.     |
| Body/UI        | **Inter**    | Google Fonts | Parágrafos, labels, menus, cards. Máxima legibilidade. |
| Mono (opcional)| **JetBrains Mono** | Google Fonts | Timestamps, códigos, tags técnicas.            |

> **Crasus** é a fonte da marca. Reservar para logotipo e chamadas de impacto visual (hero, banners). Não usar em corpo de texto.

---

### 2.2 Hierarquia Tipográfica

```
DISPLAY (Crasus)
  Tamanho: 56–72px | Weight: 700 | Line-height: 1.1
  Uso: Nome da marca no header, banners hero especiais.

H1 — Manchete Principal (Barlow Condensed)
  Tamanho: 40px | Weight: 700 | Line-height: 1.2
  Uso: Título da notícia no topo do artigo.

H2 — Título de Seção (Barlow Condensed)
  Tamanho: 28px | Weight: 600 | Line-height: 1.3
  Uso: Títulos das seções temáticas (Política, Esportes...).

H3 — Subtítulo / Card Destaque (Barlow Condensed)
  Tamanho: 22px | Weight: 600 | Line-height: 1.35
  Uso: Título de card de notícia em destaque.

H4 — Card Normal (Inter)
  Tamanho: 18px | Weight: 600 | Line-height: 1.4
  Uso: Título de card secundário no grid.

H5 — Label de Colunista / Módulo (Inter)
  Tamanho: 15px | Weight: 600 | Uppercase | Letter-spacing: 0.08em
  Uso: Labels de seção, nome de colunista.

BODY — Texto de Artigo (Inter)
  Tamanho: 16px | Weight: 400 | Line-height: 1.7
  Uso: Corpo de texto de notícias e colunas.

SMALL — Metadado / Caption (Inter)
  Tamanho: 13px | Weight: 400 | Color: --color-gray
  Uso: Data, autor, tempo de leitura, legenda de foto.

LABEL / TAG (Inter)
  Tamanho: 11px | Weight: 700 | Uppercase | Letter-spacing: 0.1em
  Uso: Badge de categoria (POLÍTICA, ESPORTES...).
```

---

## 3. COMPONENTES

### 3.1 Botões

#### Botão Primário (CTA)
```
Background:   --color-orange        (#F08900)
Text:         #FFFFFF
Font:         Inter, 14px, weight 700, uppercase
Padding:      12px 24px
Border-radius: 4px
Border:        none
Hover:        background #D4780A  (escurece 10%)
Active:       background #B8660A  (escurece 20%)
Focus:        outline 2px solid --color-sky, offset 2px
```

#### Botão Secundário (Outline)
```
Background:   transparent
Text:         --color-navy          (#0D2550)
Border:       2px solid --color-navy
Font:         Inter, 14px, weight 700, uppercase
Padding:      10px 22px
Border-radius: 4px
Hover:        background --color-navy, text #FFFFFF
```

#### Botão Ghost (Terciário)
```
Background:   transparent
Text:         --color-brand-blue    (#2D5AB0)
Border:       none
Font:         Inter, 14px, weight 600
Padding:      8px 16px
Hover:        text --color-sky, underline
Uso:          "Ver mais", "Leia também", links internos
```

#### Botão Destaque / Breaking News
```
Background:   --color-gold          (#FFC107)
Text:         --color-black         (#000000)
Font:         Barlow Condensed, 14px, weight 700, uppercase
Padding:      8px 16px
Border-radius: 0px  (estilo jornalístico reto)
Uso:          badges de "URGENTE", "AO VIVO", "EXCLUSIVO"
```

---

### 3.2 Inputs de Formulário

#### Input Padrão (Newsletter, Busca)
```
Height:         48px
Background:     #FFFFFF
Border:         1.5px solid #D0D5DD
Border-radius:  4px
Font:           Inter, 15px, color --color-charcoal
Padding:        0 16px
Placeholder:    color --color-gray (#6E6E6E)

Focus:
  Border-color: --color-brand-blue (#2D5AB0)
  Box-shadow:   0 0 0 3px rgba(45, 90, 176, 0.15)

Error:
  Border-color: --color-error (#E53935)
  Box-shadow:   0 0 0 3px rgba(229, 57, 53, 0.12)

Success:
  Border-color: --color-success (#1DB954)
```

#### Campo de Busca (Header)
```
Background:     --color-steel (#2C3E55)
Border:         none
Border-radius:  20px
Font:           Inter, 14px, color #FFFFFF
Padding:        0 48px 0 20px  (espaço para ícone de lupa)
Placeholder:    rgba(255,255,255,0.5)
Ícone:          lupa branca (16px), posicionada à direita
Hover/Focus:    background rgba(255,255,255,0.1)
```

---

### 3.3 Cards de Notícia

#### Card Hero (Destaque Principal)
```
Layout:         imagem ocupa 60% da largura, texto à direita
Imagem:         aspect-ratio 16/9, border-radius 6px
Badge cat.:     tag laranja (#F08900) sobre a imagem (top-left)
Título (H1):    Barlow Condensed, 36px, weight 700, --color-navy
Subtítulo:      Inter, 15px, --color-charcoal, line-height 1.6
Meta:           Inter, 12px, --color-gray | "Por Autor · 2h atrás"
Background:     #FFFFFF
Border-radius:  6px
Shadow:         0 2px 12px rgba(0,0,0,0.08)
```

#### Card Médio (Grid de Notícias)
```
Layout:         imagem em cima, conteúdo embaixo (stacked)
Imagem:         aspect-ratio 16/9, border-radius 4px 4px 0 0
Badge cat.:     tag pequena sobre a imagem (top-left)
Título (H4):    Inter, 17px, weight 600, --color-navy
  Hover:        color --color-brand-blue
Meta:           Inter, 12px, --color-gray
Background:     #FFFFFF
Border-radius:  4px
Shadow:         0 1px 6px rgba(0,0,0,0.07)
Hover:          shadow 0 4px 16px rgba(0,0,0,0.12), translate Y(-2px)
Transition:     all 0.2s ease
```

#### Card Horizontal (Lista / Sidebar)
```
Layout:         imagem à esquerda (96x72px), texto à direita
Imagem:         border-radius 4px
Título:         Inter, 14px, weight 600, --color-navy
Meta:           Inter, 11px, --color-gray
Separador:      border-bottom 1px solid #EAECF0
Padding:        12px 0
```

#### Card de Colunista
```
Layout:         avatar circular (56px) + nome + área + chamada
Avatar:         border 3px solid --color-orange
Nome:           Inter, 15px, weight 700, --color-navy
Área:           Inter, 12px, weight 500, --color-sky, uppercase
Chamada:        Inter, 14px, italic, --color-charcoal, line-height 1.5
Background:     #FFFFFF
Border-left:    4px solid --color-brand-blue
Padding:        20px
Border-radius:  0 4px 4px 0
Shadow:         0 1px 6px rgba(0,0,0,0.06)
```

---

## 4. ESTÉTICA — REGRAS VISUAIS

### 4.1 Border-Radius

```
--radius-none   : 0px      → Tags "URGENTE", banners de alerta, elementos editoriais rígidos
--radius-sm     : 4px      → Cards, inputs, botões — padrão do portal
--radius-md     : 6px      → Cards hero, modais, tooltips
--radius-lg     : 12px     → Componentes de destaque, seções com fundo colorido
--radius-xl     : 20px     → Input de busca, badges de categoria arredondadas
--radius-full   : 9999px   → Avatares, pílulas de status ("AO VIVO"), ícones de redes sociais
```

> **Regra da marca:** O logotipo usa formas orgânicas arredondadas. O design do portal equilibra isso com cantos mais retos (`4px`) para manter a seriedade jornalística, aplicando bordas mais curvas apenas em elementos de destaque e interação.

---

### 4.2 Sombras (Box-Shadow)

```
--shadow-xs   : 0 1px 3px rgba(0,0,0,0.06)              → Cards em repouso na sidebar
--shadow-sm   : 0 1px 6px rgba(0,0,0,0.08)              → Cards no grid de notícias
--shadow-md   : 0 4px 16px rgba(0,0,0,0.12)             → Cards em hover, dropdowns
--shadow-lg   : 0 8px 32px rgba(0,0,0,0.16)             → Modais, overlays, nav mobile
--shadow-brand: 0 4px 20px rgba(45,90,176,0.25)         → Botão primário em hover (azul)
--shadow-cta  : 0 4px 20px rgba(240,137,0,0.35)         → Botão CTA laranja em hover
```

---

### 4.3 Espaçamentos (Escala de 4px)

```
--space-1  :  4px    → Micro-espaçamentos internos (ícone + label)
--space-2  :  8px    → Gap entre badge e título de card
--space-3  : 12px    → Padding interno de card compacto
--space-4  : 16px    → Padding padrão de componentes
--space-5  : 20px    → Espaço entre elementos de formulário
--space-6  : 24px    → Margin entre cards no grid
--space-8  : 32px    → Padding de seção no mobile
--space-10 : 40px    → Margin entre seções temáticas
--space-12 : 48px    → Padding de seção no desktop
--space-16 : 64px    → Separação de blocos maiores (hero → grid)
--space-20 : 80px    → Espaço de rodapé e grandes blocos
```

---

### 4.4 Grid & Layout

```
Max-width do container : 1280px
Colunas (desktop)      : 12 colunas, gap 24px
Colunas (tablet)       : 8 colunas, gap 16px
Colunas (mobile)       : 4 colunas, gap 12px

Breakpoints:
  --bp-sm  : 480px
  --bp-md  : 768px
  --bp-lg  : 1024px
  --bp-xl  : 1280px
```

---

### 4.5 Tokens de Transição

```
--transition-fast   : all 0.15s ease        → Hover de link, badge
--transition-base   : all 0.2s ease         → Cards, botões
--transition-slow   : all 0.35s ease        → Menu mobile, modal
```

---

## 5. IDENTIDADE VISUAL — DIRETRIZES DE USO DO LOGO

### Análise do logotipo
- Forma principal: "A" estilizado em azul escuro (`#2D5AB0`) com arco superior arredondado.
- Detalhe: ponto quadrado laranja (`#D4630E`) — representa o "ponto final" da notícia, precisão e assinatura da marca.
- Estilo: Geométrico, orgânico e moderno. Transmite autoridade (azul) + energia (laranja).

### Regras de aplicação
```
Fundo claro (branco / light gray) → Logo azul + ponto laranja (versão padrão)
Fundo escuro (navy / steel / black) → Logo branco + ponto laranja
Fundo laranja / orange             → Logo branco + ponto branco ou navy
Tamanho mínimo                     → 32px de altura (digital) / 20mm (impresso)
Área de proteção                   → Espaço equivalente à largura do "A" em todos os lados
```

---

## 6. RESUMO — CSS CUSTOM PROPERTIES (Variáveis Prontas para Dev)

```css
:root {
  /* === CORES === */
  --color-brand-blue   : #2D5AB0;
  --color-orange       : #F08900;
  --color-orange-logo  : #D4630E;
  --color-navy         : #0D2550;
  --color-sky          : #0099D6;
  --color-gold         : #FFC107;
  --color-black        : #000000;
  --color-steel        : #2C3E55;
  --color-charcoal     : #3A3D45;
  --color-gray         : #6E6E6E;
  --color-gray-light   : #F4F5F7;
  --color-white        : #FFFFFF;
  --color-success      : #1DB954;
  --color-error        : #E53935;

  /* === TIPOGRAFIA === */
  --font-display : 'Crasus', sans-serif;
  --font-heading : 'Barlow Condensed', sans-serif;
  --font-body    : 'Inter', sans-serif;

  /* === BORDER-RADIUS === */
  --radius-none  : 0px;
  --radius-sm    : 4px;
  --radius-md    : 6px;
  --radius-lg    : 12px;
  --radius-xl    : 20px;
  --radius-full  : 9999px;

  /* === SOMBRAS === */
  --shadow-xs    : 0 1px 3px rgba(0,0,0,0.06);
  --shadow-sm    : 0 1px 6px rgba(0,0,0,0.08);
  --shadow-md    : 0 4px 16px rgba(0,0,0,0.12);
  --shadow-lg    : 0 8px 32px rgba(0,0,0,0.16);
  --shadow-brand : 0 4px 20px rgba(45,90,176,0.25);
  --shadow-cta   : 0 4px 20px rgba(240,137,0,0.35);

  /* === ESPAÇAMENTO === */
  --space-1  :  4px;
  --space-2  :  8px;
  --space-3  : 12px;
  --space-4  : 16px;
  --space-5  : 20px;
  --space-6  : 24px;
  --space-8  : 32px;
  --space-10 : 40px;
  --space-12 : 48px;
  --space-16 : 64px;
  --space-20 : 80px;

  /* === TRANSIÇÕES === */
  --transition-fast : all 0.15s ease;
  --transition-base : all 0.2s ease;
  --transition-slow : all 0.35s ease;
}
```

---

*Blog_Aros Design System v1.0 — Aros Arte Digital · 2026*
