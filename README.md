# projeto-fabrica-de-software-docs
Esse projeto é feito para a documentação da disciplina de Qualidade de Software e busca desenvolver um mini e-commerce, chamado EvoSports.

<h2>Tipos de Dados:</h2>
<ul>
  <li>nomeProduto: string</li>
  <li>descricaoProduto: string</li>
  <li>tamanhoProduto: string</li>
  <li>valorProduto: decimal(9,2)</li>
  <li>imgProduto: string</li>
  <li>statusProduto: integer (0 = inativo; 1 = ativo)</li>
</ul>

<h2>Como consumir a API?</h2>
<h4>Listar Produtos</h4>
<ul>
  <li>Envie a requisição <b>GET</b> para o seguinte endpoint: https://apoleon.com.br/api/listarProdutos</li>
</ul>

<h4>Inserir um novo produto</h4>
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

<h4>Editar um produto</h4>
<ul>
  <li>Envie a requisição <b>PUT</b> para o seguinte endpoint: https://apoleon.com.br/api/produto/{id}</li>
  <li>Formatação dos dados para envio ao endpoint: </li>
</ul>


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
