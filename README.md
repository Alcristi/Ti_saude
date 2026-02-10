# TI Saúde - Main Repository

Este repositório principal orquestra os serviços de Backend e Frontend do projeto TI Saúde utilizando Docker Compose.

## Estrutura do Repositório

O projeto está dividido em submódulos Git:

- **ti_saude**: Backend da aplicação (NestJS + Prisma + PostgreSQL).
- **ti-saude-front**: Frontend da aplicação (Quasar Framework/Vue.js).
- **docker-compose.yml**: Arquivo de orquestração dos contêineres.

## Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Git](https://git-scm.com/downloads)

## Como Rodar o Projeto

1. **Clone o repositório**:
   Como este repositório utiliza submódulos, é necessário cloná-lo de forma recursiva:

   ```bash
   git clone --recursive git@github.com:Alcristi/Ti_saude.git
   cd Ti_saude
   ```

   Se você já clonou sem a opção `--recursive`, inicie os submódulos com:
   ```bash
   git submodule update --init --recursive
   ```

2. **Inicie os serviços com Docker Compose**:
   ```bash
   docker compose up --build -d
   ```

## Serviços Disponíveis

Após subir os contêineres, os serviços estarão acessíveis nas seguintes portas:

- **Frontend**: [http://localhost:8080](http://localhost:8080)
- **Backend API**: [http://localhost:3000/api](http://localhost:3000/api)
- **PgAdmin (Gerenciador de Banco de Dados)**: [http://localhost:5050](http://localhost:5050)
  - **Email**: `admin@admin.com`
  - **Senha**: `root`
- **PostgreSQL**: Porta `5432`

## Desenvolvimento

Para trabalhar em um módulo específico, navegue até a pasta correspondente:

- **Backend**: `cd ti_saude`
- **Frontend**: `cd ti-saude-front`

Cada pasta é um repositório Git independente. Lembre-se de commitar as alterações dentro do submódulo e, em seguida, commitar a atualização da referência do submódulo no repositório raiz.
