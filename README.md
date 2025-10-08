<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pookie Love 💋</title>
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
      z-index: 2;
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
      z-index: 2;
    }

    button:hover {
      background-color: #ff4757;
      transform: scale(1.05);
    }

    .floating {
      position: absolute;
      font-size: 1.8em;
      animation: float 8s linear infinite;
      opacity: 0.8;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) scale(0.8);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.2);
        opacity: 0;
      }
    }

    .cat-paw {
      position: absolute;
      bottom: 10px;
      right: 15px;
      font-size: 3em;
      animation: pawMove 3s ease-in-out infinite alternate;
      z-index: 2;
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
      const types = ['💋', 'To my Pookiee 💖', '💋', '💖 Pookie 💋'];
      el.textContent = types[Math.floor(Math.random() * types.length)];
      el.style.left = Math.random() * 100 + 'vw';
      el.style.animationDuration = 6 + Math.random() * 4 + 's';
      document.body.appendChild(el);

      setTimeout(() => el.remove(), 10000);
    }

    setInterval(createFloating, 700);

    function nextPage() {
      document.body.innerHTML = `
        <div style="text-align:center; color:white;">
          <h2>Love you sooo much my dear Supidee 💞</h2>
          <p>Stay safe, Chinnu 🐾</p>
          <div class="cat-paw">🐾</div>
        </div>
      `;
      setInterval(createFloating, 700);
    }
  </script>
</body>
</html>

