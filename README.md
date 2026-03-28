<!DOCTYPE html>
<html>
<head>
  <title>For Bubu ❤️</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      text-align: center;
      color: white;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      overflow-x: hidden;
    }

    section {
      height: 100vh;
      display: none;
      padding: 40px;
    }

    .active {
      display: block;
    }

    h1 {
      margin-top: 100px;
    }

    p {
      max-width: 700px;
      margin: auto;
      font-size: 18px;
    }

    button {
      margin-top: 30px;
      padding: 15px 25px;
      border-radius: 25px;
      border: none;
      background: white;
      color: #ff4d6d;
      font-size: 16px;
      cursor: pointer;
    }

    img {
      width: 200px;
      border-radius: 15px;
      margin: 10px;
    }

    .heart {
      position: absolute;
      color: white;
      animation: float 6s linear infinite;
    }

    @keyframes float {
      from { transform: translateY(100vh); }
      to { transform: translateY(-10vh); opacity: 0; }
    }
  </style>
</head>

<body>

<section id="s1" class="active">
  <p id="p1"></p>
  <button onclick="next(2)">Click ❤️</button>
</section>

<section id="s2">
  <p id="p2"></p>
  <button onclick="next(3)">Next</button>
</section>

<section id="s3">
  <p id="p3"></p>

  <img src="photo1.jpg">
  <img src="photo2.jpg">
  <img src="photo3.jpg">
  <img src="photo4.jpg">

  <br>
  <button onclick="next(4)">Next ❤️</button>
</section>

<section id="s4">
  <p id="p4"></p>
  <button onclick="next(5)">Last ❤️</button>
</section>

<section id="s5">
  <p id="p5"></p>
  <button onclick="alert('I love you Bubu ❤️')">Yes</button>
  <button onclick="move(this)">No 😄</button>
</section>

<script>

const text = [
`Dear bubu I am sorry for eveyrthinf till now and what ive been till now`,

`So Ill just be frank and honest . Ive not been the best ive had many faults in me I dont wanna loose you lets sort everything and make our reln work and I really will do my beat to be a good boyf for you but one real thing see i really really love you and i cammot imagine a life without you . I really always want you really .`,

`I really am always in love with you and tbh the feelings that ive for you are really very different . Things are really really messed uo but still ik we cam figure out and even that ik if im all good reln will be as u want i really really love you the most and i do really mean this ik u might be nkt seeing mt actions but i give you a promise from this moment you will`,

`Please lets just fix everything together because i always want us to be togetjer and i really will do anything to keep u with me and yes i want you and only you and you are the love of my life my everything i cant be without you`,

`So pls im sorry and lets fix
Yes or yes no option u have`
];

function type(id, text) {
  let i = 0;
  let el = document.getElementById(id);
  el.innerHTML = "";

  function typing() {
    if (i < text.length) {
      el.innerHTML += text.charAt(i);
      i++;
      setTimeout(typing, 30);
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

function hearts() {
  let h = document.createElement("div");
  h.className = "heart";
  h.innerHTML = "❤️";
  h.style.left = Math.random()*100 + "vw";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(), 6000);
}

setInterval(hearts, 300);

type("p1", text[0]);

</script>

</body>
</html>
