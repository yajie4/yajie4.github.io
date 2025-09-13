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
  <video width="640" height="360" controls autoplay muted>
    <source src="YOUR-VIDEO-FILE.mp4" type="video/mp4"> <!-- CUSTOMIZE VIDEO FILE -->
    Your browser does not support the video tag.
  </video>

  <div>
    <h2>ENTER PASSWORD TO CONTINUE</h2>
    <h6><i>Clue: The day I promised</i></h6>
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
