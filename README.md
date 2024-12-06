# :briefcase: ERP Empresarial

Este repositório contém o projeto desenvolvido para o módulo empresarial de um sistema ERP, focado na funcionalidade de gerenciamento de empresas, seus funcionários, tarefas e atribuições dessas tarefas aos funcionários.

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript no servidor.
- **Express**: Framework para construção de APIs e gerenciamento de rotas.
- **PostgreSQL**: Banco de dados relacional utilizado para armazenar dados.
- **JWT (JSON Web Token)**: Sistema de autenticação para proteger rotas da API.
- **Nunjucks**: Template engine para renderização de páginas dinâmicas.
- **axios**: Biblioteca para realizar requisições HTTP entre frontend e backend.

## Descrição

O sistema foi desenvolvido com arquitetura Cliente-Servidor, oferecendo uma interface gráfica e um conjunto de APIs para operações CRUD nas tabelas de **empresa**, **funcionario** e **tarefa**. O sistema gerencia os relacionamentos entre as entidades, garantindo que haja um relacionamento 1:N entre empresa e funcionário e um relacionamento N:N entre funcionário e tarefa.

- `empresa`: Tabela que contém informações sobre as empresas cadastradas no sistema.
- `funcionario`: Tabela que contém os dados dos funcionários de cada empresa.
- `tarefa`: Tabela que contém as tarefas a serem realizadas pelos funcionários.
- `funcionariotarefa`: Tabela do relacionamento N:N entre funcionário e tarefa. Contém as associações dos funcionários às tarefas que lhe foram atribuídas.

## Estrutura do Projeto
   ```bash
   erp_empresarial/
   │
   ├── backend/                  # Diretório do back-end
   │   ├── apps/                 # Módulos de funcionalidades do back-end
   │   ├── database/             # Configurações do banco de dados
   │   ├── node_modules/         # Módulos Node.js para o back-end
   │   ├── routes/               # Rotas da API
   │   ├── .env                  # Variáveis de ambiente do backend
   │   ├── .gitignore            # Arquivos a serem ignorados no controle de versão
   │   ├── app.js                # Arquivo principal do servidor
   │   ├── databaseConfig.sql    # Script de configuração do banco de dados
   │   ├── package-lock.json     # Controle de versões exatas das dependências
   │   └── package.json          # Gerenciamento de dependências do backend
   │
   ├── frontend/                 # Diretório do front-end
   │   ├── apps/                 # Módulos de funcionalidades do front-end
   │   ├── node_modules/         # Módulos Node.js para o front-end
   │   ├── routes/               # Rotas do front-end
   │   ├── static/               # Arquivos estáticos (CSS, JS, imagens)
   │   ├── .env                  # Variáveis de ambiente do front-end
   │   ├── .gitignore            # Arquivos a serem ignorados no controle de versão
   │   ├── app.js                # Arquivo principal do front-end
   │   ├── package-lock.json     # Controle de versões exatas das dependências
   │   └── package.json          # Gerenciamento de dependências do frontend
   └── 
   ```

## Funcionalidades Implementadas
1. **APIs**:
   - Operações CRUD para empresas, funcionários, tarefas e atribuições das tarefas aos funcionários.

2. **Segurança**:
   - Proteção de rotas com JWT.
   - Sistema de login para controle de acesso.

3. **Front-End**:
   - Funções integradas com as APIs do back-end.
   - Tela de login e controle de sessão.
   - Layout customizado para as interfaces.

## Como Executar

1. **Clonar o repositório**:
   ```bash
   git clone https://github.com/camilymilsoni/bsi-trabalho2-dw3.git

2. **Instalar as dependências do backend e frontend**:
   
   - No diretório `backend/`:
     
     ```bash
      npm i

   - No diretório `frontend/`:
     
     ```bash
      npm i

3. **Configurar as variáveis de ambiente (.env)**:

   No repositório clonado, você verá um arquivo chamado `.env.example` dentro do diretório `backend/`. O próximo passo é criar o arquivo .env com as configurações corretas para a aplicação:

   - Renomear o arquivo `.env.example` para `.env` apenas no diretório `backend/`:
  
     ```bash
     mv .env.example .env

   - Configurar as variáveis de ambiente:
  
     - Abra o arquivo `.env` no diretório `backend/` e edite as variáveis de ambiente necessárias.

4. **Iniciar o servidor**:

   - No diretório `backend/`:
     
     ```bash
      node app.js

   - No diretório `frontend/`:
     
     ```bash
      node app.js

5. **Acessar a aplicação**:

   - Abra o navegador e vá para o seguinte endereço:
  
     ```bash
     localhost:30000
     
   - Faça o login utilizando as seguintes credenciais:
  
      - Usuário: `admin`
      - Senha: `admin`
     
