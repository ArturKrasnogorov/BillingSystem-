<!DOCTYPE html>
<html>
<head>
    <title>Simple Login</title>
</head>
<body>
    <h2>Login Form</h2>
    <form action="login.php" method="post">
        <label>Username:</label><br>
        <input type="text" name="username" required><br><br>

        <label>Password:</label><br>
        <input type="password" name="password" required><br><br>

        <input type="submit" value="Login">
    </form>
</body>
</html>

<?php
// Sample username and password (in a real app, you'd use a database)
$correct_username = "admin";
$correct_password = "12345";

// Get submitted data
$username = $_POST['username'];
$password = $_POST['password'];

// Simple validation
if ($username === $correct_username && $password === $correct_password) {
    echo "✅ Login successful! Welcome, $username.";
} else {
    echo "❌ Invalid username or password.";
}
?>


