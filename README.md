# This-is-for-u-
To my fav one 🎀
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For You ✨</title>

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    background: linear-gradient(to right,#ff758c,#ff7eb3);
    overflow:hidden;
    color:white;
}

/* Page Styling */
.page{
    position:absolute;
    width:100%;
    height:100%;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:20px;
    transition: opacity 1s ease;
}

/* Buttons */
button{
    padding:12px 25px;
    font-size:18px;
    border:none;
    border-radius:25px;
    margin:10px;
    cursor:pointer;
}

#openBtn{
    background:#ff1493;
    color:white;
}

#ignoreBtn{
    background:#ff4d4d;
    color:white;
    position:absolute;
}

/* Glow text */
.message{
    font-size:20px;
    max-width:650px;
    line-height:1.8;
    text-shadow:0 0 10px #fff,0 0 20px #ffb6c1,0 0 30px #ff69b4;
}

/* Hearts */
.heart{
    position:fixed;
    color:#ff0033;
    font-size:20px;
    animation: floatUp 6s linear infinite;
}

@keyframes floatUp{
    0%{transform: translateY(100vh) scale(1); opacity:1;}
    100%{transform: translateY(-10vh) scale(1.5); opacity:0;}
}

/* Stars */
.star{
    position:fixed;
    width:3px;
    height:3px;
    background:white;
    border-radius:50%;
    animation: twinkle 2s infinite alternate;
}

@keyframes twinkle{
    0%{opacity:0.2; transform:scale(1);}
    100%{opacity:1; transform:scale(1.5);}
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div id="page1" class="page">
    <h1>Firstly this is for youu 💌</h1>
    <button id="openBtn">Open 💖</button>
    <button id="ignoreBtn">Ignore 😏</button>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page" style="opacity:0; pointer-events:none;">
    <div class="message" id="typedText"></div>
</div>

<script>
const openBtn = document.getElementById("openBtn");
const ignoreBtn = document.getElementById("ignoreBtn");
const page1 = document.getElementById("page1");
const page2 = document.getElementById("page2");
const typedText = document.getElementById("typedText");

/* Ignore button runs */
ignoreBtn.addEventListener("mouseover", ()=>{
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    ignoreBtn.style.left = x + "px";
    ignoreBtn.style.top = y + "px";
});

ignoreBtn.addEventListener("click", ()=>{
    alert("Chundariiiii 💖");
});

/* Open button */
openBtn.addEventListener("click", ()=>{
    page1.style.opacity="0";
    setTimeout(()=>{
        page1.style.display="none";
        page2.style.opacity="1";
        page2.style.pointerEvents="auto";
        startTyping();
    },1000);
});

/* Typing effect */
const message = `Sometimes I don’t know how to explain it…

But nee ente life il vannappol entho change undayi.
Ninte chiriyum, ninte presence um… athokke enikku valare special aanu.
It’s not just liking… it’s something more peaceful and real.
Among everyone… nee thanne enikku heart-il oru special place und. 🫶✨`;

let i = 0;
function startTyping(){
    if(i < message.length){
        typedText.innerHTML += message.charAt(i) === "\n" ? "<br>" : message.charAt(i);
        i++;
        setTimeout(startTyping,40);
    }
}

/* Floating hearts */
setInterval(()=>{
    const heart = document.createElement("div");
    heart.className="heart";
    heart.innerHTML="❤️";
    heart.style.left=Math.random()*window.innerWidth+"px";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),6000);
},800);

/* Sparkling stars */
setInterval(()=>{
    const star = document.createElement("div");
    star.className="star";
    star.style.left=Math.random()*window.innerWidth+"px";
    star.style.top=Math.random()*window.innerHeight+"px";
    document.body.appendChild(star);
    setTimeout(()=>star.remove(),2000);
},300);
</script>

</body>
</html>
