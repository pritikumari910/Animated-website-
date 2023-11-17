﻿# Animated-website-
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Sidcup Family Golf</title>
    <link
      rel="shortcut icon"
      href="https://sidcupfamilygolf.com/wp-content/themes/puttosaurus/favicons/favicon-32x32.png"
      type="image/x-icon"
    />
    <link
      href="https://cdn.jsdelivr.net/npm/remixicon@3.4.0/fonts/remixicon.css"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="style.css" />
    <style>
      * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "montserrat";
    color: #fff;
  }
  
  html,
  body {
    height: 100%;
  
    width: 100%;
  }
  *::selection {
    background-color: #fff;
    color: #95c11e;
  }
  
  body::-webkit-scrollbar {
    display: block;
    width: 8px;
    background: #95c11e;
  }
  body::-webkit-scrollbar-thumb {
    background-color: #fff;
  
    border-radius: 50px;
  }
  body {
    overflow-x: hidden;
  }
  #cursor {
    height: 20px;
    width: 20px;
    background-color: #95c11e;
    border-radius: 50%;
    position: fixed;
    z-index: 99;
    transition: all linear 0.1s;
  }
  #cursor-blur {
    height: 500px;
    width: 500px;
    background-color: rgba(150, 193, 30, 0.3);
    border-radius: 50%;
    position: fixed;
    filter: blur(80px);
    z-index: 9;
    transition: all linear 0.4s;
  }
  #nav {
    height: 130px;
    width: 100%;
    /* background-color: red; */
    display: flex;
    align-items: center;
    padding: 0 120px;
    gap: 50px;
    position: fixed;
    justify-content: flex-start;
    z-index: 999;
  }
  #nav img {
    height: 4.5vw;
  }
  #nav h4 {
    text-transform: uppercase;
    font-weight: 500;
    cursor: pointer;
    font-size: 1.15vw;
  }
  video {
    height: 100%;
    width: 100%;
    object-fit: cover;
    z-index: -1;
    position: fixed;
  }
  
  #main {
    position: relative;
    background-color: rgba(0, 0, 0, 0.39);
  }
  
  #page1 {
    height: 100vh;
    width: 100%;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
    z-index: 10;
  }
  #page1 h1 {
    font-size: 7.5vw;
    font-weight: 900;
    position: relative;
  }
  #page1 h1::before {
    content: "EAT. DRINK. PLAY.";
    position: absolute;
    color: #000;
    top: -5px;
    left: -5px;
    -webkit-text-stroke: 1.5px #95c11e;
    z-index: -1;
  }
  #page1 h2 {
    font-size: 30px;
    font-weight: 800;
    margin-top: 10px;
    margin-bottom: 20px;
  }
  #page1 p {
    font-size: 1.2vw;
    font-weight: 500;
    width: 40%;
  }
  #page1 #arrow {
    height: 250px;
    width: 250px;
    background-color: transparent;
    border: 2px solid #95c11e;
    position: absolute;
    display: flex;
    left: -2%;
    bottom: 0%;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    transition: all ease 0.5s;
  }
  #page1 #arrow i {
    font-size: 50px;
    font-weight: 100;
  }
  #page1 #arrow:hover {
    scale: 0.4;
    background-color: #95c11e;
  }
  #page2 {
    min-height: 100vh;
    width: 100%;
    z-index: 10;
  }
  
  #scroller {
    /* background-color: red; */
    white-space: nowrap;
    overflow-x: auto;
    overflow-y: hidden;
    position: relative;
    z-index: 10;
  }
  #scroller::-webkit-scrollbar {
    display: none;
  }
  #scroller-in {
    display: inline-block;
    white-space: nowrap;
    animation-name: scroll;
    animation-duration: 40s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }
  
  #scroller h4 {
    display: inline-block;
    font-size: 120px;
    font-weight: 900;
    font-family: gilroy;
    margin-right: 20px;
    transition: all linear 0.3s;
    color: #000;
    -webkit-text-stroke: 2px #ffffff;
  }
  #scroller h4:hover {
    color: #95c11e;
    -webkit-text-stroke: 2px #95c11e;
  }
  
  @keyframes scroll {
    from {
      transform: translateX(0);
    }
    to {
      transform: translateX(-100%);
    }
  }
  
  #about-us {
    height: 40vh;
    width: 100%;
    /* background-color: red; */
    display: flex;
    padding: 0 50px;
    align-items: center;
    position: relative;
    z-index: 10;
    justify-content: space-around;
  }
  #about-us img {
    height: 220px;
    width: 220px;
    border-radius: 20px;
    object-fit: cover;
  }
  #about-us-in {
    width: 50%;
    text-align: center;
  }
  #about-us-in h3 {
    font-size: 54px;
    font-weight: 800;
    margin-bottom: 30px;
  }
  #about-us-in p {
    font-size: 20px;
    line-height: 26px;
  }
  
  #cards-container {
    /* background-color: red; */
    height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 70px;
    position: relative;
    z-index: 10;
  }
  .card {
    height: 80%;
    width: 24%;
    /* background-color: blue; */
    border-radius: 20px;
    background-size: cover;
    background-position: center;
    overflow: hidden;
    transition: all ease 0.6s;
  }
  #card1 {
    background-image: url(https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/home-toptracer-1024x682.jpg?strip=all&lossy=1&sharp=1&ssl=1);
  }
  #card2 {
    background-image: url(https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/hero-4-1024x1024.jpg?strip=all&lossy=1&sharp=1&ssl=1);
  }
  #card3 {
    background-image: url(https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/home-lessons-1024x682.jpg?strip=all&lossy=1&sharp=1&ssl=1);
  }
  .overlay {
    height: 100%;
    width: 100%;
    background-color: #95c11e;
    padding: 30px;
    padding-top: 160px;
    opacity: 0;
    transition: all ease 0.6s;
  }
  .overlay h4 {
    color: #000;
    font-size: 40px;
    text-transform: uppercase;
    white-space: nowrap;
    margin-bottom: 20px;
    font-weight: 800;
  }
  .overlay p {
    color: #000;
    font-size: 18px;
  }
  .card:hover .overlay {
    opacity: 1;
  }
  .card:hover {
    transform: rotate3d(-1, 1, 0, 20deg);
  }
  
  #green-div {
    height: 30vh;
    display: flex;
    align-items: center;
    justify-content: space-between;
    /* background-color: red; */
    background: linear-gradient(to left bottom, #119f3a, #ace022);
  }
  #green-div h4 {
    width: 45%;
    line-height: 50px;
    color: #000;
    text-align: center;
    font-weight: 800;
    font-size: 27px;
    text-transform: uppercase;
  }
  #green-div img {
    height: 100%;
    object-fit: cover;
    width: 14%;
  }
  
  #page3 {
    height: 100vh;
    width: 100%;
    background-color: #000;
    display: flex;
    align-items: center;
    position: relative;
    justify-content: center;
  }
  #page3 > p {
    font-size: 35px;
    font-weight: 700;
    width: 60%;
    line-height: 45px;
    text-align: center;
  }
  
  #page3 img {
    position: absolute;
    height: 60px;
  }
  #page3 #colon1 {
    left: 15%;
    top: 25%;
  }
  #page3 #colon2 {
    bottom: 30%;
    right: 15%;
  }
  #page4 {
    height: 30vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 70px;
    position: relative;
  }
  .elem {
    height: 70%;
    width: 26%;
    overflow: hidden;
    border-radius: 20px;
    position: relative;
  }
  
  .elem h2 {
    height: 100%;
    width: 100%;
    background-color: #95c11e;
    display: flex;
    color: #000;
    font-weight: 800;
    align-items: center;
    justify-content: center;
    transition: all ease 0.5s;
    font-size: 2vw;
    position: absolute;
    z-index: 10;
  }
  .elem img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    transition: all ease 0.5s;
    scale: 1.1;
  }
  .elem:hover h2 {
    color: #fff;
    background-color: transparent;
  }
  .elem:hover img {
    scale: 1;
  }
  #page4 h1 {
    font-size: 6.4vw;
    position: absolute;
    top: -15%;
    font-weight: 900;
    font-family: gilroy;
    color: #000;
    -webkit-text-stroke: 2px #fff;
  }
  #footer {
    height: 40vh;
    width: 100%;
    background: linear-gradient(to left bottom, #119f3a 0%, #a3d421 80%);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 6.5vw;
    padding: 0 100px;
  }
  #footer > img {
    position: absolute;
    left: 0;
    height: 100%;
    z-index: 0;
  }
  #f1 img {
    height: 100px;
  }
  #f1,
  #f2,
  #f3,
  #f4 {
    width: fit-content;
    position: relative;
    z-index: 99;
    /* background-color: red; */
  }
  #f2 h3 {
    font-size: 1.6vw;
    white-space: nowrap;
    text-transform: uppercase;
    color: #000;
    font-weight: 900;
    margin-bottom: 8px;
  }
  
  #f3 h3 {
    font-size: 1.6vw;
    white-space: nowrap;
    text-transform: uppercase;
    color: #000;
    font-weight: 800;
    margin-bottom: 8px;
  }
  #f4 h4 {
    font-size: 1vw;
    white-space: nowrap;
    text-transform: uppercase;
    color: #000;
    font-weight: 600;
    line-height: 20px;
    margin-bottom: 8px;
  }
    </style>
  </head>

  <body>
    <div id="nav">
      <img
        src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/logo-white.svg"
        alt=""
      />
      <h4>TOPTRACER RANGE</h4>
      <h4>Golf Lessons</h4>
      <h4>Adventure Golf</h4>
      <h4>coffee shop</h4>
      <h4>leagues</h4>
    </div>
    <div id="cursor"></div>
    <div id="cursor-blur"></div>

    <video
      autoplay
      loop
      muted
      src="https://sidcupfamilygolf.com/wp-content/uploads/2023/02/hero.mp4"
    ></video>
    <div id="main">
      <div id="page1">
        <h1>EAT. DRINK. PLAY.</h1>
        <h2>WELCOME TO SIDCUP FAMILY GOLF!</h2>
        <p>
          Sidcup Family Golf is a multipurpose golf facility located in Sidcup,
          South East London. Passionate about technology, player development and
          making golf fun and accessible to everyone.
        </p>
        <div id="arrow">
          <i class="ri-arrow-down-line"></i>
        </div>
      </div>
      <div id="page2">
        <div id="scroller">
          <div id="scroller-in">
            <h4>TOPTRACER RANGE</h4>
            <h4>GOLF LESSONS</h4>
            <h4>ADVENTURE GOLF</h4>
            <h4>COFFEE SHOP</h4>
            <h4>LEAGUES</h4>
          </div>
          <div id="scroller-in">
            <h4>TOPTRACER RANGE</h4>
            <h4>GOLF LESSONS</h4>
            <h4>ADVENTURE GOLF</h4>
            <h4>COFFEE SHOP</h4>
            <h4>LEAGUES</h4>
          </div>
        </div>
        <div id="about-us">
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/home-about-1-300x200.jpg?strip=all&lossy=1&sharp=1&ssl=1"
            alt=""
          />
          <div id="about-us-in">
            <h3>ABOUT US</h3>
            <p>
              Home to a 46-bay, multi-tier, floodlit driving range, powered by
              Toptracer Range technology. Complimented by a practice green and
              bunker, coffee shop and American Golf Store. There truly is
              something for everyone as we also boast two outdoor 18-hole
              dinosaur themed crazy golf courses.
            </p>
          </div>
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/home-about-2-300x200.jpg?strip=all&lossy=1&sharp=1&ssl=1"
            alt=""
          />
        </div>
        <div id="cards-container">
          <div class="card" id="card1">
            <div class="overlay">
              <h4>TopRacer Range</h4>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nulla
                quam molestias magni cupiditate architecto et enim quas facere
                ipsum tempora?
              </p>
            </div>
          </div>
          <div class="card" id="card2">
            <div class="overlay">
              <h4>Adventure Golf</h4>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nulla
                quam molestias magni cupiditate architecto et enim quas facere
                ipsum tempora?
              </p>
            </div>
          </div>
          <div class="card" id="card3">
            <div class="overlay">
              <h4>Golf Lessons</h4>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nulla
                quam molestias magni cupiditate architecto et enim quas facere
                ipsum tempora?
              </p>
            </div>
          </div>
        </div>
        <div id="green-div">
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/themes/puttosaurus/img/dots-side.svg"
            alt=""
          />
          <h4>
            SIGN UP FOR SIDCUP NEWS AND SPECIAL OFFERS STRAIGHT TO YOUR INBOX
          </h4>
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/themes/puttosaurus/img/dots-side.svg"
            alt=""
          />
        </div>
      </div>
      <div id="page3">
        <p>
          Excellent couple of hours, relax and enjoy in the fun. Staff were
          accommodating, friendly and very helpful. Café on site for
          refreshments etc. Will keep children enterntained during the holidays.
          Worth a visit if you haven’t been.
        </p>
        <img
          id="colon1"
          src="https://eiwgew27fhz.exactdn.com/wp-content/themes/puttosaurus/img/quote-left.svg"
          alt=""
        />
        <img
          id="colon2"
          src="https://eiwgew27fhz.exactdn.com/wp-content/themes/puttosaurus/img/quote-right.svg"
          alt=""
        />
      </div>
      <div id="page4">
        <h1>WHAT ARE YOU WAITING FOR?</h1>
        <div class="elem">
          <h2>TOPTRACER RANGE</h2>
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/page-toptracer-1024x683.jpg?strip=all&lossy=1&sharp=1&ssl=1"
            alt=""
          />
        </div>
        <div class="elem">
          <h2>TOPTRACER RANGE</h2>
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/page-lessons-1024x683.jpg?strip=all&lossy=1&sharp=1&ssl=1"
            alt=""
          />
        </div>
        <div class="elem">
          <h2>TOPTRACER RANGE</h2>
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/page-ag-1024x682.jpg?strip=all&lossy=1&sharp=1&ssl=1"
            alt=""
          />
        </div>
      </div>
      <div id="footer">
        <img
          src="https://eiwgew27fhz.exactdn.com/wp-content/themes/puttosaurus/img/dots-footer.svg"
          alt=""
        />
        <div id="f1">
          <img
            src="https://eiwgew27fhz.exactdn.com/wp-content/uploads/2023/02/logo-white.svg"
            alt=""
          />
        </div>
        <div id="f2">
          <h3>TOPTRACER Ranges</h3>
          <h3>Golf Lessons</h3>
          <h3>Adventure Golf</h3>
        </div>
        <div id="f3">
          <h3>coffee shop</h3>
          <h3>LEAGUES</h3>
          <h3>Contact us</h3>
        </div>
        <div id="f4">
          <h4>
            A20, SIDCUP BYPASS <br />
            CHISLEHURST <br />
            KENT <br />
            BR7 6RP <br />
            TEL: 0208 309 0181 <br />
            GET DIRECTIONS <br />
          </h4>
        </div>
      </div>
    </div>

    <script
      src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.1/gsap.min.js"
      integrity="sha512-qF6akR/fsZAB4Co1QDDnUXWnaQseLGXoniuSuSlPQK6+aWhlMZcHzkasCSlnWoe+TJuudlka1/IQ01Dnhgq95g=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    ></script>
    <script
      src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.1/ScrollTrigger.min.js"
      integrity="sha512-IHDCHrefnBT3vOCsvdkMvJF/MCPz/nBauQLzJkupa4Gn4tYg5a6VGyzIrjo6QAUy3We5HFOZUlkUpP0dkgE60A=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    ></script>
    <script src="script.js">
    var crsr = document.querySelector("#cursor");
var blur = document.querySelector("#cursor-blur");

document.addEventListener("mousemove", function (dets) {
  crsr.style.left = dets.x + "px";
  crsr.style.top = dets.y + "px";
  blur.style.left = dets.x - 250 + "px";
  blur.style.top = dets.y - 250 + "px";
});

var h4all = document.querySelectorAll("#nav h4");
h4all.forEach(function (elem) {
  elem.addEventListener("mouseenter", function () {
    crsr.style.scale = 3;
    crsr.style.border = "1px solid #fff";
    crsr.style.backgroundColor = "transparent";
  });
  elem.addEventListener("mouseleave", function () {
    crsr.style.scale = 1;
    crsr.style.border = "0px solid #95C11E";
    crsr.style.backgroundColor = "#95C11E";
  });
});

gsap.to("#nav", {
  backgroundColor: "#000",
  duration: 0.5,
  height: "110px",
  scrollTrigger: {
    trigger: "#nav",
    scroller: "body",
    // markers:true,
    start: "top -10%",
    end: "top -11%",
    scrub: 1,
  },
});

gsap.to("#main", {
  backgroundColor: "#000",
  scrollTrigger: {
    trigger: "#main",
    scroller: "body",
    // markers: true,
    start: "top -25%",
    end: "top -70%",
    scrub: 2,
  },
});

gsap.from("#about-us img,#about-us-in", {
  y: 90,
  opacity: 0,
  duration: 1,
  scrollTrigger: {
    trigger: "#about-us",
    scroller: "body",
    // markers:true,
    start: "top 70%",
    end: "top 65%",
    scrub: 1,
  },
});
gsap.from(".card", {
  scale: 0.8,
  // opacity:0,
  duration: 1,
  stagger: 0.1,
  scrollTrigger: {
    trigger: ".card",
    scroller: "body",
    // markers:false,
    start: "top 70%",
    end: "top 65%",
    scrub: 1,
  },
});
gsap.from("#colon1", {
  y: -70,
  x: -70,
  scrollTrigger: {
    trigger: "#colon1",
    scroller: "body",
    // markers:true,
    start: "top 55%",
    end: "top 45%",
    scrub: 4,
  },
});
gsap.from("#colon2", {
  y: 70,
  x: 70,
  scrollTrigger: {
    trigger: "#colon1",
    scroller: "body",
    // markers:true,
    start: "top 55%",
    end: "top 45%",
    scrub: 4,
  },
});
gsap.from("#page4 h1", {
  y: 50,
  scrollTrigger: {
    trigger: "#page4 h1",
    scroller: "body",
    // markers:true,
    start: "top 75%",
    end: "top 70%",
    scrub: 3,
  },
});

    </script>
  </body>
</html>
