<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shelfie - Book Recommendation Chatbot</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #1e1e2f, #2c2c54);
      color: white;
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    header {
      margin-bottom: 20px;
    }

    header h1 {
      font-size: 3rem;
      background: linear-gradient(90deg, #ff8a00, #e52e71);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    header p {
      font-size: 1.2rem;
      opacity: 0.8;
    }

    .bot-icon {
      width: 80px;
      height: 80px;
      background: linear-gradient(135deg, #ff8a00, #e52e71);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.5);
      margin: 20px auto;
      animation: float 3s ease-in-out infinite;
    }

    .bot-icon img {
      width: 50px;
      height: 50px;
    }

    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }

    footer {
      margin-top: 30px;
      font-size: 0.8rem;
      opacity: 0.7;
    }
  </style>
</head>
<body>

  <header>
    <h1>📚 Shelfie</h1>
    <p>Your personal book recommendation assistant</p>
  </header>

  <div class="bot-icon">
    <img src="https://cdn-icons-png.flaticon.com/512/4712/4712108.png" alt="Bot Icon">
  </div>

  <footer>
    Powered by IBM Watson Assistant
  </footer>
  <script>
  window.watsonAssistantChatOptions = {
    integrationID: "8f04df1b-ff82-45be-bf27-6554b51599d9", // The ID of this integration.
    region: "au-syd", // The region your integration is hosted in.
    serviceInstanceID: "d5952d7d-068a-479b-a16b-f680f7c8b248", // The ID of your service instance.
    onLoad: async (instance) => { await instance.render(); }
  };
  setTimeout(function(){
    const t=document.createElement('script');
    t.src="https://web-chat.global.assistant.watson.appdomain.cloud/versions/" + (window.watsonAssistantChatOptions.clientVersion || 'latest') + "/WatsonAssistantChatEntry.js";
    document.head.appendChild(t);
  });
</script>


</body>
</html>
