# Rafitcha-QA

Este repositório foi criado para fornecer exemplos práticos e educativos de testes em QA, tanto manuais quanto automatizados, testes pessoais e com foco em aplicações web e APIs. Ele é ideal para iniciantes que estão aprendendo sobre Quality Assurance e desejam ver exemplos de testes reais.

Aqui você encontrará:
- Testes manuais com casos de uso simples.
- Testes de API utilizando Postman.
- Testes automatizados com Cypress.
- Dicas sobre como testar e depurar aplicações.

Este repositório é um excelente ponto de partida para quem quer aprender mais sobre o mundo de QA.


## 🔧 Ferramentas utilizadas
- [Cypress](https://www.cypress.io/)
- [Postman](https://www.postman.com/)
- [JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
- [Jest](https://jestjs.io/)
- [Insomnia](https://insomnia.rest/)
- [Swagger](https://swagger.io/)



O que é um repositório ?

Um repositório (ou repo) é um espaço onde você armazena e gerencia o código-fonte de um projeto. Ele funciona como uma "biblioteca" para seu código e outros arquivos importantes (documentação, testes, configurações), e pode ser local (no seu computador) ou remoto (em serviços como GitHub, GitLab, Bitbucket).

No contexto de desenvolvimento de software, os repositórios são usados para:

1. Versionamento de Código
O repositório permite o controle de versões, o que significa que você pode manter um histórico completo das alterações feitas no código ao longo do tempo. Isso é muito útil para poder:

Reverter para versões anteriores do código.

Colaborar com outras pessoas sem sobrescrever o trabalho de alguém.

Ver as mudanças feitas por diferentes desenvolvedores.

2. Colaboração
Em projetos colaborativos, vários desenvolvedores podem trabalhar no mesmo repositório. Usando ferramentas de controle de versão (como Git), é possível gerenciar alterações, resolver conflitos e unir diferentes partes do código de maneira organizada.

3. Armazenamento e Organização
O repositório organiza os arquivos do projeto, como código-fonte, bibliotecas, testes, e até documentação. Ele pode ser estruturado em pastas e arquivos para facilitar o gerenciamento do projeto.

4. Backup e Acesso Remoto
Se o repositório for hospedado remotamente (por exemplo, no GitHub), você tem um backup do seu código, o que reduz o risco de perda. Além disso, você pode acessar o repositório de qualquer lugar, desde que tenha uma conexão com a internet.

5. Automação e Integração Contínua
Repositórios também podem ser configurados para rodar processos automáticos como testes, builds e deploys quando há atualizações no código. Isso é conhecido como Integração Contínua (CI) e Entrega Contínua (CD).

Exemplos de Repositórios:
GitHub: Plataforma popular para hospedagem de repositórios Git, onde desenvolvedores podem compartilhar código, colaborar e usar funcionalidades como "issues", "pull requests" e "actions".

GitLab: Outra plataforma de hospedagem de repositórios Git, com recursos de CI/CD integrados.

Bitbucket: Serviço similar ao GitHub, com foco em equipes e integração com o Jira.

Estrutura Básica de um Repositório Git
Dentro de um repositório, você pode ter diversas pastas e arquivos, como:

README.md: Arquivo de documentação onde você explica o propósito do projeto, como usá-lo, como rodar os testes, etc.

.gitignore: Arquivo onde você especifica quais arquivos ou pastas não devem ser versionados.

Pasta "src" ou "app": Contém o código-fonte do projeto.

Pasta "tests": Contém os testes do projeto.

Pasta "docs": Pode conter a documentação do projeto.

Exemplificando:
Quando você cria um repositório no GitHub, você pode adicionar seu código, gerenciar issues (tarefas ou bugs), criar branches para novas funcionalidades e colaborar com outros desenvolvedores.

Em resumo, um repositório é um local centralizado e organizado para armazenar e gerenciar o código e outros arquivos importantes de um projeto. Ele é essencial para o trabalho em equipe e o controle de versões no desenvolvimento de software.



- Tecnologias Utilizadas

Este repositório utiliza as seguintes ferramentas e tecnologias:

- **Cypress**: Framework para automação de testes end-to-end em aplicações web.
- **Postman**: Ferramenta para realizar e testar APIs REST.
- **Jira**: Para gestão de tarefas e bugs.
- **Git/GitHub**: Para versionamento de código e colaboração.



- Como Rodar os Testes

  ## Como Rodar os Testes?

### Testes Manuais
Os testes manuais estão localizados na pasta `testes-manuais`. Eles incluem casos de teste em planilhas e listas de verificação. Para visualizá-los:

1. Acesse a pasta `testes-manuais`.
2. Abra os arquivos `casos-de-teste-exemplo.xlsx` e `bugs-comuns.md`.

### Testes de API
Os testes de API estão na pasta `testes-api`. Para rodar os testes do Postman:

1. Baixe o arquivo `exemplo-usuarios.postman_collection.json`.
2. Importe o arquivo para o Postman.
3. Execute os testes diretamente no Postman.

### Testes Automatizados (Cypress)
Os testes automatizados estão na pasta `testes-automatizados`.

1. Acesse a pasta `testes-automatizados`.
2. Execute o comando `npm install` para instalar as dependências.
3. Inicie o Cypress com o comando:
   ```bash
   npx cypress open
Isso abrirá a interface gráfica do Cypress onde você pode rodar os testes automaticamente.

bash
Copiar
Editar



### 4. **Exemplos de Testes**
Seria interessante incluir alguns exemplos rápidos de testes manuais, de API e automatizados para que o visitante entenda o que esperar do repositório.


## Exemplos de Testes

### Teste Manual de Login (exemplo.xlsx)
Um caso de teste simples onde o usuário deve:
1. Entrar na página de login.
2. Preencher o campo de e-mail e senha.
3. Verificar se o login é bem-sucedido e redireciona para o painel principal.

### Teste de API - GET Usuários (Postman)
- Envia um request GET para `/users`.
- Verifica se o status code é 200 e se a resposta contém a lista de usuários.

### Teste Automatizado - Login com Cypress (login.spec.cy.js)
```javascript
describe('Teste de Login - Aplicação Web', () => {
  it('Deve realizar login com sucesso', () => {
    cy.visit('https://exemplo.com/login');
    cy.get('#email').type('usuario@teste.com');
    cy.get('#senha').type('senha123');
    cy.get('#botao-login').click();
    cy.url().should('include', '/dashboard');
  });
});



Incluir uma seção de contribuição explicando como outros desenvolvedores podem contribuir para o repositório, abrir pull requests ou adicionar novos testes.

Este projeto é **aberto** e contribuições são bem-vindas!

Se você deseja contribuir:
1. Fork o repositório.
2. Crie uma branch para a sua funcionalidade (`git checkout -b nova-funcionalidade`).
3. Faça o commit das suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`).
4. Envie o código para o seu repositório forkado (`git push origin nova-funcionalidade`).
5. Abra um Pull Request para o repositório original.

Fique à vontade para adicionar novos testes, corrigir bugs ou melhorar a documentação.

  
Licença
Se você optar por tornar o repositório open source, adicione uma seção de licença explicando qual licença você está utilizando (exemplo: MIT).


Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.




## 👩‍💻 Autora

**Rafaela Marcionila**  
Especialista em QA com foco em testes manuais, automatizados e funcionais para aplicações Web e Mobile.  
Experiência com Cielo, Keeggo Technology e outras empresas do setor de pagamentos digitais.  
📍 São Paulo - SP  
📧 marcionila.qa@email.com 
📎 [LinkedIn](https://www.linkedin.com/in/rafaela-marcionila-799557193/)

