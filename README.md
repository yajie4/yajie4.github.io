<!DOCTYPE html>
<html>
<head>
  <title>Welcome</title>
</head>
<body>
  <h2>Enter Password to Continue</h2>
  <input type="password" id="password" placeholder="Enter password">
  <button onclick="checkPassword()">Submit</button>

  <script>
    function checkPassword() {
      const input = document.getElementById("password").value;
      if (input === "yourSecret") {
        window.location.href = "messages.html";
      } else {
        alert("Incorrect password.");
      }
    }
  </script>
</body>
</html>
