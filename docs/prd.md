# Serviços Locais — PRD

## Identificação

- **Aluno:** João Gabriel Camilo Pires
- **Projeto:** Serviços Locais

## Descrição do Projeto

O **Serviços Locais** é uma aplicação web criada para facilitar o encontro entre pessoas que precisam de serviços e profissionais da própria região, como eletricistas, encanadores, pedreiros, diaristas, pintores e jardineiros.

A plataforma permitirá pesquisar profissionais por categoria e localização, visualizar informações dos prestadores, salvar favoritos e realizar o cadastro de novos prestadores.

## Público-alvo

O projeto possui dois públicos principais:

- **Clientes/Visitantes:** pessoas que procuram profissionais para realizar serviços locais.
- **Prestadores de Serviço:** profissionais que desejam divulgar seus serviços e aparecer nas buscas da plataforma.

## Escopo

O sistema permitirá:

- Pesquisar prestadores por categoria.
- Filtrar prestadores por cidade ou bairro.
- Visualizar uma lista de profissionais encontrados.
- Visualizar o perfil e os dados de um prestador.
- Salvar prestadores como favoritos.
- Cadastrar novos prestadores.
- Editar dados de um prestador cadastrado.
- Excluir um cadastro.
- Utilizar o CEP para auxiliar no preenchimento do endereço.
- Validar os dados inseridos nos formulários.
- Visualizar e editar informações de perfil.

## Atores do Sistema

### Cliente/Visitante

Usuário que acessa a aplicação para pesquisar, visualizar e salvar prestadores de serviço.

### Prestador de Serviço

Profissional que cadastra suas informações e serviços para aparecer nas buscas da plataforma.

## Histórias de Usuário

- Como cliente, quero pesquisar prestadores por categoria para encontrar o profissional que preciso.
- Como cliente, quero filtrar prestadores por cidade ou bairro para encontrar profissionais próximos.
- Como cliente, quero visualizar os detalhes de um prestador para decidir se desejo entrar em contato.
- Como cliente, quero salvar prestadores como favoritos para encontrá-los novamente depois.
- Como prestador, quero cadastrar meus dados e serviços para aparecer nas buscas.
- Como prestador, quero informar meu CEP e ter o endereço preenchido automaticamente para agilizar o cadastro.
- Como prestador, quero editar meu cadastro para manter minhas informações atualizadas.
- Como prestador, quero excluir meu cadastro caso não queira mais aparecer na plataforma.
- Como usuário, quero receber mensagens claras quando preencher algum campo incorretamente.

## Regras de Negócio

- O prestador deverá preencher os campos obrigatórios para concluir o cadastro.
- O CEP informado será consultado utilizando a API ViaCEP.
- Caso o CEP seja válido, os dados de endereço disponíveis serão preenchidos automaticamente.
- Caso o CEP seja inválido ou não seja encontrado, o sistema deverá informar o usuário.
- Os prestadores poderão ser pesquisados e filtrados por categoria e localização.
- O cliente poderá salvar prestadores como favoritos.
- Os formulários deverão validar os dados antes do envio.
- Os dados de categorias, prestadores e serviços serão armazenados utilizando JSON Server durante o desenvolvimento.
- Os favoritos serão armazenados utilizando o `localStorage` do navegador.