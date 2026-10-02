# API ORM

Base de estudo de **Prisma ORM** com TypeScript e MySQL, com o modelo `Alunos` e a migration inicial já configurados.

Projeto da disciplina de Banco de Dados Não Relacional do 3° semestre de Tecnologia em Sistemas para Internet (TSI).

> **Status:** em desenvolvimento. Por enquanto o projeto contém a configuração do Prisma, o modelo de dados e a migration; as rotas da API ainda não foram implementadas.

## Tecnologias

- [Node.js](https://nodejs.org/) + [TypeScript](https://www.typescriptlang.org/)
- [Prisma ORM 7](https://www.prisma.io/) com adapter MariaDB
- MySQL
- [tsx](https://tsx.is/)

## Pré-requisitos

- Node.js 20 ou superior
- MySQL em execução

## Como executar

```bash
# 1. Instalar as dependências
npm install

# 2. Configurar o ambiente
cp .env.example .env   # ajuste a DATABASE_URL com seus dados do MySQL

# 3. Aplicar a migration e gerar o Prisma Client
npx prisma migrate dev
npx prisma generate
```

## Variáveis de ambiente

| Variável | Descrição | Exemplo |
| --- | --- | --- |
| `DATABASE_URL` | String de conexão com o MySQL | `mysql://usuario:senha@localhost:3306/apiorm` |

## Modelo de dados

**Alunos**

| Campo | Tipo | Observações |
| --- | --- | --- |
| `id` | Int | Chave primária, autoincremento |
| `nome` | String | |
| `email` | String | Único |
| `idade` | Int | |
| `criadoEm` | DateTime | Preenchido automaticamente |

## Estrutura

```text
apiOrm/
├── prisma/
│   ├── migrations/
│   └── schema.prisma
├── prisma.ts          # instância do Prisma Client
└── prisma7.config.ts
```

## Autor

Pedro Lucas Francisco de Almeida
