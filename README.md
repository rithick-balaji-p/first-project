<!DOCTYPE html>
<html>
<head>
  <title>Sign Up</title>
  <style>
    body { background-color: #f0f8ff; font-family: Arial; }
    h2 { color: darkblue; text-align: center; }
    form { border: 2px solid black; padding: 15px; width: 300px; margin: auto; background-color: white; }
    label { font-weight: bold; }
    input { margin: 5px; padding: 5px; width: 90%; }
    input[type=submit] { background-color: lightgreen; border: 1px solid black; cursor: pointer; }
  </style>
</head>
<body>
<center>
  <h2>Sign Up</h2>
  
  <form onsubmit="return signup()">
    <label>Username:</label><br>
    <input type="text" id="username"><br>
    <label>Email:</label><br>
    <input type="text" id="email"><br>
    <label>Password:</label><br>
    <input type="password" id="password"><br>
    <label>Re-enter Password:</label><br>
    <input type="password" id="repassword"><br><br>
    <input type="submit" value="Sign Up">
  </form>
  <p>Already have an account? <a href="login.html">Login</a></p>
</center>
<script>
  function signup() {
    var user = document.getElementById("username").value;
    var email = document.getElementById("email").value;
    var pass = document.getElementById("password").value;
    var repass = document.getElementById("repassword").value;
    if(user=="" || email=="" || pass=="" || repass=="") {
      alert("Please fill all fields");
      return false;
    }
    if(pass !== repass) {
      alert("Passwords do not match!");
      return false;
    }
    alert("Sign up successful!.");
    return true;
  }
</script>
</body>
</html> 
