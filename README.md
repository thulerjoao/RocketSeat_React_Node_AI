# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week)** da **Rocketseat**.

## 📋 Descrição

API REST desenvolvida em Node.js com TypeScript, utilizando Fastify como framework web e PostgreSQL como banco de dados.

## 🛠️ Tecnologias Utilizadas

### Backend
- **Node.js** - Runtime JavaScript
- **TypeScript** - Linguagem de programação
- **Fastify** - Framework web rápido e eficiente
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **pgvector** - Extensão para vetores no PostgreSQL
- **Zod** - Validação de schemas

### Ferramentas de Desenvolvimento
- **Drizzle Kit** - CLI para migrações e seeds
- **Docker Compose** - Containerização do banco de dados

## 🏗️ Arquitetura

O projeto segue uma arquitetura modular com:

- **Routes** - Endpoints da API
- **Database** - Configuração e schemas do banco
- **Environment** - Validação de variáveis de ambiente

## 🚀 Setup e Configuração

### Pré-requisitos
- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

### Instalação

1. **Clone o repositório**
```bash
git clone <repository-url>
cd service
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

4. **Inicie o banco de dados**
```bash
docker-compose up -d
```

5. **Execute as migrações e seeds**
```bash
npx drizzle-kit migrate
```

5. **popule o banco com os seed**
```bash
npm run db:seed
```

6. **Inicie o servidor**
```bash
# Desenvolvimento
npm run dev

# Produção
npm start
```

## 📡 Endpoints

- `GET /health` - Health check
- `GET /rooms` - Lista todas as salas

## 🗄️ Banco de Dados

O projeto utiliza PostgreSQL com a extensão pgvector para operações com vetores, configurado via Docker Compose.

## 📝 Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento com hot reload
- `npm start` - Inicia o servidor em modo produção
- `npm run db:seed` - Executa os seeds do banco de dados 