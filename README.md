<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Marquis Footwear — Premium Shoes</title>
<style>
:root {
  --bg: #f7f8fa;
  --card: #ffffff;
  --accent: #18314f;
  --gold: #d4af37;
  --muted: #555;
  --radius: 16px;
  font-family: "Poppins", system-ui, sans-serif;
}
* { box-sizing: border-box; }
body {
  margin: 0;
  background: linear-gradient(180deg, var(--bg), #eaeaea);
  color: #111;
  display: flex;
  justify-content: center;
  padding: 40px;
  transition: background 0.5s ease;
}
.wrap {
  max-width: 1150px;
  width: 100%;
  animation: fadeIn 1.2s ease;
}
@keyframes fadeIn { from {opacity: 0;} to {opacity: 1;} }

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 0;
}
.logo {
  font-weight: 800;
  letter-spacing: 1px;
  font-size: 24px;
  color: var(--accent);
}
nav a {
  color: var(--muted);
  margin-left: 18px;
  text-decoration: none;
  transition: color 0.3s ease;
}
nav a:hover { color: var(--gold); }

.hero {
  background: linear-gradient(90deg, rgba(24,49,79,0.05), rgba(24,49,79,0.02));
  border-radius: 20px;
  padding: 40px 30px;
  display: flex;
  gap: 40px;
  align-items: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.06);
  transition: all 0.4s ease;
}
.hero:hover {
  transform: translateY(-3px);
}

.shoe img {
  width: 360px;
  height: auto;
  border-radius: 20px;
  box-shadow: 0 15px 30px rgba(0,0,0,0.12);
  transition: transform 0.3s ease;
}
.shoe img:hover {
  transform: scale(1.05);
}

.info h2 {
  margin: 0;
  font-size: 32px;
  color: var(--accent);
}
.info p {
  color: var(--muted);
  line-height: 1.6;
  max-width: 440px;
}
.btn {
  display: inline-block;
  margin-top: 18px;
  padding: 12px 22px;
  border-radius: 12px;
  background: linear-gradient(90deg, var(--accent), #345d7e);
  color: white;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
}
.btn:hover {
  background: linear-gradient(90deg, #345d7e, var(--accent));
  transform: translateY(-3px);
}

.list {
  display: flex;
  gap: 16px;
  margin-top: 20px;
  flex-wrap: wrap;
}
.card {
  background: var(--card);
  padding: 16px;
  border-radius: var(--radius);
  flex: 1;
  box-shadow: 0 8px 25px rgba(0,0,0,0.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.1);
}
.card img {
  width: 100%;
  border-radius: 12px;
  height: 160px;
  object-fit: cover;
  margin-bottom: 8px;
}
.price {
  color: var(--gold);
  font-weight: 700;
}

footer {
  margin-top: 26px;
  color: var(--muted);
  font-size: 14px;
  text-align: center;
}

@media(max-width: 880px) {
  .hero { flex-direction: column; text-align: center; }
  .shoe img { width: 100%; }
  .list { flex-direction: column; }
}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <div class="logo">Marquis</div>
    <nav>
      <a href="#">New</a>
      <a href="#">Men</a>
      <a href="#">Women</a>
      <a href="#">Custom</a>
    </nav>
  </header>

  <section class="hero">
    <div class="shoe">
      <img src="https://images.unsplash.com/photo-1595950653106-6c9ebd614d3a?w=800" alt="Luxury shoe">
    </div>
    <div class="info">
      <h2>Performance + Elegance</h2>
      <p>Engineered for comfort, finished with a timeless silhouette. Hand-stitched welt and memory-foam insole for all-day wear.</p>
      <a href="#" class="btn">Explore Now</a>

      <div class="list">
        <div class="card">
          <img src="https://images.unsplash.com/photo-1556906781-9e4533b1f681?w=600" alt="Leather Originals">
          <div>Leather Originals</div>
          <div class="price">From PKR 73,000</div>
        </div>
        <div class="card">
          <img src="https://images.unsplash.com/photo-1606813902788-5c093aa64b9f?w=600" alt="Urban Runners">
          <div>Urban Runners</div>
          <div class="price">From PKR 45,000</div>
        </div>
        <div class="card">
          <img src="https://images.unsplash.com/photo-1528701800489-20be3c2b6a49?w=600" alt="Custom Order">
          <div>Custom Order</div>
          <div class="price">Made to Order</div>
        </div>
      </div>
    </div>
  </section>

  <footer>
    © <span id="yr"></span> Marquis Footwear — Crafted with precision & passion
  </footer>
</div>

<script>
document.getElementById('yr').textContent = new Date().getFullYear();
</script>
</body>
</html>
