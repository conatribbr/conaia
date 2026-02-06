<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CONA íA - Consultora Nacional de Inteligência Artificial</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f9;
      margin: 0;
      padding: 0;
    }
    header {
      background: #003366;
      color: white;
      padding: 20px;
      text-align: center;
    }
    main {
      max-width: 800px;
      margin: 40px auto;
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h1 {
      color: #003366;
    }
    .chat-box {
      border: 1px solid #ccc;
      padding: 10px;
      height: 300px;
      overflow-y: auto;
      margin-bottom: 10px;
      background: #fafafa;
    }
    .input-box {
      display: flex;
    }
    .input-box input {
      flex: 1;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .input-box button {
      padding: 10px 20px;
      margin-left: 10px;
      background: #003366;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .input-box button:hover {
      background: #0055aa;
    }
  </style>
</head>
<body>
  <header>
    <h1>CONA íA</h1>
    <p>Consultora Nacional de Inteligência Artificial em Tributação Federal</p>
  </header>
  <main>
    <h2>Bem-vindo!</h2>
    <p>Digite sua dúvida sobre tributação federal e receba uma resposta clara e objetiva.</p>
    
    <div class="chat-box" id="chatBox">
      <p><strong>CONA íA:</strong> Olá! Sou sua consultora em tributação federal. Qual sua dúvida?</p>
    </div>
    
    <div class="input-box">
      <input type="text" id="userInput" placeholder="Digite sua pergunta...">
      <button onclick="sendMessage()">Enviar</button>
    </div>
  </main>

  <script>
    function sendMessage() {
      const input = document.getElementById("userInput");
      const chatBox = document.getElementById("chatBox");
      const userText = input.value.trim();
      if(userText !== "") {
        chatBox.innerHTML += `<p><strong>Você:</strong> ${userText}</p>`;
        // Simulação de resposta (aqui você conecta com backend/IA real)
        chatBox.innerHTML += `<p><strong>CONA íA:</strong> Estou analisando sua questão sobre "${userText}". Em breve darei uma resposta detalhada.</p>`;
        input.value = "";
        chatBox.scrollTop = chatBox.scrollHeight;
      }
    }
  </script>
</body>
</html>
