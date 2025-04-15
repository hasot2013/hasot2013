<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Samis Evreni Giriş</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(#0e0e0e, #333);
      color: white;
      text-align: center;
      padding-top: 100px;
    }
    input {
      padding: 10px;
      margin: 10px;
      font-size: 16px;
      width: 80%;
      max-width: 300px;
    }
    #emailDiv {
      display: none;
    }
    #adminPanel {
      display: none;
    }
  </style>
</head>
<body>
  <h1>Samis Evreni</h1>
  <input type="text" id="nickname" placeholder="Takma adınızı girin">
  <br>
  <input type="password" id="password" placeholder="Şifrenizi girin">
  <br>
  <div id="emailDiv">
    <input type="email" id="email" placeholder="Gmail adresinizi girin">
    <br>
  </div>
  <button onclick="girisYap()">Giriş Yap</button>

  <div id="adminPanel">
    <h2>Hoş geldin Hasot!</h2>
    <p>Admin Paneline başarıyla giriş yaptınız.</p>
  </div>

  <script>
    function girisYap() {
      var nick = document.getElementById("nickname").value;
      var pass = document.getElementById("password").value;
      var email = document.getElementById("email").value;

      if (nick === "Hasot" && pass === "4116") {
        document.getElementById("emailDiv").style.display = "block";
        if (email === "celikhasancihan@gmail.com") {
          document.getElementById("adminPanel").style.display = "block";
        } else if (email !== "") {
          alert("Bu e-posta admin değil!");
        }
      } else if (nick !== "" && pass !== "") {
        alert("Hoş geldin " + nick + "!");
      } else {
        alert("Lütfen takma ad ve şifre girin.");
      }
    }
  </script>
</body>
</html>
