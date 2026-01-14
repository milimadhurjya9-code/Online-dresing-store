# Online-dresing-store
All dresses available 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Elegance Dresses</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    background:#f4f4f4;
}

header{
    background:#111;
    color:#fff;
    padding:15px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

header h1{margin:0;}

.cart{
    background:#f4a6c1;
    color:#111;
    padding:8px 12px;
    border-radius:5px;
    cursor:pointer;
}

.hero{
    background:url("https://images.unsplash.com/photo-1520975916090-3105956dac38") center/cover;
    height:60vh;
    display:flex;
    align-items:center;
    justify-content:center;
    color:white;
    text-align:center;
}

.hero h2{
    font-size:42px;
}

section{
    padding:40px;
}

.products{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.product{
    background:white;
    border-radius:8px;
    overflow:hidden;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.product img{
    width:100%;
    height:300px;
    object-fit:cover;
}

.product-info{
    padding:15px;
    text-align:center;
}

button{
    background:#111;
    color:white;
    border:none;
    padding:10px 15px;
    cursor:pointer;
    border-radius:5px;
}

button:hover{
    background:#f4a6c1;
    color:#111;
}

#cartBox{
    display:none;
    background:white;
    position:fixed;
    top:10%;
    right:5%;
    width:300px;
    padding:20px;
    box-shadow:0 0 15px rgba(0,0,0,0.3);
    border-radius:8px;
}

footer{
    background:#111;
    color:white;
    text-align:center;
    padding:15px;
}
</style>
</head>

<body>

<header>
    <h1>Elegance</h1>
    <div class="cart" onclick="toggleCart()">🛒 Cart (<span id="count">0</span>)</div>
</header>

<div class="hero">
    <div>
        <h2>Fashion That Speaks</h2>
        <p>Modern • Stylish • Affordable</p>
    </div>
</div>

<section>
<h2>Dress Collection</h2>

<div class="products">
    <div class="product">
        <img src="https://images.unsplash.com/photo-1542060748-10c28b62716f">
        <div class="product-info">
            <h3>Floral Dress</h3>
            <p>₹2499</p>
            <button onclick="addToCart(2499)">Add to Cart</button>
        </div>
    </div>

    <div class="product">
        <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab">
        <div class="product-info">
            <h3>Evening Gown</h3>
            <p>₹4999</p>
            <button onclick="addToCart(4999)">Add to Cart</button>
        </div>
    </div>

    <div class="product">
        <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b">
        <div class="product-info">
            <h3>Casual Dress</h3>
            <p>₹1899</p>
            <button onclick="addToCart(1899)">Add to Cart</button>
        </div>
    </div>

    <div class="product">
        <img src="https://images.unsplash.com/photo-1618354691229-c5a0b0e3c5c1">
        <div class="product-info">
            <h3>Traditional Wear</h3>
            <p>₹3299</p>
            <button onclick="addToCart(3299)">Add to Cart</button>
        </div>
    </div>
</div>
</section>

<div id="cartBox">
    <h3>Your Cart</h3>
    <p>Items: <span id="items">0</span></p>
    <p>Total: ₹<span id="total">0</span></p>
    <button onclick="checkout()">Checkout</button>
</div>

<footer>
    <p>© 2026 Elegance Dresses</p>
</footer>

<script>
let items = 0;
let total = 0;

function addToCart(price){
    items++;
    total += price;
    document.getElementById("count").innerText = items;
    document.getElementById("items").innerText = items;
    document.getElementById("total").innerText = total;
}

function toggleCart(){
    let cart = document.getElementById("cartBox");
    cart.style.display = cart.style.display === "block" ? "none" : "block";
}

function checkout(){
    alert("Order placed successfully!");
    items = 0;
    total = 0;
    document.getElementById("count").innerText = 0;
    document.getElementById("items").innerText = 0;
    document.getElementById("total").innerText = 0;
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Login – Elegance</title>
<style>
body{
    font-family:Arial;
    background:#f4a6c1;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}
.box{
    background:white;
    padding:30px;
    border-radius:8px;
    width:300px;
    text-align:center;
}
input{
    width:100%;
    padding:10px;
    margin:10px 0;
}
button{
    background:#111;
    color:white;
    border:none;
    padding:10px;
    width:100%;
}
a{color:#111;}
</style>
</head>
<body>

<div class="box">
<h2>Login</h2>
<input type="text" placeholder="Username">
<input type="password" placeholder="Password">
<button onclick="login()">Login</button>
<p>New user? <a href="signup.html">Sign up</a></p>
</div>

<script>
function login(){
    alert("Login successful!");
    window.location.href="index.html";
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Signup – Elegance</title>
<style>
body{
    font-family:Arial;
    background:#111;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}
.box{
    background:white;
    padding:30px;
    border-radius:8px;
    width:300px;
    text-align:center;
}
input{
    width:100%;
    padding:10px;
    margin:10px 0;
}
button{
    background:#f4a6c1;
    border:none;
    padding:10px;
    width:100%;
}
</style>
</head>
<body>

<div class="box">
<h2>Create Account</h2>
<input type="text" placeholder="Username">
<input type="email" placeholder="Email">
<input type="password" placeholder="Password">
<button onclick="signup()">Sign Up</button>
</div>

<script>
function signup(){
    alert("Account created successfully!");
    window.location.href="login.html";
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Payment – Elegance</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{
    font-family:Arial;
    background:#f4f4f4;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}
.box{
    background:white;
    padding:30px;
    width:320px;
    border-radius:8px;
    text-align:center;
    box-shadow:0 0 15px rgba(0,0,0,0.2);
}
button{
    width:100%;
    padding:12px;
    margin:10px 0;
    border:none;
    cursor:pointer;
    border-radius:5px;
    font-size:16px;
}
.upi{background:#5f259f;color:white;}
.card{background:#111;color:white;}
.success{
    display:none;
    color:green;
    margin-top:15px;
}
</style>
</head>

<body>

<div class="box">
<h2>Complete Payment</h2>
<p>Total Amount: ₹<span id="amount"></span></p>

<button class="upi" onclick="pay()">Pay via UPI</button>
<button class="card" onclick="pay()">Pay via Card</button>

<p class="success" id="success">✅ Payment Successful! Order Placed.</p>
</div>

<script>
document.getElementById("amount").innerText =
    localStorage.getItem("total") || 0;

function pay(){
    document.getElementById("success").style.display="block";
    setTimeout(()=>{
        localStorage.clear();
        window.location.href="index.html";
    },2000);
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Admin Panel – Elegance</title>
<style>
body{font-family:Arial;background:#f4f4f4;padding:40px;}
.box{background:white;padding:20px;border-radius:8px;max-width:400px;margin:auto;}
input,button{width:100%;padding:10px;margin:10px 0;}
button{background:#111;color:white;border:none;}
</style>
</head>
<body>

<div class="box">
<h2>Add New Dress</h2>
<input id="name" placeholder="Dress Name">
<input id="price" placeholder="Price">
<input id="image" placeholder="Image URL">
<button onclick="add()">Add Dress</button>
</div>

<script>
function add(){
    let dresses = JSON.parse(localStorage.getItem("dresses")) || [];
    dresses.push({
        name: name.value,
        price: price.value,
        image: image.value
    });
    localStorage.setItem("dresses", JSON.stringify(dresses));
    alert("Dress added!");
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>My Orders – Elegance</title>
<style>
body{font-family:Arial;background:#f4f4f4;padding:40px;}
.box{background:white;padding:20px;border-radius:8px;max-width:400px;margin:auto;}
</style>
</head>
<body>

<div class="box">
<h2>Order History</h2>
<p>Total Orders: <span id="orders"></span></p>
</div>

<script>
document.getElementById("orders").innerText =
    localStorage.getItem("orders") || 0;
</script>

</body>
</html>
