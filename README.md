# Desafio 2 - Desenvolvimento de REST API para Gestão de Ativos

Este projeto é parte de um desafio de desenvolvimento de uma API para gestão de ativos financeiros. A API permite cadastrar e gerenciar ativos financeiros, bem como realizar pedidos de compra e venda desses ativos.

## Funcionalidades

- Cadastro de ativos financeiros, incluindo informações como nome, descrição e preço.
- Listagem de todos os ativos cadastrados.
- Realização de pedidos de compra e venda de ativos, associando-os a um preço específico e status.
- Listagem de todos os pedidos de compra e venda realizados.

## Tecnologias Utilizadas

O projeto foi desenvolvido utilizando as seguintes tecnologias:

- Node.js: Plataforma de desenvolvimento JavaScript.
- Nest.js: Framework para desenvolvimento de APIs em Node.js.
- MongoDB: Banco de dados NoSQL para persistência dos dados.
- Prisma: ORM (Object-Relational Mapping) para interação com o banco de dados.
- Docker: Plataforma para criação e gerenciamento de containers.

## Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas em seu ambiente de desenvolvimento:

- Node.js (versão 18.16.1)
- Docker

## Configuração e Execução

Siga estas etapas para configurar e executar o projeto em sua máquina local:

1. Clone este repositório: `git clone https://github.com/guilhermealves-dev/nestjs-api-fullcycle-challenge-2.git`
2. Navegue até o diretório do projeto: `cd nestjs-api-fullcycle-challenge-2`
3. Instale as dependências: `npm install`
4. Execute o comando: `docker-compose up` para iniciar o MongoDB mais a aplicação
5. O servidor estará acessível em: `http://localhost:3000`

# Endpoints da API

A API possui os seguintes endpoints para interação:

## Ativos Financeiros

### Listar Ativos

- **URL:** `/api/assets`
- **Método:** GET
- **Descrição:** Retorna todos os ativos financeiros cadastrados.
- **Resposta de Sucesso:**
  - **Código:** 200 (OK)
  - **Exemplo de Resposta:**
    ```json
    [
        {
            "id": "asset1",
            "symbol": "ASSET1"
        },
        {
            "id": "asset2",
            "symbol": "ASSET2"
        }
    ]
    ```

### Cadastrar Ativo

- **URL:** `/api/assets`
- **Método:** POST
- **Descrição:** Cadastra um novo ativo financeiro.
- **Corpo da Requisição:**
  - **Estrutura:**
    ```json
    {
        "id": "asset2",
        "symbol": "ASSET2"
    }
    ```
- **Resposta de Sucesso:**
  - **Código:** 201 (Created)
  - **Exemplo de Resposta:**
    ```json
    {
        "id": "asset2",
        "symbol": "ASSET2"
    }
    ```

## Pedidos

### Listar Pedidos

- **URL:** `/api/orders`
- **Método:** GET
- **Descrição:** Retorna todos os pedidos de compra e venda realizados.
- **Resposta de Sucesso:**
  - **Código:** 200 (OK)
  - **Exemplo de Resposta:**
    ```json
    [
        {
            "id": "6497b94aa2bac8111728bae3",
            "asset_id": "asset1",
            "price": 100,
            "status": "PENDING"
        },
        {
            "id": "6497ba56a2bac8111728bae4",
            "asset_id": "asset2",
            "price": 500,
            "status": "PENDING"
        }
    ]
    ```

### Cadastrar Pedido

- **URL:** `/api/orders`
- **Método:** POST
- **Descrição:** Cadastra um novo pedido de compra ou venda de ativo.
- **Corpo da Requisição:**
  - **Estrutura:**
    ```json
    {
        "asset_id": "asset2",
        "price": 100
    }
    ```
- **Resposta de Sucesso:**
  - **Código:** 201 (Created)
  - **Exemplo de Resposta:**
    ```json
    {
        "id": "6497ba56a2bac8111728bae4",
        "asset_id": "asset2",
        "price": 500,
        "status": "PENDING"
    }
    ```

## Agradecimentos

Gostaria de expressar gratidão à Full Cycle pelos ensinamentos valiosos fornecidos durante essa semana da [Imersão Full Stack](https://imersao.fullcycle.com.br/). Agradeço por proporcionar a oportunidade de aprender e aplicar esses novos conhecimentos.

## Licença

[![MIT License](https://img.shields.io/badge/license-MIT-green)](https://opensource.org/licenses/MIT) 

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/GPL-3.0)

[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)
## 🔗 Autor

| [![website](https://www.guilhermealves.dev/assets/images/mini-logo.png)](https://www.guilhermealves.dev/) | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/guilherme-alves-905454233/)     |
| :----------- | :---------- |
