# chechefullstacksystem
# 🏫 Creche FullStack System

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Node.js](https://img.shields.io/badge/Node.js-v14+-green)
![MongoDB](https://img.shields.io/badge/MongoDB-v4+-green)
![License](https://img.shields.io/badge/license-MIT-blue)

Sistema completo de gestão para creches e escolas infantis. Desenvolvido com **Node.js**, **Express**, **MongoDB** e **React**.

---

## 📋 Sobre o Projeto

API RESTful para gestão completa de creche, com módulos para:

- 👑 **Administração** - Gestão geral do sistema
- 📋 **Secretário** - Gestão administrativa diária
- 👨‍🏫 **Educador** - Gestão de turmas e alunos
- 👨‍👩‍👦 **Responsável** - Acompanhamento dos alunos
- 👶 **Alunos** - CRUD completo
- 🏫 **Turmas** - CRUD completo
- 📋 **Frequência** - Controle de presença
- 💰 **Pagamentos** - Gestão financeira
- 📊 **Dashboard** - Métricas e relatórios

---

## 🎯 Módulos do Sistema

| Módulo | Descrição | Status |
|--------|-----------|--------|
| **Autenticação** | Login, registro e recuperação de senha | ✅ |
| **Administração** | Gestão completa do sistema | ✅ |
| **Secretário** | Gestão administrativa diária | ✅ |
| **Educador** | Gestão de turmas e alunos | ✅ |
| **Responsável** | Acompanhamento dos alunos | ✅ |
| **Alunos** | CRUD completo | ✅ |
| **Turmas** | CRUD completo | ✅ |
| **Frequência** | Controle de presença | ✅ |
| **Pagamentos** | Gestão financeira | ✅ |
| **Dashboard** | Métricas e relatórios | ✅ |

---

## 🛠️ Tecnologias Utilizadas

### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)

---

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

| Ferramenta | Versão | Download |
|------------|--------|----------|
| **Node.js** | v14+ | [https://nodejs.org/](https://nodejs.org/) |
| **MongoDB** | v4+ | [https://www.mongodb.com/](https://www.mongodb.com/) |
| **Git** | v2+ | [https://git-scm.com/](https://git-scm.com/) |
| **NPM** | v6+ | (já vem com Node.js) |

---

## 🚀 Instalação e Execução

#Configuração do banco de dados MongoDB

Nome do banco de dados: `crechesystemfullstack`

## Coleções e campos

O aplicativo usa estas coleções do MongoDB:

- `usuários`
  - `nome`, `email`, `senha`, `telefone`, `foto`, `tipo`, `status`, carimbos de data e hora
- `alunos`
  - `nome`, `data_nascimento`, `turma`, `responsavel`, `contato`, `ativo`, timestamps
- `educadores`
  - `nome`, `email`, `funcao`, `especialidade`, `telefone`, `turmas`, `ativo`, timestamps
- `turmas`
  - `nome`, `descricao`, `educador`, `alunos`, `capacidade`, `sala`, `horario`, `ativo`, timestamps
- `frequências`
  - `aluno`, `dados`, `status`, `justificativa`, `registrado_por`, carimbos de data/hora
- `pagamentos`
  - `aluno`, `valor`, `mes`, `ano`, `tipo`, `observacao`, `status`, `data_pagamento`, `metodo_pagamento`, timestamps
- `administradores`
  - `nome`, `email`, `senha`, `role`, `status`, carimbos de data e hora

Os modelos Mongoose definem o esquema ativo e os nomes das coleções. O arquivo `src/config/database.schema.js` documenta a estrutura do banco de dados usada pela configuração da primeira execução.

## Criação do banco de dados pela primeira vez

Execute estes comandos a partir de `backend/minha-api`:

```bash
npm install
npm run db:create
npm run dev
```

`npm run db:create` conecta-se ao URI do MongoDB em `.env`, cria as coleções e índices necessários e inicializa o primeiro usuário administrador, caso ele ainda não exista.

## Variáveis ​​de ambiente

Obrigatórias:

```bash
MONGO_URI=mongodb+srv://<usuário>:<senha>@<cluster>/<banco de dados>?retryWrites=true&w=majority
JWT_SECRET=<segredo aleatório>
```

Opcional: sobrescrita da senha de administrador na primeira execução:

```bash
DEFAULT_ADMIN_NAME=Administrador
DEFAULT_ADMIN_EMAIL=admin@creche.com
DEFAULT_ADMIN_PASSWORD=Admin@123456
```

Altere a senha padrão do administrador após o primeiro login.

## Login de administrador padrão

Se não houver um administrador, a configuração cria:

```text
Email: admin@creche.com
Senha: Admin@123456
Função: admin
```




Instalar as dependências
npm install

att:antes de tudo criar a base de no mongoose e conetar com a sua,


