# AI-FAKE-SHOP

This is a simple web application which is created with the help of HTML,CSS and Javascript.This web application is having a responsive "My Cart" which is the most important component of an e-Commerce website. It stores all basic information related to products that customers added to their buying list. An ideal shopping cart comes with all basic features including adding, removing products, calculating price, and locally storing cart information for non-logged users.

The cart section functionality is carried out with the help of javascript that allows users to add and remove items from a cart, typically on an e-commerce website. The script uses JavaScript to dynamically update the cart display based on user interactions, such as adding or removing items. The shopping cart script typically uses an array to store the items in the cart, and it also uses functions to add and remove items from the cart.

## Creation of Project

This project can be easily developed with the help of following steps which are mentioned below:

### Step-1: HTML

The first thing which every website has is the HTML file.This gives the backbone for every website and here in this project a file is created with the index.html and the following code is added:

```

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI-FAKE-SHOP</title>

    <!-- box icons  -->
    <link href='https://unpkg.com/boxicons@2.1.2/css/boxicons.min.css' rel='stylesheet'>
    <!-- styles  -->
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <!-- HEADER  -->
    <header>
        <!-- NAV  -->
        <div class="nav container">
            <a href="#" class="logo"><span>AI </span>FAKE-SHOP</a>

            <!-- CART ICON  -->
            <i class='bx bx-shopping-bag' id="cart-icon"></i>

            <!-- CART  -->
            <div class="cart">
                <h2 class="cart-title">Your Cart</h2>

                <!-- CONTENT  -->
                <div class="cart-content">
                </div>

                <!-- TOTAL   -->
                <div class="total">
                    <div class="total-title">Total</div>
                    <div class="total-price">$0</div>
                </div>
                <!-- BUY BUTTON  -->
                <button type="button" class="btn-buy">Buy Now</button>
                <!-- CART CLOSE  -->
                <i class='bx bx-x' id="cart-close"></i>
            </div>
       </header>


    <!-- SHOP SECTION  -->
    <section class="shop container">
        <h2 class="section-title">Shop Products</h2>

        <!-- CONTENT  -->
        <div class="shop-content">
            <!-- BOX 1 -->
            <div class="product-box">
                <img src="./img/pics/product1.jpg" alt="" class="product-img">
                <h2 class="product-title">Nike Shoes</h2>
                <span class="product-price">$79.5</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 2 -->
            <div class="product-box">
                <img src="./img/pics/product2.jpg" alt="" class="product-img">
                <h2 class="product-title">BACKPACK</h2>
                <span class="product-price">$59.5</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 3 -->
            <div class="product-box">
                <img src="./img/pics/product3.jpg" alt="" class="product-img">
                <h2 class="product-title">METAL BOTTLE</h2>
                <span class="product-price">$29.5</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 4 -->
            <div class="product-box">
                <img src="./img/pics/product4.jpg" alt="" class="product-img">
                <h2 class="product-title">METAL SUNGLASSES</h2>
                <span class="product-price">$105</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 5 -->
            <div class="product-box">
                <img src="./img/pics/product5.jpg" alt="" class="product-img">
                <h2 class="product-title">PS5 Controller</h2>
                <span class="product-price">$95</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 6 -->
            <div class="product-box">
                <img src="./img/pics/product6.jpg" alt="" class="product-img">
                <h2 class="product-title">Galaxy Z Fold</h2>
                <span class="product-price">$1400</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 7 -->
            <div class="product-box">
                <img src="./img/pics/product7.jpg" alt="" class="product-img">
                <h2 class="product-title">Nokon Camera</h2>
                <span class="product-price">$1700</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
            <!-- BOX 8 -->
            <div class="product-box">
                <img src="./img/pics/product8.jpg" alt="" class="product-img">
                <h2 class="product-title">Apple Watch</h2>
                <span class="product-price">$110.5</span>
                <i class='bx bx-shopping-bag add-cart'></i>
            </div>
        </div>
    </section>

    <!-- link js  -->
    <script src="index.js"></script>
</body>

</html>

```

### Step-2: CSS

The second thing which comes in a website is to make the website visually very appealing to the users, so the here comes the role of CSS which gives the website more stylish and customised looks. To implement CSS a file is created with the name style.css and the following code is added:

```

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');

/* Globals  */
*{
    font-family: 'Poppins', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
    scroll-behavior: smooth;
    scroll-padding: 2rem;
   
}
/* Variables  */
:root{
    --main-color: #ffffff;
    --sec-color: #ffffff;
    --text-color: #171427;
    --bg-color: #eb3553;
    background-image: url("https://img.freepik.com/premium-vector/pink-watercolor-wet-wash-splash-background_70155-529.jpg");
}
::selection{
    color: var(--text-color);
    background-color: var(--main-color);
}
.container{
    max-width: 1068px;
    margin: auto;
    width: 100%;
}
section{
    padding: 4rem 0 3rem;
}
body{
    color: var(--text-color);
}
img{
    width: 100%;
}

/* =======================================  */
/* HEADER  */
header{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: var(--bg-color);
    box-shadow: 0 1px 4px hsl(0 4% 15% / 10%);
    z-index: 100;
}
.nav{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 0;
}
.logo{
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--sec-color);
    text-transform: uppercase;
}
.logo span{
    color: var(--main-color);
    font-weight: 700;
}
#cart-icon{
    font-size: 1.8rem;
    cursor: pointer;
}

/* CART  */
.cart{
    position: fixed;
    top: 0;
    right: 0;
    right: -100%; 
    width: 360px;
    height: 100vh;
    overflow-y: auto;
    overflow-x: hidden;
    padding: 20px;
    background-color: var(--bg-color);
    box-shadow: -2px solid 4px hsl(0 4% 15% / 10%);
    border: 1px solid var(--main-color);
    transition: 1.5s;
}
.cart.active{
    right: 0;
    transition: .5s;
}
.cart-title{
    text-align: center;
    font-size: 1.5rem;
    font-weight: 600;
    margin-top: 2rem;
}
.cart-box{
    display: grid;
    grid-template-columns: 32% 50% 18%;
    align-items: center;
    gap: 1rem;
    margin-top: 1rem;
}
.cart-img{
    width: 100px;
    height: 100px;
    object-fit: contain;
    padding: 10px;
}
.detail-box{
    display: grid;
    row-gap: .5rem;
}
.cart-product-title{
    font-size: 1rem;
    text-transform: uppercase;
}
.cart-price{
    font-weight: 500;
}
.cart-quantity{
    border: 1px solid var(--text-color);
    outline-color: var(--main-color);
    width: 2.4rem;
    text-align: center;
    font-size: 1rem;
}
.cart-remove{
    font-size: 24px;
    color: var(--main-color);
    cursor: pointer;
}
.total{
    display: flex;
    justify-content: flex-end;
    margin-top: 1.5rem;
    border-top: 1px solid var(--text-color);
}
.total-title{
    font-size: 1rem;
    font-weight: 600;
}
.total-price{
    margin-left: .5rem;
}
.btn-buy{
    display: flex;
    margin: 1.5rem auto 0 auto;
    padding: 12px 20px;
    border: none;
    background-color: var(--sec-color);
    color: var(--bg-color);
    font-size: 1rem;
    font-weight: 500;
    cursor: pointer;
}
.btn-buy:hover{
    background-color: var(--text-color);
}
#cart-close{
    position: absolute;
    top: 1rem;
    right: .8rem;
    font-size: 2rem;
    color: var(--text-color);
    cursor: pointer;
}

/* SHOP SECTION  */
.shop{
    margin-top: 2rem;
}
.section-title{
    font-style: 1.5rem;
    font-weight: 600;
    text-align: center;
    margin-bottom: 1.5rem;
}
.shop-content{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, auto));
    gap: 1.5rem;
}
.product-box{
    position: relative;
}
.product-box:hover{
    padding: 10px;
    border: 1px solid var(--text-color);
    transition: .4s;
}
.product-img{
    width: 100%;
    aspect-ratio: 1/1;
    object-fit: cover;
    margin-bottom: .5rem;
}
.product-title{
    font-size: 1.1rem;
    font-weight: 600;
    text-transform: uppercase;
    margin-bottom: .5rem;
}
.product-price{
    font-weight: 500;
}
.add-cart{
    position: absolute;
    bottom: 0;
    right: 0;
    background-color: var(--text-color);
    color: var(--bg-color);
    padding: 10px;
    cursor: pointer;
}
.add-cart:hover{
    background-color: hsl(249, 32%, 17%);
}


/* ================ RESPONSIVE & BREAKPOINTS ============= */
@media (max-width: 1080px){
    .nav{
        padding: 15px;
    }
    .container{
        width: 90%;
        margin: 0 auto;
    }
    section{
        padding: 3rem 0 2rem;
    }
    .shop{
        margin-top: 2rem;
    }
}

/* For Medium Devices */
@media (max-width: 400px){
    .nav{
        padding: 11px;
    }
    .logo{
        font-size: 1rem;
    }
    .cart{
        width: 320px;
    }
}

/* For Small Devices */
@media (max-width: 360px){
    .shop{
        margin-top: 1rem;
    }
    .cart{
        width: 280px;
    }
}

```

### Step-3: Javascript

The final thing which comes in the website is the functionality of the website here the functionality involves regarding the cart section that is "My Cart" and the fuctionality involves the adding of elements,removing of elements from the cart by the users.A file is created with the name index.js and the following code is added :

```

// OPEN & CLOSE CART
const cartIcon = document.querySelector("#cart-icon");
const cart = document.querySelector(".cart");
const closeCart = document.querySelector("#cart-close");

cartIcon.addEventListener("click", () => {
  cart.classList.add("active");
});

closeCart.addEventListener("click", () => {
  cart.classList.remove("active");
});

// Start when the document is ready
if (document.readyState == "loading") {
  document.addEventListener("DOMContentLoaded", start);
} else {
  start();
}

// =============== START ====================
function start() {
  addEvents();
}

// ============= UPDATE & RERENDER ===========
function update() {
  addEvents();
  updateTotal();
}

// =============== ADD EVENTS ===============
function addEvents() {
  // Remove items from cart
  let cartRemove_btns = document.querySelectorAll(".cart-remove");
  console.log(cartRemove_btns);
  cartRemove_btns.forEach((btn) => {
    btn.addEventListener("click", handle_removeCartItem);
  });

  // Change item quantity
  let cartQuantity_inputs = document.querySelectorAll(".cart-quantity");
  cartQuantity_inputs.forEach((input) => {
    input.addEventListener("change", handle_changeItemQuantity);
  });

  // Add item to cart
  let addCart_btns = document.querySelectorAll(".add-cart");
  addCart_btns.forEach((btn) => {
    btn.addEventListener("click", handle_addCartItem);
  });

  // Buy Order
  const buy_btn = document.querySelector(".btn-buy");
  buy_btn.addEventListener("click", handle_buyOrder);
}

// ============= HANDLE EVENTS FUNCTIONS =============
let itemsAdded = [];

function handle_addCartItem() {
  let product = this.parentElement;
  let title = product.querySelector(".product-title").innerHTML;
  let price = product.querySelector(".product-price").innerHTML;
  let imgSrc = product.querySelector(".product-img").src;
  console.log(title, price, imgSrc);

  let newToAdd = {
    title,
    price,
    imgSrc,
  };

  // handle item is already exist
  if (itemsAdded.find((el) => el.title == newToAdd.title)) {
    alert("This Item Is Already Exist!");
    return;
  } else {
    itemsAdded.push(newToAdd);
  }

  // Add product to cart
  let cartBoxElement = CartBoxComponent(title, price, imgSrc);
  let newNode = document.createElement("div");
  newNode.innerHTML = cartBoxElement;
  const cartContent = cart.querySelector(".cart-content");
  cartContent.appendChild(newNode);

  update();
}

function handle_removeCartItem() {
  this.parentElement.remove();
  itemsAdded = itemsAdded.filter(
    (el) =>
      el.title !=
      this.parentElement.querySelector(".cart-product-title").innerHTML
  );

  update();
}

function handle_changeItemQuantity() {
  if (isNaN(this.value) || this.value < 1) {
    this.value = 1;
  }
  this.value = Math.floor(this.value); // to keep it integer

  update();
}

function handle_buyOrder() {
  if (itemsAdded.length <= 0) {
    alert("There is No Order to Place Yet! \nPlease Make an Order first.");
    return;
  }
  const cartContent = cart.querySelector(".cart-content");
  cartContent.innerHTML = "";
  alert("Your Order is Placed Successfully :)");
  itemsAdded = [];

  update();
}

// =========== UPDATE & RERENDER FUNCTIONS =========
function updateTotal() {
  let cartBoxes = document.querySelectorAll(".cart-box");
  const totalElement = cart.querySelector(".total-price");
  let total = 0;
  cartBoxes.forEach((cartBox) => {
    let priceElement = cartBox.querySelector(".cart-price");
    let price = parseFloat(priceElement.innerHTML.replace("$", ""));
    let quantity = cartBox.querySelector(".cart-quantity").value;
    total += price * quantity;
  });

  // keep 2 digits after the decimal point
  total = total.toFixed(2);
  // or you can use also
  // total = Math.round(total * 100) / 100;

  totalElement.innerHTML = "$" + total;
}

// ============= HTML COMPONENTS =============
function CartBoxComponent(title, price, imgSrc) {
  return `
    <div class="cart-box">
        <img src=${imgSrc} alt="" class="cart-img">
        <div class="detail-box">
            <div class="cart-product-title">${title}</div>
            <div class="cart-price">${price}</div>
            <input type="number" value="1" class="cart-quantity">
        </div>
        <!-- REMOVE CART  -->
        <i class='bx bxs-trash-alt cart-remove'></i>
    </div>`;
}


```

## Code Explanation

The HTML version using in the over here is HTML-5 and the elements in the navbar which comprises of logo and cart section are all placed in the grid arrangement which customised and visually enhanced with the CSS code and the HTML code gives the layout to the above website.In the CSS code the media queries are used which helps the website to become responsive in naturewhich helps the whole website including the cart section to visualize by user properly from any devices.The functionality which is the main attraction of the website without which this website seems to be incomplete revolves around the Javascript and the following elements are used by Javascript as follows:

1.A container to hold the items in the cart.

2.A function to add items to the cart.

3.A function to remove items from the cart.

4.A function to calculate the total cost of the items in the cart.

5.An event listener to add items to the cart when the user clicks the 'Add to Cart' which the right button on the every product card in the "Shop Product" section of the website.

6.An event listener to remove items from the cart when the user clicks the 'Remove' button.

7.A display of the number of items in the cart and the total cost.

8.The ability to save the cart data to the local storage.

The javascript code handles dynamic data changes, such as new items being added or removed from the cart, without breaking the cart functionality.

## Links

Hosted Link: https://suk-18.github.io/AI-FAKE-SHOP.github.io/

Video Explanation Link: https://drive.google.com/file/d/1ny-D8zBOF1U2UFcbNM92TdzyIZpSi-Mt/view?usp=sharing

Repository Link: https://github.com/suk-18/AI-FAKE-SHOP.github.io




