<div align="center">

# ⚡ Dashboard Analítico CPA

**Plataforma SaaS de gestão financeira e operacional para equipes de CPA, com controle diário, metas, despesas e painel administrativo em tempo real.**

[![Tech Stack](https://skillicons.dev/icons?i=nextjs,react,ts,express,prisma,postgres,tailwind,docker)](https://skillicons.dev)

</div>

---

## 📋 Sobre o Projeto

O **Dashboard Analítico CPA** é uma plataforma fullstack projetada para profissionais e equipes que operam com CPA (Custo por Aquisição). Centraliza o controle financeiro diário, o gerenciamento de equipes, o acompanhamento de metas e a visualização de métricas de performance — tudo em um dashboard com design dark mode e interface glassmorphism.

### Problemas que resolve

- **Controle financeiro fragmentado** — consolida depósitos, saques, lucros e despesas em um único painel
- **Gestão de equipes descentralizada** — permite criar equipes, convidar operadores por código e acompanhar rankings de performance
- **Falta de visibilidade operacional** — exibe métricas em tempo real como ROI, faturamento, lucro líquido e evolução financeira
- **Acompanhamento de CPA Negativo** — módulo dedicado para registrar e calcular resultados de operações CPA

---

## 🛠 Tecnologias Utilizadas

### Frontend
| Tecnologia | Versão | Finalidade |
|:---|:---|:---|
| **Next.js** | 16.2.3 | Framework React com SSR e App Router |
| **React** | 19.2.4 | Biblioteca de interfaces |
| **TypeScript** | 5.x | Tipagem estática |
| **Tailwind CSS** | 4.x | Estilização utilitária |
| **Recharts** | 3.8.1 | Gráficos e visualizações de dados |
| **Axios** | 1.15.0 | Requisições HTTP |
| **Lucide React** | 1.7.0 | Biblioteca de ícones |

### Backend
| Tecnologia | Versão | Finalidade |
|:---|:---|:---|
| **Express.js** | 4.19.2 | API REST |
| **Prisma ORM** | 5.12.0 | Mapeamento objeto-relacional |
| **PostgreSQL** | 15 | Banco de dados relacional |
| **JSON Web Token** | 9.0.2 | Autenticação JWT |
| **bcryptjs** | 2.4.3 | Hash de senhas |
| **web-push** | 3.6.7 | Notificações push (VAPID) |

### Infraestrutura
| Tecnologia | Finalidade |
|:---|:---|
| **Docker Compose** | Container PostgreSQL para desenvolvimento |
| **PM2** | Gerenciamento de processos em produção |
| **Nginx** | Reverse proxy (frontend + API) |
| **Netlify** | Deploy do frontend |
| **Render** | Deploy do backend |

---

## ✨ Funcionalidades

### Módulo Individual
- 📊 **Dashboard principal** — métricas consolidadas de faturamento, investimento, lucro líquido e ROI global
- 📅 **Controle Diário** — registro de ciclos com depósito, saque, baú e cooperação por plataforma
- 📉 **CPA Negativo** — módulo dedicado para operações CPA com cálculo automático de resultado
- 💰 **Gestão de Despesas** — cadastro e categorização de despesas com totalizadores
- 🎯 **Metas** — definição de objetivos financeiros com acompanhamento de progresso
- 📈 **Gráficos de Evolução** — visualização da evolução financeira e distribuição de capital via Recharts
- 👤 **Perfil do Usuário** — edição de nome e foto de perfil com upload de imagem
- 🔔 **Notificações Push** — notificações via Web Push API com Service Worker
- 🔒 **Ocultação de Valores** — toggle para mascarar valores financeiros na interface
- ⚙️ **Configurações** — gerenciamento de conta, notificações e redefinição de dados

### Módulo de Equipe
- 👥 **Criação e gerenciamento de equipes** — com código de convite exclusivo
- 🏆 **Ranking de operadores** — classificação por lucro gerado
- 📊 **Dashboard de equipe** — métricas agregadas por time
- 💸 **Remessas de equipe** — controle de depósitos, saques e valores por operador
- 🎯 **Metas de equipe** — objetivos por plataforma com status ativo/encerrado
- 📋 **Operações** — registro de operações por plataforma e rede
- 💳 **Despesas de equipe** — controle financeiro compartilhado

### Painel Administrativo
- 🛡 **Métricas globais** — total de usuários, equipes, operadores e receita da plataforma
- 👤 **Gestão de usuários** — alteração de roles, ban/ativação e exclusão
- 📜 **Feed de atividades** — registro em tempo real de ações na plataforma
- 📋 **Logs de auditoria** — histórico detalhado de atividades dos usuários

### PWA
- 📱 **Progressive Web App** — instalável no celular com manifest.json e Service Worker
- 🔔 **Push Notifications** — notificações nativas no desktop e mobile

---

## 📁 Estrutura do Projeto

```
Dashboard-AnalItico-CPA/
├── backend/
│   ├── src/
│   │   └── index.ts              # API Express — todas as rotas (auth, CRUD, admin, teams)
│   ├── prisma/
│   │   └── schema.prisma         # Schema do banco de dados (16 modelos)
│   ├── prisma.config.ts          # Configuração do Prisma
│   ├── package.json              # Dependências do backend
│   └── tsconfig.json             # Configuração TypeScript
├── frontend/
│   ├── src/
│   │   ├── app/                  # App Router (Next.js 16)
│   │   │   ├── dashboard/        # Páginas do dashboard
│   │   │   │   ├── admin/        # Painel administrativo
│   │   │   │   ├── daily-control/# Controle diário
│   │   │   │   ├── cpa-negativo/ # CPA Negativo
│   │   │   │   ├── expenses/     # Despesas
│   │   │   │   ├── goals/        # Metas
│   │   │   │   ├── team/         # Gestão de equipe
│   │   │   │   ├── settings/     # Configurações
│   │   │   │   └── links/        # Links
│   │   │   ├── login/            # Página de login
│   │   │   ├── register/         # Página de registro
│   │   │   ├── layout.tsx        # Layout raiz (fontes, providers)
│   │   │   └── globals.css       # Estilos globais (tema dark, glassmorphism)
│   │   ├── components/           # Componentes reutilizáveis
│   │   │   ├── dashboard/        # Seções do dashboard (gráficos, finanças, greeting)
│   │   │   ├── cards/            # Cards de métricas
│   │   │   ├── layout/           # AppLayout, AuthGuard, Modal, Toast, DashboardContext
│   │   │   ├── sidebar/          # Sidebar com navegação responsiva
│   │   │   └── header/           # Header com controles
│   │   └── lib/                  # Utilitários (api, auth, push)
│   ├── public/
│   │   ├── manifest.json         # Configuração PWA
│   │   └── sw.js                 # Service Worker para push notifications
│   ├── tailwind.config.ts        # Tema customizado (cores, animações, fontes)
│   └── package.json              # Dependências do frontend
├── docker-compose.yml            # Container PostgreSQL
├── ecosystem.config.js           # Configuração PM2
├── nginx.conf                    # Reverse proxy Nginx
└── netlify.toml                  # Configuração de deploy Netlify
```

---

## 🚀 Instalação e Execução

### Pré-requisitos

- **Node.js** 18+ e **npm**
- **PostgreSQL** 15+ (ou Docker)
- **Git**

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/Dashboard-AnalItico-CPA.git
cd Dashboard-AnalItico-CPA
```

### 2. Inicie o banco de dados com Docker

```bash
docker-compose up -d
```

### 3. Configure o Backend

```bash
cd backend
npm install
```

Crie o arquivo `.env` na pasta `backend/` (veja a seção [Configuração](#-configuração)).

Gere o Prisma Client e execute as migrações:

```bash
npx prisma generate
npx prisma db push
```

Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

O backend estará disponível em `http://localhost:3001`.

### 4. Configure o Frontend

```bash
cd frontend
npm install
npm run dev
```

O frontend estará disponível em `http://localhost:3000`.

### 5. Produção (opcional)

Utilizando PM2 para gerenciar ambos os processos:

```bash
# Na raiz do projeto
npm install -g pm2
pm2 start ecosystem.config.js
```

---

## ⚙️ Configuração

### Variáveis de Ambiente — Backend (`backend/.env`)

```env
# Banco de dados
DATABASE_URL="postgresql://USUARIO:SENHA@HOST:5432/NOME_DO_BANCO"
DIRECT_URL="postgresql://USUARIO:SENHA@HOST:5432/NOME_DO_BANCO"

# Autenticação
JWT_SECRET="sua_chave_secreta_jwt"

# Push Notifications (VAPID)
VAPID_PUBLIC_KEY="sua_chave_publica_vapid"
VAPID_PRIVATE_KEY="sua_chave_privada_vapid"

# Servidor
PORT=3001
FRONTEND_URL="http://localhost:3000"
```

### Variáveis de Ambiente — Frontend (`frontend/.env.local`)

```env
NEXT_PUBLIC_API_URL="http://localhost:3001"
```

> **Nota:** Para gerar chaves VAPID, utilize: `npx web-push generate-vapid-keys`

---

## 💻 Uso

1. **Acesse** `http://localhost:3000` no navegador
2. **Registre-se** com nome, e-mail e senha na página `/register`
3. **Faça login** na página `/login`
4. **Dashboard** — visualize métricas consolidadas de faturamento, investimento e lucro
5. **Controle Diário** — crie planilhas por plataforma e registre ciclos com depósito, saque, baú e cooperação
6. **CPA Negativo** — registre operações CPA com cálculo automático de resultado
7. **Despesas** — cadastre despesas por categoria para descontar do lucro
8. **Metas** — defina objetivos financeiros e acompanhe o progresso
9. **Equipe** — crie uma equipe ou entre com código de convite, gerencie operadores e acompanhe rankings
10. **Ajustes** — edite perfil, ative notificações push ou redefina dados

> Usuários com role `ADMIN` têm acesso ao painel administrativo com métricas globais e gestão de usuários.

---

## 🖼 Screenshots

<div align="center">

> _Seção reservada para capturas de tela do projeto._
>
> Para adicionar screenshots, salve as imagens na pasta `docs/screenshots/` e referencie aqui:
>
> ```markdown
> ![Dashboard Principal](docs/screenshots/dashboard.png)
> ![Controle Diário](docs/screenshots/daily-control.png)
> ![Painel de Equipe](docs/screenshots/team.png)
> ```

</div>

---

## 📝 Scripts Disponíveis

### Backend (`backend/`)

| Script | Comando | Descrição |
|:---|:---|:---|
| `dev` | `npm run dev` | Inicia o servidor com nodemon (hot reload) |
| `build` | `npm run build` | Compila TypeScript para `dist/` |
| `start` | `npm start` | Executa o build compilado (`dist/index.js`) |

### Frontend (`frontend/`)

| Script | Comando | Descrição |
|:---|:---|:---|
| `dev` | `npm run dev` | Inicia o Next.js em modo de desenvolvimento |
| `build` | `npm run build` | Gera o build de produção |
| `start` | `npm start` | Inicia o servidor Next.js de produção |
| `lint` | `npm run lint` | Executa o ESLint |

---

## 🗺 Roadmap

- [ ] Separação das rotas do backend em módulos (controllers/routes)
- [ ] Testes automatizados (unitários e de integração)
- [ ] Exportação de relatórios financeiros em PDF/CSV
- [ ] Gráficos comparativos entre períodos (semanal, mensal)
- [ ] Sistema de notificações in-app (além do push)
- [ ] Modo claro (light theme)
- [ ] Logs estruturados com níveis de severidade
- [ ] Rate limiting e validação de entrada com Zod/Joi

---

## 👨‍💻 Autor

Desenvolvido por **Pedro Lucas**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/)

---

<div align="center">

Feito com ☕ e TypeScript

</div>
