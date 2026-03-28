<!DOCTYPE html>
<html>
<head>
  <title>For Bubu ❤️</title>

  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Quicksand', sans-serif;
      text-align: center;
      overflow-x: hidden;
    }

    section {
      height: 100vh;
      display: none;
      padding: 40px;
      color: #4a2c2a;
      position: relative;
    }

    .active {
      display: block;
    }

    /* Background overlay for readability */
    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(255, 245, 247, 0.7);
      backdrop-filter: blur(4px);
      z-index: 0;
    }

    .content {
      position: relative;
      z-index: 1;
    }

    p {
      max-width: 700px;
      margin: auto;
      font-size: 20px;
      margin-top: 120px;
      line-height: 1.6;
    }

    button {
      margin-top: 40px;
      padding: 14px 28px;
      border-radius: 30px;
      border: none;
      background: #ff9aa2;
      color: white;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      transform: scale(1.08);
      background: #ff7f8a;
    }

    /* Different backgrounds for each section */
    #s1 { background: url('https://i.pinimg.com/originals/ff/9c/8c/ff9c8c6c4a7c0d8d8e6e2e0d2f6a6c4e.jpg') center/cover no-repeat; }
    #s2 { background: url('https://i.pinimg.com/originals/0c/fb/4e/0cfb4e92f3f2d8e2f4b2b2d6d9c2c2c7.jpg') center/cover no-repeat; }
    #s3 { background: url('https://i.pinimg.com/originals/3d/8c/f5/3d8cf5c7c7f3f4f2d6e2d8f3e2d2c2c3.jpg') center/cover no-repeat; }
    #s4 { background: url('https://i.pinimg.com/originals/9f/4c/6b/9f4c6b6c7f3d8e2f4d2c2c2d2f2e2e2e.jpg') center/cover no-repeat; }
    #s5 { background: url('https://i.pinimg.com/originals/5c/2f/8e/5c2f8e8e8c7f2d8e2f4f2d2c2c2e2d2c.jpg') center/cover no-repeat; }

  </style>
</head>

<body>

<section id="s1" class="active">
  <div class="overlay"></div>
  <div class="content">
    <p id="p1"></p>
    <button onclick="next(2)">Tap here ❤️</button>
  </div>
</section>

<section id="s2">
  <div class="overlay"></div>
  <div class="content">
    <p id="p2"></p>
    <button onclick="next(3)">Next 🧸</button>
  </div>
</section>

<section id="s3">
  <div class="overlay"></div>
  <div class="content">
    <p id="p3"></p>
    <button onclick="next(4)">Next 💖</button>
  </div>
</section>

<section id="s4">
  <div class="overlay"></div>
  <div class="content">
    <p id="p4"></p>
    <button onclick="next(5)">Almost there 🫶</button>
  </div>
</section>

<section id="s5">
  <div class="overlay"></div>
  <div class="content">
    <p id="p5"></p>
    <button onclick="alert('I love you Bubu ❤️🧸')">Yes ❤️</button>
    <button onclick="move(this)">No 😄</button>
  </div>
</section>

<script>

const text = [
`Dear bubu I am sorry for eveyrthinf till now and what ive been till now 🧸❤️`,

`So Ill just be frank and honest . Ive not been the best ive had many faults in me I dont wanna loose you lets sort everything and make our reln work and I really will do my beat to be a good boyf for you but one real thing see i really really love you and i cammot imagine a life without you . I really always want you really . 💖`,

`I really am always in love with you and tbh the feelings that ive for you are really very different . Things are really really messed uo but still ik we cam figure out and even that ik if im all good reln will be as u want i really really love you the most and i do really mean this ik u might be nkt seeing mt actions but i give you a promise from this moment you will 🫶`,

`Please lets just fix everything together because i always want us to be togetjer and i really will do anything to keep u with me and yes i want you and only you and you are the love of my life my everything i cant be without you ❤️`,

`So pls im sorry and lets fix  
Yes or yes no option u have 😤❤️`
];

function type(id, text) {
  let i = 0;
  let el = document.getElementById(id);
  el.innerHTML = "";

  function typing() {
    if (i < text.length) {
      el.innerHTML += text.charAt(i);
      i++;
      setTimeout(typing, 25);
    }
  }
  typing();
}

function next(n) {
  document.querySelectorAll("section").forEach(s => s.classList.remove("active"));
  document.getElementById("s" + n).classList.add("active");
  type("p"+n, text[n-1]);
}

function move(btn) {
  btn.style.position = "absolute";
  btn.style.top = Math.random()*80 + "%";
  btn.style.left = Math.random()*80 + "%";
}

type("p1", text[0]);

</script>

</body>
</html>
