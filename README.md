# sanskriti-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Sanskriti | Saree Catalogue</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins&display=swap" rel="stylesheet">
</head>
<body>

<header>
  <h1>SANSKRITI</h1>
  <p class="tagline">Timeless Indian Handlooms</p>
</header>

<!-- SEARCH -->
<div class="search-box">
  <input type="text" id="searchInput" placeholder="Search sarees..." onkeyup="searchSarees()">
</div>

<!-- CATALOGUE -->
<section class="catalogue">

  <h2>Maheshwari Sarees</h2>
  <div class="grid">
    <div class="card">Maheshwari Silk – Gold Border</div>
    <div class="card">Maheshwari Cotton – Classic Black</div>
  </div>

  <h2>Dhakai Sarees</h2>
  <div class="grid">
    <div class="card">Dhakai Jamdani – Floral</div>
    <div class="card">Dhakai Muslin – White Gold</div>
  </div>

  <h2>Tissue Sarees</h2>
  <div class="grid">
    <div class="card">Golden Tissue Saree</div>
    <div class="card">Ivory Tissue Silk</div>
  </div>

  <h2>Khadi Sarees</h2>
  <div class="grid">
    <div class="card">Handspun Khadi – Natural</div>
    <div class="card">Khadi Cotton – Black Gold</div>
  </div>

</section>

<footer>
  <p>© 2025 SANSKRITI | Handcrafted Elegance</p>
</footer>

<script src="script.js"></script>
</body>
</html>
body {
  margin: 0;
  background: #121212;
  color: white;
  font-family: 'Poppins', sans-serif;
}

/* HEADER */
header {
  text-align: center;
  padding: 40px 20px;
  border-bottom: 2px solid #d4af37;
}

header h1 {
  font-family: 'Playfair Display', serif;
  color: #d4af37;
  font-size: 3rem;
  letter-spacing: 3px;
}

.tagline {
  color: #eee;
}

/* SEARCH */
.search-box {
  text-align: center;
  margin: 20px;
}

.search-box input {
  width: 80%;
  padding: 12px;
  border-radius: 30px;
  border: none;
  outline: none;
  font-size: 1rem;
}

/* CATALOGUE */
.catalogue {
  padding: 30px;
}

h2 {
  color: #d4af37;
  border-left: 5px solid #d4af37;
  padding-left: 10px;
  margin-top: 40px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin-top: 15px;
}

.card {
  background: #1e1e1e;
  padding: 20px;
  border: 1px solid #d4af37;
  border-radius: 10px;
  text-align: center;
  transition: 0.3s;
}

.card:hover {
  background: #d4af37;
  color: black;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 15px;
  background: black;
  border-top: 1px solid #d4af37;
}
function searchSarees() {
  let input = document.getElementById("searchInput").value.toLowerCase();
  let cards = document.getElementsByClassName("card");

  for (let i = 0; i < cards.length; i++) {
    let text = cards[i].innerText.toLowerCase();
    cards[i].style.display = text.includes(input) ? "block" : "none";
  }
}
