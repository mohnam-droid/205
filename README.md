<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تسجيل الدخول</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input {
            width: 100%;
            padding: 10px;
            box-sizing: border-box;
        }
        .button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #0056b3;
        }
        .error {
            color: red;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>تسجيل الدخول</h2>
        <div class="form-group">
            <label for="username">اسم المستخدم:</label>
            <input type="text" id="username" placeholder="أدخل اسم المستخدم">
        </div>
        <div class="form-group">
            <label for="password">كلمة المرور:</label>
            <input type="password" id="password" placeholder="أدخل كلمة المرور">
        </div>
        <button class="button" onclick="login()">تسجيل الدخول</button>
        <div class="error" id="error"></div>
    </div>
    <script>
        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const error = document.getElementById('error');

            // تحقق من اسم المستخدم وكلمة المرور
            if (username === 'admin' && password === '1234') {
                window.location.href = 'passengers.html';
            } else {
                error.textContent = 'اسم المستخدم أو كلمة المرور غير صحيح.';
            }
        }
    </script>
</body>
</html>
