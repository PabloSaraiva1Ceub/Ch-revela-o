<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Chá Revelação</title>
  <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Poppins:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: #333;
      text-align: center;
      padding: 20px;
      overflow-x: hidden;
    }
    .box {
      background: white;
      border-radius: 20px;
      padding: 20px;
      max-width: 500px;
      margin: 20px auto;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
      position: relative;
    }
    .box h1 {
      font-family: 'Fredoka One', cursive;
      font-size: 2em;
      color: #6a11cb;
    }
    .box p {
      margin: 10px 0;
      font-size: 1.1em;
    }
    .gift {
      width: 150px;
      margin: 0 auto;
      cursor: pointer;
      transition: transform 0.3s;
      animation: bounce 2s infinite;
    }
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    .balloons {
      position: absolute;
      top: -40px;
      left: 0;
      right: 0;
      display: flex;
      justify-content: center;
      gap: 20px;
      z-index: 1;
      animation: float 5s ease-in-out infinite;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    .balloon {
      width: 30px;
      height: 40px;
      border-radius: 50% 50% 50% 50%;
      background: #6a11cb;
    }
    .balloon.green { background: #4caf50; }
    .bear-img {
      width: 80px;
      height: auto;
      position: absolute;
      top: 20px;
    }
    .left-bear { left: -40px; }
    .right-bear { right: -40px; }
    .footer {
      margin-top: 20px;
      font-size: 0.9em;
      color: #555;
    }
    @media (max-width: 500px) {
      .box {
        padding: 15px;
      }
      .box h1 {
        font-size: 1.5em;
      }
      .bear-img {
        display: none;
      }
    }
  </style>
</head>
<body>
  <div class="box">
    <img src="https://cdn-icons-png.flaticon.com/512/992/992700.png" class="bear-img left-bear" alt="Urso de gravata">
    <img src="https://cdn-icons-png.flaticon.com/512/992/992700.png" class="bear-img right-bear" alt="Urso de gravata">
    <div class="balloons">
      <div class="balloon"></div>
      <div class="balloon green"></div>
      <div class="balloon"></div>
    </div>
    <img src="https://cdn-icons-png.flaticon.com/512/3595/3595455.png" alt="Caixa surpresa" class="gift">
    <h1>Você está convidado!</h1>
    <p><strong>Chá Revelação</strong></p>
    <p>Dia <strong>21 de junho</strong> às <strong>17h</strong></p>
    <p>Local: Casa da <strong>Vovó Dinha</strong> 🏡</p>
    <p>Traga fraldas <strong>M ou G</strong> das melhores marcas 💝</p>
    <div class="footer">Esperamos por você com muito amor 💜💚</div>
  </div>
</body>
</html>
