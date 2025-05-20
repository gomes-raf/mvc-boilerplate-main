# Boilerplate
## Models, Controllers e Endpoints
Models: Faz a conexão do projeto diretamente com o Banco de Dados e cria as funções CRUD que são chamadas em Controllers.

Controllers: É responsável por fazer a ligação entre o Models e o Views, recebendo a requisição e chamando o Models e logo após é chamado por Views.

View: Recebe os comandos do Controllers e transforma em algo interativo com o usuário.

## JSON
O envio e o recebimento de dados ocorre por meio da interação citada anteriormente entre Models, Controllers e Views. Um exemplo de rota é: 
```js
router.post('/delete/:id', controller.destroy);
```
Essa rota consiste em deletar um aluno criado, puxando este comando de Controllers.

## HTML
O HTML permite criar e exibir as informações de uma forma primária e básica facilitando uma visão inicial do projeto.