<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Convite Chá Revelação</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #d1e7dd, #e0ccff);
      color: #333;
      text-align: center;
      padding: 40px;
    }

    .card {
      background: white;
      border-radius: 15px;
      padding: 40px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      max-width: 500px;
      margin: 0 auto;
    }

    .title {
      font-size: 28px;
      color: #5e9474; /* Verde sóbrio */
      margin-bottom: 20px;
    }

    .hidden {
      display: none;
    }

    .reveal-btn {
      background-color: #8e44ad; /* Roxo */
      color: white;
      border: none;
      padding: 15px 25px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
      transition: background-color 0.3s ease;
    }

    .reveal-btn:hover {
      background-color: #732d91;
    }

    .gift-box {
      margin-top: 25px;
      background-color: #f6f6f6;
      border-left: 5px solid #5e9474;
      padding: 15px;
      border-radius: 8px;
    }

    .footer {
      margin-top: 30px;
      font-size: 14px;
      color: #777;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1 class="title">Chá Revelação à Vista!</h1>
    <p>Adivinha... É menino ou menina? 🤔</p>
    <button class="reveal-btn" onclick="revealDetails()">Clique para Revelar o Convite</button>

    <div id="details" class="hidden">
      <h2 style="color: #8e44ad;">Você está convidado(a)!</h2>
      <p><strong>Data:</strong> 22 de Junho de 2025<br>
         <strong>Horário:</strong> 16h<br>
         <strong>Local:</strong> Casa da Vovó, Rua das Flores, nº 123</p>

      <div class="gift-box">
        🎁 <strong>Presente:</strong> Se quiser ajudar, traga fraldas M ou G!<br>
        Damos preferência às melhores marcas: *Pampers, Huggies ou Mamypoko*.<br>
        Afinal, nosso bebê merece o melhor! 💚💜
      </div>
    </div>

    <div class="footer">
      Esperamos por você com muito carinho! 🌟
    </div>
  </div>

  <script>
    function revealDetails() {
      document.getElementById("details").classList.remove("hidden");
    }
  </script>

</body>
</html>
