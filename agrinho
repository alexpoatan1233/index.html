<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Agro Forte - Agrinho</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    background:#f4f4f4;
    color:#333;
}

header{
    background:linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
    url('https://images.unsplash.com/photo-1500937386664-56d1dfef3854?auto=format&fit=crop&w=1600&q=80');
    background-size:cover;
    background-position:center;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    color:white;
}

.hero h1{
    font-size:4rem;
    margin-bottom:20px;
}

.hero p{
    font-size:1.3rem;
    margin-bottom:25px;
}

.btn{
    padding:15px 30px;
    border:none;
    background:#4CAF50;
    color:white;
    font-size:18px;
    border-radius:8px;
    cursor:pointer;
    transition:0.3s;
}

.btn:hover{
    background:#2e7d32;
}

section{
    padding:80px 10%;
}

.titulo{
    text-align:center;
    margin-bottom:50px;
    color:#2e7d32;
    font-size:2.5rem;
}

.sobre{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
    align-items:center;
}

.sobre img{
    width:100%;
    border-radius:15px;
}

.sobre p{
    line-height:1.8;
    font-size:1.1rem;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:white;
    padding:25px;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
    transition:0.3s;
}

.card:hover{
    transform:translateY(-10px);
}

.card h3{
    color:#2e7d32;
    margin-bottom:10px;
}

.estatisticas{
    background:#2e7d32;
    color:white;
}

.stats{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    gap:20px;
    text-align:center;
}

.numero{
    font-size:3rem;
    font-weight:bold;
}

footer{
    background:#1b5e20;
    color:white;
    text-align:center;
    padding:25px;
}

#mensagem{
    margin-top:20px;
    font-size:20px;
    color:#2e7d32;
    text-align:center;
}

@media(max-width:768px){
    .hero h1{
        font-size:2.5rem;
    }

    .sobre{
        grid-template-columns:1fr;
    }
}
</style>
</head>
<body>

<header>
    <div class="hero">
        <h1>AGRO FORTE</h1>
        <p>O campo alimenta o mundo e fortalece o Brasil.</p>
        <button class="btn" onclick="mostrarMensagem()">
            Descubra Mais
        </button>
    </div>
</header>

<section>
    <h2 class="titulo">Sobre o Agro</h2>

    <div class="sobre">
        <img src="https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=1200&q=80">

        <div>
            <p>
                O agronegócio é um dos setores mais importantes da economia brasileira.
                Ele produz alimentos, gera empregos e movimenta milhões de pessoas em todo o país.
            </p>

            <br>

            <p>
                Com tecnologia, sustentabilidade e inovação, o agro contribui para o desenvolvimento
                das cidades e para a qualidade de vida da população.
            </p>

            <div id="mensagem"></div>
        </div>
    </div>
</section>

<section>
    <h2 class="titulo">Pilares do Agro Forte</h2>

    <div class="cards">

        <div class="card">
            <h3>🌱 Sustentabilidade</h3>
            <p>Produção responsável respeitando o meio ambiente.</p>
        </div>

        <div class="card">
            <h3>🚜 Tecnologia</h3>
            <p>Máquinas modernas aumentam a produtividade no campo.</p>
        </div>

        <div class="card">
            <h3>🌎 Alimentação</h3>
            <p>O agro produz alimentos para milhões de pessoas.</p>
        </div>

        <div class="card">
            <h3>💼 Empregos</h3>
            <p>Geração de renda e oportunidades para a população.</p>
        </div>

    </div>
</section>

<section class="estatisticas">
    <h2 class="titulo" style="color:white;">Números do Agro</h2>

    <div class="stats">

        <div>
            <div class="numero" data-numero="100">0</div>
            <p>Milhões de toneladas produzidas</p>
        </div>

        <div>
            <div class="numero" data-numero="50">0</div>
            <p>Milhões de empregos</p>
        </div>

        <div>
            <div class="numero" data-numero="27">0</div>
            <p>Estados beneficiados</p>
        </div>

        <div>
            <div class="numero" data-numero="100">0</div>
            <p>% de dedicação ao futuro</p>
        </div>

    </div>
</section>

<footer>
    <h3>Projeto Agrinho 2025 - Agro Forte</h3>
    <p>Desenvolvido com HTML, CSS e JavaScript.</p>
</footer>

<script>
function mostrarMensagem(){
    document.getElementById("mensagem").innerHTML =
    "🌾 O agro conecta o campo e a cidade, promovendo desenvolvimento e qualidade de vida!";
}

const numeros = document.querySelectorAll(".numero");

const animarNumeros = () => {
    numeros.forEach(numero => {
        const alvo = +numero.getAttribute("data-numero");
        let atual = 0;

        const incremento = alvo / 100;

        const contador = setInterval(() => {
            atual += incremento;

            if(atual >= alvo){
                numero.innerText = alvo;
                clearInterval(contador);
            } else {
                numero.innerText = Math.floor(atual);
            }
        }, 20);
    });
};

const observador = new IntersectionObserver((entradas)=>{
    entradas.forEach(entrada=>{
        if(entrada.isIntersecting){
            animarNumeros();
            observador.disconnect();
        }
    });
});

observador.observe(document.querySelector(".estatisticas"));
</script>

</body>
</html>
