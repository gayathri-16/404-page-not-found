<template>
  <div id="container">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Lekton:wght@700&family=Press+Start+2P&family=Space+Mono&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Space+Mono&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
    <header>
    <div class="title">
      <h3> 404 NOT FOUND </h3>
    </div>
   </header>
  <section><span></span></section>
   <div class="face">
     <div class="eyes">
       <div class="eye"></div>
         <div class="eye"></div>
      </div>
   </div>
    
  <div class="info">
    <h1> I have bad news <br> <br> for you </h1>
    <p>The page you are looking <br> for might be removed or is <br> temporarily unavailable</p>
     <button class="bth">BACK  TO   HOMEPAGE</button>
  </div>

<h2>Gayathri @ DevChallenges.io</h2>
  </div>
</template>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
  
<script>

  document.querySelector('body').addEventListener('mousemove',eyeball);
  function eyeball(){
    var eye =document.querySelectorAll('.eye');
    eye.forEach(function(eye){
      let x = (eye.getBoundingClientRect().left) + (eye.clientWidth / 2);
      let y = (eye.getBoundingClientRect().top) + (eye.clientHeight / 2);
      let radian = Math.atan2(event.pageX-x, event.pageY-y);
      let rot = (radian * (180 / Math.PI) * -1) + 270;
      eye.style.transform = "rotate("+ rot + "deg)";
    })
  }
  
function createBubble(){
  const section = document.querySelector('section')
  const createElement = document.createElement('span')
  var size = Math.random()*60;

  createElement.style.width = 20 + size + 'px';
   createElement.style.height = 20 + size + 'px';
    createElement.style.left = Math.random() * innerWidth + "px";
    section.appendChild(createElement);

    setTimeout(()=>{
      createElement.remove()
    },4000)

}
setInterval(createBubble,50)

</script>

<style>
#container{
  margin:auto;
  padding: auto;
  display: flex;
  width:100%;
  height:100vh;
 background:linear-gradient(to left,#db6d92, #f15448);
  overflow: hidden;
   box-sizing:border-box;
}
.title{
  padding:10px 0px 0px 10px;
}
.title h3{
  font-family:arial;
  font-size:17px;
  letter-spacing: 0ch;
}
.face{
  position:relative;
  width:300px;
  height:300px;
  border-radius:50%;
  background:#ffcd00;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top:10rem;
  margin-left:6rem;
 }
.face::before{
  content:'';
  position:absolute;
  top:210px;
  width:150px;
  height: 20px;
  background:#b57700;
  border-bottom-left-radius: 0px;
  border-bottom-right-radius: 0px;
  }
  .eyes{
    position:relative;
    top:-40px;
    display:flex;
  }
  .eyes .eye{
    position: relative;
    width:80px;
    height:80px;
    display:block;
    margin:0 15px;
    background:#fff;
    border-radius: 50%;

  }
  .eyes .eye::before{
    content: '';
    position: absolute;
    top:50%;
    left:25px;
    transform:translate(-50%,-50%);
    width:40px;
    height:40px;
    background: #333;
    border-radius:50%;

  }
.info{
  margin-top:10rem;
  margin-left:15rem;
  }
  .info h1{
    font-family: 'Press Start 2p', cursive;
    font-size:35px;
    color:rgb(44, 43, 43)
  }
  .info p{
    padding-top:3rem;
    font-size:20px;
    font-family: 'Space Mono', monospace;
    color:rgb(230, 223, 223);
  }
  .info .bth{
    width:160px;
    height:50px;
    margin-top:2rem;
    border:none;
    background:rgb(24, 24, 24);
    color:rgb(212, 212, 212);
    font-size:12px;
    font-family: 'Lekton', sans-serif;
  }
  h2{
    margin-top:44rem;
    margin-left:-43rem;
  }
  footer{
    margin-top:45rem;
    margin-left:-40rem;
  }
 section span:before{
   content:'';
   position:absolute;
   width:100%;
   height:100%;
   transform: scale(0.25)translate(-70%,-70%);
   background: radial-gradient(#fff,transparent);
   border-radius:50%;
 }
  section span{
   
    position:absolute;
    bottom:-10px;
    background:transparent;
    border-radius:50%;
    pointer-events: none;
    box-shadow: inset 0 0 10px rgba(255,255,255,0.5);
    animation: animate 4s linear infinite;
  }
  @keyframes animate
  { 0%{
    transform: translateY(0%);
    opacity:1;
  }
  99%{
    opacity:1;
  }
  100%{
    transform: translateY(-1200%);
    opacity:0;
  }

  }
  @media only screen and (max-width:600px) {
  #container{
    margin:auto;
    padding: auto;
  width:100%;
  height:100vh;
 }
.title{
  padding:0px;
}
.title h3{
  font-family:arial;
  font-size:1em;
  letter-spacing: 0ch;
}
.face{
  position:relative;
  width:180px;
  height:180px;
  border-radius:50%;
  margin-top:5rem;
  margin-left:1.5rem;
 }
.face::before{
  content:'';
  position:absolute;
  top:120px;
  width:60px;
  height: 10px;
 
  }
  .eyes{
    position:relative;
    top:-30px;
    display:flex;
  }
  .eyes .eye{
    position: relative;
    width:45px;
    height:45px;
    display:block;
    margin:0 18px;
    
  }
  .eyes .eye::before{
    content: '';
    position: absolute;
    top:50%;
    left:15px;
    transform:translate(-50%,-50%);
    width:25px;
    height:25px;
    background: #333;
    border-radius:50%;

  }
.info{
  margin-top:18rem;
  margin-left:-18em;
  }
  .info h1{
    font-family: 'Press Start 2p', cursive;
    font-size:25px;
    margin-top:3rem;
   
  }
  .info p{
    padding-top:2rem;
    font-size:15px;
   
  }
  .info .bth{
    width:150px;
    height:40px;
    margin-top:1rem;
    font-size:14px;
    
  }
  h2{
    font-size:14px;
    margin-top:43rem;
    margin-left:-18rem;
  }
 section span:before{
   content:'';
   position:absolute;
   width:100%;
   height:100%;
   transform: scale(0.25)translate(-70%,-70%);
   background: radial-gradient(#fff,transparent);
   border-radius:50%;
 }
 
  }
</style>




