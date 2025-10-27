# banco-web-tests

Este projeto tem como objetivo demonstrar aos alunos da Mentoria 2.0 como automatizar testes de aplicações web utilizando Cypress e JavaScript, com organização de código através de Custom Commands e geração de relatórios avançados.

## Objetivo

Automatizar cenários de testes para a aplicação web "banco-web" consumindo a API "banco-api", exemplificando boas práticas de automação de testes end-to-end com Cypress.

## Componentes do Projeto

- **Cypress**: Framework principal de automação de testes.
- **Custom Commands**: Comandos personalizados para reutilização de código e melhor organização dos testes.
- **cypress-mochawesome-reporter**: Geração de relatórios detalhados e visuais dos testes executados.
- **Estrutura de Pastas**:
  - `cypress/e2e/`: Scripts de testes automatizados.
  - `cypress/support/commands/`: Implementação dos Custom Commands.
  - `cypress/fixtures/`: Dados de apoio (ex: credenciais).
  - `cypress/reports/`: Relatórios gerados após execução dos testes.

## Pré-requisitos

- Node.js (versão recomendada: 18+)
- npm (geralmente instalado junto com o Node.js)
- Clonar e executar:
  - [banco-api](https://github.com/juliodelimas/banco-api)
  - [banco-web](https://github.com/juliodelimas/banco-web)

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/brumff/banco-web-tests.git
   cd banco-web-tests
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Certifique-se de que a API e a aplicação web estejam rodando localmente.

## Execução dos Testes

- Para rodar todos os testes em modo headless:
  ```bash
  npm test
  ```
- Para rodar os testes com interface gráfica:
  ```bash
  npm run cy:open
  ```
- Para rodar os testes com navegador visível:
  ```bash
  npm run cy:headed
  ```

## Relatórios

Após a execução dos testes, os relatórios em HTML estarão disponíveis em `cypress/reports/html/index.html`.

## Estrutura dos Testes

- `cypress/e2e/login.cy.js`: Testes de autenticação e login.
- `cypress/e2e/transferencias.cy.js`: Testes de transferências bancárias.

## Custom Commands

Os Custom Commands estão organizados em `cypress/support/commands/`:

- `common.js`: Comandos utilitários comuns a vários testes.
- `login.js`: Comandos para automação de login.
- `transferencias.js`: Comandos para automação de transferências.

Para utilizar um Custom Command em um teste, basta importar o arquivo desejado em `cypress/support/e2e.js`.

## Dados de Teste

- Os dados de teste (ex: credenciais) estão em `cypress/fixtures/credenciais.json`.

## Contribuição

Sinta-se à vontade para abrir issues ou pull requests para melhorias!

---
Mentoria 2.0 | Automação de Testes com Cypress
