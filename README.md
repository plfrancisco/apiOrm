# API ORM

![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![status](https://img.shields.io/badge/status-em%20andamento-yellow)

Base de estudo de Prisma ORM com TypeScript e MySQL, desenvolvida na
disciplina de Banco de Dados Não Relacional do 3° semestre de Tecnologia em
Sistemas para Internet (TSI). Por enquanto o projeto contém a configuração
do Prisma, o modelo de dados e a migration inicial; as rotas da API ainda
não foram implementadas.

## Sumário

- [Visão geral](#visão-geral)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Como executar](#como-executar)
- [Stack técnica](#stack-técnica)
- [Autor](#autor)

## Visão geral

**Modelo `Alunos`**

| Campo | Tipo | Observações |
|---|---|---|
| `id` | Int | Chave primária, autoincremento |
| `nome` | String | |
| `email` | String | Único |
| `idade` | Int | |
| `criadoEm` | DateTime | Preenchido automaticamente |

## Estrutura do projeto

```
apiOrm/
├── prisma/
│   ├── migrations/
│   └── schema.prisma
├── prisma.ts            # instância do Prisma Client
├── prisma7.config.ts
└── .env.example
```

## Como executar

Pré-requisitos: Node.js 20+ e MySQL em execução.

```bash
git clone https://github.com/plfrancisco/apiOrm.git
cd apiOrm

# Instalar dependências
npm install

# Configurar o ambiente (ajuste a DATABASE_URL)
cp .env.example .env

# Aplicar a migration e gerar o Prisma Client
npx prisma migrate dev
npx prisma generate
```

## Stack técnica

Node.js · TypeScript · Prisma ORM 7 · MySQL · tsx

## Autor

**Pedro Lucas Francisco**
