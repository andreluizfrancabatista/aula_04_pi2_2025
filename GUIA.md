# 📝 Roteiro Passo a Passo – API de Games

## 1️⃣ Preparação do ambiente

* Crie uma pasta para o projeto.
* Inicialize um projeto Node.js.
* Instale as dependências necessárias (**express, mongoose, dotenv, cors**).
* Configure o **.gitignore** para não versionar o `.env` e a pasta `node_modules`.

---

## 2️⃣ Estrutura do projeto

Organize o projeto em pastas, por exemplo:

* **`src/models`** → Schema do banco de dados.
* **`src/controllers`** → Regras de negócio (funções que lidam com os dados).
* **`src/routes`** → Definição das rotas da API.
* **`src/server.js`** → Inicialização do servidor.
* **`src/db.js`** → Arquivo para conectar ao MongoDB.

---

## 3️⃣ Variáveis de ambiente

* Crie o arquivo `.env` com:

  * A string de conexão do MongoDB Atlas.
  * A porta da aplicação.
* Crie também um `.env.example` (com placeholders, sem dados reais).

---

## 4️⃣ Banco de dados (MongoDB Atlas)

* Configure o cluster no **MongoDB Atlas**.
* Pegue a **string de conexão**.
* No arquivo de conexão (`db.js`), configure para que a aplicação se conecte ao banco usando a variável do `.env`.

---

## 5️⃣ Definição do Schema (Games)

* No diretório `models`, crie um **Schema simples** com os campos:

  * título (string)
  * gênero (string)
  * plataforma (string)
  * lançamento (número)
* Defina quais campos são obrigatórios.

---

## 6️⃣ Controllers (lógica de negócio)

Implemente funções para:

* Criar um novo game.
* Listar todos os games.
* Buscar game por ID.
* Atualizar game existente.
* Deletar game.

Cada função deve lidar com possíveis erros e, se necessário, encaminhar para o middleware de erro.

---

## 7️⃣ Rotas

* No diretório `routes`, defina as rotas da API.
* As rotas devem chamar as funções criadas no controller.
* Agrupe todas sob o prefixo `/games`.

Exemplo (sem código):

* `POST /games` → cria um game.
* `GET /games` → lista todos os games.
* `GET /games/:id` → busca game específico.
* `PUT /games/:id` → atualiza um game.
* `DELETE /games/:id` → remove um game.

---

## 8️⃣ Middlewares

* Configure **middlewares globais** (JSON, CORS).
* Implemente um **middleware de tratamento de erros** que:

  * Diferencie erros de validação.
  * Trate IDs inválidos.
  * Retorne erro genérico para casos inesperados.
* (Opcional para bônus) Adicione um **middleware de log** que mostre no console cada requisição recebida.

---

## 9️⃣ Servidor

* No arquivo `server.js`:

  * Configure os middlewares globais.
  * Conecte ao banco.
  * Importe as rotas.
  * Crie a rota inicial (`/`) para health-check.
  * Configure o middleware de erros.
  * Inicie o servidor na porta definida no `.env`.

---

## 🔟 Testes da API

* Use Postman ou Insomnia para testar as rotas:

  * Criar (POST).
  * Listar todos (GET).
  * Buscar por ID (GET).
  * Atualizar (PUT).
  * Deletar (DELETE).
* Salve ou exporte as requisições de teste.

---

## 📌 Entregáveis

* Repositório no GitHub com:

  * Código completo.
  * `.env.example`.
  * `README.md` explicando como rodar a aplicação.
* Export ou prints do Postman.
* Relatório curto explicando as funcionalidades e os middlewares.

---

Quer que eu também prepare uma **rubrica de avaliação (com pesos por critério: CRUD, middlewares, organização, etc.)** para você usar na correção?
