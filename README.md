# TesteLogincy.js-Projeto-QA-cypress12
Projeto de testes automatizado utilizando Cypress.
describe('Testar a página de login',()=>{
    it('Testar a tela de login',()=>{
        cy.visit('https://127.0.0.1:5500/login.html')
        cy.get ('span[class="login-from-title"]')
        .contains('Faça seu login').should('contain','Faça seu login')
        cy.get('input[id="login"]').should('be.visible')  
        .click().type('Automação de testes').should('have.value', 'Automação de testes')
         cy.get('input[id="senha"]' ).should('be.visible') 
         cy.get('input[id="senha"]') 
         .click().type('12345678').should('have.value', '12345678')
         /*verificar que a imagem do projeto existe*/
         cy.get('img[src="./imagens/login.png"]')
         .should('be.visible')
         cy.get('img'[class="margin-left-50"]')
            .should('be.visible')
            /*verificar que o botão de login existe */
            cy.get('button[class="login-form-btn"]').contains('login')
            .should('be.visible').click()
                      
