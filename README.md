# Documentação do Projeto Fábrica de Software
Esse projeto é feito para a documentação da disciplina de Qualidade de Software e busca desenvolver um mini e-commerce, chamado EvoSports.

<br/>

<h1>Tipos de Dados:</h1>
<ul>
  <li>nomeProduto: string</li>
  <li>descricaoProduto: string</li>
  <li>tamanhoProduto: string</li>
  <li>valorProduto: decimal(9,2)</li>
  <li>imgProduto: string</li>
  <li>statusProduto: integer (0 = inativo; 1 = ativo)</li>
</ul>

<br/>

<h1>Como consumir a API?</h1>

<h2>Listar produtos</h2>
<ul>
  <li>Envie a requisição <b>GET</b> para o seguinte endpoint: https://apoleon.com.br/api/produtos</li>
</ul>

<br/><br/>

<h2>Inserir um novo produto</h2>
<ul>
  <li>Envie a requisição <b>POST</b> para o seguinte endpoint: https://apoleon.com.br/api/produto</li>
  <li>Formatação dos dados para envio ao endpoint: </li>
</ul>


   ```json
    {
      "nomeProduto": "Nome do Produto",
      "descricaoProduto": "Descrição do produto",
      "tamanhoProduto": "Tamanho do Produto",
      "valorProduto": "Valor do produto (sem aspas)" ,
      "imgProduto": "Imagem do Produto",
      "qrCodeProduto": "QR Code do Produto",
      "statusProduto": "Status do Produto (sem aspas)" 
    }
   ```

<br/><br/>

<h2>Editar um produto</h2>
<ul>
  <li>Envie a requisição <b>PUT</b> para o seguinte endpoint: https://apoleon.com.br/api/produto/{id}</li>
  <li>Formatação dos dados para envio ao endpoint: </li>



   ```json
    {
      "nomeProduto": "Nome do Produto editado",
      "descricaoProduto": "Descrição do produto editado",
      "tamanhoProduto": "Tamanho do Produto editado",
      "valorProduto": "Valor do produto editado (sem aspas)" ,
      "imgProduto": "Imagem do Produto editado",
      "qrCodeProduto": "QR Code do Produto editado",
      "statusProduto": "Status do Produto editado (sem aspas)" 
    }
   ```
<li>Resposta esperada:</li>

  ```json
    {
      "status": true,
      "message": "Produto atualizado com sucesso!"
    }
  ```

<li>Caso a requisição falhe: </li>

 ```json
    {
      "status": false,
      "message": "Mensagem de erro"
    }
  ```

</ul>
  

<br/><br/>

<h2>Desativar um produto</h2>
<ul>
  <li>Envie a requisição <b>PATCH</b> para o seguinte endpoint: https://apoleon.com.br/api/produto/{id}/desativar</li>
  <li>Resposta esperada: </li>

  ```json
    {
        "status": true,
        "message": "Produto desativado com sucesso!"
    }
  ```

<li>Caso a requisição falhe: </li>

 ```json
    {
      "status": false,
      "message": "Mensagem de erro"
    }
  ```
</ul>

<br/><br/>

<h2>Ativar um produto</h2>
<ul>
  <li>Envie a requisição <b>PATCH</b> para o seguinte endpoint: https://apoleon.com.br/api/produto/{id}/ativar</li>
  <li>Resposta esperada: </li>

  ```json
    {
        "status": true,
        "message": "Produto ativado com sucesso!"
    }
  ```

<li>Caso a requisição falhe: </li>

 ```json
    {
      "status": false,
      "message": "Mensagem de erro"
    }
  ```
</ul>

<hr/>

<h2>Listar usuários</h2>
<ul>
  <li>Envie a requisição <b>GET</b> para o seguinte endpoint: https://apoleon.com.br/api/listarUsuarios</li>
  <li>Resposta esperada: </li>

  ```json
    {
      "id": "id do usuário",
      "name": "nome do usuário",
      "email": "email do usuário",
      "email_verified_at": "data de verificação do email",
      "created_at": "data de criação do usuário",
      "updated_at": "data de atualização do usuário"
    }
  ```

<li>Caso a requisição falhe: </li>

 ```json
    {
      "status": false,
      "message": "Mensagem de erro"
    }
  ```
</ul>
