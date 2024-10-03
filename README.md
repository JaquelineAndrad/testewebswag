Projeto de Automação de Testes com Cypress
Descrição
Este projeto é uma automação de testes funcional desenvolvida com o framework Cypress para testar as funcionalidades da aplicação web SauceDemo. O objetivo é garantir a qualidade das principais interações do usuário com o sistema, como login, adição e remoção de itens do carrinho, e fluxo de checkout.

Funcionalidades Testadas
Login com credenciais válidas e inválidas
Adição de itens ao carrinho
Remoção de itens do carrinho
Cancelamento de compra
Checkout do carrinho
Logout da aplicação
Pré-requisitos
Para rodar o projeto localmente, você precisa ter instalado:

Node.js (versão 14 ou superior)
Git

Como rodar o projeto

Clone o repositório:git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio


Instale as dependências: Certifique-se de estar no diretório raiz do projeto e execute:
npm install

Rodar os testes: Para rodar todos os testes usando o Cypress:
npx cypress open

Ou para rodar os testes diretamente no terminal:
npx cypress run


Claro! Um bom arquivo README.md é essencial para explicar o que o seu projeto faz, como ele funciona e como outros podem usar e contribuir com ele. Aqui está um modelo que você pode usar como ponto de partida para o seu projeto de automação de testes com Cypress:

Projeto de Automação de Testes com Cypress
Descrição
Este projeto é uma automação de testes funcional desenvolvida com o framework Cypress para testar as funcionalidades da aplicação web SauceDemo. O objetivo é garantir a qualidade das principais interações do usuário com o sistema, como login, adição e remoção de itens do carrinho, e fluxo de checkout.

Funcionalidades Testadas
Login com credenciais válidas e inválidas
Adição de itens ao carrinho
Remoção de itens do carrinho
Cancelamento de compra
Checkout do carrinho
Logout da aplicação
Pré-requisitos
Para rodar o projeto localmente, você precisa ter instalado:

Node.js (versão 14 ou superior)
Git
Como rodar o projeto
Clone o repositório:

bash
Copiar código
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
Instale as dependências: Certifique-se de estar no diretório raiz do projeto e execute:

bash
Copiar código
npm install
Rodar os testes: Para rodar todos os testes usando o Cypress:

bash
Copiar código
npx cypress open
Ou para rodar os testes diretamente no terminal:
npx cypress run


Estrutura do Projeto
cypress/e2e/: Contém os testes end-to-end.
cypress/fixtures/: Contém dados de exemplo usados nos testes (se aplicável).
cypress/support/: Contém comandos customizados e configuração global dos testes.
cypress.config.js: Arquivo de configuração do Cypress.
Exemplo de Teste
Aqui está um exemplo de um teste de login funcional:

describe('Teste de Login', () => {
  it('Deve fazer login com credenciais válidas', () => {
    cy.visit('https://www.saucedemo.com/v1/')
    cy.get('#user-name').type('standard_user')
    cy.get('#password').type('secret_sauce')
    cy.get('#login-button').click()
    cy.url().should('include', '/inventory.html')
  })
})

Integração Contínua
Este projeto utiliza GitHub Actions para rodar automaticamente os testes Cypress em cada push ou pull request.
O workflow está configurado em .github/workflows/cypress.yml e pode ser ajustado conforme necessário.



