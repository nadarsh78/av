
<html lang="ml">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🌼 Vishu 🌼</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Malayalam&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(to bottom, #ffd6ec, #ffe066, #b5fffc);
      font-family: 'Noto Sans Malayalam', sans-serif;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      overflow: hidden;
      position: relative;
    }

    .greeting {
      font-size: 2em;
      color: #ff2e63;
      text-shadow: 0 0 10px #fff, 0 0 20px #ff8fab;
      animation: fadeInUp 2s ease, zoomOut 1s ease 9s forwards;
    }

    .subtext {
      font-size: 1.1em;
      margin-top: 15px;
      color: #6a1b4d;
      text-shadow: 0 0 5px #fff;
      animation: fadeIn 2s ease 2s, zoomOut 1s ease 9s forwards;
    }

    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(40px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }

    @keyframes zoomOut {
      to { transform: scale(0); opacity: 0; }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: url('https://i.imgur.com/fU9x3LE.png') no-repeat center/contain;
      animation: floatHeart 10s linear infinite;
      opacity: 0.7;
    }

    @keyframes floatHeart {
      0% {
        transform: translateY(100vh) rotate(0deg);
        opacity: 0;
      }
      20% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(360deg);
        opacity: 0;
      }
    }

    .overlay {
      position: absolute;
      width: 100%;
      height: 100%;
      background: white;
      top: 0;
      left: 0;
      z-index: 100;
      opacity: 0;
      pointer-events: none;
      animation: showEnd 1s ease 10s forwards;
    }

    @keyframes showEnd {
      to {
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <div class="greeting">🌸 ഹാപ്പി വിഷു അമ്മുക്കുട്ടി! 🌼</div>
  <div class="subtext">ഇന്ന് നിന്നെ കാണുന്നതും, ആശംസിക്കാനുമാണ് ഏറ്റവും വലിയ വിഷു സമ്മാനം ✨</div>

  <div class="overlay"></div>

  <script>
    // Floating hearts
    for (let i = 0; i < 25; i++) {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDelay = Math.random() * 5 + 's';
      heart.style.animationDuration = 6 + Math.random() * 4 + 's';
      document.body.appendChild(heart);
    }
  </script>

</body>
</html>
