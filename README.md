<div align="center">

# Dashboard Analítico CPA

**Plataforma SaaS de gestão financeira e operacional para equipes de CPA, com controle diário, metas, despesas e painel administrativo em tempo real.**

<p align="center">
  <img src="https://img.shields.io/badge/NEXT.JS-0A0A0A?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/REACT-0A0A0A?style=for-the-badge&logo=react&logoColor=white" alt="React">
  <img src="https://img.shields.io/badge/TYPESCRIPT-0A0A0A?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/EXPRESS.JS-0A0A0A?style=for-the-badge&logo=express&logoColor=white" alt="Express.js">
  <img src="https://img.shields.io/badge/PRISMA-0A0A0A?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma">
  <img src="https://img.shields.io/badge/POSTGRESQL-0A0A0A?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/TAILWIND_CSS-0A0A0A?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/DOCKER-0A0A0A?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
</p>

</div>

---

## Sobre o Projeto

O **Dashboard Analítico CPA** é uma plataforma fullstack projetada para profissionais e equipes que operam com CPA (Custo por Aquisição).

O sistema centraliza o controle financeiro diário, gerenciamento de equipes, acompanhamento de metas e visualização de métricas de performance em uma única plataforma.

A aplicação utiliza uma interface em **dark mode**, combinada com elementos de **glassmorphism**, gráficos e componentes interativos para apresentar os dados operacionais de forma organizada.

### Problemas que resolve

* **Controle financeiro fragmentado** — consolida depósitos, saques, lucros e despesas em um único painel.
* **Gestão de equipes descentralizada** — permite criar equipes, convidar operadores por código e acompanhar métricas de performance.
* **Falta de visibilidade operacional** — apresenta métricas como ROI, faturamento, lucro líquido e evolução financeira.
* **Acompanhamento de CPA Negativo** — disponibiliza um módulo específico para registrar operações e calcular resultados.

---

## Tecnologias Utilizadas

### Frontend

| Tecnologia       | Versão | Finalidade                           |
| :--------------- | :----- | :----------------------------------- |
| **Next.js**      | 16.2.3 | Framework React com SSR e App Router |
| **React**        | 19.2.4 | Biblioteca de interfaces             |
| **TypeScript**   | 5.x    | Tipagem estática                     |
| **Tailwind CSS** | 4.x    | Estilização utilitária               |
| **Recharts**     | 3.8.1  | Gráficos e visualizações de dados    |
| **Axios**        | 1.15.0 | Requisições HTTP                     |
| **Lucide React** | 1.7.0  | Biblioteca de ícones                 |

### Backend

| Tecnologia         | Versão | Finalidade                   |
| :----------------- | :----- | :--------------------------- |
| **Express.js**     | 4.19.2 | API REST                     |
| **Prisma ORM**     | 5.12.0 | Mapeamento objeto-relacional |
| **PostgreSQL**     | 15     | Banco de dados relacional    |
| **JSON Web Token** | 9.0.2  | Autenticação JWT             |
| **bcryptjs**       | 2.4.3  | Hash de senhas               |
| **web-push**       | 3.6.7  | Notificações Push via VAPID  |

### Infraestrutura

| Tecnologia         | Finalidade                                |
| :----------------- | :---------------------------------------- |
| **Docker Compose** | Container PostgreSQL para desenvolvimento |
| **PM2**            | Gerenciamento de processos em produção    |
| **Nginx**          | Reverse Proxy para frontend e API         |
| **Netlify**        | Deploy do frontend                        |
| **Render**         | Deploy do backend                         |

---

## Funcionalidades

### Módulo Individual

* **Dashboard principal** — métricas consolidadas de faturamento, investimento, lucro líquido e ROI global.
* **Controle Diário** — registro de ciclos com depósito, saque, baú e cooperação por plataforma.
* **CPA Negativo** — módulo dedicado para operações CPA com cálculo automático de resultado.
* **Gestão de Despesas** — cadastro e categorização de despesas com totalizadores.
* **Metas** — definição de objetivos financeiros com acompanhamento de progresso.
* **Gráficos de Evolução** — visualização da evolução financeira e distribuição de capital através do Recharts.
* **Perfil do Usuário** — edição de nome e foto de perfil com upload de imagem.
* **Notificações Push** — notificações através da Web Push API e Service Worker.
* **Ocultação de Valores** — opção para mascarar valores financeiros na interface.
* **Configurações** — gerenciamento de conta, notificações e redefinição de dados.

### Módulo de Equipe

* **Criação e gerenciamento de equipes** — criação de equipes através de código de convite exclusivo.
* **Ranking de operadores** — classificação baseada no lucro gerado.
* **Dashboard de equipe** — visualização de métricas agregadas.
* **Remessas de equipe** — controle de depósitos, saques e valores por operador.
* **Metas de equipe** — definição de objetivos por plataforma.
* **Operações** — registro de operações por plataforma e rede.
* **Despesas de equipe** — controle financeiro compartilhado.

### Painel Administrativo

* **Métricas globais** — visualização de usuários, equipes, operadores e receita da plataforma.
* **Gestão de usuários** — alteração de roles, ativação, bloqueio e exclusão.
* **Feed de atividades** — registro das ações realizadas na plataforma.
* **Logs de auditoria** — histórico detalhado das atividades dos usuários.

### Progressive Web App

* **Progressive Web App** — aplicação instalável em dispositivos móveis.
* **Service Worker** — suporte a funcionalidades offline e notificações.
* **Push Notifications** — notificações nativas em desktop e dispositivos móveis.

---

## Estrutura do Projeto

```text
Dashboard-AnalItico-CPA/
│
├── backend/
│   ├── src/
│   │   └── index.ts
│   │       # API Express — autenticação, CRUD, administração e equipes
│   │
│   ├── prisma/
│   │   └── schema.prisma
│   │       # Schema do banco de dados
│   │
│   ├── prisma.config.ts
│   ├── package.json
│   └── tsconfig.json
│
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── dashboard/
│   │   │   │   ├── admin/
│   │   │   │   ├── daily-control/
│   │   │   │   ├── cpa-negativo/
│   │   │   │   ├── expenses/
│   │   │   │   ├── goals/
│   │   │   │   ├── team/
│   │   │   │   ├── settings/
│   │   │   │   └── links/
│   │   │   │
│   │   │   ├── login/
│   │   │   ├── register/
│   │   │   ├── layout.tsx
│   │   │   └── globals.css
│   │   │
│   │   ├── components/
│   │   │   ├── dashboard/
│   │   │   ├── cards/
│   │   │   ├── layout/
│   │   │   ├── sidebar/
│   │   │   └── header/
│   │   │
│   │   └── lib/
│   │       └── # API, autenticação e Push
│   │
│   ├── public/
│   │   ├── manifest.json
│   │   └── sw.js
│   │
│   ├── tailwind.config.ts
│   └── package.json
│
├── docker-compose.yml
├── ecosystem.config.js
├── nginx.conf
└── netlify.toml
```

---

## Arquitetura

```text
                         ┌─────────────────────┐
                         │       USUÁRIO       │
                         └──────────┬──────────┘
                                    │
                                    ▼
                    ┌─────────────────────────────┐
                    │          NEXT.JS            │
                    │                             │
                    │ React + TypeScript          │
                    │ Tailwind CSS                │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                         ┌───────────────────┐
                         │      NGINX        │
                         │   Reverse Proxy   │
                         └─────────┬─────────┘
                                   │
                    ┌──────────────┴──────────────┐
                    │                             │
                    ▼                             ▼
          ┌─────────────────┐          ┌─────────────────┐
          │    FRONTEND     │          │     EXPRESS     │
          │                 │          │       API       │
          │     Next.js     │          │   TypeScript    │
          └─────────────────┘          └────────┬────────┘
                                                │
                                                ▼
                                      ┌──────────────────┐
                                      │      PRISMA      │
                                      │       ORM        │
                                      └────────┬─────────┘
                                               │
                                               ▼
                                      ┌──────────────────┐
                                      │    POSTGRESQL    │
                                      │     DATABASE     │
                                      └──────────────────┘

                          ┌───────────────────────────┐
                          │      PUSH NOTIFICATIONS   │
                          │       Web Push / VAPID    │
                          └───────────────────────────┘
```

---

## Instalação e Execução

### Pré-requisitos

* **Node.js 18+**
* **npm**
* **PostgreSQL 15+** ou Docker
* **Git**

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/Dashboard-AnalItico-CPA.git
cd Dashboard-AnalItico-CPA
```

### 2. Inicie o banco de dados

Utilizando Docker Compose:

```bash
docker-compose up -d
```

### 3. Configure o Backend

```bash
cd backend
npm install
```

Crie o arquivo:

```text
backend/.env
```

Depois configure as variáveis de ambiente.

Gere o Prisma Client:

```bash
npx prisma generate
```

Aplique a estrutura do banco:

```bash
npx prisma db push
```

Inicie o servidor:

```bash
npm run dev
```

O backend estará disponível em:

```text
http://localhost:3001
```

### 4. Configure o Frontend

Em outro terminal:

```bash
cd frontend
npm install
npm run dev
```

O frontend estará disponível em:

```text
http://localhost:3000
```

### 5. Produção

Para gerenciamento dos processos em produção:

```bash
npm install -g pm2
pm2 start ecosystem.config.js
```

---

## Configuração

### Backend

Crie:

```text
backend/.env
```

Exemplo:

```env
DATABASE_URL="postgresql://USUARIO:SENHA@HOST:5432/NOME_DO_BANCO"
DIRECT_URL="postgresql://USUARIO:SENHA@HOST:5432/NOME_DO_BANCO"

JWT_SECRET="sua_chave_secreta_jwt"

VAPID_PUBLIC_KEY="sua_chave_publica_vapid"
VAPID_PRIVATE_KEY="sua_chave_privada_vapid"

PORT=3001
FRONTEND_URL="http://localhost:3000"
```

### Frontend

Crie:

```text
frontend/.env.local
```

Configure:

```env
NEXT_PUBLIC_API_URL="http://localhost:3001"
```

### Chaves VAPID

Para gerar as chaves utilizadas pelo sistema de notificações:

```bash
npx web-push generate-vapid-keys
```

> As chaves privadas e demais credenciais não devem ser publicadas no repositório.

---

## Uso

1. Acesse `http://localhost:3000`.
2. Crie uma conta através da página `/register`.
3. Faça login através da página `/login`.
4. Acesse o Dashboard.
5. Registre operações no módulo **Controle Diário**.
6. Registre operações no módulo **CPA Negativo**.
7. Cadastre despesas e acompanhe seus impactos financeiros.
8. Crie metas e acompanhe seu progresso.
9. Crie ou entre em uma equipe através do código de convite.
10. Configure perfil e notificações.

Usuários com a role `ADMIN` possuem acesso ao painel administrativo, incluindo métricas globais e gerenciamento de usuários.

---

## Screenshots

<div align="center">

*Seção reservada para capturas de tela do projeto.*

As imagens podem ser adicionadas em:

```text
docs/screenshots/
```

Exemplo:

```markdown
![Dashboard Principal](docs/screenshots/dashboard.png)

![Controle Diário](docs/screenshots/daily-control.png)

![Painel de Equipe](docs/screenshots/team.png)
```

</div>

---

## Scripts Disponíveis

### Backend

| Script  | Comando         | Descrição                            |
| :------ | :-------------- | :----------------------------------- |
| `dev`   | `npm run dev`   | Inicia o servidor em desenvolvimento |
| `build` | `npm run build` | Compila o TypeScript                 |
| `start` | `npm start`     | Executa o build de produção          |

### Frontend

| Script  | Comando         | Descrição                           |
| :------ | :-------------- | :---------------------------------- |
| `dev`   | `npm run dev`   | Inicia o Next.js em desenvolvimento |
| `build` | `npm run build` | Gera o build de produção            |
| `start` | `npm start`     | Inicia o servidor Next.js           |
| `lint`  | `npm run lint`  | Executa o ESLint                    |

---

## Roadmap

* [ ] Separação das rotas do backend em módulos
* [ ] Testes automatizados unitários
* [ ] Testes de integração
* [ ] Exportação de relatórios financeiros em PDF
* [ ] Exportação de dados em CSV
* [ ] Gráficos comparativos entre períodos
* [ ] Sistema de notificações in-app
* [ ] Modo claro
* [ ] Logs estruturados
* [ ] Rate Limiting
* [ ] Validação de entrada com Zod ou Joi

---

## Autor

Desenvolvido por **João Rei dos Bugs**.

<p align="left">
  <img src="https://img.shields.io/badge/GITHUB-0A0A0A?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</p>

---

<div align="center">

**Dashboard Analítico CPA**

Fullstack • SaaS • Analytics • Financial Management

</div>
