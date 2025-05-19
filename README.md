
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
    }
    .box {
      background: white;
      border-radius: 20px;
      padding: 20px;
      max-width: 500px;
      margin: 20px auto;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
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
      width: 100%;
      max-width: 300px;
      margin: 0 auto 20px;
      cursor: pointer;
      transition: transform 0.3s;
    }
    .gift:hover {
      transform: scale(1.05);
    }
    .balloons {
      display: flex;
      justify-content: center;
      gap: 10px;
      margin: 20px 0;
    }
    .balloon {
      width: 30px;
      height: 40px;
      border-radius: 50% 50% 50% 50%;
      background: #6a11cb;
      position: relative;
    }
    .balloon.green {
      background: #4caf50;
    }
    .bear {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background: #f3c6a7;
      margin: 10px auto;
      position: relative;
    }
    .bear::before,
    .bear::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: #f3c6a7;
      border-radius: 50%;
      top: -10px;
    }
    .bear::before {
      left: -10px;
    }
    .bear::after {
      right: -10px;
    }
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
    }
  </style>
</head>
<body>
  <div class="box">
    <img src="https://cdn-icons-png.flaticon.com/512/3595/3595455.png" alt="Caixa surpresa" class="gift">
    <h1>Você está convidado!</h1>
    <p><strong>Chá Revelação</strong></p>
    <p>Dia <strong>21 de junho</strong> às <strong>17h</strong></p>
    <p>Local: Casa da <strong>Vovó Dinha</strong> 🏡</p>
    <div class="balloons">
      <div class="balloon"></div>
      <div class="balloon green"></div>
      <div class="balloon"></div>
    </div>
    <div class="bear"></div>
    <p>Traga fraldas <strong>M ou G</strong> das melhores marcas 💝</p>
    <div class="footer">Esperamos por você com muito amor 💜💚</div>
  </div>
</body>
</html>
