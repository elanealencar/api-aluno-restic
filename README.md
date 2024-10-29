# API de Gerenciamento de Alunos 🚀

Este projeto é uma API RESTful desenvolvida em Node.js e Express.js para gerenciar uma lista de alunos, com operações de CRUD (Criar, Ler, Atualizar e Deletar) mantidas em memória. Esta API foi projetada para fins de aprendizado de desenvolvimento de APIs e consolidar os conceitos de HTTP e métodos REST.

## Índice 📑

- [Funcionalidades](#funcionalidades-)
- [Instalação](#instalação-)
- [Como Usar](#como-usar-)
- [Endpoints da API](#endpoints-da-api-)
  - [POST /alunos](#post-alunos)
  - [GET /alunos](#get-alunos)
  - [PUT /alunosid](#put-alunosid)
  - [DELETE /alunosid](#delete-alunosid)
- [Estrutura do Projeto](#estrutura-do-projeto-)
- [Tecnologias Utilizadas](#tecnologias-utilizadas-)
- [Contribuição](#contribuição-)

## Funcionalidades ✨

- Adicionar um novo aluno.
- Visualizar todos os alunos cadastrados.
- Atualizar dados de um aluno específico.
- Remover um aluno da lista.

## Instalação ⚙️

1. **Clone este repositório**:
   ```bash
   git clone <URL_DO_REPOSITORIO>

2. **Acesse o diretório do projeto:**

   ```bash
   cd <NOME_DO_DIRETORIO>

3. **Instale as dependências:**

   ```bash
   npm install

4. **Inicie o servidor:**

   ```bash
   node server.js

O servidor será executado em http://localhost:3000. Certifique-se de que nenhuma outra aplicação está usando essa porta.

## Como Usar 👨‍💻
Para testar os endpoints, use uma ferramenta como Postman.

## Endpoints da API 🔗

**POST /alunos**

Descrição: Cria um novo aluno.

- URL: /alunos
- Método: POST
- Corpo da Requisição:
   ```json
   {
  "nome": "Nome do Aluno",
  "email": "email@example.com",
  "nome_curso": "Curso"
   }

- Resposta: Retorna o aluno criado com um ID gerado.

**GET /alunos**

Descrição: Retorna todos os alunos cadastrados.

- URL: /alunos
- Método: GET
- Resposta: Array com todos os alunos cadastrados.
  
**PUT /alunos/**

Descrição: Atualiza os dados de um aluno específico.

- URL: /alunos/:id
- Método: PUT
- Parâmetro: id - ID do aluno que será atualizado

- Corpo da Requisição:
   ```json
   {
  "nome": "Novo Nome",
  "email": "novoemail@example.com",
  "nome_curso": "Novo Curso"
   }

- Resposta: Retorna o aluno atualizado ou null se o ID não for encontrado.

**DELETE /alunos/**

Descrição: Remove um aluno específico.

- URL: /alunos/:id
- Método: DELETE
- Parâmetro: id - ID do aluno que será removido
- Resposta: 204 No Content se a exclusão for bem-sucedida.

## Estrutura do Projeto 📂

**```bash
├── server.js                   # Configuração do servidor e rotas da API
└── repositories
  └── alunosRepository.js      # Funções de manipulação de dados dos alunos (CRUD)**


## Tecnologias Utilizadas 🛠️
- Node.js
- Express.js
- UUID - Para geração de IDs únicos

## Contribuição 🤝
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com melhorias e correções.

1. Faça um fork do projeto
2. Crie uma branch para sua feature (git checkout -b feature/nova-feature)
3. Faça commit das suas alterações (git commit -m 'Adiciona nova feature')
4. Faça push para a branch (git push origin feature/nova-feature)
5. Abra um Pull Request
