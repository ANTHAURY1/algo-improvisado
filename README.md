# algo-improvisado

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>💌 Una carta para ti,  💌</title>
  <style>
    body {
      background: linear-gradient(135deg, #ffdee9, #ffc0cb);
      font-family: 'Poppins', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      overflow: hidden;
    }

    .container {
      text-align: center;
    }

    .envelope {
      width: 220px;
      height: 140px;
      background: #ffb6c1;
      position: relative;
      margin: auto;
      border-radius: 8px;
      box-shadow: 0 6px 15px rgba(0,0,0,0.15);
      transition: transform 0.6s;
      cursor: pointer;
    }

    .envelope::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      border-left: 110px solid transparent;
      border-right: 110px solid transparent;
      border-bottom: 70px solid #ff8da1;
      border-radius: 6px 6px 0 0;
      transition: transform 0.6s;
      transform-origin: top;
    }

    .message {
      display: none;
      background: white;
      border-radius: 20px;
      padding: 25px;
      margin-top: 20px;
      max-width: 320px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      animation: aparecer 1s ease forwards;
    }

    @keyframes aparecer {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .message h1 {
      color: #d63384;
      font-size: 22px;
    }

    .message p {
      color: #333;
      font-size: 17px;
      line-height: 1.5;
      margin: 15px 0;
    }

    .firma {
      color: #555;
      font-style: italic;
      font-size: 15px;
    }

    .btn {
      display: inline-block;
      background: #d63384;
      color: white;
      padding: 10px 20px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 10px;
    }

    /* Animación al abrir */
    .open .envelope {
      transform: translateY(-30px);
    }

    .open .envelope::before {
      transform: rotateX(180deg);
    }

    .open .message {
      display: block;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="envelope" onclick="abrirCarta()"></div>
    <div class="message" id="carta">
      <h1>💖 Para ti,  💖</h1>
      <p>“No sé si el destino existe, pero si lo hace...  
      me alegra que te haya cruzado en mi camino.” 🌹</p>
      <p class="firma">— Con cariño, Stiven 💫</p>
      <a class="btn" href="https://wa.me/573114346108">Responder por WhatsApp 💬</a>
    </div>
  </div>

  <script>
    function abrirCarta() {
      document.querySelector('.container').classList.toggle('open');
    }
  </script>
</body>
</html>
