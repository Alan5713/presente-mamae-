<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Feliz Dia das Mães</title>

<style>

body{
    margin:0;
    padding:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ffd6e7,#fff0f5);
    font-family:Arial, sans-serif;
    overflow:hidden;
}

/* Card */
.card{
    width:90%;
    max-width:400px;
    background:white;
    padding:40px 25px;
    border-radius:25px;
    text-align:center;
    box-shadow:0 10px 30px rgba(0,0,0,0.15);
    z-index:10;
}

h1{
    color:#c2185b;
    margin-bottom:20px;
    font-size:32px;
}

p{
    font-size:18px;
    color:#555;
    margin-bottom:30px;
}

/* Botão */
#btn{
    width:100%;
    border:none;
    padding:18px;
    border-radius:15px;
    background:#ff4d8d;
    color:white;
    font-size:18px;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

#btn:active{
    transform:scale(0.96);
}

/* Mensagem escondida */
#mensagem{
    display:none;
    margin-top:25px;
    font-size:20px;
    color:#c2185b;
    font-weight:bold;
    animation:fade 0.6s;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(20px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}

</style>
</head>

<body>

<div class="card">

    <h1>Feliz Dia das Mães 💖</h1>

    <p>
        Mãe, clique no botão para resgatar seu presente 🎁
    </p>

    <button id="btn">
        Lavo a louça por 1 semana
    </button>

    <div id="mensagem">
        💕 Eu sabia que você preferia meu abraço! <br><br>
        Feliz Dia das Mães! <br>
        Te amo 💖
    </div>

</div>

<script>

const btn = document.getElementById("btn");
const mensagem = document.getElementById("mensagem");

btn.addEventListener("click", function(){

    // muda texto do botão
    btn.innerHTML = "Um beijo e abraço 💕";

    // muda cor
    btn.style.background = "#c2185b";

    // mostra mensagem
    mensagem.style.display = "block";

});

</script>

</body>
</html>
