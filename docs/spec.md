# Serviços Locais — Especificação Técnica (spec.md)

## Identificação
- **Aluno:** João Gabriel Camilo Pires
- **Projeto:** Serviços Locais

> Este documento confirma e trava as versões das tecnologias sugeridas em `docs/architecture.md`, para orientar o desenvolvimento e agentes de IA (Copilot, Cursor etc.).

## Stack Técnica — Versões Confirmadas

| Camada             | Tecnologia    | Versão      | Uso no projeto                                                  |
|--------------------|---------------|-------------|--------------------------------------------------------------------|
| CSS Framework      | Bootstrap     | 5.3.8       | Navbar, Cards (listagem de prestadores), Modal (detalhes), grid responsivo |
| JavaScript         | Vanilla JS    | ES6+        | Filtros, favoritos, chamadas assíncronas (`fetch`/`async-await`)   |
| API Pública        | ViaCEP        | v1          | Autopreenchimento de endereço via CEP no cadastro de Prestador     |
| API Fake           | JSON Server   | (definir ao iniciar o dev, ex: `json-server@0.17.x`) | Persistência de `categorias` e `prestadores`  |
| Persistência local | localStorage  | —           | Lista de prestadores favoritos do visitante                        |

## Justificativa da Escolha — Framework CSS

Avaliação do Bootstrap 5.3.8 contra os critérios definidos na Atividade 5, comparado às alternativas (Materialize, BeerCSS, Bulma):

1. **Responsividade:** grid baseado em Flexbox com breakpoints simples (`col-12 col-md-6 col-lg-4`) cobre exatamente a transição mobile → tablet → desktop já validada no protótipo Stitch, sem precisar escrever media queries manuais.
2. **Componentes e utilidades:** os três componentes que o `architecture.md` já define como substitutos do protótipo — Navbar, Cards (listagem) e Modal (detalhes do prestador) — existem prontos no framework, além de classes utilitárias (`mt-3`, `bg-primary`, `d-flex`) que agilizam ajustes de espaçamento e cor sem CSS customizado extra.
3. **Ecossistema CSS/JS:** desde a v5 o Bootstrap não depende de jQuery — o JS dos componentes interativos (Modal, Navbar colapsável) vem pronto via bundle próprio (com Popper para posicionamento), então não preciso implementar abertura/fechamento de modal na mão.
4. **Saúde do projeto (GitHub):** é o framework mais ativo entre os avaliados — release estável mais recente é a 5.3.8 (ago/2025), com uma versão 6 já em desenvolvimento ativo, o que indica manutenção contínua e baixo risco de abandono.
5. **Licença:** MIT, compatível com projeto acadêmico/open-source, sem restrição de uso.

**Comparado às alternativas:** Materialize/BeerCSS foram descartados porque o visual "Material Design" não é o que busco pro projeto (queria algo mais neutro/comercial); Bulma foi descartado porque não traz componentes JS prontos (Modal, Navbar colapsável precisariam ser implementados do zero em JS puro), o que aumentaria o escopo de código sem necessidade.

## Justificativa da Escolha — API Pública

**ViaCEP** foi escolhida porque resolve diretamente a história de usuário #6 do PRD ("Como Prestador, quero informar meu CEP e ter o endereço preenchido automaticamente"):
- **Valor comercial/funcional:** reduz o atrito no formulário de cadastro do prestador — ele digita só o CEP e número, em vez de preencher rua/bairro/cidade manualmente, o que tende a reduzir abandono de cadastro.
- **Consistência de dados:** padroniza o campo `cidade` da entidade Prestador, o que é importante porque a história de usuário #2 do PRD (filtro por cidade/bairro) depende desses dados estarem bem formatados.
- **Facilidade de uso:** não exige chave de autenticação/API key, resposta em JSON simples, documentação clara — adequada tanto pro escopo do MVP quanto pra uma eventual evolução do projeto.

## Endpoint de referência

GET https://viacep.com.br/ws/{cep}/json/

- Sucesso: retorna `logradouro`, `bairro`, `localidade` (cidade), `uf`.
- Erro (CEP inexistente): retorna `{ "erro": true }` — tratar antes de preencher os campos `cidade` e `endereco` da entidade Prestador.

## Modelo de Dados
Ver diagrama ER completo em `docs/architecture.md` (entidades `Categoria`, `Prestador`, `Servico`).

## Observações para desenvolvimento (e agentes de IA)
- Usar exclusivamente classes utilitárias e componentes nativos do Bootstrap 5.3.x (`card`, `modal`, `navbar`, `row`/`col-*`, `mt-*`, `bg-*` etc.) — não incluir jQuery.
- Incluir Bootstrap via CDN: CSS no `<head>`, JS bundle (com Popper) antes do `</body>`.
- Toda chamada à ViaCEP deve checar o campo `erro` antes de preencher os inputs do formulário de cadastro do Prestador.
- Favoritos ficam apenas no `localStorage` — não existe entidade "Favorito" no `db.json` (decisão já registrada no PRD/architecture).