# Serviços Locais — PRD

## Identificação

- **Aluno:** João Gabriel Camilo Pires
- **Projeto:** Serviços Locais

## Descrição do Projeto

O **Serviços Locais** é uma plataforma web que conecta pessoas que precisam de serviços locais a prestadores da própria região, como pedreiros, eletricistas, encanadores, diaristas, pintores e jardineiros.

A ideia é facilitar a busca por profissionais, permitindo pesquisar por categoria e localização, visualizar informações dos prestadores e salvar favoritos.

## Público-alvo

O projeto é voltado para dois públicos principais:

- Pessoas que procuram profissionais para realizar serviços locais.
- Prestadores de serviço que desejam divulgar seu trabalho na plataforma.

## Escopo

O sistema permitirá:

- Pesquisar prestadores por categoria.
- Filtrar prestadores por cidade ou bairro.
- Visualizar os dados de um prestador.
- Cadastrar novos prestadores.
- Editar cadastros.
- Excluir cadastros.
- Salvar prestadores como favoritos.
- Utilizar o CEP para auxiliar no preenchimento do endereço.
- Validar os dados dos formulários antes do envio.

## Atores do Sistema

### Visitante

Usuário que acessa a plataforma para pesquisar e visualizar prestadores de serviço.

### Prestador de Serviço

Profissional que cadastra suas informações para aparecer nas buscas da plataforma.

## Histórias de Usuário

- Como visitante, quero pesquisar prestadores por categoria para encontrar o profissional que preciso.
- Como visitante, quero filtrar prestadores por cidade ou bairro para encontrar profissionais próximos.
- Como visitante, quero visualizar os dados de um prestador para decidir se desejo entrar em contato.
- Como visitante, quero salvar prestadores como favoritos para encontrá-los novamente depois.
- Como prestador, quero cadastrar meus dados e serviços para aparecer nas buscas.
- Como prestador, quero informar meu CEP e ter parte do endereço preenchida automaticamente.
- Como prestador, quero editar meu cadastro para manter minhas informações atualizadas.
- Como prestador, quero excluir meu cadastro caso não queira mais aparecer na plataforma.
- Como usuário, quero receber mensagens de erro quando preencher algum campo incorretamente.

## Regras de Negócio

- O prestador deverá informar os dados obrigatórios para realizar o cadastro.
- O CEP informado será consultado utilizando a API ViaCEP.
- Caso o CEP seja válido, as informações de endereço disponíveis serão preenchidas automaticamente.
- Caso o CEP seja inválido, o sistema deverá informar o usuário.
- Prestadores poderão ser pesquisados por categoria e localização.
- O usuário poderá salvar prestadores como favoritos.
- Os formulários deverão validar os dados antes do envio.
- Os dados dos prestadores serão utilizados posteriormente com JSON Server durante o desenvolvimento da aplicação.
- Os favoritos serão armazenados utilizando `localStorage`.