# Serviços Locais

Aplicação web para encontrar prestadores de serviço do bairro (pedreiro, eletricista, encanador, diarista, pintor e jardineiro).

**Aluno:** João Gabriel Camilo
**Etapa atual:** Entrega 2: A Casca (Layout e Framework CSS)

## Como executar

1. Abra esta pasta no VS Code.
2. No terminal, execute `npm install`.
3. Abra `index.html` com a extensão **Live Server**.

> Use o Live Server: abrindo o arquivo direto (`file://`), o navegador bloqueia os ícones do `icones.svg`.

## Tecnologias

- HTML5 semântico
- CSS3 (Flexbox, Grid, variáveis CSS, `clamp()`)
- Bootstrap 5.3.6, instalado via NPM e carregado de `node_modules` (sem CDN)
- Fonte Plus Jakarta Sans (Google Fonts)

## Estrutura

```
servicos-locais/
├── assets/
│   ├── css/style.css     # Design System e ajustes sobre o Bootstrap
│   └── img/              # Fotos (WebP + PNG de fallback), logo e ícones SVG
├── index.html            # Início: busca e categorias
├── prestadores.html      # Busca com filtros e lista de prestadores
├── prestador.html        # Detalhes do prestador
├── favoritos.html        # Prestadores favoritos
├── perfil-cliente.html   # Perfil do cliente
├── cadastro.html         # Cadastro de prestador
├── editar-perfil.html    # Edição do perfil do prestador
├── package.json
└── .gitignore
```

## Responsividade

- **Celular (< 992px):** uma coluna, menu fixo na parte inferior, filtros em painel lateral (offcanvas).
- **Desktop (≥ 992px):** menu no cabeçalho, filtros fixos na lateral, cards em 2 ou 3 colunas, detalhes e formulários em duas colunas.

## Componentes do Bootstrap utilizados

- Grid (`row`, `col-*`, `row-cols-*`) e utilitários de Flexbox/espaçamento
- Card, Button, Badge, Input group, Form controls, Form check, Select, List group
- **Componentes JavaScript:** Offcanvas (menu do perfil), Offcanvas responsivo (`offcanvas-lg`, filtros) e Modal (excluir cadastro e editar dados do cliente)

## Design System

Definido como variáveis CSS em `assets/css/style.css`:

- **Cores:** laranja `#a83301` (ação principal), azul `#41636e` (secundária), fundo `#faf8ff`, campos `#f0f1ff`, texto `#131b2e`
- **Tipografia:** Plus Jakarta Sans com tamanhos fluidos via `clamp()` (`--fs-titulo`, `--fs-subtitulo`, `--fs-secao`...)
- **Formas:** raios (`--raio`, `--raio-grande`, `--raio-pilula`) e sombras (`--sombra`, `--sombra-media`) padronizados

## Checklist

### RA1: Frameworks CSS e layouts responsivos
- [x] ID 01: Protótipo para mobile e desktop (Stitch)
- [x] ID 02: Layout responsivo com o grid/Flexbox do Bootstrap
- [x] ID 03: Layout com CSS puro usando Flexbox e Grid
- [x] ID 04: Componentes do Bootstrap (card, button) e componentes JavaScript (modal, offcanvas)
- [x] ID 05: Unidades relativas (rem, em, %, vw, vh)
- [x] ID 06: Design System consistente (cores, tipografia, componentes)
- [ ] ID 07: Sass (SCSS)
- [x] ID 08: Tipografia fluida com `clamp()` e media queries mobile first
- [x] ID 09: Imagens responsivas com `object-fit`
- [x] ID 10: Imagens em WebP com `<picture>`, `srcset` e `loading="lazy"`

### RA2: Formulários e validações
- [ ] ID 11: Validação HTML nativa com mensagens de erro/sucesso (campos `required`, `type` e `maxlength` já existem; faltam as mensagens)
- [ ] ID 12: Validações com REGEX
- [x] ID 13: Checkbox, radio e select
- [ ] ID 14: Web Storage

### RA3: Ferramentas de desenvolvimento
- [x] ID 15: Node.js e NPM
- [x] ID 16: Git com branch `main` e `.gitignore`
- [x] ID 17: README padronizado com checklist
- [x] ID 18: Arquivos organizados de forma modular
- [ ] ID 19: ESLint e Prettier

### RA4: Bibliotecas JavaScript
- [ ] ID 20: jQuery
- [ ] ID 21: Plugin jQuery

### RA5: Requisições assíncronas
- [ ] ID 22: Persistir formulário em API fake
- [ ] ID 23: Exibir dados de API fake
- [ ] ID 24: API pública (ViaCEP)

## Observações

Nesta etapa as páginas ainda não têm lógica JavaScript própria: busca, filtros, favoritos e formulários são apenas visuais. Menus e modais funcionam com o JavaScript do Bootstrap.
