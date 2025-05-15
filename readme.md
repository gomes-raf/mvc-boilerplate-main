# Boilerplate
## Models, Controllers e Endpoints
Models: Faz a conexão do projeto diretamente com o Banco de Dados e cria as funções CRUD como pode ser visto no trecho a seguir:
```javascript
    // Função de deletar do CRUD
async delete(id) {
    await db.query('DELETE FROM professor WHERE id = $1', [id]);
}
``` 


Controllers: É responsável por fazer a ligação entre o Models e o Views, recebendo a requisição e chamando o Models e logo após é chamado por Views, como podemos ver:

```js
// Deletar professor, código inserido em Controller
exports.delete = async (req, res) => {
  const { id } = req.params;
  await Professor.delete(id);
  res.redirect('/professores');
};
```

Endpoint: São os pontos de entrada que o usuário pode interagir com o servidor, sendo dentro do projeto: adição de alunos, adição de cursos, editar aluno, editar curso, etc.