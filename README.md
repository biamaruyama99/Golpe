<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Um Convite Especial</title>

<style>
body {
  margin: 0;
  padding: 0;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-family: Arial, sans-serif;
  color: white;
  background: linear-gradient(45deg, #ff0080, #ffcc00, #00ffcc, #6600ff);
  background-size: 400% 400%;
  animation: bg 6s infinite alternate;
}

@keyframes bg {
  0% {background-position: 0% 50%;}
  100% {background-position: 100% 50%;}
}

.container {
  background: rgba(0,0,0,0.6);
  padding: 40px;
  border-radius: 25px;
  box-shadow: 0 0 25px gold;
  max-width: 90%;
}

h1 {
  font-size: 32px;
}

p {
  font-size: 20px;
  margin-bottom: 30px;
}

button {
  padding: 15px 30px;
  font-size: 18px;
  margin: 10px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
}

#sim {
  background-color: #00ff99;
}

#sim:hover {
  transform: scale(1.1);
}

#nao {
  background-color: #ff3333;
  position: absolute;
}

.confete {
  position: fixed;
  width: 10px;
  height: 10px;
  top: -10px;
  animation: cair linear infinite;
}

@keyframes cair {
  to {
    transform: translateY(110vh);
  }
}
</style>
</head>

<body>

<div class="container">
  <h1>🎉 Um convite especial 🎉</h1>
  <p>Você aceita cair nesse golpe? 😏💘</p>

  <button id="sim" onclick="aceitou()">SIM 💕</button>
  <button id="nao">NÃO 😜</button>
</div>

<script>
const nao = document.getElementById("nao");

function fugir() {
  const largura = window.innerWidth - 100;
  const altura = window.innerHeight - 50;

  nao.style.left = Math.random() * largura + "px";
  nao.style.top = Math.random() * altura + "px";
}

nao.addEventListener("mouseover", fugir);
nao.addEventListener("touchstart", fugir);

function aceitou() {
  alert("Eu sabiaaa 😏🎊 Agora não tem mais volta! Carnaval garantido comigo 💃🕺");
}

for (let i = 0; i < 60; i++) {
  let confete = document.createElement("div");
  confete.classList.add("confete");
  confete.style.left = Math.random() * 100 + "vw";
  confete.style.animationDuration = (Math.random() * 3 + 2) + "s";
  confete.style.backgroundColor =
    ["#ff0080", "#ffcc00", "#00ffcc", "#6600ff"][Math.floor(Math.random() * 4)];
  document.body.appendChild(confete);
}
</script>

</body>
</html>
