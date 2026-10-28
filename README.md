# 🥝 Kiwi Estética

**Site da Kiwi Estética SPA**, desenvolvido com o objetivo de apresentar tratamentos naturais e terapias integrativas que promovem bem-estar, equilíbrio e autocuidado. A plataforma também inclui um **sistema administrativo para gerenciamento de agendamentos**.

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white)
![Sass](https://img.shields.io/badge/Sass-CC6699?style=flat-square&logo=sass&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Licença MIT](https://img.shields.io/badge/licen%C3%A7a-MIT-green?style=flat-square)

[Fluxos](#-fluxos-principais) · [Sobre](#-sobre-o-projeto) · [Funcionalidades](#-funcionalidades) · [Tecnologias](#-tecnologias-utilizadas) · [Como executar](#%EF%B8%8F-como-executar-o-projeto) · [Créditos](#-créditos-do-projeto)

---

## Em resumo

| | |
| --- | --- |
| **O que é** | Site de um SPA com catálogo de tratamentos e agendamento online |
| **Diferencial** | Painel administrativo para gerenciar os agendamentos |
| **Frontend** | React, estilizado com Bootstrap e Sass |
| **Backend** | Node.js + Express com API REST |
| **Banco de dados** | MySQL |
| **Tipo** | Projeto acadêmico fullstack feito em equipe |

---

## 📸 Fluxos principais

### Workflow do cliente

<img src="./client/public/images/fluxo-do-cliente.gif" alt="Fluxo do cliente navegando e agendando um tratamento" width="400px">

### Workflow do(a) administrador(a)

<img src="./client/public/images/fluxo-do-adm.gif" alt="Fluxo do administrador gerenciando agendamentos" width="400px">

---

## 📌 Sobre o projeto

Aplicação **fullstack** composta por:

| Camada | Tecnologia |
| --- | --- |
| Frontend | React |
| Backend | Node.js + Express |
| Banco de dados | MySQL |
| Estilização | Bootstrap e Sass |

---

## 🚀 Funcionalidades

- Catálogo de serviços categorizado
- Sistema de agendamento online
- Painel administrativo protegido
- Interface responsiva
- Integração completa frontend + backend
- Envio de confirmação via WhatsApp para cliente e profissional

### 👤 Área do cliente

- Visualização de procedimentos por categorias
- Informações do SPA
- Agendamento online

### 👩‍💼 Área administrativa

- Login administrativo seguro
- Dashboard com principais procedimentos e categorias mais solicitadas
- Gerenciamento de agendamentos (pendentes e confirmados)

### 🗺 Páginas

| Área | Rota | Página |
| --- | --- | --- |
| Cliente | `/` | Home |
| Cliente | `/sobre` | Sobre |
| Cliente | `/catalogo` | Catálogo |
| Cliente | `/agendar` | Agendar |
| Admin | `/login` | Login |
| Admin | `/dashboard` | Dashboard |
| Admin | `/agendamentos` | Agendamentos |

---

## 🛠 Tecnologias utilizadas

### Front-end

| Tecnologia | Para que serve |
| --- | --- |
| **React** | Interface dinâmica e componentizada |
| **Framer Motion** | Animações e transições |
| **Axios** | Integração com API |
| **Bootstrap** | Estruturação de layout responsivo e componentes de interface |
| **Sass** | Organização e escalabilidade de estilos |

### Back-end

| Tecnologia | Para que serve |
| --- | --- |
| **Node.js** | Execução do servidor |
| **Express** | Estruturação de rotas e API REST |
| **MySQL** | Persistência de dados estruturados |

---

## 🗄 Banco de dados

O projeto possui um script SQL pronto localizado em:

```
server/db/script.sql
```

Esse arquivo contém toda a estrutura necessária para criação do banco local: ele cria o banco `kiwi_estetica` e as tabelas `administradores` e `agendamentos`.

> [!TIP]
> Para criar um login de administrador, coloque a senha desejada em `server/generate_hash.js`, rode `node generate_hash.js` dentro da pasta **server** e salve o hash gerado na coluna `senha` da tabela `administradores`.

---

## ⚙️ Como executar o projeto

**Pré-requisitos:** Node.js e MySQL.

### 1️⃣ Clonar o repositório

```bash
git clone https://github.com/lunajulia107/kiwi-estetica.git
```

### 2️⃣ Instalar as dependências

**Client**

```bash
cd client
npm install
```

**Server**

```bash
cd server
npm install
```

### 3️⃣ Configurar as variáveis de ambiente

Criar arquivo `.env` dentro da pasta **server**:

```env
DB_HOST=
DB_USER=
DB_PASSWORD=
DB_NAME=
DB_PORT=
SECRET_KEY=
WHATSAPP_PROFESSIONAL_NUMBER=
```

### 4️⃣ Rodar a aplicação

**Back-end**

```bash
cd server
npm run dev
```

**Front-end**

```bash
cd client
npm run start
```

> [!NOTE]
> O servidor roda por padrão na porta `5000`, que é o endereço que o frontend usa para chamar a API (`http://localhost:5000/api`).

---

## 📁 Estrutura do projeto

```
kiwi-estetica/
├── client/                 → frontend
│   ├── public/
│   │   ├── images/         → logotipo, imagens das páginas e GIFs dos fluxos
│   │   └── sass/           → estilos em Sass
│   └── src/
│       ├── components/     → componentes do site e do painel admin
│       ├── json/           → dados de serviços e clientes
│       └── pages/          → páginas do site e do painel admin
└── server/                 → backend
    ├── app/                → servidor Express
    ├── auth/               → autenticação do admin
    ├── db/                 → conexão e script SQL
    ├── models/             → modelos de admin e agendamentos
    └── routes/             → rotas da API
```

---

## 🤝 Créditos do projeto

Projeto acadêmico desenvolvido em equipe, com divisão de responsabilidades. A proposta surgiu da necessidade de facilitar o gerenciamento de agendas, já que ainda é muito comum o uso de métodos manuais, como agendas físicas, o que pode dificultar a organização, visualização e controle de horários.

| Área | Responsável |
| --- | --- |
| 💻 Desenvolvimento e implementação | Julia Gomes |
| 🎨 UI Design | Samara Duarte |
| 🔎 UX Research | Camila Bonilha |

### 💡 Observações

Projeto desenvolvido com foco em:

- Experiência do usuário
- Performance
- Organização de código

---

## 📄 Licença

Este projeto está sob a licença **MIT**.
