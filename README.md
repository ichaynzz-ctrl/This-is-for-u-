<!DOCTYPE html>
<html>
<head>
<title>Itz for u Devuzzee 🎀</title>

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    text-align:center;
    background: linear-gradient(135deg,#ff9a9e,#fad0c4);
    overflow:hidden;
    color:white;
}

/* Glow Text */
.glow{
    font-size:28px;
    text-shadow:0 0 10px white,0 0 20px pink,0 0 30px red;
}

/* Buttons */
button{
    padding:12px 25px;
    font-size:18px;
    border:none;
    border-radius:20px;
    cursor:pointer;
    margin:10px;
}

#open{background:#ff4da6;}
#ignore{
    background:#ff3333;
    position:absolute;
}

/* Floating Hearts */
.heart{
    position:fixed;
    font-size:20px;
    animation:float 5s linear infinite;
}

@keyframes float{
    0%{transform:translateY(0);opacity:1;}
    100%{transform:translateY(-800px);opacity:0;}
}

/* Sparkling stars */
.star{
    position:fixed;
    color:white;
    animation:twinkle 2s infinite alternate;
}

@keyframes twinkle{
    from{opacity:0.2;}
    to{opacity:1;}
}

/* Next Page */
#nextPage{
    display:none;
    padding:40px;
}
</style>
</head>

<body>

<h1 class="glow">Firstly this is for youu 🎀</h1>

<button id="open" onclick="openPage()">Open 💖</button>
<button id="ignore" onmouseover="moveBtn()">Ignore 😏</button>

<div id="nextPage">
<h2 class="glow">Penneee oru krym... You are something special for me 🥹🎀</h2>

<p class="glow">
Sometimes I don’t know how to explain it…<br>
But nee ente life il vannappol entho change undayi.<br>
Ninte chiriyum, ninte presence um… athokke enikku valare special aanu.<br>
It’s not just liking… it’s something more peaceful and real.<br>
Among everyone… nee thanne enikku heart-il oru special place und. 🫶✨
</p>
</div>

<script>

/* Open Button */
function openPage(){
    alert("Chundariiiii 💖");
    document.getElementById("nextPage").style.display="block";
}

/* Ignore Button Running */
function moveBtn(){
    var btn=document.getElementById("ignore");
    var x=Math.random()*(window.innerWidth-100);
    var y=Math.random()*(window.innerHeight-50);
    btn.style.left=x+"px";
    btn.style.top=y+"px";
}

/* Floating Hearts + Roses */
setInterval(function(){
    var heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML="🌹";
    heart.style.left=Math.random()*window.innerWidth+"px";
    heart.style.bottom="0px";
    document.body.appendChild(heart);

    setTimeout(function(){
        heart.remove();
    },5000);
},600);

/* Sparkling Stars */
setInterval(function(){
    var star=document.createElement("div");
    star.className="star";
    star.innerHTML="✨";
    star.style.left=Math.random()*window.innerWidth+"px";
    star.style.top=Math.random()*window.innerHeight+"px";
    document.body.appendChild(star);

    setTimeout(function(){
        star.remove();
    },2000);
},500);

</script>

</body>
</html>
