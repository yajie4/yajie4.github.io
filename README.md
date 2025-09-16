<html>
<head>
  <title>HELLO HUBBY</title> <!-- CUSTOMIZE TITLE -->
  <style>
    body {
      background-color: #111;
      color: white;
      font-family: sans-serif;
      text-align: center;
      padding: 40px;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <iframe width="640" height="360" src="https://www.youtube.com/embed/GUlq0b6Wi5M" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <div>
    <h2><p style="color: #00B03B;"> ENTER PASSWORD TO CONTINUE</p></h2>
    <h6><i><p style="color: #32874E;">Clue: The day I promised</p></i></h6>
    <input type="password" id="password" placeholder="ENTER PASSWORD"> <!-- CUSTOMIZE PLACEHOLDER -->
    <button onclick="checkPassword()">SUBMIT</button>
  </div>

  <script>
    function checkPassword() {
      const input = document.getElementById("password").value;
      if (input === "070235") { <!-- CUSTOMIZE PASSWORD -->
        window.location.href = "MESSAGES.HTML"; <!-- CUSTOMIZE TARGET PAGE -->
      } else {
        alert("INCORRECT PASSWORD."); <!-- CUSTOMIZE ERROR MESSAGE -->
      }
    }
  </script>
</body>
</html>
