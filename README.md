```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For My Babu ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    min-height:100vh;
    overflow:hidden;
    font-family:"Segoe UI",sans-serif;
    color:white;
    background:
        radial-gradient(circle at 20% 20%, #ff4d88 0%, transparent 30%),
        radial-gradient(circle at 80% 80%, #8b2be2 0%, transparent 30%),
        linear-gradient(135deg,#12001f,#2b0038,#12001f);
}

/* STARS */

.stars{
    position:fixed;
    inset:0;
    z-index:0;
    pointer-events:none;
}

.star{
    position:absolute;
    width:3px;
    height:3px;
    background:white;
    border-radius:50%;
    box-shadow:0 0 8px white;
    animation:twinkle 2s infinite alternate;
}

@keyframes twinkle{
    from{opacity:.2;transform:scale(.6)}
    to{opacity:1;transform:scale(1.4)}
}

/* PAGE */

.page{
    position:absolute;
    inset:0;

    display:flex;
    justify-content:center;
    align-items:center;

    padding:20px;

    opacity:0;
    visibility:hidden;
    transform:scale(1.15);

    transition:
        opacity .8s ease,
        transform .8s ease,
        visibility .8s;
}

.page.active{
    opacity:1;
    visibility:visible;
    transform:scale(1);
}

/* GLASS CARD */

.card{
    position:relative;
    z-index:5;

    width:min(92%,700px);
    max-height:90vh;
    overflow:auto;

    padding:45px 30px;

    text-align:center;

    background:rgba(255,255,255,.09);
    border:1px solid rgba(255,255,255,.2);

    backdrop-filter:blur(20px);
    -webkit-backdrop-filter:blur(20px);

    border-radius:35px;

    box-shadow:
        0 25px 80px rgba(0,0,0,.5),
        inset 0 0 30px rgba(255,255,255,.04);
}

/* GLOW */

.card:before{
    content:"";
    position:absolute;
    inset:-2px;
    border-radius:35px;
    background:linear-gradient(
        45deg,
        transparent,
        rgba(255,100,180,.5),
        transparent,
        rgba(180,80,255,.5),
        transparent
    );
    z-index:-1;
    filter:blur(12px);
}

/* TEXT */

.small{
    letter-spacing:4px;
    text-transform:uppercase;
    font-size:13px;
    opacity:.75;
}

h1{
    font-size:clamp(38px,8vw,65px);
    margin:15px 0;
    line-height:1.1;

    text-shadow:
        0 0 15px rgba(255,100,180,.8),
        0 0 35px rgba(255,50,150,.5);
}

h2{
    font-size:clamp(25px,5vw,38px);
    margin:15px 0;
}

p{
    font-size:18px;
    line-height:1.8;
    opacity:.92;
    margin:12px 0;
}

/* HEART */

.big-heart{
    font-size:85px;
    display:inline-block;

    filter:drop-shadow(0 0 20px #ff4d9d);

    animation:heartbeat 1.3s infinite;
}

@keyframes heartbeat{
    0%,100%{transform:scale(1)}
    50%{transform:scale(1.2)}
}

/* BUTTON */

button{
    margin-top:28px;
    padding:15px 32px;

    border:none;
    border-radius:50px;

    background:linear-gradient(90deg,#ff4f9a,#ff8ac5);

    color:white;

    font-size:17px;
    font-weight:bold;

    cursor:pointer;

    box-shadow:
        0 8px 25px rgba(255,50,150,.4);

    transition:.3s;
}

button:hover{
    transform:translateY(-4px) scale(1.05);
    box-shadow:
        0 12px 35px rgba(255,50,150,.65);
}

/* PAGE 1 */

.babu{
    color:#ff9dca;
}

/* PAGE 2 */

.typewriter{
    min-height:100px;
    font-size:24px;
    font-weight:500;
    color:#ffd1e5;
}

.cursor{
    animation:blink .7s infinite;
}

@keyframes blink{
    50%{opacity:0}
}

/* PAGE 3 GIFT */

.gift{
    width:150px;
    height:120px;

    margin:35px auto;

    position:relative;

    cursor:pointer;

    transition:.5s;
}

.gift:hover{
    transform:scale(1.08);
}

.gift-body{
    position:absolute;
    bottom:0;
    width:150px;
    height:95px;

    border-radius:8px;

    background:linear-gradient(135deg,#ff4d8d,#d91f65);

    box-shadow:0 15px 30px rgba(0,0,0,.4);
}

.gift-lid{
    position:absolute;
    top:5px;
    left:-8px;

    width:166px;
    height:35px;

    border-radius:8px;

    background:linear-gradient(135deg,#ff74aa,#e82d70);

    transition:.6s;
}

.ribbon{
    position:absolute;
    left:63px;
    top:0;

    width:25px;
    height:120px;

    background:#ffd45c;
}

.bow{
    position:absolute;
    top:-30px;
    left:38px;

    font-size:65px;

    z-index:5;
}

.gift.open .gift-lid{
    transform:translateY(-70px) rotate(-8deg);
}

/* CHOCOLATE */

.chocolate{
    display:none;

    margin:25px auto;

    animation:chocolateAppear 1s ease;
}

.chocolate.show{
    display:block;
}

.choco{
    width:240px;
    height:140px;

    margin:auto;

    border-radius:18px;

    background:
        linear-gradient(90deg,
        transparent 31%,
        rgba(255,255,255,.1) 32%,
        transparent 34%),
        linear-gradient(0deg,
        transparent 48%,
        rgba(255,255,255,.1) 49%,
        transparent 51%),
        #542817;

    border:8px solid #36150d;

    box-shadow:
        0 20px 40px rgba(0,0,0,.5),
        0 0 30px rgba(255,190,100,.2);

    display:flex;
    justify-content:center;
    align-items:center;

    font-size:65px;
}

@keyframes chocolateAppear{
    0%{
        transform:scale(0) rotate(-20deg);
        opacity:0;
    }
    70%{
        transform:scale(1.15) rotate(5deg);
    }
    100%{
        transform:scale(1) rotate(0);
        opacity:1;
    }
}

/* PROMISE */

.promise{
    margin-top:25px;
    padding:25px;

    border-radius:25px;

    background:rgba(255,255,255,.07);

    border:1px solid rgba(255,255,255,.12);
}

.promise-line{
    margin:15px 0;
}

.final{
    color:#ff9dca;
    font-size:27px;
    font-weight:bold;

    text-shadow:0 0 15px rgba(255,100,180,.8);
}

/* FLOATING HEARTS */

.heart{
    position:fixed;
    bottom:-50px;

    z-index:1;

    pointer-events:none;

    animation:floatHeart linear forwards;

    filter:drop-shadow(0 0 8px rgba(255,100,180,.8));
}

@keyframes floatHeart{
    0%{
        transform:translateY(0) rotate(0);
        opacity:0;
    }

    15%{
        opacity:1;
    }

    100%{
        transform:translateY(-110vh) rotate(360deg);
        opacity:0;
    }
}

/* MOBILE */

@media(max-width:600px){

    .card{
        padding:35px 20px;
    }

    p{
        font-size:16px;
    }

    .typewriter{
        font-size:20px;
    }

    .gift{
        transform:scale(.85);
    }
}
</style>
</head>

<body>

<!-- STARS -->
<div class="stars" id="stars"></div>


<!-- ================= PAGE 1 ================= -->

<section class="page active" id="page1">

<div class="card">

    <div class="small">
        A little surprise for you ✨
    </div>

    <div class="big-heart">
        ❤️
    </div>

    <h1>
        Happy Girlfriend Day
    </h1>

    <h2 class="babu">
        My Babu 🥹💕
    </h2>

    <p>
        Today is Girlfriend Day...
    </p>

    <p>
        But for me, every day feels special
        because <strong>you are in my life.</strong>
    </p>

    <button onclick="nextPage(2)">
        Open My Heart 💌
    </button>

</div>

</section>


<!-- ================= PAGE 2 ================= -->

<section class="page" id="page2">

<div class="card">

    <div class="big-heart">
        💗
    </div>

    <div class="small">
        Something I want you to know...
    </div>

    <h2>
        I Will Always Be Yours
    </h2>

    <div class="typewriter">
        <span id="typing"></span>
        <span class="cursor">|</span>
    </div>

    <button onclick="nextPage(3)">
        There Is Something For You 🎁
    </button>

</div>

</section>


<!-- ================= PAGE 3 ================= -->

<section class="page" id="page3">

<div class="card">

    <div class="small">
        A sweet surprise 🍫
    </div>

    <h2>
        I Got You A Little Gift
    </h2>

    <p>
        But first...
        you have to open it. 👀
    </p>

    <div class="gift" id="gift" onclick="openGift()">

        <div class="bow">
            🎀
        </div>

        <div class="gift-lid"></div>

        <div class="gift-body">
            <div class="ribbon"></div>
        </div>

    </div>

    <div class="chocolate" id="chocolate">

        <div class="choco">
            🍫
        </div>

        <h2>
            Chocolate for the Beautiful Girl ❤️
        </h2>

        <p>
            Because someone as sweet and beautiful
            as you deserves something sweet. 🥰
        </p>

        <button onclick="nextPage(4)">
            One Last Surprise 💍
        </button>

    </div>

</div>

</section>


<!-- ================= PAGE 4 ================= -->

<section class="page" id="page4">

<div class="card">

    <div class="big-heart">
        💍
    </div>

    <div class="small">
        My heart's promise
    </div>

    <h1>
        My Promise To You
    </h1>

    <div class="promise">

        <p class="promise-line">
            ❤️ I promise to stand beside you
            through your good days and your difficult days.
        </p>

        <p class="promise-line">
            ❤️ I promise to listen to you,
            respect you and support your dreams.
        </p>

        <p class="promise-line">
            ❤️ I promise to keep choosing you,
            even when life isn't perfect.
        </p>

        <p class="promise-line">
            ❤️ I promise to make you smile
            whenever I can.
        </p>

        <p class="promise-line">
            ❤️ I promise that I'll keep trying
            to make our journey beautiful.
        </p>

        <p class="final">
            As long as you want me by your side,
            I will choose you...
            again and again. ❤️
        </p>

    </div>

    <p>
        Years may pass,
        everything around us may change...
    </p>

    <p>
        But I hope that one day,
        after many years,
        we still look at each other
        with the same love we have today.
    </p>

    <h2 class="babu">
        Happy Girlfriend Day, Babu ❤️
    </h2>

    <p>
        Forever yours. 🫶
    </p>

</div>

</section>


<script>

/* ================= STARS ================= */

const stars = document.getElementById("stars");

for(let i=0;i<100;i++){

    const star=document.createElement("div");

    star.className="star";

    star.style.left=Math.random()*100+"%";
    star.style.top=Math.random()*100+"%";

    star.style.animationDelay=
        Math.random()*3+"s";

    stars.appendChild(star);
}


/* ================= PAGE CHANGE ================= */

function nextPage(number){

    document.querySelectorAll(".page")
    .forEach(page=>{
        page.classList.remove("active");
    });

    document
        .getElementById("page"+number)
        .classList.add("active");

    if(number===2){
        startTyping();
    }

    createBurst();
}


/* ================= TYPING ================= */

let typingStarted=false;

function startTyping(){

    if(typingStarted) return;

    typingStarted=true;

    const text=
        "No matter how many days pass, no matter how many years go by... my heart will always find its way back to you. I will always be yours, Babu. ❤️";

    const element=
        document.getElementById("typing");

    let i=0;

    function type(){

        if(i<text.length){

            element.textContent+=text.charAt(i);

            i++;

            setTimeout(type,45);

        }

    }

    type();
}


/* ================= GIFT ================= */

function openGift(){

    const gift=
        document.getElementById("gift");

    const chocolate=
        document.getElementById("chocolate");

    gift.classList.add("open");

    setTimeout(()=>{

        gift.style.display="none";

        chocolate.classList.add("show");

    },700);

}


/* ================= FLOATING HEARTS ================= */

function createHeart(){

    const heart=
        document.createElement("div");

    heart.className="heart";

    const hearts=[
        "❤️",
        "💖",
        "💕",
        "💗",
        "💓",
        "💘",
        "💞",
        "✨"
    ];

    heart.innerHTML=
        hearts[Math.floor(Math.random()*hearts.length)];

    heart.style.left=
        Math.random()*100+"vw";

    heart.style.fontSize=
        (15+Math.random()*30)+"px";

    heart.style.animationDuration=
        (5+Math.random()*6)+"s";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },11000);
}

setInterval(createHeart,450);


/* ================= HEART BURST ================= */

function createBurst(){

    for(let i=0;i<15;i++){

        setTimeout(()=>{

            const heart=
                document.createElement("div");

            heart.className="heart";

            heart.innerHTML="💖";

            heart.style.left=
                (40+Math.random()*20)+"vw";

            heart.style.bottom="45%";

            heart.style.fontSize=
                "25px";

            heart.style.animationDuration=
                "2s";

            document.body.appendChild(heart);

            setTimeout(()=>{
                heart.remove();
            },2500);

        },i*70);
    }
}

</script>

</body>
</html>
```
