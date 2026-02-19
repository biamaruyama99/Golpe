<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Um Convite Especial</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(45deg, #ff0080, #ffcc00, #00ccff, #00ff88);
    background-size: 400% 400%;
    animation: gradient 8s ease infinite;
    font-family: 'Comic Sans MS', cursive;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
}

@keyframes gradient {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

.container {
    background: rgba(255,255,255,0.9);
    padding: 40px;
    border-radius: 25px;
    box-shadow: 0 0 30px rgba(0,0,0,0.3);
    position: relative;
}

h1 {
    font-size: 32px;
    color: #ff0080;
}

p {
    font-size: 22px;
}

button {
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 15px;
    cursor: pointer;
    margin: 10px;
    transition: 0.3s;
}

#sim {
    background-color: #00cc66;
    color: white;
}

#nao {
    background-color: #ff3333;
    color: white;
    position: absolute;
}

#resposta {
    margin-top: 20px;
    font-size: 22px;
    color: #ff0080;
    font-weight: bold;
}
</style>
</head>

<body>

<!-- Música -->
<iframe width="0" height="0"
src="https://www.youtube.com/embed/tMWpm_GOLaA?autoplay=1&loop=1&playlist=tMWpm_GOLaA"
frameborder="0"
allow="autoplay">
</iframe>

<div class="container">
    <h1>🎉 Um convite especial para Rodrigo 🎭</h1>
    <p>Você aceita cair nesse golpe?</p>

    <button id="sim" onclick="aceitou()">Sim</button>
    <button id="nao" onmouseover="fugir()">Não</button>

    <div id="resposta"></div>
</div>

<script>
function fugir() {
    const botao = document.getElementById("nao");
    const largura = window.innerWidth - 100;
    const altura = window.innerHeight - 100;

    botao.style.left = Math.random() * largura + "px";
    botao.style.top = Math.random() * altura + "px";
}

function aceitou() {
    document.getElementById("resposta").innerHTML =
    "💘 Eu sempre soube, a gente não pode fugir! 💃🏽✨";
}
</script>

</body>
</html>
