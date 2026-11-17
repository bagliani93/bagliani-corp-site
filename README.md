# Landing page Bagliani Corp — versão 3 (skill landing-page-design)

Construída seguindo a skill `landing-page-design` de [elayadesign/ai-design-skills](https://github.com/elayadesign/ai-design-skills).
Arquivos:

- `index.html` — a página (HTML, CSS e JavaScript juntos). Sem servidor, banco de dados ou build.
- `404.html` — página de erro com a marca. Configure na hospedagem como página 404.
- `assets/fonts/Geist-Variable.woff2` — a fonte do site, hospedada aqui mesmo (licença OFL em `OFL.txt`).
- `assets/hero.svg`, `administrativo.svg`, `operacional.svg` — as ilustrações, editáveis.
- `assets/og.png` — imagem de compartilhamento (WhatsApp, LinkedIn), 1200×630.
- `assets/favicon.svg` — ícone da aba.

## Antes de publicar (obrigatório)

1. **Endereço do site.** As meta tags apontam para `https://bagliani-corp.vercel.app`. Se usar um domínio próprio, troque esse endereço no `<head>` do `index.html` (`canonical`, `og:url`, `og:image`, `twitter:image`).
2. **Horário de atendimento** do Levi: constante `LEVI.horario` no segundo `<script>`.

## Quando tiver o conteúdo

- **Prova social no hero** (`<p class="hero-prova" hidden>`): remova `hidden` e escreva um fato real (número de clientes, um depoimento curto). Não invente.
- **Seção de depoimentos** (`<section id="prova" hidden>`): remova `hidden` e preencha os três cartões com depoimentos reais (nome, cargo, empresa).
- **Termos de uso**: a skill pede links de privacidade e termos no rodapé. Privacidade já está lá (texto factual: o site não guarda dados). Termos não foram escritos porque dependem de texto jurídico seu.

## Como funciona

- **Formulário**: monta um link `https://wa.me/5511942166994?text=...` com os dados e abre o WhatsApp. Valida campos vazios e se o contato é um telefone com DDD ou um email.
- **Levi**: chatbot por palavras-chave, sem IA externa. Textos em `LEVI.respostas`, palavras-chave em `LEVI.intencoes`.
- **Cookies**: o site não usa cookies nem rastreamento, então não precisa de aviso de cookies. Se adicionar Google Analytics ou similar, aí precisa.

## Sistema visual (resumo da skill)

- Uma fonte só: Geist. Pesos 400 a 700, sem itálico.
- Tamanhos de texto só da escala do Tailwind, aplicados pelas classes `heading-1` a `caption-5` (definidas no topo do CSS).
- Espaçamentos só da tabela: 2, 4, 8, 12, 16, 24, 32, 40, 48, 64, 80, 96 px (variáveis `--s-25` a `--s-900`).
- Fundos planos, sem gradiente (a única exceção, prevista pela skill, é o gradiente no texto do título do hero).
- Ícones Phosphor (licença MIT), embutidos no HTML.
- Movimento com a curva `cubic-bezier(.22,1,.36,1)`: menu flutuante, menu mobile em tela cheia com links entrando em sequência, seções que sobem ao rolar, tagline que acende palavra por palavra. Tudo respeita `prefers-reduced-motion`.
- Cores de fundo: azul-marinho da marca, mantido por ser pedido explícito (a skill sugere cinzas neutros; a própria skill diz que o pedido do cliente prevalece).
