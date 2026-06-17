# DevTask - Sistema de Gerenciamento de Tarefas para Equipes de TI

## Integrantes do Grupo
* Breno De Angeli
* Gabriel de Martin Vasconcelos
* Marcos Vinicius Candido


## Tema Escolhido
**DevTask:** Sistema simplificado voltado para equipes de desenvolvimento controlarem suas sprints e demandas (Bugs, Features, Refatorações) através de uma interface web integrada a uma API assíncrona.

## Como Executar o Projeto

Pré-requisitos
Antes de iniciar, verifique se o Node.js versão 18 ou superior está instalado na sua
máquina. Para confirmar, abra o terminal e execute:
    node -v
    npm -v
Ambos os comandos devem retornar um número de versão. Caso o Node.js não esteja
instalado, baixe em nodejs.org e siga o instalador padrão.
Também é recomendável ter o Visual Studio Code com a extensão Live Server instalada,
para servir o front-end de forma prática.
Estrutura de Pastas
Organize os arquivos do projeto nas seguintes pastas antes de executar:
      devtask/
        ├── server/
        │ ├── server.ts
        │ ├── package.json
        │ └── tsconfig.json
        └── client/
            ├── index.html
            ├── styles.css
            └── app.ts
    ⚠ Atenção: O back-end (server/) e o front-end (client/) ficam em pastas separadas. Cada um
    tem seu próprio terminal durante a execução.

Passo a Passo

Terminal 1 — Iniciar o Servidor (Back-end)

1. Acesse a pasta do servidor
Abra o terminal e navegue até a pasta server/ dentro do projeto.
    cd devtask/server

2. Instale as dependências
Este comando lê o package.json e baixa todas as bibliotecas necessárias (Express,
CORS, TypeScript etc.). Execute apenas uma vez.
    npm install

3. Inicie o servidor em modo desenvolvimento
O ts-node compila e executa o server.ts diretamente, sem precisar gerar arquivos .js
separados. Deixe este terminal aberto durante todo o uso.
    npm run dev

Se tudo correr bem, o terminal exibirá:
    [DEVTASK] API rodando em http://localhost:3000
    [DEVTASK] Rotas disponíveis:
    GET http://localhost:3000/tarefas
    POST http://localhost:3000/tarefas
    PATCH http://localhost:3000/tarefas/:id/status

Terminal 2 — Compilar o Front-end

4. Abra um segundo terminal
Não feche o Terminal 1. Abra uma nova janela ou aba do terminal.

5. Acesse a pasta do client
Navegue até a pasta onde estão os arquivos HTML, CSS e TypeScript do front-end.
cd devtask/client

6. Compile o TypeScript
O comando abaixo transforma o app.ts em app.js, que é o arquivo que o navegador
consegue executar. O arquivo app.js será gerado na mesma pasta.

    npx tsc app.ts --target ES2022 --strict

    ⚠ Atenção: Recompile o app.ts sempre que fizer alterações no código TypeScript do frontend.

Navegador — Abrir a Interface

7. Abra o index.html com o Live Server

    No VS Code, clique com o botão direito sobre o arquivo index.html e selecione Open
    with Live Server. A interface abrirá automaticamente no navegador em
    http://localhost:5500.
