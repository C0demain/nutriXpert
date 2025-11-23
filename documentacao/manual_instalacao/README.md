# 💻 Manual de Instalação

## 🚀 Guia completo para configurar todo o ecossistema  
Do setup inicial ao ambiente final de produção, este manual explica passo a passo como instalar e executar todas as partes do projeto **nutriXpert**, garantindo uma instalação rápida, padronizada e sem complicações.


## 📦 Componentes da instalação

Para facilitar a navegação, o processo está dividido em três módulos independentes:

<details><summary>Instalação Agent</summary>

# nutriXpert-agent

## Pré-requisitos

* **Python 3.10+**
* **PostgreSQL** (ou outro banco compatível, configurado via `DATABASE_URL`)


## Como rodar o projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/SEU_USUARIO/nutriXpert-agent.git
cd nutriXpert-agent
```

### 2. Criar ambiente virtual

```bash
python -m venv .venv
source .venv/bin/activate   # Linux/Mac
.venv\Scripts\activate      # Windows
```

### 3. Instalar dependências

```bash
pip install -r requirements.txt
```

### 4. Iniciar o servidor local

```bash
uvicorn main:app --reload --host 127.0.0.1 --port 8000
```

### 5. (Opcional) Executar o ADK Web UI

```bash
adk web
```

**Swagger UI:** [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
**Redoc:** [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)


## Rodando com Docker

```bash
docker-compose up --build
```

## Variáveis de ambiente

Crie o arquivo `.env` na raiz:

```ini
# Google API (opcional para usar modelos Gemini)
GOOGLE_GENAI_USE_VERTEXAI=FALSE
GOOGLE_API_KEY=YOUR_API_KEY

# Configuração do FastAPI
FASTAPI_HOST=0.0.0.0
FASTAPI_PORT=8000
UVICORN_RELOAD=true

# Configuração do agente
ADK_APP_NAME=nutriXpert
DATABASE_URL=postgresql+psycopg2://myuser:mypassword@localhost:5432/mydb
ADK_MODEL=gemini-2.0-flash
ADK_SERIALIZE_RUNNER=false
```

🔗 Gere sua API Key em [Google AI Studio](https://aistudio.google.com/app/apikey).
O modelo padrão é o **Gemini 2.0 Flash**, gratuito no plano básico.

---

## Estrutura do Banco de Dados SQL

O **nutriXpert-agent** utiliza o **SQLAlchemy ORM** integrado com o **Google ADK**, o que significa que algumas tabelas são **criadas automaticamente** pelo ADK e outras **foram definidas manualmente** para o projeto.

### **Tabelas criadas automaticamente pelo ADK**

Essas tabelas são gerenciadas internamente pelo **SessionService** e **StateManager** do ADK.
Você **não precisa criar nem mapear manualmente** — elas são criadas automaticamente no banco configurado em `DATABASE_URL`.

| Tabela        | Finalidade                                                                      | Gerenciada pelo ADK |
| ------------- | ------------------------------------------------------------------------------- | ------------------- |
| `sessions`    | Armazena o histórico completo das conversas (mensagens do usuário e do agente). | ✅                   |
| `events`      | Guarda eventos de estado e ações internas do agente.                            | ✅                   |
| `user_states` | Estado persistente de cada usuário (memória de longo prazo).                    | ✅                   |
| `app_states`  | Estado global do aplicativo (configurações do agente).                          | ✅                   |

Essas tabelas são usadas para restaurar contextos e estados entre sessões e garantir que o agente "lembre" informações mesmo após o restart.

---

### **Tabelas criadas manualmente pelo projeto**

| Tabela           | Finalidade                                                                                         | Gerenciada pelo ADK |
| ---------------- | -------------------------------------------------------------------------------------------------- | ------------------- |
| `alimentos_taco` | Tabela de alimentos com composição nutricional baseada na base TACO (usada nas consultas via RAG). | ❌                   |
| `feedbacks`      | Tabela de feedbacks de usuários sobre respostas do agente (Human-in-the-Loop).                     | ❌                   |

Essas tabelas são definidas no código Python (via SQLAlchemy models) e são parte essencial do aprendizado contínuo do agente.

---

### Exemplo de fluxo completo

1. Usuário pergunta:
   `Explique rapidamente o que é proteína.`
2. O agente responde.
3. O frontend envia um `POST /feedback` com nota e comentário.
4. O backend armazena o feedback e gera embeddings.
5. Nas próximas perguntas do mesmo usuário, o agente ajusta automaticamente o tom e nível de detalhe.


</details>
<details><summary>Instalação Backend</summary>
  
# nutriXpert-backend

API desenvolvida com **Spring Boot** para gerenciamento de informações nutricionais.  
Documentação Swagger: [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

---

## 🚀 Pré-requisitos

- [Java 17+](https://adoptium.net/)
- [Maven](https://maven.apache.org/)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) (Recomendado)

---

## 📥 Clonando o repositório

```bash
git clone https://github.com/C0demain/nutriXpert-backend.git
cd nutriXpert-backend
```

---


## ⚙️ Configurando variáveis de ambiente

O projeto utiliza um arquivo `.env` para armazenar configurações sensíveis (como credenciais de banco de dados e chave JWT).

1. Copie o arquivo de exemplo:

```bash
cp .env.example .env

2. Edite o arquivo `.env` com os valores corretos (exemplo):

```dotenv
JWT_SECRET=my_secret_key
DB_CONNECTION_STRING=jdbc:postgresql://localhost:5432/postgres
DB_USER=postgres
DB_PASSWORD=postgres
```


---

## 🛠️ Executando no IntelliJ IDEA

No IntelliJ, você pode usar uma configuração pronta para carregar automaticamente o `.env`:

> Basta abrir o projeto, selecionar a configuração **NutriXpert** no canto superior direito e clicar em **Run**.

---

## ▶️ Executando via linha de comando

Se preferir, você pode declarar as variáveis diretamente no terminal antes de rodar:

```bash
export JWT_SECRET=my_secret_key
export DB_CONNECTION_STRING=jdbc:postgresql://localhost:5432/postgres
export DB_USER=postgres
export DB_PASSWORD=postgres

./mvnw spring-boot:run
```

> Windows (PowerShell):

```powershell
$env:JWT_SECRET="my_secret_key"
$env:DB_CONNECTION_STRING="jdbc:postgresql://localhost:5432/postgres"
$env:DB_USER="postgres"
$env:DB_PASSWORD="postgres"
./mvnw spring-boot:run
```
---

## 🛠️ Configurando o IntelliJ IDEA

1. Abra o projeto no IntelliJ (`File > Open` → selecione a pasta `nutriXpert-backend`).  
2. Aguarde o IntelliJ baixar as dependências Maven.
3. Selecionar a configuração **NutriXpert** no canto superior direito e clicar em **Run**
---

## ▶️ Executando o projeto

No IntelliJ:  
- Escolha a configuração criada no canto superior direito e clique em **Run** .  

Via terminal (usando o wrapper Maven incluso):

```bash
./mvnw spring-boot:run
```

Se o Maven já estiver instalado globalmente:

```bash
mvn spring-boot:run
```

A API ficará disponível em:  
- [http://localhost:8080](http://localhost:8080)  
- Swagger: [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

  </details>

<details><summary>Instalação Frontend</summary>
  
  # nutriXpert-frontend

Aplicação frontend responsável pela interface de interação com o usuário, consumindo os serviços e APIs do projeto **nutriXpert**.

---

## 🚀 Pré-requisitos

Antes de iniciar, é necessário ter instalado:

- Node.js 18+  
- Gerenciador de pacotes (uma das opções abaixo):
  - npm  
  - pnpm  
  - yarn  
  - bun

---

## 📥 Instalando Dependências

Após clonar o projeto, acesse a pasta do frontend e execute:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

---

## ▶️ Rodando em Ambiente de Desenvolvimento

Para iniciar o servidor de desenvolvimento local (porta padrão `http://localhost:3000`):

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

Após rodar o comando, o frontend estará disponível no navegador.

---

## ⚙️ Configuração de Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto, seguindo o exemplo:

```ini
VITE_API_URL=http://localhost:8080
```

Onde:

- `VITE_API_URL` → endereço da API backend do **nutriXpert**

Se estiver usando outra porta ou domínio, altere o valor conforme necessário.

---

## 🛠️ Build para Produção

Para gerar os arquivos otimizados de produção:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Os arquivos finais serão gerados na pasta `dist`.

---

## 🔍 Visualizando o Build Localmente

Para testar localmente a versão de produção:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

A aplicação será executada simulando o modo de produção.

---

## 🧪 Dicas de Desenvolvimento

- Certifique-se de que o **backend** esteja rodando antes do frontend.
- Caso esteja usando outro domínio ou porta, atualize o `.env`.
- Em ambiente de produção, configure `VITE_API_URL` para o domínio público do servidor backend.

---
</details>
