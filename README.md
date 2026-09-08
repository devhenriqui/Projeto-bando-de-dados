# Banco de Dados — Plataforma de Aprendizado de Bateria

Banco de dados desenvolvido para uma plataforma web voltada ao aprendizado de bateria.

O sistema permite organizar cursos, aulas e exercícios, além de acompanhar o progresso dos alunos e salvar aulas favoritas.

## Minimundo

Uma plataforma de ensino de bateria será desenvolvida para permitir que alunos aprendam a tocar o instrumento por meio de cursos, aulas e exercícios.

Para utilizar a plataforma, o aluno deverá realizar um cadastro informando seu nome, e-mail, senha e nível de conhecimento em bateria. Cada usuário terá um registro próprio no sistema.

A plataforma disponibilizará diversos cursos de bateria, sendo que cada curso possuirá um título, uma descrição, um nível de dificuldade e uma ordem de apresentação.

Cada curso será composto por várias aulas. As aulas terão título, descrição, vídeo, duração e uma ordem dentro do curso. Dessa forma, o aluno poderá acompanhar o conteúdo de maneira organizada.

As aulas também poderão possuir exercícios práticos. Cada exercício terá informações como título, descrição, nível de dificuldade e BPM inicial recomendado para a execução.

O sistema deverá registrar o progresso dos alunos. Dessa forma, será possível identificar quais aulas um determinado usuário já iniciou ou concluiu e qual é o percentual de progresso em cada aula.

O usuário também poderá adicionar aulas aos seus favoritos para encontrá-las posteriormente com mais facilidade.

Um usuário poderá acompanhar várias aulas e uma mesma aula poderá ser acompanhada por vários usuários. Da mesma forma, um usuário poderá favoritar várias aulas e uma aula poderá estar nos favoritos de vários usuários.

O banco de dados será responsável por armazenar e relacionar todas essas informações, permitindo que a aplicação apresente os conteúdos e o progresso de cada aluno de forma organizada.

## Objetivo

O objetivo deste banco de dados é fornecer uma estrutura simples para um site onde usuários possam aprender bateria de forma organizada, acompanhando sua evolução ao longo das aulas.

## Principais funcionalidades

* Cadastro de usuários
* Organização dos conteúdos por cursos
* Cadastro de aulas
* Cadastro de exercícios de bateria
* Controle de progresso dos alunos
* Sistema de aulas favoritas
* Classificação das aulas e exercícios por nível

## Estrutura do banco

### Usuários

Armazena os dados dos alunos cadastrados na plataforma.

Principais campos:

* `id_usuario`
* `nome`
* `email`
* `senha`
* `nivel`
* `criado_em`

### Cursos

Representa os cursos disponíveis na plataforma.

Principais campos:

* `id_curso`
* `titulo`
* `descricao`
* `nivel`
* `ordem`

### Aulas

Cada curso pode possuir várias aulas.

Principais campos:

* `id_aula`
* `id_curso`
* `titulo`
* `descricao`
* `video_url`
* `duracao_min`
* `ordem`

### Exercícios

Contém os exercícios utilizados durante as aulas.

Principais campos:

* `id_exercicio`
* `id_aula`
* `titulo`
* `descricao`
* `nivel`
* `bpm_inicial`

### Progresso

Registra o avanço de cada usuário nas aulas.

Principais campos:

* `id_progresso`
* `id_usuario`
* `id_aula`
* `status`
* `percentual`
* `atualizado_em`

### Favoritos

Permite que o usuário salve aulas para acessar posteriormente.

Principais campos:

* `id_favorito`
* `id_usuario`
* `id_aula`
* `criado_em`

## Relacionamentos

* Um usuário pode ter vários registros de progresso.
* Uma aula pode aparecer no progresso de vários usuários.
* Um curso pode possuir várias aulas.
* Uma aula pode possuir vários exercícios.
* Um usuário pode favoritar várias aulas.
* Uma aula pode ser favoritada por vários usuários.

## Modelo

O diagrama ER apresenta a estrutura e os relacionamentos entre as principais tabelas do banco.

## Tecnologias

Este projeto pode ser implementado utilizando:

* MySQL

## Projeto

Este banco foi planejado como parte de uma plataforma de estudos de bateria, podendo posteriormente ser integrado a uma aplicação Front-End e Back-End.

## Possíveis melhorias futuras

* Sistema de certificados
* Ranking de alunos
* Comentários nas aulas
* Avaliação dos exercícios
* Histórico de estudos
* Metas semanais
* Sistema de níveis e conquistas
* Integração com metrônomo
