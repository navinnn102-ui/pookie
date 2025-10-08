<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pookie Love Everywhere 💋</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      width: 100vw;
      overflow: hidden;
      background: url('pookie.gif') no-repeat center center fixed;
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      color: white;
      font-family: 'Poppins', sans-serif;
      text-align: center;
      position: relative;
    }

    h1 {
      font-size: 2em;
      background: rgba(0, 0, 0, 0.5);
      padding: 10px 20px;
      border-radius: 25px;
      z-index: 5;
    }

    button {
      margin-top: 20px;
      padding: 12px 25px;
      font-size: 1em;
      color: #fff;
      background-color: #ff6b81;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s ease;
      z-index: 5;
    }

    button:hover {
      background-color: #ff4757;
      transform: scale(1.05);
    }

    .floating {
      position: absolute;
      font-size: 1.8em;
      animation: floatAround 10s ease-in-out infinite;
      opacity: 0.9;
      z-index: 2;
      user-select: none;
      pointer-events: none;
    }

    @keyframes floatAround {
      0% {
        transform: translate(0, 0) rotate(0deg) scale(1);
        opacity: 0.8;
      }
      25% {
        transform: translate(30px, -40px) rotate(30deg) scale(1.2);
        opacity: 1;
      }
      50% {
        transform: translate(-20px, 50px) rotate(-40deg) scale(1);
        opacity: 0.8;
      }
      75% {
        transform: translate(40px, 20px) rotate(60deg) scale(1.1);
      }
      100% {
        transform: translate(0, 0) rotate(360deg) scale(1);
        opacity: 0.9;
      }
    }

    .cat-paw {
      position: absolute;
      bottom: 10px;
      right: 15px;
      font-size: 3em;
      animation: pawMove 3s ease-in-out infinite alternate;
      z-index: 3;
    }

    @keyframes pawMove {
      from {
        transform: rotate(0deg) translateY(0);
      }
      to {
        transform: rotate(-10deg) translateY(-10px);
      }
    }
  </style>
</head>
<body>
  <h1>Happy Bday to my Supidee Pookie 💖</h1>
  <button onclick="nextPage()">Next Baby ➜</button>
  <div class="cat-paw">🐾</div>

  <script>
    function createFloating() {
      const el = document.createElement('div');
      el.classList.add('floating');
      const texts = ['💋', '💖 To my Pookiee 💖', '💋', '💋 Pookie 💋', '💋💋'];
      el.textContent = texts[Math.floor(Math.random() * texts.length)];
      
      // random positions all over the screen
      el.style.left = Math.random() * 100 + 'vw';
      el.style.top = Math.random() * 100 + 'vh';
      // random rotation angle
      el.style.transform = `rotate(${Math.random() * 360}deg)`;
      // random animation duration for variety
      el.style.animationDuration = 5 + Math.random() * 10 + 's';

      document.body.appendChild(el);
      setTimeout(() => el.remove(), 15000);
    }

    setInterval(createFloating, 400);

    function nextPage() {
      document.body.innerHTML = `
        <div style="text-align:center; color:white; position:relative;">
          <h2 style="font-size:2em;">Love you sooo much my dear Supidee 💞</h2>
          <p style="font-size:1.3em;">Stay safe, Chinnu 🐾</p>
          <div class="cat-paw">🐾</div>
        </div>
      `;
      setInterval(createFloating, 400);
    }
  </script>
</body>
</html>
