<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- Hamburger Menu Button -->


<!-- Side Menu -->
<nav id="side-menu">
    <a href="index.html">Home</a>
    <a href="#shop">Shop</a>
    <a href="#about">About</a>
    <a href="contact.html">Contact</a>
</nav>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@700&display=swap" rel="stylesheet">

<style>
    /* Hamburger Button */
.hamburger {
    font-size: 28px;
    cursor: pointer;
    padding: 0px;
    position: fixed;
    left: 10px;
    top: 10px;
    z-index: 2000;
}
    /* Side Menu Styling */
#side-menu {
    position: fixed;
    left: -220px;
    top: 0;
    width: 200px;
    height: 100%;
    background: #ffffff;
    box-shadow: 2px 0 10px rgba(0,0,0,0.1);
    display: flex;
    flex-direction: column;
    padding-top: 60px;
    transition: 0.3s ease;
    z-index: 1500;
}
#side-menu a {
    padding: 15px;
    text-decoration: none;
    color: #333;
    font-size: 18px;
    border-bottom: 1px solid #e5e5e5;
}#side-menu a {
    padding: 15px;
    text-decoration: none;
    color: #333;
    font-size: 18px;
    border-bottom: 1px solid #e5e5e5;
}
#side-menu a:hover {
    background: #f2f2f2;
}
    /* Price drop styling & small animations */
.price-row { margin: 8px 0; display:flex; justify-content:center; align-items:center; gap:10px; }
.old-price {
  color: #888;
  text-decoration: line-through;
  font-size: 0.95rem;
  opacity: 0.95;
  transition: transform .25s ease, opacity .25s ease;
}
.new-price {
  color: #e11d48; /* red-ish */
  font-size: 1.1rem;
  font-weight: 700;
}

/* small pop animation when inserted */
.pop {
  animation: pop 260ms ease;
}
@keyframes pop {
  0%   { transform: scale(0.95); opacity: 0; }
  60%  { transform: scale(1.05); opacity: 1; }
  100% { transform: scale(1); }
}

body { margin: 0; font-family: Arial, sans-serif; background: #f8f8f8; }
/* Header */
header {
    background: #60a5fa;
    color: #fff;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
}

header h1 {
    margin-left: 60;
    font-size: 52px;               
    font-family: 'Baloo 2', cursive;  
}

nav {
    display: flex;
    gap: 20px;       
    margin-right: 100px; 
}

nav a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
}

nav a:hover {
    color: #3b82f6; 
    transition: color 0.3s; 
}

/* Cart Icon */
.cart-icon {
    position: absolute;
    right: 20px;
    top: 20px;
    cursor: pointer;
    font-size: 24px;
}

.top-header {
    display: flex;
    align-items: center;
    justify-content: space-between;  /* space between hamburger, title, cart */
    padding: 10px 20px;
    position: relative;
    z-index: 2000;
}

.hamburger {
    font-size: 28px;
    position: absolute;
    cursor: pointer;
}

.site-title {
    margin: 0;
    font-size: 24px;
    text-align: center;
    flex: 1;               /* allows the heading to center itself */
    padding-left: 20px;    /* keeps space from hamburger */
}



.cart-count {
    background: red;
    color: white;
    font-size: 12px;
    padding: 3px 7px;
    border-radius: 50%;
    vertical-align: top;
    margin-left: 5px;
}

/* Hero */ 
.hero {
    position: relative;
    text-align: center;
    padding: 80px 20px;
    overflow: hidden;
    color: #000; /* black text */
}

/* Semi-transparent image overlay */
.hero::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url('BackgroundPicture.jpg') center/cover no-repeat;
    opacity: 0.4; /* adjust opacity here */
    z-index: 0;
}

.hero h2,
.hero p {
    position: relative;
    z-index: 1; /* text stays above the image */
    font-family: 'Baloo 2', cursive;
}

.hero h2 {
    font-size: 40px;
    margin-bottom: 10px;
}

.hero p {
    font-size: 18px;
}



/* Products */
.products {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 40px;
    max-width: 1200px;
    margin: auto;
}

/* Product Cards */
.product-card {
    background-color: #FFF9C4; /* soft yellow */
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s, box-shadow 0.2s;
    text-align: center;
}

/* Hover effect for card */
.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}

/* Image placeholder */
.product-card img {
    width: 100%;
    height: 200px; /* adjust as needed */
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 15px;
    background-color: #f0f0f0; /* light grey placeholder */
}

/* Product title & description */
.product-card h3 {
    font-family: 'Baloo 2', cursive;
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 10px;
}

.product-card p {
    font-family: 'Baloo 2', cursive;
    font-size: 16px;
    color: #333;
}

/* Add to Cart Button */
.product-card .add-to-cart-btn {
    background-color: #3b82f6; /* blue button */
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-family: 'Baloo 2', cursive;
    font-weight: 600;
    transition: background-color 0.2s, transform 0.2s;
}

.product-card .add-to-cart-btn:hover {
    background-color: #2563eb; /* slightly darker blue on hover */
    transform: translateY(-2px);
}




/* Cart Panel */
#cart-panel {
    position: fixed;
    right: 0;
    top: 0;
    width: 320px;
    height: 100%;
    background: white;
    box-shadow: -4px 0 10px rgba(0,0,0,0.2);
    padding: 20px;
    display: none;
    overflow-y: auto;
    z-index: 999;
}
#cart-panel h3 { margin-top: 0; }
.cart-item {
    padding: 10px 0;
    border-bottom: 1px solid #ddd;
}
.cart-item div {
    display: flex;
    align-items: center;
    gap: 5px;
    margin-top: 5px;
}
.cart-item button {
    background: none;
    border: none;
    color: red;
    cursor: pointer;
    font-size: 16px;
}
.cart-item span {
    min-width: 20px;
    text-align: center;
}
.checkout-btn {
    background: green;
    color: white;
    padding: 12px;
    width: 100%;
    border: none;
    border-radius: 6px;
    margin-top: 15px;
    font-size: 18px;
    cursor: pointer;
}

/* Modal for product details */
.modal {
    display: none;
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.6);
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.modal-content {
    background: white;
    padding: 20px;
    width: 90%;
    max-width: 400px;
    border-radius: 10px;
}

.close-btn {
    float: right;
    font-size: 24px;
    cursor: pointer;
}

/* Contact & Footer */
footer {
    background: #1e3a8a;
    color: #fff;
    padding: 20px;
    text-align: center;
    margin-top: 40px;
}
.contact {
    text-align: center;
    padding: 20px;
    font-size: 18px;
}
.sale-banner {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background: #dc2626; /* red */
    color: white;
    text-align: center;
    padding: 12px 0;
    font-size: 18px;
    font-weight: bold;
    z-index: 9999;
    animation: slideUp 0.8s ease-out;
    box-shadow: 0 -2px 8px rgba(0,0,0,0.2);
}

@keyframes slideUp {
    from { transform: translateY(100%); }
    to   { transform: translateY(0); }
}

</style>
</head>

<body>
<header class="top-header">
    <div id="menu-btn" class="hamburger">☰</div>

    <h1 class="site-title">Eminent Services</h1>

    <div id="cart-icon" class="cart-icon">🛒</div>
</header>

<section>
    <div class="hero">
    <h2>Affordable Stationery Packs for Parents & Schools</h2> 
    <p>Quality stationery delivered nationwide.</p>
    <p class="custom-note" style="font-size: 14px; margin-top: 8px; font-weight: bold; text-align: center;">
    FOR A CUSTOMIZED STATIONERY PACK, CONTACT US ON
    <br>
    <a href="https://wa.me/27713535297" 
       style="text-decoration: none; display: block; text-align: center; margin-top: 6px;
              font-size: 18px; font-weight: bold;">
        071 3535 297
    </a>

</section>

<section class="products">

<!-- Basic Pack -->
<div class="product-card" data-price="1999.99" onclick="showProductDetails('Basic Pack')">
  <img src="BasicPack.jpg" alt="Basic Pack">
    <h3>Basic Pack</h3>
    <div class="price-row">
        <span class="new-price">R1999.99</span>
    </div>
    <button class="add-to-cart-btn" 
        onclick="addToCart('Basic Pack', parseFloat(this.closest('.product-card').dataset.price)); event.stopPropagation();">
        Add to Cart
    </button>

</div>
    <!-- Standard Pack -->
    <div class="product-card" data-price="1999.99" onclick="showProductDetails('Standard Pack')">
        <img src="StandardPack.jpg" alt="Standard Pack">
         <h3>Standard Pack</h3>

        <div class="price-row">
            <span class="new-price">R1999.99</span>
            <span class="old-price" aria-hidden="true"></span>
        </div>
       <button class="add-to-cart-btn"
       onclick="addToCart('Standard Pack', parseFloat(this.closest('.product-card').dataset.price)); event.stopPropagation();">
         Add to Cart
       </button>
    </div>

    <!-- Deluxe Pack -->
    <div class="product-card" data-price="1999.99" onclick="showProductDetails('Deluxe Pack')">
        <img src="DeluxePack.jpg" alt="Deluxe Pack">
         <h3>Deluxe Pack</h3>
        
        <div class="price-row">
            <span class="new-price">R1999.99</span>
            <span class="old-price" aria-hidden="true"></span>
            
        </div>
        <button class="add-to-cart-btn"
        onclick="addToCart('Deluxe Pack', parseFloat(this.closest('.product-card').dataset.price)); event.stopPropagation();">
          Add to Cart
          </button>
    </div>

    <!-- Customised Pack-->
    <div class="product-card" data-price="1999.99" onclick="showProductDetails('Customised Pack')">
        <img src="CustomisedPack.jpg" alt="Customised Pack">
         <h3>Customised Pack</h3>
        
        <div class="price-row">
            <span class="new-price">R1999.99</span>
            <span class="old-price" aria-hidden="true"></span>
        </div>
        <button class="add-to-cart-btn"
        onclick="addToCart('Customised Pack', parseFloat(this.closest('.product-card').dataset.price)); event.stopPropagation();">
          Add to Cart
          </button>
    </div>

</section>

<div class="contact" style="text-align: center; font-family: 'Baloo 2', cursive;"> 
    <p><strong style="color: black;">We deliver nationwide</strong></p>
    <p style="color: #3b82f6;">Prices may vary based on your custom package details.</p> 
    <p style="color: #3b82f6;">We will provide a personalised quote for your specific needs!!!</p> 
</div>


<!-- CART PANEL -->
<div id="cart-panel">
    <button onclick="toggleCart()" style="float:right; background:red; color:white; border:none; padding:5px 10px; border-radius:5px; cursor:pointer;">Close ×</button>
    <h3>Your Cart</h3>
    <div id="cart-items"></div>
    <h3>Total: R<span id="cart-total">0.00</span></h3>
    <button class="checkout-btn" onclick="checkout()">Checkout</button>
</div>

<!-- PRODUCT DETAILS MODAL -->
<div id="product-modal" class="modal">
    <div class="modal-content">
        <span class="close-btn" onclick="closeModal()">×</span>
        <h2 id="modal-title"></h2>
        <ul id="modal-items"></ul>
    </div>
</div>

<footer>
    © 2025 Eminent Services — All Rights Reserved
</footer>

<script>
// Product item lists
const productDetails = {
    "Basic Pack": [
        "2 × A4 Exercise Books",
        "1 × Ruler",
        "1 × Pencil Set (6 pack)",
        "1 × Eraser",
        "1 × Sharpener"
    ],
    "Standard Pack": [
       "2 × A4 Exercise Books",
        "1 × Ruler",
        "1 × Pencil Set (6 pack)",
        "1 × Eraser",
        "1 × Sharpener"
    ],
    "Deluxe Pack": [
       "2 × A4 Exercise Books",
        "1 × Ruler",
        "1 × Pencil Set (6 pack)",
        "1 × Eraser",
        "1 × Sharpener"
    ],
    "Customised Pack": [
        "2 × A4 Exercise Books",
        "1 × Ruler",
        "1 × Pencil Set (6 pack)",
        "1 × Eraser",
        "1 × Sharpener"
    ]
};

// Call once on page load to generate old (struck) prices as 30% above current
function applyPriceDrops() {
  // Select all product cards that have a data-price attribute
  document.querySelectorAll('.product-card[data-price]').forEach(card => {
    const priceStr = card.dataset.price;                         // "199.99"
    const price = parseFloat(priceStr);
    if (isNaN(price)) return;

    // compute old price = 30% higher
    const oldPrice = (price * 1.3);
    const oldPriceText = 'R' + oldPrice.toFixed(2);

    // find the old-price span and new-price span
    const oldEl = card.querySelector('.old-price');
    const newEl = card.querySelector('.new-price');

    if (oldEl) {
      oldEl.textContent = oldPriceText;
      // subtle pop effect to draw attention
      oldEl.classList.remove('pop');
      void oldEl.offsetWidth; // trigger reflow for repeated animation
      oldEl.classList.add('pop');
    }

    // ensure new-price displays correctly (in case markup mismatch)
    if (newEl) {
      newEl.textContent = 'R' + price.toFixed(2);
    }
  });
}

// run on load
document.addEventListener('DOMContentLoaded', function() {
  applyPriceDrops();
});


// Show modal
function showProductDetails(name) {
    document.getElementById("modal-title").textContent = name;

    let itemsHTML = productDetails[name]
        .map((item, index) => `
        <li>
           <input type="checkbox" id="${name}-item-${index}" data-item="${item}" checked>
           <label for="${name}-item-${index}">${item}</label>
        </li>
        `)
        .join("");

    document.getElementById("modal-items").innerHTML = itemsHTML;

    document.getElementById("product-modal").style.display = "flex";

    if (!document.getElementById("add-selected-btn")) {
        const btn = document.createElement("button");
        btn.id = "add-selected-btn";
        btn.textContent = "Add Selected Items to Cart";
        btn.style.cssText = "margin-top:15px;padding:10px 20px;background:#3b82f6;color:white;border:none;border-radius:6px;cursor:pointer;";
        btn.onclick = function() { addSelectedToCart(name); };
        document.querySelector(".modal-content").appendChild(btn);
    }
}

function addSelectedToCart(packName) {
    const selectedItems = Array.from(
        document.querySelectorAll(`#product-modal input[type="checkbox"]:checked`)
    ).map(cb => cb.dataset.item);

    if (selectedItems.length === 0) {
        alert("Please select at least one item to add.");
        return;
    }
// Initialize an empty cart
let cart = [];

// Function to add item to cart
function addToCart(productName, price) {
    cart.push({ name: productName, price: price });
    console.log(cart); // check cart in console
    alert(`${productName} added to cart!`);
    updateCartDisplay(); // optional: update cart counter or UI
}

// Optional: display cart items somewhere
function updateCartDisplay() {
    const cartContainer = document.getElementById('cart-items');
    if (!cartContainer) return;

    cartContainer.innerHTML = ''; // clear previous
    cart.forEach((item, index) => {
        const div = document.createElement('div');
        div.textContent = `${item.name} - R${item.price.toFixed(2)}`;
        cartContainer.appendChild(div);
    });
}

    // Calculate price per item (optional: divide pack price by total items)
    const packCard = Array.from(document.querySelectorAll('.product-card'))
        .find(c => c.querySelector('h3').textContent === packName);
    const packPrice = parseFloat(packCard.dataset.price);

    const pricePerItem = packPrice / productDetails[packName].length;

    selectedItems.forEach(item => {
        addToCart(item, pricePerItem);
    });

    closeModal();
}

// Close modal
function closeModal() {
    document.getElementById("product-modal").style.display = "none";
}

let cart = JSON.parse(localStorage.getItem("cart")) || [];

function saveCart() { localStorage.setItem("cart", JSON.stringify(cart)); }

function updateCart() {
    document.getElementById("cart-count").textContent = cart.length;
    let itemsHTML = "";
    let total = 0;
    cart.forEach((item,index) => {
        total += item.price * item.quantity;
        itemsHTML += `
<div class="cart-item">
    ${item.name} - R${(item.price * item.quantity).toFixed(2)}
    <div>
        <button onclick="decreaseQty(${index})">-</button>
        <span>${item.quantity}</span>
        <button onclick="increaseQty(${index})">+</button>
        <button onclick="removeItem(${index})">❌</button>
    </div>
</div>`;
    });
    document.getElementById("cart-items").innerHTML = itemsHTML;
    document.getElementById("cart-total").textContent = total.toFixed(2);
}

function addToCart(name, price) {
    const existingIndex = cart.findIndex(item => item.name === name);
    if(existingIndex >= 0){ cart[existingIndex].quantity += 1; } 
    else { cart.push({name, price, quantity: 1}); }
    saveCart();
    updateCart();
    alert(name + " added to cart!");
}

function removeItem(index) { cart.splice(index, 1); saveCart(); updateCart(); }

function toggleCart() {
    const panel = document.getElementById("cart-panel");
    panel.style.display = panel.style.display === "block" ? "none" : "block";
    updateCart();
}

function checkout() {
    if(cart.length === 0) { alert("Your cart is empty!"); return; }
    let message = "Hello! I'd like to place an order:\n\n";
    cart.forEach(item => { message += `• ${item.name} - R${item.price}\n`; });
    message += `\nTotal: R${document.getElementById("cart-total").textContent}`;
    window.open(`https://wa.me/27713535297?text=${encodeURIComponent(message)}`, "_blank");
}

function increaseQty(index) { cart[index].quantity += 1; saveCart(); updateCart(); }
function decreaseQty(index) {
    if(cart[index].quantity > 1){ cart[index].quantity -= 1; } 
    else { removeItem(index); }
    saveCart(); updateCart();
}

updateCart();
</script>
<script>
document.getElementById("menu-btn").onclick = function() {
    let menu = document.getElementById("side-menu");
    if(menu.style.left === "0px") {
        menu.style.left = "-220px"; // hide
    } else {
        menu.style.left = "0px"; // show
    }
};
</script>
</body>
<!-- Floating sale banner -->
<div class="sale-banner">
    Order now while stocks last!!! Sale ends on the 15th of December!!! 
</div>

</html>
