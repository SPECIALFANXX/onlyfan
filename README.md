<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fan Club Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        .login-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .login-container h2 {
            margin-bottom: 20px;
            text-align: center;
        }
        .login-container input[type="text"],
        .login-container input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .login-container input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            border: none;
            border-radius: 5px;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
        }
        .login-container input[type="submit"]:hover {
            background-color: #45a049;
        }
        .error-message {
            color: red;
            text-align: center;
            display: none;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Fan Club Login</h2>
        <form onsubmit="return validateForm()">
            <label for="fan-id">FAN ID</label>
            <input type="text" id="fan-id" name="fan-id" required>
            <label for="passcode">Passcode</label>
            <input type="password" id="passcode" name="passcode" required>
            <input type="submit" value="Login">
            <p class="error-message" id="error-message">Invalid FAN ID or Passcode.</p>
        </form>
    </div>

    <script>
        function validateForm() {
            const fanId = document.getElementById('fan-id').value;
            const passcode = document.getElementById('passcode').value;
            const errorMessage = document.getElementById('error-message');

            if (fanId === '0689256' && passcode === 'XX34Y8KV10') {
                window.location.href = 'https://onlyfans.com/maddymay69';
                return false; // Prevent form submission since we're redirecting
            } else {
                errorMessage.style.display = 'block';
                return false; // Prevent form submission
            }
        }
    </script>
</body>
</html>
