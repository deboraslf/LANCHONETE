<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Cardápio Lanchonete</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;600&display=swap');

  body {
    margin: 0; padding: 0;
    font-family: 'Montserrat', sans-serif;
    background: #fff8f0;
    color: #3a3a3a;
  }
  header {
    background: #ff6f3c;
    color: white;
    padding: 1.5rem 1rem;
    text-align: center;
    box-shadow: 0 4px 12px rgb(255 111 60 / 0.4);
  }
  header h1 {
    margin: 0;
    font-weight: 600;
    font-size: 2.5rem;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  main {
    max-width: 800px;
    margin: 2rem auto 5rem auto;
    padding: 0 1rem;
  }

  section.menu-section {
    margin-bottom: 2rem;
  }
  section.menu-section h2 {
    border-bottom: 3px solid #ff6f3c;
    padding-bottom: 0.3rem;
    margin-bottom: 1rem;
    font-weight: 600;
    font-size: 1.8rem;
    text-transform: uppercase;
  }

  .menu-item {
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.75rem;
    padding-bottom: 0.3rem;
    border-bottom: 1px solid #ffe3d0;
  }
  .menu-item:last-child {
    border-bottom: none;
  }
  .menu-item-name {
    font-weight: 600;
    font-size: 1.1rem;
  }
  .menu-item-desc {
    font-weight: 300;
    color: #71503d;
    font-size: 0.9rem;
    font-style: italic;
  }
  .menu-item-price {
    font-weight: 600;
    color: #ff6f3c;
    font-size: 1.1rem;
  }

  footer {
    background: #ff6f3c;
    color: white;
    text-align: center;
    padding: 2rem 1rem 3rem 1rem;
    position: relative;
  }
  footer .github-text {
    margin-bottom: 1rem;
    font-size: 1.2rem;
    font-weight: 600;
  }
  #qrcode {
    margin: 0 auto;
    width: 150px;
    height: 150px;
  }
  @media (max-width: 480px) {
    header h1 {
      font-size: 1.8rem;
    }
    main {
      margin: 1rem auto 4rem auto;
    }
    section.menu-section h2 {
      font-size: 1.4rem;
    }
    .menu-item-name, .menu-item-price {
      font-size: 1rem;
    }
    .menu-item-desc {
      font-size: 0.85rem;
    }
  }
</style>
</head>
<body>
<header>
  <h1>Lanchonete Sabor & Cia</h1>
</header>

<main>
  <section class="menu-section" id="salgados">
    <h2>Salgados</h2>
    <div class="menu-item">
      <div>
        <div class="menu-item-name">Coxinha de Frango</div>
        <div class="menu-item-desc">Massa crocante, recheio saboroso de frango desfiado.</div>
      </div>
      <div class="menu-item-price">R$ 6,00</div>
    </div>
    <div class="menu-item">
      <div>
        <div class="menu-item-name">Esfiha de Carne</div>
        <div class="menu-item-desc">Massa leve recheada com carne temperada.</div>
      </div>
      <div class="menu-item-price">R$ 7,50</div>
    </div>
    <div class="menu-item">
      <div>
        <div class="menu-item-name">Rissole de Queijo</div>
        <div class="menu-item-desc">Recheio cremoso de queijo derretido.</div>
      </div>
      <div class="menu-item-price">R$ 5,50</div>
    </div>
  </section>

  <section class="menu-section" id="bebidas">
    <h2>Bebidas</h2>
    <div class="menu-item">
      <div class="menu-item-name">Refrigerante 350ml</div>
      <div class="menu-item-price">R$ 4,00</div>
    </div>
    <div class="menu-item">
      <div class="menu-item-name">Suco Natural 300ml</div>
      <div class="menu-item-price">R$ 5,00</div>
    </div>
    <div class="menu-item">
      <div class="menu-item-name">Café Expresso</div>
      <div class="menu-item-price">R$ 3,50</div>
    </div>
  </section>

  <section class="menu-section" id="combos">
    <h2>Combos</h2>
    <div class="menu-item">
      <div>
        <div class="menu-item-name">Combo Coxinha + Refrigerante</div>
        <div class="menu-item-desc">Economize com essa combinação deliciosa</div>
      </div>
      <div class="menu-item-price">R$ 9,50</div>
    </div>
    <div class="menu-item">
      <div>
        <div class="menu-item-name">Combo Esfiha + Suco Natural</div>
        <div class="menu-item-desc">Combo saudável e saboroso.</div>
      </div>
      <div class="menu-item-price">R$ 10,00</div>
    </div>
  </section>
</main>

<footer>
  <div class="github-text">Nos acompanhe no GitHub</div>
  <div id="qrcode"></div>
  <div style="margin-top: 1rem; font-size: 0.9rem;">github.com/seu-usuario</div>
</footer>

<script src="https://cdn.jsdelivr.net/npm/qrcode@1.5.1/build/qrcode.min.js"></script>
<script>
  const githubUrl = 'https://github.com/seu-usuario'; // Replace 'seu-usuario' with your GitHub user or repo URL
  const qrcodeContainer = document.getElementById('qrcode');
  QRCode.toCanvas(qrcodeContainer, githubUrl, { width: 150, margin: 2 }, function (error) {
    if (error) console.error(error);
  });
</script>
</body>
</html>


      
      

        
