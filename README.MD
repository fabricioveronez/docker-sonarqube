# Docker Sonarqube

O objetivo é criar um ambiente com SonarQube e PostgreSQL para uso em qualquer ambiente que tenha o Docker. O projeto foi criado com base no vídeo [“Instalando e Configurando o SonarQube com Docker Compose”](https://www.youtube.com/watch?v=HSFHgti6nXg) no meu canal no YouTube.

## Serviços criados

- **SonarQube**: Ferramenta para análise contínua de código.
- **PostgreSQL**: Banco de dados utilizado pelo SonarQube para armazenar dados.

## Variáveis de Ambiente

- **SonarQube**:
  - `SONAR_JDBC_URL`: Especifica a URL de conexão JDBC para o banco de dados PostgreSQL.
  - `SONAR_JDBC_USERNAME`: Define o nome de usuário para acessar o banco de dados.
  - `SONAR_JDBC_PASSWORD`: Define a senha para acessar o banco de dados.

- **PostgreSQL**:
  - `POSTGRES_USER`: Define o nome de usuário do banco de dados PostgreSQL.
  - `POSTGRES_PASSWORD`: Define a senha do banco de dados PostgreSQL.
  - `POSTGRES_DB`: Especifica o nome do banco de dados a ser utilizado pelo PostgreSQL.

## Volumes

- `sonar_data`: Armazena dados do SonarQube de forma persistente.
- `sonar_logs`: Armazena logs do SonarQube de forma persistente.
- `sonar_db`: Armazena dados do banco de dados PostgreSQL de forma persistente.

Este arquivo configura a rede e volumes necessários para que o SonarQube e o PostgreSQL funcionem corretamente e persistam os dados.

## Executando a Criação do Projeto

Para criar e iniciar os serviços definidos no arquivo `compose.yaml`, utilize o seguinte comando:

```sh
docker compose up -d
```