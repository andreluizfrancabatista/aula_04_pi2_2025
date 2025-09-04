# Atividade Avaliativa 02 
# 🎮 API de Games

## 📌 Contexto

Você foi contratado para desenvolver uma **API REST** para gerenciar uma coleção de **games**.
O sistema deverá permitir que usuários cadastrem, consultem, atualizem e removam informações de jogos, de forma organizada e segura.

---

## 📚 Requisitos da Atividade

### 🔹 Estrutura do Projeto

* Criar uma aplicação **Node.js** utilizando o **Express.js**.
* Usar variáveis de ambiente com o pacote **dotenv**.
* Conectar a aplicação ao banco de dados **MongoDB Atlas**.
* Estruturar o projeto em pastas (ex.: `models`, `controllers`, `routes`, etc).

### 🔹 Banco de Dados

* Criar um **Schema simples** para uma coleção de **games**, com pelo menos os seguintes campos:

  * `titulo` (string, obrigatório)
  * `genero` (string, obrigatório)
  * `plataforma` (string, obrigatório)
  * `lancamento` (número, obrigatório)

### 🔹 Funcionalidades (CRUD)

A API deve permitir:

1. **Criar** um novo game.
2. **Listar** todos os games cadastrados.
3. **Buscar** um game pelo seu ID.
4. **Atualizar** as informações de um game existente.
5. **Deletar** um game pelo ID.

### 🔹 Middlewares

* Utilizar **middlewares globais** (ex.: `express.json()`, `cors`).
* Implementar **middleware de erro centralizado** para tratar erros de:

  * Validação de dados.
  * IDs inválidos.
  * Erros internos do servidor.
* (Opcional para bônus) Criar um middleware específico para registrar (fazer um log) cada requisição recebida.

---

## 📌 Entregáveis

1. **Repositório no GitHub** com:

   * Código completo da aplicação.
   * Arquivo `.env.example` (com placeholders, sem expor credenciais reais).

2. **API funcional**, com as rotas testadas (POSTMAN).

   * Print ou exportação das requisições utilizadas nos testes.

3. **Readme.md** deve conter:

   * Descrição das funcionalidades implementadas.
   * Explicação dos middlewares criados.
   * Desafios encontrados e como foram resolvidos.
   * Instruções claras no `README.md` para rodar o projeto.

---

## 🎯 Critérios de Avaliação

* Funcionamento correto do CRUD.
* Conexão com MongoDB Atlas e uso de `.env`.
* Organização do código em pastas (boa arquitetura).
* Implementação correta dos middlewares.
* Clareza do `README.md`.
---

Quer que eu monte também um **roteiro passo a passo para os alunos seguirem (sem código, só guia)**, ou você prefere deixar aberto para ver como eles resolvem por conta própria?
