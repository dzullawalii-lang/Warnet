# Warnet
Gaktau
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>7 Malam di Warnet - Coming Soon</title>

<link href="https://fonts.googleapis.com/css2?family=Creepster&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:black;
    overflow:hidden;
    font-family:Arial, sans-serif;
    color:white;
}

/* VIDEO BACKGROUND */
video{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    object-fit:cover;
    z-index:-2;
    filter:brightness(35%);
}

.overlay{
    position:fixed;
    width:100%;
    height:100%;
    background:rgba(0,0,0,0.55);
    z-index:-1;
}

/* MAIN */
.container{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    text-align:center;
    padding:20px;
}

/* TITLE */
.title{
    font-size:80px;
    color:red;
    font-family:'Creepster', cursive;
    text-shadow:
    0 0 10px red,
    0 0 20px darkred,
    0 0 40px red;
    animation:flicker 2s infinite;
}

.subtitle{
    margin-top:15px;
    font-size:22px;
    color:#ddd;
    max-width:700px;
    line-height:1.5;
}

.coming{
    margin-top:40px;
    font-size:45px;
    font-weight:bold;
    animation:blink 1.5s infinite;
}

.btn{
    margin-top:35px;
    padding:15px 40px;
    border:none;
    background:red;
    color:white;
    font-size:20px;
    cursor:pointer;
    border-radius:10px;
    transition:0.3s;
    box-shadow:0 0 20px red;
}

.btn:hover{
    transform:scale(1.1);
    background:darkred;
}

.warning{
    position:absolute;
    bottom:20px;
    font-size:14px;
    color:#aaa;
    letter-spacing:2px;
}

@keyframes flicker{
    0%{opacity:1;}
    50%{opacity:0.7;}
    100%{opacity:1;}
}

@keyframes blink{
    0%{opacity:1;}
    50%{opacity:0.3;}
    100%{opacity:1;}
}

.blood{
    position:absolute;
    width:100%;
    top:0;
    left:0;
    pointer-events:none;
    opacity:0.4;
}

@media(max-width:700px){
    .title{
        font-size:50px;
    }

    .coming{
        font-size:30px;
    }

    .subtitle{
        font-size:18px;
    }
}
</style>
</head>

<body>

<!-- VIDEO -->
<video autoplay muted loop>
    <source src="warnet.mp4" type="video/mp4">
</video>

<div class="overlay"></div>

<!-- BLOOD -->
<img class="blood" src="https://i.imgur.com/qh7p6rn.png">

<!-- CONTENT -->
<div class="container">

    <h1 class="title">7 MALAM DI WARNET</h1>

    <p class="subtitle">
        Sebuah game horror Roblox bertema warnet Indonesia tahun 2010.
        Bertahan hidup selama 7 malam di warnet tua yang penuh misteri.
    </p>

    <div class="coming">
        COMING SOON...
    </div>

    <button class="btn" onclick="playRadio()">
        NYALAKAN RADIO WARNET
    </button>

</div>

<div class="warning">
    "AKU MELIHATMU..."
</div>

<!-- RADIO -->
<audio id="radio">
    <source src="radio.mp3" type="audio/mp3">
</audio>

<!-- HORROR SOUND -->
<audio id="horrorSound" autoplay loop>
    <source src="horror.mp3" type="audio/mp3">
</audio>

<script>

/* PLAY RADIO */
function playRadio(){
    document.getElementById("radio").play();
}

/* AUTOPLAY HORROR */
document.body.addEventListener("click", () => {
    document.getElementById("horrorSound").play();
});

/* TITLE GLITCH */
setInterval(()=>{
    document.title =
    Math.random() > 0.5 ?
    "7 Malam di Warnet" :
    "AKU DI BELAKANGMU";
},1000);

/* SCREEN FLASH */
setInterval(()=>{
    document.body.style.filter =
    "brightness(" + (Math.random()*1.5) + ")";
},300);

</script>

</body>
</html>
