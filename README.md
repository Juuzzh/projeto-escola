# projeto-escola
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jubs Drinks</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #fef6f0;
      color: #333;
    }

    header {
      background-color: #ff4d6d;
      color: white;
      padding: 1rem;
      text-align: center;
      font-size: 2rem;
      font-weight: bold;
      letter-spacing: 2px;
    }

    .container {
      padding: 2rem;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }

    .drink-card {
      background: white;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      padding: 1rem;
      text-align: center;
    }

    .drink-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
      cursor: pointer;
    }

    .drink-name {
      margin: 1rem 0 0.5rem;
      font-size: 1.2rem;
      font-weight: bold;
    }

    .drink-price {
      color: #ff4d6d;
      font-size: 1rem;
    }

    footer {
      text-align: center;
      padding: 1rem;
      background: #ff4d6d;
      color: white;
      margin-top: 2rem;
    }

    /* Modal */
    .modal {
      display: none;
      position: fixed;
      z-index: 10;
      padding-top: 60px;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0,0,0,0.9);
    }

    .modal-content {
      margin: auto;
      display: block;
      max-width: 80%;
      max-height: 80%;
      border-radius: 10px;
    }

    #caption {
      margin: 1rem auto;
      text-align: center;
      color: #fff;
      font-size: 1.2rem;
    }

    .close {
      position: absolute;
      top: 30px;
      right: 45px;
      color: #fff;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>JUBS DRINKS</header>

  <div class="container">
    <div class="drink-card">
      <img src="Outback-redbull.jpg" alt="Drink Tropical" onclick="openModal(this)">
      <div class="drink-name">Drink Tropical</div>
      <div class="drink-price">R$ 19,90</div>
    </div>
    <div class="drink-card">
      <img src="outback-apresenta-novo-drink-nao-alcoolico-pink-lemonade-geek-publicitario-696x379-1.png" alt="Pink Lemonade" onclick="openModal(this)">
      <div class="drink-name">Pink Lemonade</div>
      <div class="drink-price">R$ 14,90</div>
    </div>
    <div class="drink-card">
      <img src="espuma-limao-3.webp" alt="Cítrico Gelado" onclick="openModal(this)">
      <div class="drink-name">Cítrico Gelado</div>
      <div class="drink-price">R$ 17,90</div>
    </div>
  </div>

  <!-- Modal -->
  <div id="imgModal" class="modal" onclick="closeModal()">
    <span class="close">&times;</span>
    <img class="modal-content" id="modalImg">
    <div id="caption"></div>
  </div>

  <footer>
    &copy; 2025 Jubs Drinks. Todos os direitos reservados.
  </footer>

  <script>
    function openModal(img) {
      var modal = document.getElementById("imgModal");
      var modalImg = document.getElementById("modalImg");
      var caption = document.getElementById("caption");

      modal.style.display = "block";
      modalImg.src = img.src;
      caption.innerHTML = img.alt;
    }

    function closeModal() {
      document.getElementById("imgModal").style.display = "none";
    }
  </script>
</body>
</html>
