<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shérif Crux - Defines The Law</title>
    <style>
        body {
            background-color: #1A1A1A;
            color: #FFFFFF;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #8B0000;
            padding: 20px;
            text-align: center;
        }

        h1 {
            margin: 0;
            font-size: 36px;
        }

        nav {
            text-align: center;
            margin-top: 20px;
        }

        nav a {
            color: #FFFFFF;
            text-decoration: none;
            margin: 0 10px;
        }

        nav a:hover {
            text-decoration: underline;
        }

        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 0 20px;
        }

        .item {
            margin-bottom: 20px;
            border-bottom: 1px solid #FFFFFF;
            padding-bottom: 20px;
        }

        .item img {
            max-width: 100%;
            height: auto;
        }

        .item h2 {
            margin-top: 0;
        }

        footer {
            background-color: #8B0000;
            padding: 20px;
            text-align: center;
            position: fixed;
            left: 0;
            bottom: 0;
            width: 100%;
        }

        /* 3D rotating logo animation */
        @keyframes spin {
            0% {
                transform: rotateY(0);
            }
            100% {
                transform: rotateY(360deg);
            }
        }

        .logo {
            width: 100px;
            height: 100px;
            animation: spin 5s infinite linear;
        }

        /* Feedback form styles */
        .feedback-form {
            margin-top: 20px;
        }

        .feedback-form textarea {
            width: 100%;
            height: 100px;
            margin-top: 10px;
        }
    </style>
    <head>

    </style>
</head>
<body>
    <header>
        <h1>Shérif Crux</h1>
        <h2></h2>
        <img class="logo" src="BUU-transformed.png" alt="Shérif Crux Logo">
                <h2></h2>
        <p>Defines The Law</p>
        <nav>
            <a href="#about">About</a>
            <a href="#products">Products</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>
    <div class="container" id="about">
        <h2>About Shérif Crux</h2>
        <p>Shérif Crux is a Lagos-based streetwear brand that popped up out of nowhere in 2024. Lagos, being such a vibrant and culturally rich city, is the perfect backdrop for a streetwear brand like Shérif Crux to make its mark.</p>
    </div>
    <div class="item">
        <h2>Lust White on Black</h2>
        <p>Price: ₦18000</p>
        <p>Sizes: S, M, L, XL</p>
        <h2>Front</h2>
        <img src="path (2).png">
        <h2>Back</h2>
        <img src="path (1).png">
        <button id="addToCartBtn1" onclick="addToCart(18000, 1)">Add to Cart</button>
        <h2>Front</h2>
        <img src="path (3).png">
        <h2></h2>
        <h2>Back</h2>

        <img src="path (4).png">

        <h2></h2>

        <button id="addToCartBtn1" onclick="addToCart(18000, 1)">Add to Cart</button>
        <h2></h2>
        <div class="feedback-form">

        <!-- Add more items here -->
    
        <div class="feedback-form">
            <!-- Feedback form content -->
        </div>
    </div>
    
    <div id="cartSummary">
        <h2>Cart Summary</h2>
        <p>Total Amount: ₦<span id="totalAmount">0</span></p>
        <p>Number of Items: <span id="itemCounter">0</span></p>
    </div>
    
    <script>
        let totalAmount = 0;
        let itemCounter = 0;
    
        function addToCart(price, quantity) {
            totalAmount += price * quantity;
            itemCounter += quantity;
    
            // Update the total amount and item counter display
            document.getElementById("totalAmount").textContent = totalAmount;
            document.getElementById("itemCounter").textContent = itemCounter;
    
            alert("Item added to cart!");
        }
    
        function sendFeedback() {
            // Logic to send feedback message
            // You can implement this using JavaScript or connect to a backend system
            alert("Feedback sent!");
        }
    </script>
                <div class="feedback-form">
                    <h2>Contact Us</h2>
                    <p>For any inquiries or feedback, please contact us at <a href="mailto:rockytrapz825@gmail.com">rockytrapz825@gmail.com</a>.</p>
                    <h3>Report Problems or Feedback</h3>
                    <textarea placeholder="Enter your message here"></textarea>
                    <button onclick="sendFeedback()">Send</button>
                    

                    <body>
                        <header>
                            <h1>Shérif Crux</h1>
                            <h2></h2>
                    
                            <!-- 3D spinning logo -->
                            <div class="logo">
                                <svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
                                    <text x="10" y="50" font-family="Verdana" font-size="20" fill="#FFFFFF">The Law</text>
                                </svg>
                            </div>
                    
                            <h2></h2>
                    
                            <p>Defines The Law</p>
                            <nav>
                                <a href="#about">About</a>
                                <a href="#products">Products</a>
                                <a href="#contact">Contact</a>
                            </nav>
                        </header>
                    
                        <!-- Rest of the content goes here -->
                    
                    </body>       

                    <h2></h2>
                </div>
            </div>
            <!-- Add more items here -->
        </div>
    
        <div class="container" id="contact">
            <h2></h2>
    
        </div>
    
        <footer>
            &copy; 2024 Shérif Crux. All rights reserved.
        </footer>
        

        <script>
            let dailyPassword = localStorage.getItem("dailyPassword");
    
            function setPassword() {
                const newPassword = prompt("Set today's password for the website:");
                if (newPassword) {
                    dailyPassword = newPassword;
                    localStorage.setItem("dailyPassword", dailyPassword);
                    alert("Password set successfully!");
                }
            }
    
            function unlockWebsite() {
                if (!dailyPassword) {
                    setPassword();
                }
                const enteredPassword = prompt("Please enter today's password:");
                if (enteredPassword === dailyPassword) {
                    document.body.style.display = "block";
                } else {
                    alert("Incorrect password!");
                }
            }
    
            function sendPasswordByEmail() {
                const email = "rockytrapz825@gmail.com";
                const subject = "Today's Website Password";
                const body = `Today's password for the website is: ${dailyPassword}`;
                window.open(`mailto:${email}?subject=${subject}&body=${body}`);
            }
    
            // Initially, hide the website content until the correct password is entered
            document.body.style.display = "none";
            unlockWebsite();
        </script>
    <html>
    
