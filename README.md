# Projeto-bando-de-dados
Projeto referente a matéria de banco de dados ministrada pelo docente Fábio Penha
Banco de dados desenvolvido para uma plataforma web voltada ao aprendizado de bateria.

O sistema permite organizar cursos, aulas e exercícios, além de acompanhar o progresso dos alunos e salvar aulas favoritas.

Objetivo

O objetivo deste banco de dados é fornecer uma estrutura simples para um site onde usuários possam aprender bateria de forma organizada, acompanhando sua evolução ao longo das aulas.

Principais funcionalidades
Cadastro de usuários
Organização dos conteúdos por cursos
Cadastro de aulas
Cadastro de exercícios de bateria
Controle de progresso dos alunos
Sistema de aulas favoritas
Classificação das aulas e exercícios por nível
Estrutura do banco
Usuários

Armazena os dados dos alunos cadastrados na plataforma.

Principais campos:

id_usuario
nome
email
senha
nivel
criado_em
Cursos

Representa os cursos disponíveis na plataforma.

Principais campos:

id_curso
titulo
descricao
nivel
ordem
Aulas

Cada curso pode possuir várias aulas.

Principais campos:

id_aula
id_curso
titulo
descricao
video_url
duracao_min
ordem
Exercícios

Contém os exercícios utilizados durante as aulas.

Principais campos:

id_exercicio
id_aula
titulo
descricao
nivel
bpm_inicial
Progresso

Registra o avanço de cada usuário nas aulas.

Principais campos:

id_progresso
id_usuario
id_aula
status
percentual
atualizado_em
Favoritos

Permite que o usuário salve aulas para acessar posteriormente.

Principais campos:

id_favorito
id_usuario
id_aula
criado_em
Relacionamentos
Um usuário pode ter vários registros de progresso.
Uma aula pode aparecer no progresso de vários usuários.
Um curso pode possuir várias aulas.
Uma aula pode possuir vários exercícios.
Um usuário pode favoritar várias aulas.
Uma aula pode ser favoritada por vários usuários.
Modelo

O diagrama ER apresenta a estrutura e os relacionamentos entre as principais tabelas do banco.

Tecnologias

Este projeto pode ser implementado utilizando:

MySQL
PostgreSQL
SQL
Banco de dados relacional
Projeto

Este banco foi planejado como parte de uma plataforma de estudos de bateria, podendo posteriormente ser integrado a uma aplicação Front-End e Back-End.

Possíveis melhorias futuras
Sistema de certificados
Ranking de alunos
Comentários nas aulas
Avaliação dos exercícios
Histórico de estudos
Metas semanais
Sistema de níveis e conquistas
Integração com metrônomo
