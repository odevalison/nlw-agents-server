# NLW Agents

Projeto desenvolvido durante o evento NLW da Rocketseat.

## 🏛️ Arquitetura

O projeto segue uma arquitetura modular com:

- **Separação de responsabilidades** entre rotas, schemas e conexão com banco
- **Validação de schemas** com Zod para type safety
- **ORM type-safe** com Drizzle para operações de banco de dados
- **Validação de variáveis de ambiente** centralizadas

## ⚙️ Setup e Configuração

### Pré-requisitos

- Node.js (versão com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd server
```

### 2. Configure o banco de dados

```bash
docker-compose up -d
```

### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Instale as dependências

```bash
npm install
```

### 5. Execute as migrations

```bash
npx drizzle-kit migrate
```

### 6. Inicie o servidor

```bash
npm run dev
```

## 🛠️ Tecnologias

- `fastify`: Framework web
- `drizzle-orm`: ORM para PostgreSQL
- `zod`: Validação de schemas
- `@fastify/cors`: Middleware CORS
- `biome`: Linter e formatter
- `typescript`: Superset JavaScript
