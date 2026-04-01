<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For You 💜</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

   body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Poppins', sans-serif;

  background-color: #dfe7dc;

  /* PIXEL GRID */
  background-image:
    linear-gradient(#ffffff22 1px, transparent 1px),
    linear-gradient(90deg, #ffffff22 1px, transparent 1px);

  background-size: 25px 25px;

  overflow: hidden;
}

    /* ===== CARD CONTAINER ===== */
    .card {
      width: 360px;
      background: #c58be0;
      border-radius: 28px;
      padding: 30px 24px 36px;
      text-align: center;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.1);
    }

    /* ===== LETTER DESIGN ===== */
    .letter {
    display: none;
   background: #fff;

   width: 380px;
   max-width: 90%;

  max-height: 500px; /* 👈 LIMIT HEIGHT */
  overflow-y: auto;  /* 👈 ENABLE SCROLL */

  padding: 30px 24px;
  border-radius: 16px;

  box-shadow: 0 10px 40px rgba(0,0,0,0.15);

  position: relative;
  font-family: 'Patrick Hand', cursive;
  line-height: 1.6;

  animation: slideFadeIn 0.5s ease;
}

    @keyframes popIn {
  from {
    opacity: 0;
    transform: translate(-50%, -60%) scale(0.9);
  }
  to {
    opacity: 1;
    transform: translate(-50%, -50%) scale(1);
  }
}

    .letter h1 {
      font-size: 28px;
      text-align: center;
      margin-bottom: 20px;
    }

    .letter p {
      margin-bottom: 14px;
      font-size: 16px;
      color: #333;
    }

    .signature {
      margin-top: 20px;
      text-align: right;
      font-weight: bold;
    }

    /* ===== IMAGE ===== */
    .cat-image {
      width: 150px;
      height: 150px;
      object-fit: cover;
      margin-bottom: 16px;
    }

    .message {
      font-weight: 700;
      margin-bottom: 24px;
    }

    .btn {
      border: none;
      padding: 14px 20px;
      border-radius: 999px;
      font-weight: 700;
      cursor: pointer;
      background: #bb72d7;
      transition: all 0.25s ease;
    }

    .btn:hover {
      background: #a85fc5;
      color: white;
      transform: scale(1.05);
    }

    #noBtn:hover {
      background: #ff7a7a;
    }

    /* ===== ENTRY ANIMATIONS ===== */
@keyframes slideFadeIn {
  from {
    opacity: 0;
    transform: translateY(40px) scale(0.95);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes slideFadeOut {
  from {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
  to {
    opacity: 0;
    transform: translateY(-30px) scale(0.95);
  }
}

.animate-in {
  animation: slideFadeIn 0.5s ease forwards;
}

.animate-out {
  animation: slideFadeOut 0.4s ease forwards;
}

.pixel-heart {
  position: fixed;
  width: 12px;
  height: 12px;
  background: #ff8fd8;
  transform: rotate(45deg);
  animation: floatUp 6s linear forwards;
  z-index: -1;
}

.pixel-heart::before,
.pixel-heart::after {
  content: '';
  position: absolute;
  width: 12px;
  height: 12px;
  background: #ff8fd8;
  border-radius: 50%;
}

.pixel-heart::before {
  top: -6px;
  left: 0;
}

.pixel-heart::after {
  left: -6px;
  top: 0;
}

@keyframes floatUp {
  0% {
    opacity: 0;
    transform: translateY(0) scale(1) rotate(45deg);
  }
  20% {
    opacity: 1;
  }
  100% {
    transform: translateY(-120vh) scale(1.5) rotate(45deg);
    opacity: 0;
  }
}

.letter::-webkit-scrollbar {
  width: 6px;
}

.letter::-webkit-scrollbar-thumb {
  background: #c58be0;
  border-radius: 10px;
}

.letter {
  background: #fff;
  border: 2px dashed #e6c8f5;
}

  </style>
</head>
<body>
  <div id="hearts-container"></div>
  <!-- FIRST CARD -->
  <div class="card" id="card">
    <img class="cat-image" id="catImage" src="cat.gif">

    <p class="message" id="mainMessage">
      Hi, I’m Ybrahim—your new applicant 😌
    </p>

    <button class="btn" id="startBtn">START</button>
    <button class="btn" id="noBtn">AYAW KO</button>
  </div>

  <!-- LETTER PAGE -->
  <div class="letter" id="letter">
    <h1>Why You Deserve Me 💜</h1>

    <p>
      I don’t believe anyone ‘deserves’ someone like they’re a prize,
      but I know what I can offer.
    </p>

    <p>
      I’m loyal and consistent, and when I date, it’s with the intention to marry.
      I don’t play games I show up and put in real effort..
    </p>

    <p>
      I’ve got a sense of humor that can make you laugh, but I know how to be serious when it matters.
      I listen. I understand. I don’t just react.
    </p>

    <p>
      I’m still growing—with goals, discipline, and purpose. I don’t give up easily, especially on someone I care about.
    </p>

    <p>
      I can be your peace when things get heavy, the kind of support you didn’t even know you needed and still keep things fun and exciting.
    </p>

    <p>
      And honestly, I’m this sure because I know what I bring to the table—but I also appreciate how easy it is to be myself when I’m talking to you.
    </p>

    <p>
      I’m not perfect — but I can be someone worth choosing.
    </p>

    <div class="signature">
      — Ybrahim
    </div>
  </div>

  <script>
    const startBtn = document.getElementById('startBtn');
    const noBtn = document.getElementById('noBtn');
    const card = document.getElementById('card');
    const letter = document.getElementById('letter');
    const catImage = document.getElementById('catImage');
    const mainMessage = document.getElementById('mainMessage');

  startBtn.addEventListener('click', () => {
  card.classList.add('animate-out');

  setTimeout(() => {
    card.style.display = 'none';
    letter.style.display = 'block';
    letter.classList.add('animate-in');
  }, 400);
});

    noBtn.addEventListener('click', () => {
      catImage.src = 'angrycat.gif';
      mainMessage.textContent = 'START MO NA YAN';
      noBtn.style.display = 'none';
    });
  

    // ===== BONUS SCREEN (PWET CHOICE) =====
    const pwetScreen = document.createElement('div');
    pwetScreen.innerHTML = `
        <div class="card" id="pwetCard" style="
        display:none;
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        animation: popIn 0.4s ease;
        z-index: 999;
        ">
        <img class="cat-image" src="cat-gun.gif">
        <p class="message">Pwet ni Ybrahim or Pwet ni Shrek</p>
        <div style="display:flex; gap:12px; justify-content:center;">
          <button class="btn" id="pwetBtn">Pwet ni Ybrahim</button>
          <button class="btn" id="shrekBtn" style="position:relative;">Pwet ni Shrek</button>
        </div>
      </div>
    `;
    document.body.appendChild(pwetScreen);

    const pwetCard = document.getElementById('pwetCard');

    // show pwet screen after letter
    const goNextBtn = document.createElement('button');
    goNextBtn.textContent = 'NEXT';
    goNextBtn.className = 'btn';
    goNextBtn.style.marginTop = '20px';
    document.getElementById('letter').appendChild(goNextBtn);

    goNextBtn.addEventListener('click', () => {
    letter.classList.add('animate-out');

    setTimeout(() => {
    letter.style.display = 'none';
    pwetCard.style.display = 'block';
    pwetCard.classList.add('animate-in');
  }, 400);
});

    // SHREK BUTTON RUNS AWAY
    document.addEventListener('mouseover', (e) => {
      if (e.target && e.target.id === 'shrekBtn') {
        const btn = e.target;
        const x = Math.random() * 200 - 100;
        const y = Math.random() * 100 - 50;
      btn.style.transition = 'transform 0.15s ease';
      btn.style.transform = `translate(${x}px, ${y}px)`;
      }
    });

    // pwet mo click reaction
    document.addEventListener('click', (e) => {
  if (e.target && e.target.id === 'pwetBtn') {
    pwetCard.classList.add('animate-out');

    setTimeout(() => {
      pwetCard.innerHTML = `
        <div style="display:flex; flex-direction:column; align-items:center; gap:16px;">
          <img class="cat-image" src="cat-cute.gif">
          <p class="message">YAY!!, PLAY MO YAN DI KO PAPAKITA PWET KO DYAN PROMISE 😭</p>
          <a href="https://drive.google.com/file/d/1GMtlkG0NDQ92ZTt8SdD_inLHNL5pLVyi/view?usp=sharing" target="_blank">
            <button class="btn">WATCH THIS</button>
          </a>
        </div>
      `;

      pwetCard.classList.remove('animate-out');
      pwetCard.classList.add('animate-in');

    }, 300);
  }
});

    let pwetSize = 1; // starting scale

    document.addEventListener('click', (e) => {
    if (e.target && e.target.id === 'shrekBtn') {
    const pwetBtn = document.getElementById('pwetBtn');

    pwetSize += 0.2; // increase size each click
    pwetBtn.style.transform = `scale(${pwetSize})`;

    pwetBtn.style.transition = 'transform 0.2s ease';
  }
});

const heartContainer = document.getElementById('hearts-container');

function createHeart(x, y) {
  const heart = document.createElement('div');
  heart.classList.add('pixel-heart');

  heart.style.left = x + 'px';
  heart.style.top = y + 'px';

  heartContainer.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 6000);
}

// spawn hearts on mouse move
document.addEventListener('mousemove', (e) => {
  if (Math.random() < 0.2) { // not too many
    createHeart(e.clientX, e.clientY);
  }
});
  </script>

</body>
</html>
