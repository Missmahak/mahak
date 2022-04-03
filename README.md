<div class="space"></div>
<div class="earth" id="cb"></div>
<div class="ball" id="ball"></div>

<button id="ufo" onclick="releaseBall();">
  <span class="capsule"></span>
  <span class="capsule"></span>
</button>

<div class="cbs">
  <button id="sun" onclick="goCelestialBody(id);">sun</button>
  <button id="mercury" onclick="goCelestialBody(id)">mercury</button>
  <button id="venus" onclick="goCelestialBody(id)">venus</button>
  <button id="earth" onclick="goCelestialBody(id)" class="info">earth</button>
  <button id="moon" onclick="goCelestialBody(id)">moon</button>
  <button id="mars" onclick="goCelestialBody(id)">mars</button>
  <button id="jupiter" onclick="goCelestialBody(id)">jupiter</button>
  <button id="saturn" onclick="goCelestialBody(id)">saturn</button>
  <button id="uranus" onclick="goCelestialBody(id)">uranus</button>
  <button id="neptune" onclick="goCelestialBody(id)">neptune</button>
  <button id="pluto" onclick="goCelestialBody(id)">pluto</button>
</div>
@import url('https://fonts.googleapis.com/css2?family=Cute+Font&display=swap');

:root {
  --clr: #ffc107a8;
}

body {
  display: flex;
  align-items: start;
  justify-content: center;
  min-height: 100vh;
  overflow: hidden;
  margin: 0;
  padding: 0;
  font-family: 'Cute Font', Arial, Helvetica, serif;
}

.space {
  position: absolute;
  z-index: -2;
  width: 100vw;
  height: 100vh;
  background: #080808;
	overflow: hidden;  
  background-image: 
    radial-gradient(2px 2px at 20px 30px, #fff, #fff0),
    radial-gradient(1px 1px at 43px 75px, #fff, #fff0),
    radial-gradient(2px 1px at 54px 184px, #fff, #fff0),
    radial-gradient(2px 2px at 93px 47px, #e6e6e6, #fff0),
    radial-gradient(1px 1px at 148px 87px, #e8e8e8, #fff0),
    radial-gradient(1px 2px at 193px 137px, #fff, #fff0),
    radial-gradient(1px 1px at 210px 154px, #f5f5f5, #fff0),
    radial-gradient(2px 1px at 243px 102px, #e2e2e2, #fff0),
    radial-gradient(2px 1px at 264px 184px, #fff, #fff0),
    radial-gradient(2px 2px at 293px 44px, #efefef, #fff0),
    radial-gradient(1px 1px at 223px 62px, #ececec, #fff0),
    radial-gradient(1px 2px at 249px 162px, #fff, #fff0),
    radial-gradient(1px 1px at 73px 99px, #eaeaea, #fff0),
    radial-gradient(1px 2px at 163px 42px, #efefef, #fff0),
        linear-gradient(180deg, #fff0 5%, #000 15%, #020202 35%, #20005840 85%, #000 100%);
		background-repeat: repeat;
		background-size: 
      333px 263px, 333px 293px, 333px 363px, 333px 463px,	433px 193px, 
      333px 203px, 633px 223px, 333px 263px, 333px 285px, 333px 179px,	
      333px 163px, 333px 363px, 533px 163px, 333px 213px, 100% 100%;
}

#cb {
   background: var(--surface);
   width: 300vh;
   height: 100vh;
   position: absolute;
   z-index: -1;
   border-radius: 100%;
   top: 80vh;
   background-size: calc(72%);
   background-repeat: repeat;
   background-position: center bottom;
   box-shadow: 0 0 5vh 0 var(--atmosphere);
}

#cb:before {
  content: "";
  position: absolute;
  width: 100%;
  text-align: center;
  font-size: 15vh;
  top: 2vh;
  color: #000b;
  text-shadow: 1px 1px 1px #fff8, 0px 0px 1px #0008;
  text-transform: uppercase;
}

#cb.sun {
  --surface: url(https://josetxu.com/demos/img/ss-sun.jpg);
  --atmosphere: #fc0;
}

#cb.mercury {
  --surface: url(https://josetxu.com/demos/img/ss-mercury.jpg);
  --atmosphere: #d9cbcb;
}

#cb.venus {
  --surface: url(https://josetxu.com/demos/img/ss-venus.jpg);
 --atmosphere: #ff9800;
}

#cb.earth {
  --surface: url(https://josetxu.com/demos/img/ss-earth.jpg);
  --atmosphere: #00bcd4;
}

#cb.moon {
  --surface: url(https://josetxu.com/demos/img/ss-moon.jpg);
	--atmosphere: #fdfdfd;
} 

#cb.mars {
  --surface: url('https://josetxu.com/demos/img/ss-mars.jpg');
	--atmosphere: #ff5722;
} 

#cb.jupiter {
  --surface: url('https://josetxu.com/demos/img/ss-jupiter.jpg');
	--atmosphere: #8f59d3;
} 

#cb.saturn {
  --surface: url('https://josetxu.com/demos/img/ss-saturn.jpg');
	--atmosphere: #93eaf5;
} 

#cb.uranus {
  --surface: url('https://josetxu.com/demos/img/ss-uranus.jpg');
	--atmosphere: #93eaf5;
} 

#cb.neptune {
  --surface: url('https://josetxu.com/demos/img/ss-neptune.jpg');
	--atmosphere: #2b1ddb;
} 

#cb.pluto {
  --surface: url('https://josetxu.com/demos/img/ss-pluto.jpg');
	--atmosphere: #93eaf5;
} 


#cb.sun:before {
    content: "sun";
}

#cb.mercury:before {
    content: "mercury";
}

#cb.venus:before {
    content: "venus";
}

#cb.earth:before {
    content: "earth";
}

#cb.moon:before {
    content: "moon";
}

#cb.mars:before {
    content: "mars";
}

#cb.jupiter:before {
    content: "jupiter";
}

#cb.saturn:before {
    content: "saturn";
}

#cb.uranus:before {
    content: "uranus";
}

#cb.neptune:before {
    content: "neptune";
}

#cb.pluto:before {
    content: "pluto";
}

.ball {
  width: 10vh;
  height: 10vh;
  border-radius: 100%;
  z-index: 0;
  position: relative;
  top: 3.5vh;
  background: radial-gradient(circle at 65% 15%, #e7e7e7 1% , #00ffff 3%, #1616a1 60%, #09113e 100%);
  background: radial-gradient(circle at 65% 15%, #e7e7e7 5%, #bbbbbb 25%, #686868 60%, #000000 100%);
}

#ufo {
  height: 8vh;
  width: 20vh;
  font-size: 2vh;
  position: absolute;
  z-index: 1;
  cursor: pointer;
  border: 0;
  background: #fff0;
  color: #fff;
  top: 2vh;
  border-radius: 100%;
}

.capsule {
  width: 11vh;
  height: 11vh;
  background: #00bcd463;
  position: absolute;
  top: 1vh;
  left: calc(50% - 5.5vh);
  z-index: -1;
  margin: 0 auto;
  border-radius: 100%;
  background-color: rgb(255 255 255 / 0.15);
  box-shadow: 0px 10px 30px 5px #fff inset;
  clip-path: polygon(0 0, 100% 0, 100% 50%, 0 50%);
  transition: all 1s ease 0s;
}

.capsule + .capsule {
  clip-path: polygon(0 50%, 100% 50%, 100% 100%, 0 100%);
  transform-origin: center center;
}

#ufo.open .capsule + .capsule {
  transform: rotate(180deg);
  transition: all 0.5s ease 0s;
}

.cbs {
  position: absolute;
  left: 0;
  top: 0;
  background: #fff0;
  padding: 8vh 2vh 2vh 2vh;
  width: 10vh;
  height: 100vh;
}

.cbs button {
  background: #0008;
  display: block;
  color: var(--clr);
  font-size: 2.5vh;
  width: 10vh;
  height: 5vh;
  border: 0.25vmin solid var(--clr);
  cursor: pointer;
  text-transform: uppercase;
  margin-bottom: 1.85vh;  
  font-family: 'Cute Font', Arial, Helvetica, serif;
  position: relative;
}

.cbs button.info {
  background: var(--clr);
  color: #000;
  box-shadow: 0 0 1vh 0 #ffc107, 0 0 1vh 0 #ffc107;
  text-shadow: 0 0 0.25vh #fff, 0 0 0.125vh #fff;
  font-weight: bold;
}

.cbs button:hover {
  background: var(--clr);
  color: #000;
}

.cbs button:before {
    left: -200%;
    content: "2";
    top: 0;
    padding: 0.5vh 1vh 0.5vh 0.5vh;
    width: 8vh;
    height: 3.5vh;
    line-height: 1.25vh;
    color: #000;
    font-size: 1.25vh;
    text-transform: lowercase;
    position: absolute;
    transition: all 0.4s ease 0s;
    text-align: right;
    z-index: 2;
}

.cbs button:after {
  left: -200%;
  content: "";
  top: 0;
  padding: 0.5vh 1vh 0.5vh 0.5vh;
  width: 8vh;
  height: 3.5vh;
  white-space: pre-wrap;
  line-height: 1.75vh;
  background: var(--clr);
  color: #000;
  font-size: 2vh;
  text-transform: lowercase;
  position: absolute;
  transition: all 0.4s ease 0s;
  text-align: right;
  border-radius: 0 0.25vh 0.25vh 0;
}

.cbs button.info:before, .cbs button.info:after {
  left: calc(100% + 0.25vh);
  transition: all 0.4s ease 0s;
}


#sun:after {
  content: "274.5 m/s \A ( 28.02 g )";
}

#mercury:after {
  content: "3.7 m/s \A ( 0.377 g )";
}

#venus:after {
  content: "8.87 m/s \A ( 0.904 g )";
}

#earth:after {
  content: "9.8 m/s \A ( 1 g )";
}

#moon:after {
  content: "1.625 m/s \A ( 0.166 g )";
}
const dropball = gsap.timeline({ paused: false, delay: 1 });

dropball.to(".ball", {
  duration: 2, 
  ease: CustomEase.create("custom", "M0,0 C0.023,0 0.152,0.473 0.176,0.561 0.222,0.728 0.269,0.963 0.278,1 0.287,0.985 0.337,0.873 0.383,0.811 0.445,0.726 0.516,0.753 0.531,0.762 0.617,0.812 0.652,0.983 0.66,1 0.73,0.916 0.811,0.997 0.812,0.998 0.824,0.994 0.833,0.986 0.85,0.986 0.857,0.986 0.915,1 0.915,1 0.915,1 1,1 1,1 "),
  y: window.innerHeight - (window.innerHeight / 3)
})

function elem(id){
  var element = document.getElementById(id);
  return element;
}

function releaseBall() {
  dropball.restart();
}

function goCelestialBody(id) {
  elem('cb').removeAttribute('class');
  elem('cb').classList.add(id);
  var vel;
  switch (id) {
    case     'sun': vel = 0.06; break;
    case 'mercury': vel = 5.40; break;
    case   'venus': vel = 2.25; break;
    case   'earth': vel = 2.00; break;
    case    'moon': vel = 12.3; break;
    case    'mars': vel = 5.36; break;
    case 'jupiter': vel = 0.80; break;
    case  'saturn': vel = 1.95; break;
    case  'uranus': vel = 2.30; break;
    case 'neptune': vel = 1.79; break;
    case   'pluto': vel = 32.2; break;
        deafault: vel = 1;
  }
  dropball.duration(vel).restart();
  
  elem('ufo').classList.add('open');
  setTimeout(function(){elem('ufo').classList.remove('open');}, 500);
  
  var btns = document.querySelectorAll('.cbs button')
  
  for(var i = 0; i<btns.length; i++){
    btns[i].classList.remove('info');
  }
  
  elem(id).classList.add('info');
  console.log(id);
}

elem('ufo').addEventListener("mouseup", function(){
	elem('ufo').classList.add('open');
  setTimeout(function(){elem('ufo').classList.remove('open');}, 500);
});

elem('earth').click();
#mars:after {
  content: "3.72 m/s \A ( 0.379 g )";
}

#jupiter:after {
  content: "24.79 m/s \A ( 2.528 g )";
}

#saturn:after {
  content: "10.44 m/s \A ( 1.065 g )";
}

#uranus:after {
  content: "8.69 m/s \A ( 0.886 g )";
}

#neptune:after {
  content: "11.15 m/s \A ( 1.14 g )";
}

#pluto:after {
  content: "0.620 m/s \A ( 0.063 g )";
}
