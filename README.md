<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Maaf Ya 💜</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(135deg, #7b2ff7, #d16bff);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      color: white;
      text-align: center;
    }

    .card {
      background: rgba(255,255,255,0.15);
      backdrop-filter: blur(10px);
      padding: 40px;
      border-radius: 30px;
      box-shadow: 0 10px 40px rgba(0,0,0,0.3);
      max-width: 500px;
      animation: pop 1s ease;
    }

    @keyframes pop {
      from {transform: scale(0.5); opacity: 0}
      to {transform: scale(1); opacity: 1}
    }

    h1 { font-size: 40px; margin-bottom: 10px; }
    p { font-size: 18px; }

    .heart {
      position: absolute;
      font-size: 20px;
      animation: float 6s linear infinite;
      opacity: 0.7;
    }

    @keyframes float {
      0% { transform: translateY(100vh) scale(0.5); }
      100% { transform: translateY(-10vh) scale(1.5); }
    }

    button {
      background: white;
      color: #7b2ff7;
      border: none;
      padding: 15px 25px;
      border-radius: 30px;
      font-size: 18px;
      cursor: pointer;
      margin-top: 20px;
      transition: 0.3s;
    }

    button:hover { transform: scale(1.1); }

    #response { font-size: 24px; margin-top: 20px; }
  </style>
</head>
<body>
  <div class="card">
    <h1>Maaf Ya 💜</h1>
    <p>
      Aku tau aku bikin kamu kesel 😭<br>
      Aku beneran minta maaf ya...<br>
      Maapinn Biyann yah udah bikin cebel🥺
    </p>

    <button onclick="forgive()">Maafin Aku Dong 🥹</button>
    <div id="response"></div>
  </div>

  <script>
    function createHeart(){
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerHTML = '💜';
      heart.style.left = Math.random()*100 + 'vw';
      heart.style.animationDuration = (Math.random()*3+3)+'s';
      document.body.appendChild(heart);
      setTimeout(()=>heart.remove(),6000);
    }
    setInterval(createHeart, 300);

    function forgive(){
      document.getElementById('response').innerHTML = 'YAY! Makasih udah maafin aku 💖🥰';
    }
  </script>
</body>
</html>
