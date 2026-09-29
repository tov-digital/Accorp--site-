# Design System — ACCORP

**Associação Cultural de Cordas de Rio Preto**
Base: Manual de Identidade Visual ACCORP. Este documento traduz o manual para uso em desenvolvimento web.

> **Legenda de origem**
> - 🟢 **Manual**: definido diretamente no Manual de Identidade Visual.
> - 🟡 **Derivado**: proposto aqui a partir do manual (escalas, tints, tokens, componentes). Deve ser validado com o responsável pela marca.

---

## 1. Essência da marca

🟢 A ACCORP nasce da crença de que a música é uma ferramenta de formação, conexão e transformação. Por meio do ensino e da valorização da música de cordas, aproxima pessoas da arte e da cultura.

**Propósito:** levar a música cada vez mais longe, preservando a tradição dos instrumentos de cordas e abrindo espaço para novas gerações.

**Valores:** música, educação, cultura, formação, comunidade e transformação por meio da arte.

**Equilíbrio central:** tradição, educação e comunidade.

### Princípios de design 🟡

1. **Elegância sóbria.** Azul profundo, dourado contido e muito respiro. O visual remete a sala de concerto, não a página promocional.
2. **O dourado é raro.** Aparece em filetes, detalhes e destaques pontuais. Nunca como fundo dominante.
3. **Tradição com acolhimento.** Tipografia serifada clássica, mas linguagem simples e acessível (a associação é educacional e comunitária).
4. **A marca respira.** Respeitar sempre a margem de segurança do logotipo.
5. **Consistência acima de novidade.** Qualquer desvio da identidade deve ser intencional e registrado no manual.

---

## 2. Cores

### 2.1 Paleta institucional 🟢

| Token | Nome | HEX | RGB | CMYK |
|---|---|---|---|---|
| `--color-navy` | Azul ACCORP | `#03223F` | 3, 34, 63 | 96, 80, 47, 54 |
| `--color-gold` | Dourado ACCORP | `#AF8A47` | 175, 138, 71 | 32, 42, 84, 7 |
| `--color-cream` | Off-white ACCORP | `#FEFDF9` | 254, 253, 249 | 0, 0, 1, 0 |

### 2.2 Cores de apoio 🟡

Derivadas da paleta para cobrir estados de interface, bordas e superfícies. Mantêm a temperatura das cores institucionais.

| Token | HEX | Uso sugerido |
|---|---|---|
| `--color-navy-90` | `#0F3556` | Hover em superfícies azuis |
| `--color-navy-70` | `#3A5670` | Texto secundário sobre fundo claro |
| `--color-navy-20` | `#C9D1D9` | Bordas e divisores sobre fundo claro |
| `--color-navy-08` | `#EDF0F3` | Superfícies alternativas claras |
| `--color-gold-dark` | `#8A6C34` | Texto dourado sobre fundo claro (contraste) e hover de links |
| `--color-gold-light` | `#D9BE8A` | Detalhes dourados sobre fundo azul |
| `--color-gold-10` | `#F5EEDF` | Destaques suaves, fundo de avisos |
| `--color-success` | `#2F6B4F` | Confirmações |
| `--color-error` | `#A63A32` | Erros |

### 2.3 Contraste (WCAG) 🟡

Razões calculadas com as cores do manual:

| Combinação | Razão aproximada | Uso permitido |
|---|---|---|
| Azul `#03223F` sobre off-white `#FEFDF9` | ~15:1 | Qualquer texto (AAA) |
| Off-white sobre azul | ~15:1 | Qualquer texto (AAA) |
| Dourado `#AF8A47` sobre azul `#03223F` | ~5:1 | Texto normal (AA) |
| Dourado `#AF8A47` sobre off-white | ~3,1:1 | **Apenas** texto grande (18px+ ou 14px bold+) e elementos decorativos |

**Regra prática:** sobre fundo claro, texto dourado pequeno deve usar `--color-gold-dark`. O dourado original fica para filetes, ícones grandes e títulos grandes.

### 2.4 Tokens semânticos 🟡

```css
:root {
  /* Marca */
  --color-navy: #03223F;
  --color-gold: #AF8A47;
  --color-cream: #FEFDF9;

  /* Apoio */
  --color-navy-90: #0F3556;
  --color-navy-70: #3A5670;
  --color-navy-20: #C9D1D9;
  --color-navy-08: #EDF0F3;
  --color-gold-dark: #8A6C34;
  --color-gold-light: #D9BE8A;
  --color-gold-10: #F5EEDF;
  --color-success: #2F6B4F;
  --color-error: #A63A32;

  /* Semânticos (tema claro) */
  --bg-page: var(--color-cream);
  --bg-surface: #FFFFFF;
  --bg-surface-alt: var(--color-navy-08);
  --bg-inverse: var(--color-navy);
  --text-primary: var(--color-navy);
  --text-secondary: var(--color-navy-70);
  --text-inverse: var(--color-cream);
  --text-accent: var(--color-gold-dark);
  --border-subtle: var(--color-navy-20);
  --border-accent: var(--color-gold);
  --link: var(--color-navy);
  --link-hover: var(--color-gold-dark);
  --focus-ring: var(--color-gold);
}
```

### 2.5 Proporção de uso 🟡

- **Off-white:** ~60% (fundo principal, respiro)
- **Azul:** ~30% (texto, seções de destaque, rodapé, cabeçalho escuro)
- **Dourado:** ~10% ou menos (filetes, detalhes, destaques)

---

## 3. Tipografia

### 3.1 Famílias institucionais 🟢

| Função | Fonte do manual | Uso |
|---|---|---|
| Títulos e destaques | **Domine** | Substituta oficial do estilo do logotipo, para títulos |
| Slogan e subtítulos | **Futura Bk BT** | Subtítulos de peças gráficas e slogan |
| Textos longos | **Gotham Book** | Corpo de texto, como no próprio manual |

> O logotipo usa uma fonte criada e estilizada exclusivamente para ele. Não é replicável. Nunca redigite o nome "ACCORP" em fonte para imitar o logo; use sempre o arquivo do logotipo.

### 3.2 Fontes para web 🟡

- **Domine** está disponível gratuitamente no Google Fonts.
- **Futura Bk BT** e **Gotham Book** são fontes comerciais. Para usá-las no site é preciso licença web (webfont). Enquanto isso, use substitutas próximas:

| Fonte do manual | Substituta gratuita | Observação |
|---|---|---|
| Futura Bk BT | **Jost** (Google Fonts) | Geométrica no estilo Futura |
| Gotham Book | **Montserrat** (Google Fonts) | Geométrica ampla, próxima da Gotham |

```css
:root {
  --font-display: "Domine", Georgia, "Times New Roman", serif;
  --font-subtitle: "Futura Bk BT", "Jost", "Century Gothic", sans-serif;
  --font-body: "Gotham Book", "Gotham", "Montserrat", "Helvetica Neue", Arial, sans-serif;
}
```

Google Fonts (substitutas e Domine):

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Domine:wght@400;500;600;700&family=Jost:wght@400;500&family=Montserrat:wght@400;500;600&display=swap" rel="stylesheet">
```

### 3.3 Escala tipográfica 🟡

Escala fluida, base 16px, razão aproximada 1,25.

| Token | Tamanho | Line-height | Fonte | Peso | Uso |
|---|---|---|---|---|---|
| `--text-display` | `clamp(2.5rem, 5vw + 1rem, 4.5rem)` | 1.1 | Domine | 700 | Título da página inicial |
| `--text-h1` | `clamp(2rem, 3vw + 1rem, 3.25rem)` | 1.15 | Domine | 700 | Título de página |
| `--text-h2` | `clamp(1.625rem, 2vw + 1rem, 2.25rem)` | 1.2 | Domine | 600 | Título de seção |
| `--text-h3` | `1.375rem` | 1.3 | Domine | 600 | Subseção, títulos de cartão |
| `--text-subtitle` | `1.125rem` | 1.4 | Futura/Jost | 400–500 | Subtítulos, slogan |
| `--text-body` | `1rem` (16px) | 1.65 | Gotham/Montserrat | 400 | Texto corrido |
| `--text-body-lg` | `1.125rem` | 1.65 | Gotham/Montserrat | 400 | Texto de introdução |
| `--text-small` | `0.875rem` | 1.5 | Gotham/Montserrat | 400 | Legendas, notas |

### 3.4 Regras de uso 🟡

- Títulos em **sentence case** (só a primeira letra maiúscula). Reservar caixa alta para elementos curtos onde a marca já a usa, como palavras-chave em painéis institucionais.
- Comprimento de linha do texto corrido: **60–75 caracteres** (`max-width: 68ch`).
- Alinhamento de texto corrido: à esquerda. Centralizado só para títulos curtos e chamadas.
- Não usar mais de dois pesos por família em uma mesma tela.
- Não alterar a fonte da marca (regra do manual). Nas peças, manter apenas as três famílias institucionais.

---

## 4. Logotipo

### 4.1 Versões 🟢

| Versão | Quando usar | Arquivo sugerido |
|---|---|---|
| **Principal** (vertical, com violino, "Associação Cultural / Cordas de Rio Preto") | Cabeçalho da home, capas, fachadas, materiais com espaço | `logo-principal.svg` |
| **Secundária** (horizontal, mais fina) | Formatos finos e retangulares: canetas, fachadas, assinaturas de e-mail. No site: barra de navegação compacta | `logo-secundaria.svg` |
| **Fundo escuro** (versão em off-white e dourado) | Sobre azul ACCORP ou fundos escuros | `logo-fundo-escuro.svg` |

Regras gerais 🟢:
- Nenhuma alteração nas proporções dos elementos ou na relação entre eles.
- O logotipo deve ser reproduzido sempre a partir do arquivo digital fornecido ou de artes-finais originais.

> **Importante para o desenvolvimento:** o manual em PDF não fornece os arquivos do logotipo. Solicite ao designer os arquivos vetoriais (SVG) de cada versão, e uma versão em PNG para favicon e redes sociais.

### 4.2 Margem de segurança 🟢

O "o" minúsculo do logotipo é a unidade de proteção. Nenhum outro elemento (texto, imagem, borda) pode invadir essa área ao redor da marca.

```css
/* Tokens 🟡: --logo-x = altura do "o" no logo renderizado. Ajuste conforme o SVG final. */
.logo {
  --logo-x: 0.25em; /* placeholder: substituir pelo valor medido no arquivo */
  padding: calc(var(--logo-x) * 1);
}
```

### 4.3 Dimensões mínimas 🟢

Medidas de impressão do manual (largura mínima da marca):

| Versão | Largura mínima (impressão) |
|---|---|
| Principal (vertical, com assinatura) | 3 cm |
| Vertical reduzida (violino + ACCORP) | 2,3 cm |
| Horizontal | 1,8 cm |
| Horizontal reduzida | 1,4 cm |

Equivalentes aproximados em tela 🟡 (96 dpi, 1 cm ≈ 38 px), com folga para legibilidade:

| Versão | Mínimo em tela |
|---|---|
| Principal | 120 px de largura |
| Vertical reduzida | 92 px |
| Horizontal | 72 px |
| Horizontal reduzida | 56 px |

Abaixo desses tamanhos, trocar para a versão reduzida seguinte. Nunca simplesmente diminuir.

### 4.4 Usos incorretos 🟢

Nunca:
- alterar as cores da marca;
- comprimir a marca;
- esticar a marca;
- girar a marca;
- alterar a fonte;
- colocar a versão dourada em fundos escuros de cores próximas (por exemplo, azul muito escuro com dourado escuro sem contraste).

```css
.logo img { height: auto; width: 100%; max-width: none; object-fit: contain; }
/* Sempre definir só largura OU altura, nunca ambas com proporção diferente. */
```

### 4.5 Escolha da versão por fundo 🟡

| Fundo | Versão do logotipo |
|---|---|
| Off-white / branco | Principal ou secundária (colorida: azul + dourado) |
| Azul ACCORP `#03223F` | Fundo escuro (off-white + dourado) |
| Fotografia | Usar sobre área escurecida (overlay azul) e a versão de fundo escuro |

---

## 5. Elemento gráfico: filete dourado

🟢 O manual usa um filete duplo dourado sob o cabeçalho das páginas e linhas douradas curtas como separadores em painéis institucionais (por exemplo, sob palavras-chave ou frases nas paredes).

```css
/* Filete duplo 🟡 */
.rule-double {
  border: 0;
  height: 6px;
  background:
    linear-gradient(var(--color-gold), var(--color-gold)) top / 100% 2px no-repeat,
    linear-gradient(var(--color-gold), var(--color-gold)) bottom / 100% 2px no-repeat;
}

/* Filete curto (separador de painel) 🟡 */
.rule-short {
  width: 3rem;
  height: 2px;
  background: var(--color-gold);
  border: 0;
  margin: var(--space-4) 0;
}
```

Uso: separar cabeçalho do conteúdo, encerrar blocos de frase institucional, dividir seções principais. Com moderação.

---

## 6. Espaçamento, grid e forma 🟡

O manual não define estes tokens; foram derivados para combinar com o caráter sóbrio da marca.

### 6.1 Espaçamento (base 8px)

```css
:root {
  --space-1: 0.25rem;  /* 4  */
  --space-2: 0.5rem;   /* 8  */
  --space-3: 0.75rem;  /* 12 */
  --space-4: 1rem;     /* 16 */
  --space-5: 1.5rem;   /* 24 */
  --space-6: 2rem;     /* 32 */
  --space-7: 3rem;     /* 48 */
  --space-8: 4rem;     /* 64 */
  --space-9: 6rem;     /* 96 */
  --space-10: 8rem;    /* 128 */
}
```

Espaçamento entre seções: `--space-9` no desktop, `--space-7` no mobile. Muito respiro faz parte da personalidade.

### 6.2 Grid e breakpoints

| Breakpoint | Largura | Colunas | Margem lateral |
|---|---|---|---|
| Mobile | < 640px | 4 | 20px |
| Tablet | 640–1023px | 8 | 32px |
| Desktop | 1024–1439px | 12 | 48px |
| Wide | ≥ 1440px | 12 | container máx. 1200px centralizado |

```css
.container { width: min(100% - 2.5rem, 1200px); margin-inline: auto; }
```

### 6.3 Raios e sombras

A identidade é clássica e precisa, sem cantos muito arredondados.

```css
:root {
  --radius-sm: 2px;   /* campos, tags */
  --radius-md: 4px;   /* botões, cartões */
  --radius-lg: 8px;   /* imagens, modais */
  --radius-full: 999px; /* apenas avatares */

  --shadow-sm: 0 1px 2px rgba(3, 34, 63, 0.08);
  --shadow-md: 0 6px 20px rgba(3, 34, 63, 0.10);
  --shadow-lg: 0 16px 40px rgba(3, 34, 63, 0.16);
}
```

Sombras usam o azul da marca com baixa opacidade, nunca preto puro. Preferir bordas finas (`--border-subtle`) e filetes dourados à sombra para separar elementos.

---

## 7. Componentes 🟡

Especificações-base em CSS. Ajuste conforme o framework do projeto.

### 7.1 Botões

| Variante | Fundo | Texto | Borda | Hover |
|---|---|---|---|---|
| **Primário** | `--color-navy` | `--color-cream` | nenhuma | fundo `--color-navy-90` |
| **Secundário** | transparente | `--color-navy` | 1px `--color-navy` | fundo `--color-navy-08` |
| **Destaque** (uso raro, 1 por tela) | `--color-gold` | `--color-navy` | nenhuma | fundo `--color-gold-light` |
| **Primário em fundo escuro** | `--color-gold` | `--color-navy` | nenhuma | fundo `--color-gold-light` |
| **Link** | transparente | `--color-navy` | sublinhado | texto `--color-gold-dark` |

```css
.btn {
  font-family: var(--font-body);
  font-weight: 500;
  font-size: 1rem;
  line-height: 1;
  padding: 0.875rem 1.75rem;
  border-radius: var(--radius-md);
  min-height: 44px; /* alvo de toque */
  transition: background-color .2s ease, color .2s ease;
}
.btn:focus-visible { outline: 2px solid var(--focus-ring); outline-offset: 3px; }
```

Texto de botão: verbos claros (“Matricule-se”, “Ver agenda”, “Apoiar a ACCORP”), em sentence case.

### 7.2 Cabeçalho (navegação)

- Fundo off-white (ou azul, com a versão de fundo escuro do logotipo).
- Logotipo à esquerda (versão secundária em telas pequenas, principal em telas amplas).
- Filete duplo dourado sob o cabeçalho, como nas páginas do manual.
- Link ativo: sublinhado dourado de 2px.
- Mobile: menu recolhível, itens em `--text-h3`.

### 7.3 Cartões

```css
.card {
  background: var(--bg-surface);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: var(--space-6);
}
.card--featured { border-top: 3px solid var(--color-gold); }
```

Evitar grades de cartões idênticos para tudo. Alternar cartões com blocos de texto corrido, imagens grandes e seções em azul.

### 7.4 Seções em azul (contraste)

Alternar seções off-white e azul para dar ritmo à página.

```css
.section--dark {
  background: var(--bg-inverse);
  color: var(--text-inverse);
}
.section--dark h1, .section--dark h2, .section--dark h3 { color: var(--color-cream); }
.section--dark .rule-short { background: var(--color-gold-light); }
```

### 7.5 Formulários

- Campos com fundo branco, borda `--border-subtle`, raio `--radius-sm`, altura mínima 44px.
- Foco: borda `--color-navy` + anel `--focus-ring`.
- Rótulos sempre visíveis acima do campo (não usar só placeholder).
- Erro: borda e mensagem em `--color-error`, com texto explicando como corrigir.

### 7.6 Painel de frase institucional

Inspirado nos painéis das paredes do manual: palavras-chave empilhadas em dourado sobre azul, com filete curto ao final.

```html
<aside class="panel-quote section--dark">
  <p class="panel-quote__text">Cordas<br>que unem<br>histórias.</p>
  <hr class="rule-short">
</aside>
```

```css
.panel-quote__text {
  font-family: var(--font-display);
  font-size: var(--text-h2);
  color: var(--color-gold-light);
  line-height: 1.25;
}
```

### 7.7 Rodapé

Fundo azul, logotipo de fundo escuro, links em off-white, filete dourado no topo. Contato e redes sociais em `--text-small`.

---

## 8. Imagens e iconografia 🟡

- **Fotografia:** instrumentos de cordas, alunos e professores em aula, apresentações, comunidade. Luz quente, tons de madeira, azul profundo e dourado. Evitar imagens frias, saturadas ou de banco genérico.
- **Tratamento:** para texto sobre foto, usar overlay em azul (`rgba(3, 34, 63, 0.6)` ou mais escuro) para garantir contraste.
- **Ícones:** traço fino (1.5px), cantos levemente arredondados, cor azul ou dourado. Preferir ícones ligados ao universo musical (nota, partitura, violino) em vez de ícones genéricos.
- **Textura:** o manual mostra couro, madeira e metal dourado. Se usar texturas, com muita sutileza.

---

## 9. Tom de voz e conteúdo 🟡

Frases institucionais que aparecem no manual (🟢) e podem servir de base para textos do site:

- “Cordas que unem histórias.”
- “Música forma pessoas, conecta histórias.”
- “Tradição, ensino, arte, comunidade.”
- “Mais música para um amanhã melhor.”
- “Música, conexão, tradição.”

Diretrizes de escrita:
- Linguagem acolhedora, clara e inspiradora. Falar de pessoas e de música antes de falar da instituição.
- Verbos ativos e botões específicos.
- Evitar jargão e frases grandiosas vazias.
- Mensagens de erro e vazio explicam o que aconteceu e o que fazer.

---

## 10. Acessibilidade 🟡

- Contraste mínimo AA (ver seção 2.3).
- Foco visível em todos os elementos interativos (`:focus-visible`).
- Alvos de toque de pelo menos 44×44px.
- Respeitar `prefers-reduced-motion`.
- `alt` descritivo em imagens informativas; `alt=""` em decorativas.
- Hierarquia de títulos correta (um único `h1` por página).
- Idioma: `<html lang="pt-BR">`.

```css
@media (prefers-reduced-motion: reduce) {
  * { animation: none !important; transition: none !important; scroll-behavior: auto !important; }
}
```

---

## 11. Movimento 🟡

Discreto, como a marca.
- Transições de 150–250ms em hover/foco, curva `ease`.
- No máximo uma animação de entrada de destaque por página (por exemplo, a apresentação do logotipo/filete dourado na home).
- Sem animações em cada seção ou em cada cartão.

---

## 12. Checklist de implementação

- [ ] Obter os arquivos SVG do logotipo (principal, secundária, fundo escuro) e favicon.
- [ ] Decidir sobre licença web de **Futura Bk BT** e **Gotham Book**, ou manter Jost e Montserrat como substitutas.
- [ ] Importar os tokens CSS (seções 2, 3, 6) em um único arquivo `tokens.css`.
- [ ] Validar com o responsável pela marca as cores de apoio, escala tipográfica e componentes marcados como 🟡.
- [ ] Testar contraste de todas as combinações de texto/fundo usadas.
- [ ] Verificar o logotipo em todos os tamanhos mínimos e fundos.
- [ ] Se algo se afastar do manual, registrar a decisão no manual (Notas Finais do MIV).

---

## 13. Arquivo único de tokens (pronto para copiar) 🟡

```css
:root {
  /* Cores — marca 🟢 */
  --color-navy: #03223F;
  --color-gold: #AF8A47;
  --color-cream: #FEFDF9;

  /* Cores — apoio 🟡 */
  --color-navy-90: #0F3556;
  --color-navy-70: #3A5670;
  --color-navy-20: #C9D1D9;
  --color-navy-08: #EDF0F3;
  --color-gold-dark: #8A6C34;
  --color-gold-light: #D9BE8A;
  --color-gold-10: #F5EEDF;
  --color-success: #2F6B4F;
  --color-error: #A63A32;

  /* Semânticos */
  --bg-page: var(--color-cream);
  --bg-surface: #FFFFFF;
  --bg-surface-alt: var(--color-navy-08);
  --bg-inverse: var(--color-navy);
  --text-primary: var(--color-navy);
  --text-secondary: var(--color-navy-70);
  --text-inverse: var(--color-cream);
  --text-accent: var(--color-gold-dark);
  --border-subtle: var(--color-navy-20);
  --border-accent: var(--color-gold);
  --focus-ring: var(--color-gold);

  /* Tipografia */
  --font-display: "Domine", Georgia, "Times New Roman", serif;
  --font-subtitle: "Futura Bk BT", "Jost", "Century Gothic", sans-serif;
  --font-body: "Gotham Book", "Gotham", "Montserrat", "Helvetica Neue", Arial, sans-serif;

  --text-display: clamp(2.5rem, 5vw + 1rem, 4.5rem);
  --text-h1: clamp(2rem, 3vw + 1rem, 3.25rem);
  --text-h2: clamp(1.625rem, 2vw + 1rem, 2.25rem);
  --text-h3: 1.375rem;
  --text-subtitle: 1.125rem;
  --text-body: 1rem;
  --text-body-lg: 1.125rem;
  --text-small: 0.875rem;

  /* Espaçamento */
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.5rem;
  --space-6: 2rem;
  --space-7: 3rem;
  --space-8: 4rem;
  --space-9: 6rem;
  --space-10: 8rem;

  /* Forma */
  --radius-sm: 2px;
  --radius-md: 4px;
  --radius-lg: 8px;
  --radius-full: 999px;
  --shadow-sm: 0 1px 2px rgba(3, 34, 63, 0.08);
  --shadow-md: 0 6px 20px rgba(3, 34, 63, 0.10);
  --shadow-lg: 0 16px 40px rgba(3, 34, 63, 0.16);
}

body {
  background: var(--bg-page);
  color: var(--text-primary);
  font-family: var(--font-body);
  font-size: var(--text-body);
  line-height: 1.65;
}
h1, h2, h3 { font-family: var(--font-display); color: var(--text-primary); }
```
