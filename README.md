<!DOCTYPE html>
<html lang="uk">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Mia i love you</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

  body, html {
    margin: 0; padding: 0; height: 100%; width: 100%;
    background: url('https://i.gifer.com/3btx.gif') no-repeat center center fixed;
    background-size: cover;
    font-family: 'Pacifico', cursive;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: #fff;
    text-shadow: 2px 2px 8px rgba(0,0,0,0.6);
  }

  /* Сердечко */
  #heart {
    font-size: 5em;
    cursor: pointer;
    animation: pulse 1.5s infinite;
    transition: transform 0.3s;
  }

  #heart.clicked {
    animation: none;
    transform: scale(1.3);
  }

  @keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.2); }
    100% { transform: scale(1); }
  }

  /* Текст */
  #message {
    font-size: 3em;
    margin-top: 20px;
    opacity: 0;
    transition: opacity 1s ease-in-out;
  }

  #message.show {
    opacity: 1;
  }
</style>
</head>
<body>

<div id="heart">❤️</div>
<div id="message">Mia, i love you ❤️</div>

<script>
  const heart = document.getElementById("heart");
  const message = document.getElementById("message");

  heart.addEventListener("click", () => {
    heart.classList.add("clicked");
    message.classList.add("show");
  });
</script>

</body>
</html>
