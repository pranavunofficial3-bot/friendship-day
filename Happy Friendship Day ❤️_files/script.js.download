/*====================================================
        FRIENDSHIP DAY WEBSITE - script.js
=====================================================*/

// ===============================
// LOADER
// ===============================

window.addEventListener("load", () => {

    setTimeout(() => {
        const loader = document.getElementById("loader");
        if(loader){
            loader.style.opacity = "0";
            loader.style.visibility = "hidden";
        }
    },2000);

});

// ===============================
// MUSIC
// ===============================

// ===============================
// MUSIC
// ===============================

const music = document.getElementById("bgMusic");
const musicBtn = document.getElementById("musicBtn");

function playMusic(){

    if(!music) return;

    if(music.paused){

        music.play();

        if(musicBtn){
            musicBtn.innerHTML='<i class="fa-solid fa-pause"></i>';
            musicBtn.classList.add("playing");
        }

    }else{

        music.pause();

        if(musicBtn){
            musicBtn.innerHTML='<i class="fa-solid fa-music"></i>';
            musicBtn.classList.remove("playing");
        }

    }

}

if(musicBtn){
    musicBtn.addEventListener("click",playMusic);
}

document.addEventListener("click",function(){

    if(music && music.paused){

        music.play().catch(()=>{});

        if(musicBtn){
            musicBtn.classList.add("playing");
            musicBtn.innerHTML='<i class="fa-solid fa-pause"></i>';
        }

    }

},{once:true});

// ===============================
// FRIENDSHIP DAY COUNTER
// ===============================

// Change this date if needed
const friendshipStart = new Date("2019-04-08");

const daysElement = document.getElementById("days");

function updateCounter(){

    if(!daysElement) return;

    const today = new Date();

    const diff = today - friendshipStart;

    const days = Math.floor(diff/(1000*60*60*24));

    daysElement.innerHTML = days;

}

updateCounter();

// ===============================
// QUOTES SLIDER
// ===============================

const quotes=[

"True friendship is one soul in two bodies. ❤️",

"A best friend makes every day brighter. 🌸",

"Friends are the family we choose. 💖",

"Life is beautiful because of friends like you. 😊",

"Distance never separates true friends. 🌍",

"Thank you for being an amazing friend. ❤️",

"Every memory with you is priceless. ✨",

"Happy Friendship Day Pragya! 🌸"

];

let quoteIndex=0;

const quoteText=document.getElementById("quoteText");

function changeQuote(){

    if(!quoteText) return;

    quoteIndex++;

    if(quoteIndex>=quotes.length){

        quoteIndex=0;

    }

    quoteText.style.opacity="0";

    setTimeout(()=>{

        quoteText.innerHTML=quotes[quoteIndex];

        quoteText.style.opacity="1";

    },400);

}

setInterval(changeQuote,3500);

// ===============================
// SURPRISE POPUP
// ===============================

const popup=document.getElementById("popup");
const surpriseBtn=document.getElementById("surpriseBtn");
const closePopup=document.getElementById("closePopup");

if(surpriseBtn){

    surpriseBtn.addEventListener("click",()=>{

        popup.style.display="flex";

    });

}

if(closePopup){

    closePopup.addEventListener("click",()=>{

        popup.style.display="none";

    });

}

window.onclick=function(e){

    if(e.target==popup){

        popup.style.display="none";

    }

}

// ===============================
// SMOOTH SCROLL
// ===============================

document.querySelectorAll('a[href^="#"]').forEach(anchor=>{

    anchor.addEventListener("click",function(e){

        e.preventDefault();

        document.querySelector(this.getAttribute("href"))
        .scrollIntoView({

            behavior:"smooth"

        });

    });

});

// ===============================
// SCROLL ANIMATION
// ===============================

const observer=new IntersectionObserver(entries=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.style.opacity="1";
entry.target.style.transform="translateY(0px)";

}

});

});

document.querySelectorAll(".friend-card,.favorite-card,.timeline-content,.reason-card,.polaroid").forEach(el=>{

el.style.opacity="0";
el.style.transform="translateY(40px)";
el.style.transition=".7s";

observer.observe(el);

});

// ===============================
// FLOATING HEARTS
// ===============================

function createHeart(){

const heart=document.createElement("div");

heart.innerHTML="💖";

heart.style.position="fixed";
heart.style.left=Math.random()*100+"vw";
heart.style.bottom="-40px";
heart.style.fontSize=(20+Math.random()*20)+"px";
heart.style.pointerEvents="none";
heart.style.zIndex="999";

document.body.appendChild(heart);

let pos=0;

const timer=setInterval(()=>{

pos+=3;

heart.style.bottom=pos+"px";

heart.style.opacity=1-pos/350;

heart.style.transform=`translateX(${Math.sin(pos/25)*20}px)`;

if(pos>900){

clearInterval(timer);

heart.remove();

}

},25);

}

setInterval(createHeart,1500);

// ===============================
// CONFETTI
// ===============================

const celebrateBtn=document.getElementById("confettiBtn");

if(celebrateBtn){

celebrateBtn.addEventListener("click",()=>{

for(let i=0;i<150;i++){

const conf=document.createElement("div");

conf.style.position="fixed";
conf.style.width="10px";
conf.style.height="10px";
conf.style.background=`hsl(${Math.random()*360},100%,60%)`;

conf.style.left=Math.random()*100+"vw";
conf.style.top="-20px";

conf.style.zIndex="9999";

conf.style.borderRadius="50%";

document.body.appendChild(conf);

let y=-20;

const speed=2+Math.random()*5;

const rotate=Math.random()*360;

const t=setInterval(()=>{

y+=speed;

conf.style.top=y+"px";

conf.style.transform=`rotate(${rotate+y}deg)`;

if(y>window.innerHeight+20){

clearInterval(t);

conf.remove();

}

},15);

}

});

}

// ===============================
// PHOTO CLICK EFFECT
// ===============================

document.querySelectorAll(".photo img").forEach(img=>{

img.addEventListener("click",()=>{

img.style.transform="scale(1.15)";

setTimeout(()=>{

img.style.transform="scale(1)";

},500);

});

});

// ===============================
// GREETING
// ===============================

setTimeout(()=>{

console.log("❤️ Happy Friendship Day Pragya ❤️");

},1000);