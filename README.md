# [README] BUILDER PROJECTS

**DESCRIÇÃO:** Workspace relacionado aos Projetos de Automatização: `Plataforma WEB`

* **Time:** Luis Garcia, Willian Suzuki

- **Desde:** 16/05/2018


## IDEIAS PARA DESENVOLVIMENTO
|Idealizado em|Nome do Projeto|Descrição|Finalizado em|Status|
|---|---|---|---|---|
|16/05/2018|Crud Generator|Projeto de criação de CRUD HTML+DB pela Entidade do Banco|*não finalizado*|*apenas idealizado*|
|16/05/2018|Swagger Generator|Projeto de criação de documentação swagger por CRUD|*não finalizado*|*apenas idealizado*|


## DETALHAMENTO TÉCNICO

## 1. Crud Generator ![project version](https://img.shields.io/badge/version-0.0.1-brightgreen.svg)
---

## Estrutura do Projeto
Camada|Tecnologias
---|---
Server|![node](https://img.shields.io/badge/node-8.11.2-yellow.svg) ![npm](https://img.shields.io/badge/npm-5.6.0-yellow.svg) ![express](https://img.shields.io/badge/express-4.x-yellow.svg)
Persistência | ![redis](https://img.shields.io/badge/redis-2.8.0-red.svg)
Client|![bootstrap](https://img.shields.io/badge/bootstrap-4.1.1-blue.svg) ![html](https://img.shields.io/badge/html-5-blue.svg) ![css](https://img.shields.io/badge/css-3-blue.svg) ![js](https://img.shields.io/badge/js-es6-blue.svg) ![js](https://img.shields.io/badge/jquery-3.1.1-blue.svg)
DevSetup|![setup](https://img.shields.io/badge/repository-git-green.svg) ![setup](https://img.shields.io/badge/ide-visualstudio-green.svg) ![setup](https://img.shields.io/badge/browser-chrome-green.svg)

## Descrição
A proposta do projeto é expor uma pequena plataforma web para geração de CRUD HTML a partir de uma endidade do banco de dados.

**STEP 1:** Criar base do projeto estilo **Dashboard SPA**

- Header com Logo e Titulo

- Sub Header logout / login

- Frame central renderizar telas

- Menu lateral:
    - MenuItem dinâmico
    
    - MenuItem (bottom) fixo: `Administrador | Configuração`
    
    - MenuItem Administrador: 
        - `Administrador > Cadastro de Usuário`
        - `Administrador > Cadastro de Perfil`
        - `Administrador > Cadastro de Entidades`
        - `Administrador > Cadastro de Menu`
        - `Administrador > Associar Telas x Menu`

**STEP 2:** Criar entidades a partir de um CRUD HTML

- Menu Administrador > Entidades

- Listar entidades: `nome | ativo | criador | dt ultima alteração | btRemoverEntidade e btEditarEntidade | btAcessarTela e btRemoverTela ou btCriarTela`

- Editar entidade
    - Input nome da Entidade
    - Input descrição Entidade
    - Checkbox: `ativo/inativo`
    - Input (incremental) Campo/Atributos
        - Input nome campo
        - Combo tipo campo: `String | Numeric | Date | Bool`
        - Input label (utilizada para a criação dos CRUDs)

**STEP 3:** Criar tela a partir de uma Entidade BD

- Criar tela de listagem com filtro e tabela (btNovo)

- Criar tela de edição com os campos da tabela

- Utilizar as labels cadastradas como Label do campo

**STEP X:** A Definir


---
## 2. Swagger Generator ![project version](https://img.shields.io/badge/version-0.0.1-brightgreen.svg)
---

## Estrutura do Projeto

Camada|Tecnologias
---|---
Server|![node](https://img.shields.io/badge/node-8.11.2-yellow.svg) ![npm](https://img.shields.io/badge/npm-5.6.0-yellow.svg) ![express](https://img.shields.io/badge/express-4.x-yellow.svg)
Util | ![swagger](https://img.shields.io/badge/swagger-0.7.5-red.svg)
Client|![bootstrap](https://img.shields.io/badge/bootstrap-4.1.1-blue.svg) ![html](https://img.shields.io/badge/html-5-blue.svg) ![css](https://img.shields.io/badge/css-3-blue.svg) ![js](https://img.shields.io/badge/js-es6-blue.svg) ![js](https://img.shields.io/badge/jquery-3.1.1-blue.svg)
DevSetup|![setup](https://img.shields.io/badge/repository-git-green.svg) ![setup](https://img.shields.io/badge/ide-visualstudio-green.svg) ![setup](https://img.shields.io/badge/browser-chrome-green.svg)

## Descrição
A proposta do projeto gerador de documentação swagger (REST) em formato de formulário com previewer JSON. No formato onde possa ser feita a entrada dos dados no seguinte formato:

- Nome do serviço
- Tipo de requisição: `Consulta: GET, Persistencia: POST, Remoção: DELETE, ...`
- Entrada de dados | Saida de dados
    - Qtd de campos (cria automaticamente os inputs)
    - Tipo de campo: `Texto: String, Numerico: Integer, Verdadeiro/Falso, Listagem, ...`
- Possibilidade de salvar projeto para futura edição
- Previewer do JSON entrada e saída
- Exportar swagger a partir do formulário versionado (0.0.1, ...)