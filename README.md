# Serviços Locais

## Identificação
- **Autor:** João Gabriel Camilo Pires

## Descrição do Projeto
Plataforma web que conecta visitantes a prestadores de serviços locais (pedreiro, eletricista, encanador, diarista, pintor, jardineiro etc.). O usuário pesquisa por categoria e cidade/bairro, visualiza o perfil de cada prestador e pode salvar favoritos. Prestadores podem se cadastrar para aparecer nas buscas.

## Prototipação no Figma
[link do Figma]

## Design System
[link do Design System]

## Framework CSS
Bootstrap

## Dependências
- Vanilla JavaScript (ES6+)
- Fetch API / async-await
- ViaCEP (API pública de endereços)
- JSON Server (API fake para persistência)

## Link para o site em produção
[link do GitHub Pages]

## Checklist de Funcionalidades
- [ ] Página de busca/listagem de prestadores
- [ ] Filtro por categoria
- [ ] Filtro por cidade/bairro
- [ ] Página de cadastro de prestador
- [ ] Validação de formulário (campos obrigatórios e regex)
- [ ] Autopreenchimento de endereço via CEP (ViaCEP)
- [ ] Página/modal de detalhes do prestador
- [ ] Favoritar prestador (localStorage)
- [ ] Edição de cadastro de prestador
- [ ] Exclusão de cadastro de prestador
- [ ] Integração com JSON Server (categorias e prestadores)
- [ ] Deploy no GitHub Pages

## Instruções de Execução

### Pré-requisitos
- [Node.js](https://nodejs.org/) instalado
- Git instalado

### Passos
```bash
# 1. Clone o repositório
git clone https://github.com/1liroujon/servicos-locais.git
cd servicos-locais

# 2. Instale o JSON Server (API fake)
npm install -g json-server

# 3. Suba a API fake (na raiz do projeto, com um arquivo db.json)
json-server --watch db.json --port 3000

# 4. Abra o index.html no navegador
# (recomenda-se usar a extensão "Live Server" do VS Code)
```

## Telas da Aplicação
<!-- adicionar prints das telas aqui -->

---

## Checklist de Indicadores de Desempenho (ID)

### RA1 - Utilizar Frameworks CSS para estilização de elementos HTML e criação de layouts responsivos
- [ ] ID 01 - Prototipa interfaces adaptáveis para no mínimo os tamanhos de tela mobile e desktop, usando ferramentas de design tradicionais (Figma, Quant UX ou Sketch) ou IA (Stitch).
- [ ] ID 02 - Implementa layout responsivo com Framework CSS (Bootstrap, Materialize) usando Flexbox ou Grid do próprio framework.
- [ ] ID 03 - Implementa layout responsivo com CSS puro, usando Flexbox ou Grid Layout.
- [ ] ID 04 - Utiliza componentes prontos de um Framework CSS (ex.: card, button) e componentes JavaScript do framework (ex.: modal, carousel).
- [ ] ID 05 - Cria layout fluido usando unidades relativas (vw, vh, %, em, rem) no lugar de unidades fixas (px).
- [ ] ID 06 - Aplica um Design System consistente (cores, tipografia, padrões de componentes) em toda a aplicação.
- [ ] ID 07 - Utiliza Sass (SCSS) com ou sem framework, aplicando variáveis, mixins e funções para modularizar o código.
- [ ] ID 08 - Aplica tipografia responsiva (media queries mobile first) ou tipografia fluida (função clamp() + unidades relativas).
- [ ] ID 09 - Aplica técnicas de responsividade de imagens usando CSS (object-fit, containers com unidades relativas).
- [ ] ID 10 - Otimiza imagens usando formatos modernos (WebP) e carregamento adaptativo (srcset, picture, ou parâmetros do Cloudinary).

### RA2 - Realizar tratamento de formulários e aplicar validações customizadas no lado cliente
- [ ] ID 11 - Implementa validação HTML nativa (campos obrigatórios, tipos, limites de caracteres) com mensagens de erro/sucesso no lado cliente.
- [ ] ID 12 - Aplica expressões regulares (REGEX) para validações customizadas (e-mail, telefone, datas, etc.)
- [ ] ID 13 - Utiliza elementos de seleção em formulários (checkbox, radio, select) para coleta de dados.
- [ ] ID 14 - Implementa leitura e escrita no Web Storage (localStorage/sessionStorage) para persistir dados localmente.

### RA3 - Aplicar ferramentas para otimização do processo de desenvolvimento web
- [ ] ID 15 - Configura ambiente com Node.js e NPM para gerenciamento de pacotes e dependências.
- [ ] ID 16 - Utiliza boas práticas de versionamento no Git/GitHub (branch main ou branches específicos, uso de .gitignore).
- [ ] ID 17 - Mantém um README.md padronizado, conforme template da disciplina, com checklist preenchido.
- [ ] ID 18 - Organiza arquivos do projeto de forma modular, seguindo padrão de exemplo fornecido.
- [ ] ID 19 - Configura linters e formatadores (ESLint, Prettier) para manter qualidade e padronização do código.

### RA4 - Aplicar bibliotecas de funções e componentes em JavaScript para aprimorar a interatividade de páginas web
- [ ] ID 20 - Utiliza jQuery para manipulação do DOM e interatividade (eventos, animações, manipulação de elementos)
- [ ] ID 21 - Integra e configura um plugin jQuery relevante (ex.: jQuery Mask Plugin) ou outra biblioteca de funções.

### RA5 - Efetuar requisições assíncronas para uma API fake e APIs públicas, permitindo a obtenção e manipulação de dados dinamicamente
- [ ] ID 22 - Realiza requisições assíncronas para uma API fake (ex.: JSON Server) para persistir dados de um formulário.
- [ ] ID 23 - Realiza requisições assíncronas para uma API fake para exibir dados na página.
- [ ] ID 24 - Realiza requisições assíncronas para APIs públicas reais (OpenWeather, ViaCEP etc.), exibindo os dados e tratando erros.