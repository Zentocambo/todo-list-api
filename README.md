<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday Uncle Devid!</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  overflow: hidden;
  background: radial-gradient(circle, #35145c, #090018);
  color: white;
  font-family: Arial, sans-serif;
  text-align: center;
}

.container {
  position: relative;
  z-index: 2;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.card {
  max-width: 700px;
  width: 100%;
  padding: 45px 25px;
  border-radius: 25px;
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.2);
  box-shadow: 0 0 50px rgba(255,105,180,.25);
  backdrop-filter: blur(10px);
}

h1 {
  font-size: clamp(42px, 9vw, 80px);
  margin: 10px 0;
  background: linear-gradient(90deg,#ffcc70,#ff5f9e,#a78bfa);
  -webkit-background-clip: text;
  color: transparent;
}

h2 {
  font-size: 30px;
  color: #ffd166;
}

p {
  font-size: 20px;
  line-height: 1.6;
}

button {
  margin-top: 25px;
  padding: 16px 30px;
  border: none;
  border-radius: 50px;
  background: linear-gradient(90deg,#ff4d8d,#8b5cf6);
  color: white;
  font-size: 18px;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 0 25px rgba(255,77,141,.5);
}

button:hover {
  transform: scale(1.05);
}

.hidden {
  display: none;
}

.balloon {
  position: absolute;
  width: 45px;
  height: 55px;
  border-radius: 50%;
  animation: float 6s infinite ease-in-out;
}

.b1 {
  background: #ff4d6d;
  left: 8%;
  top: 15%;
}

.b2 {
  background: #ffd166;
  right: 10%;
  top: 20%;
  animation-delay: 1s;
}

.b3 {
  background: #06d6a0;
  left: 15%;
  bottom: 15%;
  animation-delay: 2s;
}

.b4 {
  background: #4cc9f0;
  right: 15%;
  bottom: 12%;
  animation-delay: 3s;
}

@keyframes float {
  0%,100% {
    transform: translateY(0) rotate(-5deg);
  }

  50% {
    transform: translateY(-35px) rotate(5deg);
  }
}

.confetti {
  position: fixed;
  width: 10px;
  height: 18px;
  top: -20px;
  animation: fall linear forwards;
}

@keyframes fall {
  to {
    transform: translateY(110vh) rotate(720deg);
  }
}

#secret {
  margin-top: 20px;
  font-size: 24px;
  color: #ffe082;
}
</style>
</head>

<body>

<div class="balloon b1"></div>
<div class="balloon b2"></div>
<div class="balloon b3"></div>
<div class="balloon b4"></div>

<div class="container">

  <div class="card">

    <div id="start">

      <div style="font-size:70px;">🎁</div>

      <h2>I have something for my uncle...</h2>

  
        <br>
        Are you ready to discover who?
      </p>

      <button onclick="reveal()">
        🎁 OPEN BRO THU
      </button>

    </div>

    <div id="birthday" class="hidden">

      <div style="font-size:75px;">
        🎂🎉🥳
      </div>

      <h1>HAPPY BIRTHDAY!</h1>

      <h2>🎉 Uncle Devid Thu! 🎉</h2>

      <p>
        Dear Uncle Devid,
        <br><br>

        Wish you rk luy ban jren hx E THIDA kan tae sl! ❤️
        <br><br>

        Thank you for being such an awesome uncle.
        We hope your special day is as incredible
        as you are!
      </p>

      <div id="secret">
        ❤️ WE LOVE YOU, UNCLE DEVID! ❤️
      </div>

      <div style="font-size:50px;margin-top:25px;">
        🎂 🎁 🎈 🎊 🥳 🎈 🎁 🎂
      </div>

    </div>

  </div>

</div>

<script>

function reveal() {

  document.getElementById("start")
    .classList.add("hidden");

  document.getElementById("birthday")
    .classList.remove("hidden");

  launchConfetti();

}

function launchConfetti() {

  const colors = [
    "#ff4d6d",
    "#ffd166",
    "#06d6a0",
    "#4cc9f0",
    "#a78bfa",
    "#ffffff"
  ];

  for (let i = 0; i < 180; i++) {

    const piece =
      document.createElement("div");

    piece.className = "confetti";

    piece.style.left =
      Math.random() * 100 + "vw";

    piece.style.background =
      colors[Math.floor(
        Math.random() * colors.length
      )];

    piece.style.animationDuration =
      (2 + Math.random() * 4) + "s";

    piece.style.animationDelay =
      Math.random() * 2 + "s";

    document.body.appendChild(piece);

    setTimeout(() => {
      piece.remove();
    }, 7000);

  }

}

</script>

</body>
</html>
