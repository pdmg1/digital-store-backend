---

````markdown
# Digital Store Backend

API backend para a loja digital, construída com Node.js e Express.  
Este projeto serve para gerenciar usuários, produtos e categorias com funcionalidades básicas de autenticação e CRUD.

---

## 🚀 Tecnologias Utilizadas

- Node.js
- Express
- Sequelize (ORM para banco de dados)
- MySQL (ou outro banco relacional compatível)
- JWT para autenticação
- Docker (opcional, para ambiente de desenvolvimento)
- Jest (para testes)

---

## 📦 Como Rodar o Projeto Localmente

### 1. Clone o repositório

```bash
git clone https://github.com/pdmg1/digital-store-backend.git
cd digital-store-backend
````

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure as variáveis de ambiente

Copie o arquivo de exemplo `.env.example` para `.env` e preencha as configurações (ex: conexão com banco, secret do JWT):

```bash
cp .env.example .env
```

### 4. Prepare o banco de dados

Certifique-se que o banco de dados está rodando e execute as migrations (ou scripts de criação) para configurar as tabelas.

### 5. Execute o projeto

```bash
npm run dev
```

Por padrão, o servidor iniciará em:

```
http://localhost:3001
```

---

## 🔧 Testes

Para rodar os testes automatizados (se existirem):

```bash
npm test
```

---

## 🛠 Estrutura do Projeto

* `src/controllers/` — Lógica dos endpoints
* `src/models/` — Modelos do banco (Sequelize)
* `src/routes/` — Definição das rotas
* `src/middleware/` — Middlewares como autenticação JWT
* `src/utils/` — Funções auxiliares

---

## 📋 Rotas Principais (exemplos)

| Método | Rota             | Descrição                           |
| ------ | ---------------- | ----------------------------------- |
| POST   | `/auth/login`    | Autenticação e geração de token JWT |
| POST   | `/auth/register` | Cadastro de usuário                 |
| GET    | `/users`         | Listar usuários (autenticado)       |
| GET    | `/products`      | Listar produtos                     |
| POST   | `/products`      | Criar produto (autenticado)         |
| GET    | `/categories`    | Listar categorias                   |

---

## 🛡️ Autenticação

* Use o endpoint `/auth/login` para obter o token JWT
* Envie o token no header `Authorization` para rotas protegidas:

```
Authorization: Bearer SEU_TOKEN_AQUI
```

---

## 🚀 Docker (Opcional)

Se o projeto suporta Docker, rode:

```bash
docker-compose up -d
```

Para iniciar containers de banco e servidor.

---

## 🤝 Contribuição

Sinta-se à vontade para abrir issues ou pull requests.

---

## 📄 Licença

MIT License

---
