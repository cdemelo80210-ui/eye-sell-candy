# eye-sell-candy
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Eye Sell Candy</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:#111;
    color:white;
}

header{
    background:linear-gradient(135deg,#ff9900,#ff6600);
    text-align:center;
    padding:60px 20px;
}

header h1{
    font-size:4rem;
}

header p{
    font-size:1.3rem;
    margin-top:10px;
}

.products{
    max-width:1100px;
    margin:auto;
    padding:50px 20px;
}

.section-title{
    text-align:center;
    font-size:2.5rem;
    margin-bottom:40px;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:#222;
    padding:25px;
    border-radius:15px;
    text-align:center;
}

.card h3{
    color:#ffb300;
    margin-bottom:10px;
}

.price{
    color:#00ff88;
    font-size:1.4rem;
    font-weight:bold;
}

.special{
    background:linear-gradient(135deg,#6a00ff,#a200ff);
    padding:30px;
    border-radius:20px;
    text-align:center;
    margin-top:50px;
}

.order-form{
    background:#222;
    padding:30px;
    border-radius:20px;
    margin-top:50px;
}

.order-form h2{
    text-align:center;
    margin-bottom:20px;
}

input, select{
    width:100%;
    padding:12px;
    margin:10px 0;
    border:none;
    border-radius:10px;
}

button{
    width:100%;
    padding:15px;
    background:#ff9900;
    color:white;
    border:none;
    border-radius:10px;
    font-size:18px;
    cursor:pointer;
}

button:hover{
    background:#ff7700;
}

#total{
    margin-top:15px;
    font-size:22px;
    text-align:center;
    color:#00ff88;
}

.payment{
    background:#1f1f1f;
    text-align:center;
    padding:30px;
    border-radius:20px;
    margin-top:40px;
}

.payment h1{
    color:#00ff88;
    font-size:3rem;
}

footer{
    text-align:center;
    padding:30px;
    color:#888;
}
</style>
</head>
<body>

<header>
    <h1>👁 Eye Sell Candy</h1>
    <p>The Sweetest Deals in School!</p>
</header>

<section class="products">

<h2 class="section-title">Candy Menu</h2>

<div class="grid">

<div class="card">
    <h3>Reese's Eggs</h3>
    <p class="price">$3 Each</p>
    <p>2 for $4</p>
</div>

<div class="card">
    <h3>Reese's Sticks</h3>
    <p class="price">$3 Each</p>
    <p>2 for $4</p>
</div>

<div class="card">
    <h3>Fast Break</h3>
    <p class="price">$3 Each</p>
    <p>2 for $4</p>
</div>

<div class="card">
    <h3>Reese's Hearts</h3>
    <p class="price">$3 Each</p>
    <p>2 for $4</p>
</div>

</div>

<div class="special">
    <h2>🔥 BEST DEAL 🔥</h2>
    <p>
        Get <strong>2 Milk Chocolate Reese's</strong> +
        <strong>1 White Chocolate Reese's</strong>
        for only <strong>$5</strong>
    </p>
</div>

<div class="order-form">

<h2>Place Your Order</h2>

<input type="text" id="name" placeholder="Your Name">

<select id="item">
    <option value="3">Reese's Egg</option>
    <option value="3">Reese's Stick</option>
    <option value="3">Fast Break</option>
    <option value="3">Reese's Heart</option>
    <option value="5">2 Milk Chocolate + 1 White Chocolate Deal</option>
</select>

<input type="number" id="quantity" value="1" min="1">

<button onclick="calculateTotal()">Calculate Total</button>

<div id="total"></div>

</div>

<div class="payment">
    <h2>💸 Pay With Cash App</h2>
    <h1>$chasepd1</h1>
    <p>
        Send payment to the Cash App above and include your
        name and candy order in the payment note.
    </p>
</div>

</section>

<footer>
    <p>© 2026 Eye Sell Candy</p>
</footer>

<script>
function calculateTotal(){

    let itemPrice = Number(document.getElementById("item").value);
    let quantity = Number(document.getElementById("quantity").value);

    let total = itemPrice * quantity;

    document.getElementById("total").innerHTML =
    "Total: $" + total.toFixed(2);
}
</script>

</body>
</html>