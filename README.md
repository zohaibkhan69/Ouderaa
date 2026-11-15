
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>OUDÉRA | Luxury Fragrances</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=DM+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --black: #171713;
  --gold: #bd9b60;
  --cream: #f7f4ed;
  --white: #fff;
  --muted: #77756e;
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  font-family:'DM Sans',sans-serif;
  background:var(--cream);
  color:var(--black);
}

a { text-decoration:none; color:inherit; }
button { cursor:pointer; font-family:inherit; }

.announcement {
  background:var(--black);
  color:white;
  text-align:center;
  padding:10px;
  font-size:11px;
  letter-spacing:2px;
}

header {
  height:82px;
  background:#fff;
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:0 7%;
  position:sticky;
  top:0;
  z-index:10;
  border-bottom:1px solid #eee;
}

.logo {
  font-family:'Playfair Display',serif;
  font-size:30px;
  font-weight:600;
  letter-spacing:5px;
}

.logo span { color:var(--gold); }

nav {
  display:flex;
  gap:32px;
  font-size:12px;
  letter-spacing:1px;
  font-weight:600;
}

nav a:hover { color:var(--gold); }

.header-actions {
  display:flex;
  align-items:center;
  gap:18px;
}

.header-actions button {
  border:0;
  background:none;
  font-size:19px;
}

.cart-count {
  background:var(--gold);
  color:white;
  border-radius:50%;
  font-size:10px;
  padding:3px 6px;
  vertical-align:top;
}

.hero {
  min-height:570px;
  display:flex;
  align-items:center;
  padding:70px 9%;
  background:
  linear-gradient(90deg,rgba(14,14,12,.94),rgba(14,14,12,.4)),
  url('https://images.unsplash.com/photo-1594035910387-fea47794261f?w=1800')
  center/cover;
  color:white;
}

.hero-content { max-width:570px; }

.eyebrow {
  color:var(--gold);
  letter-spacing:4px;
  font-size:11px;
  margin-bottom:22px;
}

.hero h1 {
  font-family:'Playfair Display',serif;
  font-size:65px;
  line-height:1.13;
  font-weight:400;
  margin-bottom:22px;
}

.hero p {
  color:#ddd;
  font-size:14px;
  line-height:1.9;
  max-width:420px;
  margin-bottom:32px;
}

.btn {
  display:inline-block;
  padding:15px 32px;
  background:var(--gold);
  color:white;
  border:1px solid var(--gold);
  font-size:11px;
  letter-spacing:2px;
  transition:.3s;
}

.btn:hover {
  background:transparent;
  color:var(--gold);
}

.features {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  background:white;
  padding:27px 7%;
  text-align:center;
  gap:20px;
}

.feature {
  font-size:12px;
  letter-spacing:1px;
}

.feature strong {
  display:block;
  margin-bottom:7px;
  font-size:13px;
}

.section {
  padding:85px 7%;
}

.section-heading {
  text-align:center;
  margin-bottom:40px;
}

.section-heading small {
  color:var(--gold);
  letter-spacing:3px;
  font-size:10px;
}

.section-heading h2 {
  font-family:'Playfair Display',serif;
  font-size:39px;
  font-weight:400;
  margin:12px 0;
}

.section-heading p {
  color:var(--muted);
  font-size:13px;
}

.categories {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:22px;
}

.category {
  height:310px;
  position:relative;
  overflow:hidden;
  background:#333;
}

.category img {
  width:100%;
  height:100%;
  object-fit:cover;
  transition:.5s;
}

.category:hover img { transform:scale(1.06); }

.category-overlay {
  position:absolute;
  inset:0;
  background:linear-gradient(transparent,rgba(0,0,0,.75));
  display:flex;
  align-items:flex-end;
  justify-content:center;
  padding:30px;
  color:white;
  font-family:'Playfair Display',serif;
  font-size:29px;
}

.shop-section { background:#fff; }

.shop-controls {
  display:flex;
  justify-content:space-between;
  align-items:center;
  flex-wrap:wrap;
  gap:15px;
  margin-bottom:30px;
}

.filters { display:flex; gap:10px; flex-wrap:wrap; }

.filter-btn {
  border:1px solid #ddd;
  background:white;
  padding:10px 18px;
  font-size:11px;
  letter-spacing:1px;
}

.filter-btn.active,
.filter-btn:hover {
  background:var(--black);
  color:white;
}

.search {
  border:1px solid #ddd;
  padding:11px 15px;
  outline:none;
  width:210px;
  font-size:12px;
}

.products {
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:25px 17px;
}

.product-card { position:relative; }

.product-image {
  height:280px;
  background:#eee;
  position:relative;
  overflow:hidden;
}

.product-image img {
  width:100%;
  height:100%;
  object-fit:cover;
  transition:.4s;
}

.product-card:hover .product-image img {
  transform:scale(1.05);
}

.tag {
  position:absolute;
  top:13px;
  left:13px;
  background:var(--gold);
  color:white;
  font-size:9px;
  padding:7px 10px;
  letter-spacing:1px;
}

.product-info { padding:16px 3px; }

.product-info small {
  color:var(--gold);
  font-size:9px;
  letter-spacing:2px;
}

.product-info h3 {
  font-family:'Playfair Display',serif;
  font-size:19px;
  margin:8px 0;
}

.product-info p {
  color:var(--muted);
  font-size:11px;
  margin-bottom:12px;
}

.price { font-weight:700; font-size:14px; }

.add-btn {
  width:100%;
  background:var(--black);
  color:white;
  border:1px solid var(--black);
  padding:12px;
  margin-top:13px;
  font-size:10px;
  letter-spacing:1.5px;
}

.add-btn:hover {
  background:var(--gold);
  border-color:var(--gold);
}

.no-results {
  grid-column:1/-1;
  text-align:center;
  padding:40px;
  color:var(--muted);
}

.promo {
  background:var(--black);
  color:white;
  display:grid;
  grid-template-columns:1fr 1fr;
  min-height:390px;
}

.promo-image {
  background:url('https://images.unsplash.com/photo-1615634260167-c8cdede054de?w=1000') center/cover;
}

.promo-content {
  padding:65px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:flex-start;
}

.promo-content h2 {
  font-family:'Playfair Display',serif;
  font-size:43px;
  font-weight:400;
  margin:15px 0;
}

.promo-content p {
  color:#ccc;
  font-size:13px;
  line-height:1.9;
  margin-bottom:25px;
}

.newsletter {
  padding:75px 20px;
  text-align:center;
}

.newsletter h2 {
  font-family:'Playfair Display',serif;
  font-size:36px;
  margin-bottom:12px;
}

.newsletter p {
  color:var(--muted);
  font-size:13px;
  margin-bottom:22px;
}

.newsletter form {
  display:flex;
  max-width:440px;
  margin:auto;
}

.newsletter input {
  flex:1;
  min-width:0;
  padding:15px;
  border:1px solid #ddd;
}

.newsletter button {
  border:0;
  background:var(--black);
  color:white;
  padding:0 20px;
  font-size:11px;
  letter-spacing:1px;
}

footer {
  background:var(--black);
  color:white;
  padding:55px 7% 20px;
}

.footer-grid {
  display:grid;
  grid-template-columns:2fr 1fr 1fr;
  gap:35px;
  margin-bottom:40px;
}

footer h3 {
  font-family:'Playfair Display',serif;
  font-size:25px;
  margin-bottom:15px;
}

footer h4 {
  color:var(--gold);
  margin-bottom:18px;
  font-size:12px;
  letter-spacing:1px;
}

footer p,footer a {
  color:#aaa;
  font-size:12px;
  line-height:2.3;
  display:block;
}

.copyright {
  border-top:1px solid #444;
  text-align:center;
  padding-top:20px;
  color:#888;
  font-size:10px;
}

.cart-panel {
  position:fixed;
  top:0;
  right:-420px;
  width:min(400px,100%);
  height:100vh;
  background:white;
  z-index:30;
  padding:25px;
  transition:.3s;
  box-shadow:-5px 0 25px #0002;
  display:flex;
  flex-direction:column;
}

.cart-panel.open { right:0; }

.cart-header {
  display:flex;
  justify-content:space-between;
  border-bottom:1px solid #ddd;
  padding-bottom:20px;
}

.cart-header h2 {
  font-family:'Playfair Display',serif;
}

.close-cart {
  border:0;
  background:none;
  font-size:23px;
}

.cart-items {
  flex:1;
  overflow:auto;
  padding:20px 0;
}

.cart-item {
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:13px 0;
  border-bottom:1px solid #eee;
  gap:10px;
}

.cart-item small { color:var(--muted); }

.qty-controls {
  display:flex;
  align-items:center;
  gap:10px;
}

.qty-controls button {
  border:1px solid #ddd;
  background:white;
  padding:5px 9px;
}

.cart-footer { border-top:1px solid #ddd; padding-top:20px; }

.cart-total {
  display:flex;
  justify-content:space-between;
  margin-bottom:20px;
  font-weight:700;
}

.checkout {
  width:100%;
  padding:15px;
  background:var(--black);
  color:white;
  border:0;
  letter-spacing:1px;
}

.overlay {
  position:fixed;
  inset:0;
  background:#0007;
  z-index:20;
  display:none;
}

.overlay.show { display:block; }

.mobile-menu { display:none; }

@media(max-width:850px) {
  header { padding:0 5%; }
  nav { gap:14px; }
  .products { grid-template-columns:repeat(2,1fr); }
  .product-image { height:260px; }
  .hero h1 { font-size:49px; }
  .promo-content { padding:35px; }
}

@media(max-width:600px) {
  header { height:70px; }
  .logo { font-size:23px; letter-spacing:3px; }
  .mobile-menu { display:block; }
  nav {
    display:none;
    position:absolute;
    top:70px;
    left:0;
    right:0;
    background:white;
    padding:25px;
    flex-direction:column;
    box-shadow:0 5px 10px #0001;
  }
  nav.show { display:flex; }
  .header-actions { gap:10px; }
  .hero {
    min-height:500px;
    padding:50px 7%;
    background-position:60% center;
  }
  .hero h1 { font-size:43px; }
  .features { grid-template-columns:1fr; gap:20px; }
  .categories { grid-template-columns:1fr; }
  .category { height:270px; }
  .section { padding:60px 5%; }
  .section-heading h2 { font-size:32px; }
  .products { gap:20px 10px; }
  .product-image { height:200px; }
  .product-info h3 { font-size:16px; }
  .shop-controls { align-items:stretch; }
  .search { width:100%; }
  .promo { grid-template-columns:1fr; }
  .promo-image { height:260px; }
  .promo-content h2 { font-size:35px; }
  .footer-grid { grid-template-columns:1fr; }
}
</style>
</head>

<body>

<div class="announcement">
  COMPLIMENTARY DELIVERY ON ORDERS ABOVE RS. 5,000
</div>

<header>
  <button class="mobile-menu" onclick="toggleMenu()">☰</button>

  <a href="#" class="logo">OUDÉ<span>RA</span></a>

  <nav id="navigation">
    <a href="#home">HOME</a>
    <a href="#shop">SHOP ALL</a>
    <a href="#categories">COLLECTIONS</a>
    <a href="#story">OUR STORY</a>
  </nav>

  <div class="header-actions">
    <button onclick="document.getElementById('searchBox').focus()">⌕</button>
    <button onclick="toggleCart()">♧ <span class="cart-count" id="cartCount">0</span></button>
  </div>
</header>

<!-- HERO -->

<section class="hero" id="home">
  <div class="hero-content">
    <div class="eyebrow">THE ART OF FINE FRAGRANCE</div>
    <h1>Make Every<br>Moment<br>Unforgettable.</h1>
    <p>
      Discover the art of extraordinary scents.
      Crafted for those who believe that a fragrance
      is more than a scent — it's an identity.
    </p>
    <a href="#shop" class="btn">EXPLORE COLLECTION</a>
  </div>
</section>

<!-- FEATURES -->

<section class="features">
  <div class="feature">
    <strong>✧ PREMIUM QUALITY</strong>
    Exceptional fragrance experiences
  </div>
  <div class="feature">
    <strong>✧ NATIONWIDE DELIVERY</strong>
    Across Pakistan
  </div>
  <div class="feature">
    <strong>✧ ELEGANT PACKAGING</strong>
    Perfect for gifting
  </div>
</section>

<!-- CATEGORIES -->

<section class="section" id="categories">
  <div class="section-heading">
    <small>DISCOVER YOUR SIGNATURE</small>
    <h2>Shop By Collection</h2>
    <p>A fragrance for every personality.</p>
  </div>

  <div class="categories">
    <a href="#shop" class="category" onclick="setCategory('Men')">
      <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?w=700" alt="Men fragrances">
      <div class="category-overlay">For Him</div>
    </a>

    <a href="#shop" class="category" onclick="setCategory('Women')">
      <img src="https://images.unsplash.com/photo-1592945403244-b3fbafd7f539?w=700" alt="Women fragrances">
      <div class="category-overlay">For Her</div>
    </a>

    <a href="#shop" class="category" onclick="setCategory('Unisex')">
      <img src="https://images.unsplash.com/photo-1615634260167-c8cdede054de?w=700" alt="Unisex fragrances">
      <div class="category-overlay">Unisex</div>
    </a>
  </div>
</section>

<!-- PRODUCTS -->

<section class="section shop-section" id="shop">
  <div class="section-heading">
    <small>THE OUDÉRA SELECTION</small>
    <h2>Our Best Sellers</h2>
    <p>Find the fragrance that speaks for you.</p>
  </div>

  <div class="shop-controls">
    <div class="filters">
      <button class="filter-btn active" onclick="setCategory('All',this)">ALL</button>
      <button class="filter-btn" onclick="setCategory('Men',this)">MEN</button>
      <button class="filter-btn" onclick="setCategory('Women',this)">WOMEN</button>
      <button class="filter-btn" onclick="setCategory('Unisex',this)">UNISEX</button>
    </div>

    <input
      id="searchBox"
      class="search"
      type="search"
      placeholder="Search fragrances..."
      oninput="renderProducts()">
  </div>

  <div class="products" id="productGrid"></div>
</section>

<!-- BRAND STORY -->

<section class="promo" id="story">
  <div class="promo-image"></div>
  <div class="promo-content">
    <div class="eyebrow">A SCENT. A STORY. A LEGACY.</div>
    <h2>Beyond Ordinary.<br>Beyond Fragrance.</h2>
    <p>
      At OUDÉRA, we believe every fragrance
      tells a story. Our collection celebrates
      elegance, individuality and timeless luxury.
      Find the scent that becomes your signature.
    </p>
    <a href="#shop" class="btn">DISCOVER MORE</a>
  </div>
</section>

<!-- NEWSLETTER -->

<section class="newsletter">
  <h2>Join The OUDÉRA Circle</h2>
  <p>Subscribe for new launches, exclusive offers and fragrance inspiration.</p>

  <form onsubmit="subscribe(event)">
    <input type="email" id="email" placeholder="Your email address" required>
    <button type="submit">SUBSCRIBE</button>
  </form>
  <p id="subscribeMessage"></p>
</section>

<!-- FOOTER -->

<footer>
  <div class="footer-grid">
    <div>
      <h3>OUDÉRA</h3>
      <p>Luxury is not just what you wear.<br>
      It's what people remember.</p>
    </div>

    <div>
      <h4>QUICK LINKS</h4>
      <a href="#home">Home</a>
      <a href="#shop">Shop fragrances</a>
      <a href="#categories">Collections</a>
      <a href="#story">Our story</a>
    </div>

    <div>
      <h4>CONTACT</h4>
      <p>Pakistan</p>
      <p>Customer Support</p>
      <p>Instagram: @oudera</p>
    </div>
  </div>

  <div class="copyright">
    © 2026 OUDÉRA. ALL RIGHTS RESERVED.
    | DEMO E-COMMERCE WEBSITE
  </div>
</footer>

<!-- CART -->

<div class="overlay" id="overlay" onclick="toggleCart()"></div>

<aside class="cart-panel" id="cartPanel">
  <div class="cart-header">
    <h2>Your Shopping Bag</h2>
    <button class="close-cart" onclick="toggleCart()">×</button>
  </div>

  <div class="cart-items" id="cartItems">
    Your bag is empty.
  </div>

  <div class="cart-footer">
    <div class="cart-total">
      <span>Total</span>
      <span id="cartTotal">Rs. 0</span>
    </div>
    <button class="checkout" onclick="checkout()">ORDER ON WHATSAPP</button>
  </div>
</aside>

<script>

// PRODUCT DATABASE

const products = [
  {
    id:1,
    name:"Royal Oud",
    category:"Men",
    price:4500,
    description:"Woody · Oud · Amber",
    image:"https://images.unsplash.com/photo-1594035910387-fea47794261f?w=600",
    tag:"BEST SELLER"
  },
  {
    id:2,
    name:"Velvet Rose",
    category:"Women",
    price:3800,
    description:"Rose · Floral · Musk",
    image:"https://images.unsplash.com/photo-1592945403244-b3fbafd7f539?w=600",
    tag:"POPULAR"
  },
  {
    id:3,
    name:"Midnight Noir",
    category:"Men",
    price:5200,
    description:"Spicy · Leather · Wood",
    image:"https://images.unsplash.com/photo-1615634260167-c8cdede054de?w=600",
    tag:"NEW"
  },
  {
    id:4,
    name:"Golden Aura",
    category:"Unisex",
    price:4800,
    description:"Amber · Vanilla · Musk",
    image:"https://images.unsplash.com/photo-1590736969955-71cc94901144?w=600",
    tag:"EXCLUSIVE"
  },
  {
    id:5,
    name:"Bloom Essence",
    category:"Women",
    price:3500,
    description:"Jasmine · Rose · Citrus",
    image:"https://images.unsplash.com/photo-1592945403244-b3fbafd7f539?w=600",
    tag:"NEW"
  },
  {
    id:6,
    name:"Oud Imperial",
    category:"Unisex",
    price:6500,
    description:"Oud · Saffron · Amber",
    image:"https://images.unsplash.com/photo-1594035910387-fea47794261f?w=600",
    tag:"LUXURY"
  },
  {
    id:7,
    name:"Ocean Mist",
    category:"Men",
    price:3200,
    description:"Fresh · Aquatic · Citrus",
    image:"https://images.unsplash.com/photo-1615634260167-c8cdede054de?w=600",
    tag:"FRESH"
  },
  {
    id:8,
    name:"Pure Elegance",
    category:"Women",
    price:4200,
    description:"Vanilla · Floral · Musk",
    image:"https://images.unsplash.com/photo-1590736969955-71cc94901144?w=600",
    tag:"POPULAR"
  }
];

let selectedCategory = "All";
let cart = [];

// DISPLAY PRODUCTS

function renderProducts() {
  const grid = document.getElementById("productGrid");
  const search = document.getElementById("searchBox").value.toLowerCase();

  const filtered = products.filter(p =>
    (selectedCategory === "All" || p.category === selectedCategory) &&
    (p.name.toLowerCase().includes(search) ||
     p.description.toLowerCase().includes(search))
  );

  grid.innerHTML = "";

  if(filtered.length === 0) {
    grid.innerHTML = '<div class="no-results">No fragrances found.</div>';
    return;
  }

  filtered.forEach(p => {
    grid.innerHTML += `
      <div class="product-card">
        <div class="product-image">
          <span class="tag">${p.tag}</span>
          <img src="${p.image}" alt="${p.name}" loading="lazy">
        </div>

        <div class="product-info">
          <small>${p.category.toUpperCase()} FRAGRANCE</small>
          <h3>${p.name}</h3>
          <p>${p.description}</p>
          <div class="price">Rs. ${p.price.toLocaleString("en-PK")}</div>
          <button class="add-btn" onclick="addToCart(${p.id})">
            ADD TO BAG +
          </button>
        </div>
      </div>
    `;
  });
}

// CATEGORY FILTER

function setCategory(category,button) {
  selectedCategory = category;

  document.querySelectorAll(".filter-btn").forEach(b =>
    b.classList.remove("active")
  );

  if(button) {
    button.classList.add("active");
  } else {
    document.querySelectorAll(".filter-btn").forEach(b => {
      if(b.textContent.trim().toLowerCase() === category.toLowerCase()) {
        b.classList.add("active");
      }
    });
  }

  renderProducts();
}

// ADD TO CART

function addToCart(id) {
  const item = cart.find(p => p.id === id);

  if(item) {
    item.quantity++;
  } else {
    cart.push({
      ...products.find(p => p.id === id),
      quantity:1
    });
  }

  updateCart();
  alert("Fragrance added to your bag!");
}

// UPDATE CART

function updateCart() {
  const count = cart.reduce((sum,p) => sum + p.quantity,0);
  const total = cart.reduce((sum,p) => sum + p.price*p.quantity,0);

  document.getElementById("cartCount").textContent = count;
  document.getElementById("cartTotal").textContent =
    "Rs. " + total.toLocaleString("en-PK");

  const container = document.getElementById("cartItems");

  if(cart.length === 0) {
    container.innerHTML = "Your bag is empty.";
    return;
  }

  container.innerHTML = cart.map(p => `
    <div class="cart-item">
      <div>
        <strong>${p.name}</strong><br>
        <small>Rs. ${p.price.toLocaleString("en-PK")}</small>
      </div>

      <div class="qty-controls">
        <button onclick="changeQty(${p.id},-1)">−</button>
        ${p.quantity}
        <button onclick="changeQty(${p.id},1)">+</button>
      </div>
    </div>
  `).join("");
}

// CHANGE QUANTITY

function changeQty(id,amount) {
  const item = cart.find(p => p.id === id);

  if(!item) return;

  item.quantity += amount;

  if(item.quantity <= 0) {
    cart = cart.filter(p => p.id !== id);
  }

  updateCart();
}

// CART OPEN/CLOSE

function toggleCart() {
  document.getElementById("cartPanel").classList.toggle("open");
  document.getElementById("overlay").classList.toggle("show");
}

function toggleMenu() {
  document.getElementById("navigation").classList.toggle("show");
}

// WHATSAPP CHECKOUT

function checkout() {
  if(cart.length === 0) {
    alert("Your shopping bag is empty!");
    return;
  }

  const phone = "923001234567"; // Replace with your WhatsApp number

  let message = "Hello OUDÉRA! I want to place an order:\n\n";

  cart.forEach(p => {
    message += `${p.name} x ${p.quantity} = Rs. ${p.price*p.quantity}\n`;
  });

  const total = cart.reduce((sum,p) => sum+p.price*p.quantity,0);

  message += `\nTotal: Rs. ${total}\n\nPlease confirm my order.`;

  window.open(
    "https://wa.me/" + phone + "?text=" + encodeURIComponent(message),
    "_blank"
  );
}

// NEWSLETTER DEMO

function subscribe(event) {
  event.preventDefault();

  document.getElementById("subscribeMessage").textContent =
    "Thank you for joining the OUDÉRA circle!";

  document.getElementById("email").value = "";
}

// INITIALIZE

renderProducts();
updateCart();

</script>

</body>
</html>
# Apex-
