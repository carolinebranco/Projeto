# Projeto
<!DOCTYPE html>
<html>
<head>
  <title>Área de Login</title>
</head>
<body>
  <h1>Área de Login</h1>
  <form id="loginForm">
    <label for="username">Nome de Usuário:</label>
    <input type="text" id="username" required><br><br>
    <label for="password">Senha:</label>
    <input type="password" id="password" required><br><br>
    <button type="submit">Entrar</button>
  </form>
  
  <script src="script.js"></script>
</body>
</html>
document.getElementById("loginForm").addEventListener("submit", function(event) {
  event.preventDefault(); // Evita que o formulário seja enviado

  // Obter valores de entrada do usuário
  var username = document.getElementById("username").value;
  var password = document.getElementById("password").value;

  // Realizar validação e lógica de login
  if (username === "usuario" && password === "senha") {
    // Login bem-sucedido, redirecionar para a página inicial
    window.location.href = "pagina-inicial.html";
  } else {
    // Login inválido, exibir mensagem de erro
    alert("Nome de usuário ou senha incorretos. Tente novamente.");
  }
});
body {
  background-color: black;
}

h1 {
  color: white;
  text-align: center;
}

form {
  background-color: white;
  width: 300px;
  margin: 0 auto;
  padding: 20px;
  border-radius: 5px;
}

label {
  display: block;
  margin-bottom: 10px;
}

input[type="text"],
input[type="password"] {
  width: 100%;
  padding: 5px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 3px;
}

button[type="submit"] {
  width: 100%;
  padding: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

button[type="submit"]:hover {
  background-color: #45a049;
}
