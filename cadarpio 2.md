<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cardápio Digital - Burguer Delícia</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            color: #fff;
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            display: flex;
            max-width: 1200px;
            width: 100%;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
        }

        .menu-container {
            flex: 3;
            padding: 30px;
            border-right: 1px solid rgba(255, 255, 255, 0.1);
        }

        .phone-container {
            flex: 2;
            padding: 30px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: rgba(0, 0, 0, 0.2);
        }

        header {
            text-align: center;
            padding: 20px 0;
            margin-bottom: 30px;
        }

        .logo {
            font-size: 2.8rem;
            margin-bottom: 15px;
            color: #ff6b6b;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #ff6b6b, #ff9e7d);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        header p {
            font-size: 1.1rem;
            opacity: 0.8;
            max-width: 600px;
            margin: 0 auto;
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }

        .menu-item {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .menu-item:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.12);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }

        .item-content {
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .item-title {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .item-title h3 {
            font-size: 1.3rem;
            color: #ff9e7d;
        }

        .item-price {
            font-weight: bold;
            color: #ff6b6b;
            font-size: 1.2rem;
        }

        .item-description {
            color: #aaa;
            margin-bottom: 15px;
            font-size: 0.95rem;
            min-height: 60px;
        }

        .item-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: auto;
        }

        .tag {
            background: #4ecdc4;
            color: #1a1a2e;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        .tag.vegetarian {
            background: #2ecc71;
        }

        .tag.spicy {
            background: #e74c3c;
            color: white;
        }

        .tag.new {
            background: #3498db;
            color: white;
        }

        /* Phone Demo */
        .phone-demo {
            width: 280px;
            height: 560px;
            background: #0f0f1a;
            border-radius: 30px;
            position: relative;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.6);
            overflow: hidden;
            border: 8px solid #222;
        }

        .phone-screen {
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #2c3e50, #1a1a2e);
            overflow-y: auto;
            padding: 15px;
        }

        .phone-header {
            text-align: center;
            padding: 15px 0;
        }

        .phone-header h3 {
            font-size: 1.2rem;
            color: #ff6b6b;
        }

        .phone-items {
            padding: 10px;
        }

        .phone-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 12px;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
        }

        .phone-item img {
            width: 50px;
            height: 50px;
            border-radius: 8px;
            margin-right: 12px;
            background: #4ecdc4;
        }

        .phone-item-content {
            flex: 1;
        }

        .phone-item-title {
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
        }

        .phone-item-name {
            font-weight: bold;
            color: #ff9e7d;
        }

        .phone-item-price {
            color: #ff6b6b;
            font-weight: bold;
        }

        .phone-item-desc {
            font-size: 0.7rem;
            color: #aaa;
            margin-top: 3px;
        }

        /* QR Code Section */
        .qr-section {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            width: 100%;
            max-width: 300px;
        }

        .qr-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: #4ecdc4;
        }

        .qr-code {
            width: 180px;
            height: 180px;
            background: #fff;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 12px;
            margin-bottom: 20px;
        }

        .qr-code i {
            font-size: 5rem;
            color: #333;
        }

        .qr-instructions {
            font-size: 0.9rem;
            color: #aaa;
            margin-bottom: 20px;
        }

        .qr-button {
            background: linear-gradient(90deg, #ff6b6b, #ff9e7d);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            width: 100%;
            max-width: 200px;
        }

        .qr-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
        }

        /* Footer */
        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Responsividade */
        @media (max-width: 900px) {
            .container {
                flex-direction: column;
            }
            
            .menu-container {
                border-right: none;
                border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            }
            
            .phone-container {
                padding: 40px 20px;
            }
        }

        @media (max-width: 480px) {
            .menu-grid {
                grid-template-columns: 1fr;
            }
            
            .phone-demo {
                transform: scale(0.85);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="menu-container">
            <header>
                <div class="logo">
                    <i class="fas fa-hamburger"></i>
                </div>
                <h1>BURGUER DELÍCIA</h1>
                <p>Cardápio Digital - Sabor autêntico em cada mordida</p>
            </header>
            
            <div class="menu-grid">
                <div class="menu-item">
                    <div class="item-content">
                        <div class="item-title">
                            <h3>Burguer Clássico</h3>
                            <div class="item-price">R$ 24,90</div>
                        </div>
                        <p class="item-description">Pão brioche, hambúrguer 180g, queijo cheddar, alface, tomate e molho especial.</p>
                        <div class="item-tags">
                            <div class="tag">Mais vendido</div>
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="item-content">
                        <div class="item-title">
                            <h3>Burguer Bacon</h3>
                            <div class="item-price">R$ 29,90</div>
                        </div>
                        <p class="item-description">Pão australiano, hambúrguer 200g, queijo prato, bacon crocante, cebola caramelizada.</p>
                        <div class="item-tags">
                            <div class="tag spicy">Picante</div>
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="item-content">
                        <div class="item-title">
                            <h3>Burguer Vegano</h3>
                            <div class="item-price">R$ 26,90</div>
                        </div>
                        <p class="item-description">Pão integral, hambúrguer de grão-de-bico, abobrinha grelhada, tomate seco e maionese vegana.</p>
                        <div class="item-tags">
                            <div class="tag vegetarian">Vegetariano</div>
                            <div class="tag new">Novidade</div>
                        </div>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="item-content">
                        <div class="item-title">
                            <h3>Double Cheddar</h3>
                            <div class="item-price">R$ 32,90</div>
                        </div>
                        <p class="item-description">Dois hambúrgueres 160g, dupla camada de cheddar cremoso, cebola roxa e molho barbecue.</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="item-content">
                        <div class="item-title">
                            <h3>Frango Crocante</h3>
                            <div class="item-price">R$ 27,90</div>
                        </div>
                        <p class="item-description">Filé de frango empanado, alface, tomate, maionese especial e pão com gergelim.</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="item-content">
                        <div class="item-title">
                            <h3>X-Tudo</h3>
                            <div class="item-price">R$ 34,90</div>
                        </div>
                        <p class="item-description">Hambúrguer, queijo, presunto, bacon, ovo, alface, tomate e batata palha.</p>
                        <div class="item-tags">
                            <div class="tag">Família</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <footer>
                <p>Horário de funcionamento: Segunda a Sábado - 11h às 23h | Domingo - 12h às 22h</p>
                <p>Delivery: (11) 5555-1234 | www.burguerdelicia.com.br</p>
            </footer>
        </div>
        
        <div class="phone-container">
            <div class="phone-demo">
                <div class="phone-screen">
                    <div class="phone-header">
                        <h3>BURGUER DELÍCIA</h3>
                        <p>Cardápio Digital</p>
                    </div>
                    
                    <div class="phone-items">
                        <div class="phone-item">
                            <div style="background:#ff6b6b; width:50px; height:50px; border-radius:8px; display:flex; align-items:center; justify-content:center; margin-right:12px;">
                                <i class="fas fa-hamburger" style="color:white;"></i>
                            </div>
                            <div class="phone-item-content">
                                <div class="phone-item-title">
                                    <span class="phone-item-name">Clássico</span>
                                    <span class="phone-item-price">R$24,90</span>
                                </div>
                                <div class="phone-item-desc">Pão brioche, carne 180g</div>
                            </div>
                        </div>
                        
                        <div class="phone-item">
                            <div style="background:#ff9e7d; width:50px; height:50px; border-radius:8px; display:flex; align-items:center; justify-content:center; margin-right:12px;">
                                <i class="fas fa-bacon" style="color:white;"></i>
                            </div>
                            <div class="phone-item-content">
                                <div class="phone-item-title">
                                    <span class="phone-item-name">Bacon</span>
                                    <span class="phone-item-price">R$29,90</span>
                                </div>
                                <div class="phone-item-desc">Bacon crocante, cebola caramelizada</div>
                            </div>
                        </div>
                        
                        <div class="phone-item">
                            <div style="background:#2ecc71; width:50px; height:50px; border-radius:8px; display:flex; align-items:center; justify-content:center; margin-right:12px;">
                                <i class="fas fa-leaf" style="color:white;"></i>
                            </div>
                            <div class="phone-item-content">
                                <div class="phone-item-title">
                                    <span class="phone-item-name">Vegano</span>
                                    <span class="phone-item-price">R$26,90</span>
                                </div>
                                <div class="phone-item-desc">Grão-de-bico, abobrinha, tomate seco</div>
                            </div>
                        </div>
                        
                        <div class="phone-item">
                            <div style="background:#3498db; width:50px; height:50px; border-radius:8px; display:flex; align-items:center; justify-content:center; margin-right:12px;">
                                <i class="fas fa-glass-whiskey" style="color:white;"></i>
                            </div>
                            <div class="phone-item-content">
                                <div class="phone-item-title">
                                    <span class="phone-item-name">Refrigerante</span>
                                    <span class="phone-item-price">R$8,90</span>
                                </div>
                                <div class="phone-item-desc">Lata 350ml - diversos sabores</div>
                            </div>
                        </div>
                        
                        <div class="phone-item">
                            <div style="background:#9b59b6; width:50px; height:50px; border-radius:8px; display:flex; align-items:center; justify-content:center; margin-right:12px;">
                                <i class="fas fa-ice-cream" style="color:white;"></i>
                            </div>
                            <div class="phone-item-content">
                                <div class="phone-item-title">
                                    <span class="phone-item-name">Brownie</span>
                                    <span class="phone-item-price">R$16,90</span>
                                </div>
                                <div class="phone-item-desc">Com sorvete de creme</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="qr-section">
                <h3 class="qr-title">Acesse pelo seu celular</h3>
                <div class="qr-code">
                    <i class="fas fa-qrcode"></i>
                </div>
                <p class="qr-instructions">Escaneie o QR Code com a câmera do seu celular para acessar nosso cardápio digital</p>
                <button class="qr-button">Ver Cardápio Completo</button>
            </div>
        </div>
    </div>
</body>
</html>
  <div class="qr-code">
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://git@github.com:deboraslf/LANCHONETE.git" alt="QR Code">
    <p>Escaneie o QR Code<br>para acessar o cardápio online</p>
  </div>
