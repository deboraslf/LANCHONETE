<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cardápio Digital - Lanchonete</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      gap: 50px;
    }

    .phone-frame {
      width: 300px;
      height: 600px;
      background: #000;
      border-radius: 40px;
      padding: 20px 10px;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .screen {
      width: 100%;
      height: 100%;
      background: white;
      border-radius: 30px;
      overflow-y: auto;
      padding: 20px;
    }

    .cardapio-item {
      margin-bottom: 20px;
      padding-bottom: 10px;
      border-bottom: 1px solid #ccc;
    }

    .cardapio-item h3 {
      margin: 0;
      color: #e91e63;
    }

    .cardapio-item p {
      margin: 5px 0 0;
      color: #555;
    }

    .qr-code {
      text-align: center;
    }

    .qr-code img {
      width: 200px;
      height: 200px;
    }

    .qr-code p {
      margin-top: 10px;
      font-size: 14px;
      color: #333;
    }
  </style>
</head>
<body>

  <div class="phone-frame">
    <div class="screen">
      <h2>🍔 Cardápio Digital</h2>
      <div class="cardapio-item">
        <h3>X-Burguer</h3>
        <p>Pão, carne, queijo, alface, tomate - R$12,00</p>
      </div>
      <div class="cardapio-item">
        <h3>X-Salada</h3>
        <p>Pão, carne, queijo, salada - R$13,50</p>
      </div>
      <div class="cardapio-item">
        <h3>Batata Frita</h3>
        <p>Porção média - R$8,00</p>
      </div>
      <div class="cardapio-item">
        <h3>Refrigerante</h3>
        <p>Lata - R$5,00</p>
      </div>
    </div>
  </div>

  <div class="qr-code">
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://git@github.com:deboraslf/LANCHONETE.git" alt="QR Code">
    <p>Escaneie o QR Code<br>para acessar o cardápio online</p>
  </div>

</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Cardápio da Lanchonete</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fff8e1;
      color: #333;
      padding: 20px;
    }

    h1 {
      color: #d84315;
      text-align: center;
    }

    table {
      width: 60%;
      margin: 0 auto;
      border-collapse: collapse;
      background-color: #ffffff;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    th, td {
      padding: 12px;
      border: 1px solid #ccc;
      text-align: left;
    }

    th {
      background-color: #ffe0b2;
    }

    tr:hover {
      background-color: #fff3e0;
    }
  </style>
</head>
<body>
  <h1>🍔 Cardápio da Lanchonete</h1>
  <table>
    <tr>
      <th>Produto</th>
      <th>Preço</th>
    </tr>
    <tr>
      <td>X-Burguer</td>
      <td>R$ 10,00</td>
    </tr>
    <tr>
      <td>Pizza de Calabresa</td>
      <td>R$ 25,00</td>
    </tr>
    <tr>
      <td>Açaí com Banana</td>
      <td>R$ 12,00</td>
    </tr>
    <tr>
      <td>Refrigerante</td>
      <td>R$ 5,00</td>
    </tr>
  </table>
</body>
</html>

