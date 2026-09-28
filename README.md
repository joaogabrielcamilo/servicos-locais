# Serviços Locais

## Identificação

- **Autor:** João Gabriel Camilo Pires

## Descrição do Projeto

O **Serviços Locais** é uma plataforma web que conecta pessoas a prestadores de serviços da própria região, como pedreiros, eletricistas, encanadores, diaristas, pintores e jardineiros.

O usuário poderá pesquisar prestadores por categoria e cidade/bairro, visualizar seus dados e salvar favoritos. Prestadores também poderão se cadastrar para aparecer nas buscas.

## Prototipação (Stitch)

Protótipo desenvolvido no Google Stitch:

https://stitch.withgoogle.com/projects/7924047218329153293

## Design System

O projeto utiliza como base visual:

- Cor primária: `#E05A2B`
- Cor secundária: `#133842`
- Cor terciária: `#E2E8F0`
- Cor neutra: `#0F172A`
- Tipografia: Plus Jakarta Sans

## Framework CSS

**Bootstrap 5.3.8**

Escolhi o Bootstrap porque possui um sistema de grid responsivo fácil de usar e vários componentes prontos que serão úteis no projeto, como navbar, cards, formulários e modal.

Além disso, os componentes interativos possuem JavaScript próprio e não dependem de jQuery. O projeto também possui boa documentação, manutenção ativa e licença MIT.

## API Pública

**ViaCEP**

A ViaCEP será utilizada no cadastro de prestadores para preencher automaticamente informações de endereço a partir do CEP.

Ela foi escolhida porque é simples de utilizar, não exige chave de acesso e ajuda a manter os dados de cidade e bairro padronizados, o que também facilita os filtros da aplicação.

## Tecnologias e Dependências

- Bootstrap 5.3.8
- Vanilla JavaScript (ES6+)
- Fetch API / async-await
- ViaCEP
- JSON Server
- localStorage

## Link para o site em produção

Em andamento.

## Checklist de Funcionalidades

- [ ] Página de busca/listagem de prestadores
- [ ] Filtro por categoria
- [ ] Filtro por cidade/bairro
- [ ] Página de cadastro de prestador
- [ ] Validação de formulário
- [ ] Autopreenchimento de endereço via ViaCEP
- [ ] Página/modal de detalhes do prestador
- [ ] Favoritar prestador
- [ ] Edição de cadastro
- [ ] Exclusão de cadastro
- [ ] Integração com JSON Server
- [ ] Deploy no GitHub Pages

## Instruções de Execução

Em andamento.

## Telas da Aplicação

Em andamento.

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
- [ ] ID 10 - Otimiza imagens usando formatos modernos (WebP) e carregamento adaptativo (srcset, picture ou parâmetros do Cloudinary).

### RA2 - Realizar tratamento de formulários e aplicar validações customizadas no lado cliente

- [ ] ID 11 - Implementa validação HTML nativa (campos obrigatórios, tipos, limites de caracteres) com mensagens de erro/sucesso no lado cliente.
- [ ] ID 12 - Aplica expressões regulares (REGEX) para validações customizadas (e-mail, telefone, datas etc.).
- [ ] ID 13 - Utiliza elementos de seleção em formulários (checkbox, radio, select) para coleta de dados.
- [ ] ID 14 - Implementa leitura e escrita no Web Storage (localStorage/sessionStorage) para persistir dados localmente.

### RA3 - Aplicar ferramentas para otimização do processo de desenvolvimento web

- [ ] ID 15 - Configura ambiente com Node.js e NPM para gerenciamento de pacotes e dependências.
- [ ] ID 16 - Utiliza boas práticas de versionamento no Git/GitHub (branch main ou branches específicos, uso de .gitignore).
- [ ] ID 17 - Mantém um README.md padronizado, conforme template da disciplina, com checklist preenchido.
- [ ] ID 18 - Organiza arquivos do projeto de forma modular, seguindo padrão de exemplo fornecido.
- [ ] ID 19 - Configura linters e formatadores (ESLint, Prettier) para manter qualidade e padronização do código.

### RA4 - Aplicar bibliotecas de funções e componentes em JavaScript para aprimorar a interatividade de páginas web

- [ ] ID 20 - Utiliza jQuery para manipulação do DOM e interatividade (eventos, animações, manipulação de elementos).
- [ ] ID 21 - Integra e configura um plugin jQuery relevante (ex.: jQuery Mask Plugin) ou outra biblioteca de funções.

### RA5 - Efetuar requisições assíncronas para uma API fake e APIs públicas

- [ ] ID 22 - Realiza requisições assíncronas para uma API fake (ex.: JSON Server) para persistir dados de um formulário.
- [ ] ID 23 - Realiza requisições assíncronas para uma API fake para exibir dados na página.
- [ ] ID 24 - Realiza requisições assíncronas para APIs públicas reais (OpenWeather, ViaCEP etc.), exibindo os dados e tratando erros.