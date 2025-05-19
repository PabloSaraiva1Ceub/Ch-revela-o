<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Chá Revelação - Convite Animado</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Poppins:wght@400;700&display=swap');

  /* Reset */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body, html {
    height: 100%;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #6a11cb, #2575fc);
    overflow-x: hidden;
  }

  .container {
    height: 100vh;
    width: 100vw;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background: linear-gradient(to bottom right, #a2d5ab 0%, #7050a1 100%);
    overflow: hidden;
  }

  /* --- CAIXA SURPRESA --- */
  .gift-box {
    width: 300px;
    height: 300px;
    background: linear-gradient(135deg, #6a11cb 0%, #b576f0 100%);
    border-radius: 40px 40px 25px 25px;
    box-shadow: 0 15px 25px rgba(0,0,0,0.3);
    position: relative;
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    animation: pulse 2s infinite ease-in-out;
    user-select: none;
    z-index: 10;
  }
  .gift-box:hover {
    box-shadow: 0 20px 35px rgba(0,0,0,0.5);
  }

  .lid {
    width: 280px;
    height: 80px;
    background: linear-gradient(135deg, #2575fc 0%, #6a11cb 100%);
    border-radius: 40px 40px 0 0;
    position: absolute;
    top: -70px;
    box-shadow: 0 10px 15px rgba(0,0,0,0.2);
    transition: transform 0.8s ease;
    transform-origin: center bottom;
    z-index: 20;
  }

  /* Texto dentro da caixa */
  .gift-text {
    font-family: 'Fredoka One', cursive;
    color: #fff;
    font-size: 1.5rem;
    margin-top: 10px;
    user-select: none;
    text-shadow: 0 0 8px #a17fff;
  }

  /* Animação de pulsar */
  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.07); }
  }

  /* Explosão de confetes */
  .confetti {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 300px;
    height: 300px;
    pointer-events: none;
    transform: translate(-50%, -50%);
    overflow: visible;
    z-index: 15;
  }
  .confetti-piece {
    position: absolute;
    width: 10px;
    height: 10px;
    opacity: 0;
    border-radius: 3px;
  }
  /* Confetes cores roxo e verde sóbrio */
  .confetti-piece.purple {
    background-color: #6a11cb;
  }
  .confetti-piece.green {
    background-color: #4caf50;
  }

  /* Tela convite */
  .invite {
    display: none;
    background: #fff;
    max-width: 520px;
    width: 90vw;
    border-radius: 30px;
    padding: 40px 30px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.15);
    text-align: center;
    position: relative;
    overflow: hidden;
    user-select: none;
    z-index: 20;
  }

  /* Balões animados */
  .balloon {
    position: absolute;
    bottom: -100px;
    width: 50px;
    height: 70px;
    border-radius: 50% / 60%;
    background: #6a11cb;
    opacity: 0.9;
    animation: floatUp linear forwards;
  }
  .balloon.green {
    background: #4caf50;
  }
  .balloon::after {
    content: "";
    position: absolute;
    bottom: -20px;
    left: 50%;
    width: 2px;
    height: 20px;
    background: #555;
    transform: translateX(-50%);
  }

  @keyframes floatUp {
    0% {
      bottom: -100px;
      opacity: 0;
      transform: translateX(0) rotate(0deg);
    }
    10% {
      opacity: 1;
    }
    100% {
      bottom: 110%;
      opacity: 0;
      transform: translateX(var(--move-x, 0)) rotate(360deg);
    }
  }

  /* Texto do convite */
  .invite h1 {
    font-family: 'Fredoka One', cursive;
    font-size: 3rem;
    color: #6a11cb;
    margin-bottom: 20px;
    text-shadow: 0 0 10px #b576f0;
  }
  .invite p {
    font-size: 1.2rem;
    margin-bottom: 15px;
    color: #444;
  }

  .invite p strong {
    color: #6a11cb;
  }

  /* Uros de gravata */
  .bears {
    display: flex;
    justify-content: center;
    gap: 40px;
    margin-top: 25px;
  }

  .bear {
    width: 100px;
    height: 120px;
    position: relative;
    animation: bounceBear 2s infinite ease-in-out;
  }

  .bear.green {
    filter: drop-shadow(0 0 2px #2e7d32);
  }
  .bear.purple {
    filter: drop-shadow(0 0 2px #6a11cb);
  }

  /* Corpo dos ursos */
  .bear-body {
    width: 100%;
    height: 90px;
    background: linear-gradient(135deg, #4caf50 0%, #81c784 100%);
    border-radius: 60% 60% 50% 50%;
    position: relative;
  }
  .bear-body.purple {
    background: linear-gradient(135deg, #6a11cb 0%, #b576f0 100%);
  }

  /* Cabeça */
  .bear-head {
    width: 70px;
    height: 70px;
    background: #f9e6d2;
    border-radius: 50%;
    position: absolute;
    top: -45px;
    left: 50%;
    transform: translateX(-50%);
    border: 3px solid #fff;
    box-shadow: 0 3px 6px rgba(0,0,0,0.1);
  }

  /* Orelhas */
  .ear {
    width: 20px;
    height: 25px;
    background: #f9e6d2;
    border-radius: 50% / 70%;
    position: absolute;
    top: -10px;
    border: 3px solid #fff;
  }
  .ear.left {
    left: 5px;
  }
  .ear.right {
    right: 5px;
  }

  /* Olhos */
  .eye {
    width: 10px;
    height: 10px;
    background: #4a4a4a;
    border-radius: 50%;
    position: absolute;
    top: 25px;
  }
  .eye.left {
    left: 20px;
  }
  .eye.right {
    right: 20px;
  }

  /* Nariz */
  .nose {
    width: 14px;
    height: 9px;
    background: #b36b5b;
    border-radius: 60% / 50%;
    position: absolute;
    top: 40px;
    left: 50%;
    transform: translateX(-50%);
  }

  /* Gravata */
  .bowtie {
    position: absolute;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    width: 40px;
    height: 30px;
    background: linear-gradient(45deg, #9c27b0, #6a11cb);
    clip-path: polygon(
      0% 50%, 25% 0%, 40% 50%, 25% 100%, 
      75% 100%, 60% 50%, 75% 0%, 100% 50%
    );
    box-shadow: 0 0 6px #b576f0;
  }
  .bowtie.green {
    background: linear-gradient(45deg, #2e7d32, #4caf50);
    box-shadow: 0 0 6px #81c784;
  }

  /* Animação bounce */
  @keyframes bounceBear {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }

  /* Mensagem final */
  .footer {
    margin-top: 25px;
    font-size: 1rem;
    color: #444;
  }

  /* Botão para reabrir a caixa */
  .btn-reopen {
    margin-top: 25px;
    padding: 10px 20px;
    font-family: 'Fredoka One', cursive;
    font-size: 1rem;
    border: none;
    background: #6a11cb;
    color: white;
    border-radius: 30px;
    cursor: pointer;
    box-shadow: 0 4px 12px #b576f0;
    transition: background 0.3s ease;
  }
  .btn-reopen:hover {
    background: #b576f0;
  }
</style>
</head>
<body>
  <div class="container">

    <!-- Tela 1: Caixa -->
    <div class="gift-box" id="giftBox" aria-label="Caixa surpresa. Clique para abrir." role="button" tabindex="0">
      <div class="lid" id="lid"></div>
      <div class="gift-text">CLIQUE PARA ABRIR 🎁</div>
    </div>

    <!-- Confetes (escondidos inicialmente) -->
    <div class="confetti" id="confetti"></div>

    <!-- Tela 2: Convite -->
    <div class="invite" id="invite">
      <h1>É CHÁ REVELAÇÃO!</h1>
      <p><strong>Data:</strong> 21 de Junho de 2025</p>
      <p><strong>Horário:</strong> 17h</p>
      <p><strong>Local:</strong> Casa da Vovó Dinha 🏡</p>
      <p>Um momento mágico está chegando... venha descobrir com a gente!</p>
      <p>🎁 Traga fraldas M ou G das melhores marcas (Pampers, Huggies ou Mamypoko).</p>

      <div class="bears" aria-label="Dois ursos de gravata">
        <div class="bear green" aria-hidden="true">
          <div class="bear-body"></div>
          <div class="bear-head">
            <div class="ear left"></div>
            <div class="ear
