# Ivangram
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudyHub</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <header>
        <h1>Studyhub </h1>
        <p>Make your subjects sound fun</p>
    </header>

    <main id="home">
        <h2>Welcome to StudyHub</h2>
        <p>Find people who can help you by offering online courses.</p>

        <button onclick="showSignup()">Sign Up</button>
    </main>

    <section id="signup" class="form-section">
        <h2>Create Your Account</h2>

        <input type="text" id="username" placeholder="Username">
        <input type="email" id="email" placeholder="Email">
        <input type="password" id="password" placeholder="Password">
        <input type="password" id="confirmPassword" placeholder="Confirm Password">

        <button onclick="createAccount()">Create Account</button>
        <button onclick="goHome()">Back</button>

        <p id="message"></p>
    </section>

    <script src="script.js"></script>

</body>
</html>
function showSignup() {
    document.getElementById("home").style.display = "none";
    document.getElementById("signup").style.display = "block";
}

function goHome() {
    document.getElementById("signup").style.display = "none";
    document.getElementById("home").style.display = "block";
}

function createAccount() {
    const username = document.getElementById("username").value;
    const email = document.getElementById("email").value;
    const password = document.getElementById("password").value;
    const confirmPassword = document.getElementById("confirmPassword").value;
    const message = document.getElementById("message");

    if (username === "" || email === "" || password === "") {
        message.textContent = "Invalid information please enter the fields    ";
        return;
    }

    if (password !== confirmPassword) {
        message.textContent = "Passwords do not match.";
        return;
    }

    message.textContent = "Account created! 🎉";
}
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background: #080d42;
    color: #222;
}

header {
    background: #000000;
    color: rgb(19, 16, 57);
    padding: 30px;
    text-align: center;
}

header h1 {
    font-size: 40px;
    margin-bottom: 10px;
}

header p {
    font-size: 18px;
}

main {
    max-width: 900px;
    margin: 50px auto;
    text-align: center;
    padding: 20px;
}

main h2 {
    font-size: 32px;
    margin-bottom: 15px;
}

main p {
    font-size: 18px;
    margin-bottom: 30px;
}

button {
    padding: 12px 25px;
    margin: 8px;
    border: none;
    border-radius: 8px;
    background: #4de31b;
    color: rgb(7, 12, 55);
    font-size: 16px;
    cursor: pointer;
}

button:hover {
    background: #d7370b;
}
.form-section {
    display: none;
    max-width: 450px;
    margin: 50px auto;
    padding: 30px;
    background: rgb(0, 0, 0);
    border-radius: 12px;
    text-align: center;
}

.form-section h2 {
    margin-bottom: 25px;
}

.form-section input {
    display: block;
    width: 100%;
    padding: 12px;
    margin: 12px 0;
    border: 1px solid #000000;
    border-radius: 8px;
    font-size: 16px;
}

#message {
    margin-top: 15px;
    font-weight: bold;
}
