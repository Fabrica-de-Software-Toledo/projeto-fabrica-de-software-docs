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
  <li>Envie a requisição <b>GET</b> para o seguinte endpoint: https://apoleon.com.br/api/listarProdutos</li>
</ul>

<br/><br/>

<h2>Inserir um novo produto</h2>
<ul>
  <li>Envie a requisição <b>POST</b> para o seguinte endpoint: https://apoleon.com.br/api/inserirProduto</li>
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
  <li>Envie a requisição <b>PATCH</b> para o seguinte endpoint: https://apoleon.com.br/api/desativarProduto/{id}</li>
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
