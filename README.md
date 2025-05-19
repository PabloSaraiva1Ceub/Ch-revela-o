<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Chá Revelação - Convite Especial</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #d1e7dd, #e0ccff);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }

    .container {
      text-align: center;
    }

    .gift-box {
      width: 200px;
      height: 200px;
      background: #8e44ad;
      border-radius: 20px;
      position: relative;
      margin: 0 auto;
      cursor: pointer;
      animation: pulse 2s infinite;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
    }

    .lid {
      width: 200px;
      height: 40px;
      background: #5e9474;
      border-radius: 20px 20px 0 0;
      position: absolute;
      top: -40px;
      left: 0;
    }

    .gift-text {
      color: white;
      font-size: 20px;
      padding-top: 80px;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    .explosion {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 300px;
      height: 300px;
      background: radial-gradient(circle, rgba(255,255,255,0.8) 20%, transparent 70%);
      border-radius: 50%;
      transform: translate(-50%, -50%) scale(0);
      transition: transform 0.5s ease-out;
      pointer-events: none;
      z-index: 1;
    }

    .show {
      transform: translate(-50%, -50%) scale(2);
    }

    .invite {
      display: none;
      background: white;
      border-radius: 20px;
      padding: 30px;
      max-width: 500px;
      margin: 20px auto;
      animation: fadeInUp 1s ease forwards;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
    }

    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(30px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .invite h1 {
      color: #8e44ad;
      margin-bottom: 10px;
    }

    .invite p {
      font-size: 18px;
      color: #333;
      margin: 10px 0;
    }

    .gift-box.open {
      animation: none;
      background: #ffffff;
      border: 4px dashed #5e9474;
    }

    .lid.hide {
      display: none;
    }

    .footer {
      font-size: 14px;
      margin-top: 20px;
      color: #777;
    }

    .emoji {
      font-size: 30px;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="explosion" id="explosion"></div>

    <div class="gift-box" id="giftBox" onclick="openGift()">
      <div class="lid" id="lid"></div>
      <div class="gift-text">CLIQUE PARA ABRIR 🎁</div>
    </div>

    <div class="invite" id="invite">
      <div class="emoji">💚💜✨</div>
      <h1>É CHÁ REVELAÇÃO!</h1>
      <p><strong>Data:</strong> 21 de Junho de 2025</p>
      <p><strong>Horário:</strong> 17h</p>
      <p><strong>Local:</strong> Casa da Vovó Dinha 🏡</p>
      <p>Venha viver esse momento mágico com a gente!</p>
      <p>🎁 Traga fraldas M ou G das melhores marcas (Pampers, Huggies ou Mamypoko).</p>
      <div class="footer">Estamos te esperando com muito amor e alegria! 💖</div>
    </div>
  </div>

  <script>
    function openGift() {
      const giftBox = document.getElementById("giftBox");
      const explosion = document.getElementById("explosion");
      const lid = document.getElementById("lid");
      const invite = document.getElementById("invite");

      // Anima explosão
      explosion.classList.add("show");

      // Troca visual da caixa
      giftBox.classList.add("open");
      lid.classList.add("hide");

      // Mostra o convite depois de um tempo
      setTimeout(() => {
        explosion.style.display = "none";
        invite.style.display = "block";
      }, 700);
    }
  </script>

</body>
</html>
