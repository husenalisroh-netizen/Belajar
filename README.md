<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Menyatakan Perasaan | Sayang Tak Bertepi</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    :root{
      --pink:#ff66b2; --pink-dark:#ff4081; --bg:#ffccf2; --heart:#ff1744;
    }
    *{box-sizing:border-box}
    body{
      margin:0; min-height:100vh; display:flex; flex-direction:column;
      align-items:center; justify-content:center;
      background: radial-gradient(circle at 30% 30%, #fff 0%, var(--bg) 60%);
      color:var(--pink-dark); font-family: 'Arial', sans-serif; text-align:center;
      overflow:hidden; padding:24px;
    }
    h1{ font-size:48px; margin:10px 0 6px }
    p.lead{ font-size:20px; color:#a4005f; margin:0 0 12px }
    .heart{
      font-size:100px; color:var(--heart); animation:beat 1.1s infinite ease-in-out;
      filter: drop-shadow(0 8px 16px rgba(255,0,64,.25));
      margin:18px 0 12px;
    }
    @keyframes beat{
      0%,20%,50%,80%,100%{ transform:scale(1) }
      40%{ transform:scale(1.18) }
      60%{ transform:scale(.92) }
    }
    .btn{
      background:var(--pink); color:#fff; border:0; border-radius:48px;
      padding:12px 24px; cursor:pointer; font-size:16px; transition:.25s;
      margin-top:14px
    }
    .btn:hover{ background:var(--pink-dark); transform:translateY(-2px) }
    .stars span{
      position:absolute; top:-10vh; font-size:12px; color:#fff; opacity:.75;
      animation:fall linear infinite;
    }
    @keyframes fall{
      to{ transform: translateY(120vh) translateX(-10vw); opacity:.1 }
    }
    footer{ position:fixed; bottom:10px; left:0; right:0; font-size:12px; color:#7a0a58 }
  </style>
</head>
<body>
  <h1>Aku Cinta Kamu! 💖</h1>
  <p class="lead">Setiap detik bersamamu adalah bahagia yang tak terhitung.</p>
  <div class="heart">💖</div>
  <button class="btn" id="btnRahasia">Klik untuk rahasia</button>

  <footer>© 2026 Bucin Tech — Halaman cinta sederhana untuk kamu</footer>

  <div class="stars" id="stars"></div>

  <script>
    // Bintang jatuh
    const stars = document.getElementById('stars');
    for(let i=0;i<40;i++){
      const s=document.createElement('span');
      s.textContent='✦';
      s.style.left=Math.random()*100+'vw';
      s.style.animationDuration=(6+Math.random()*6)+'s';
      s.style.animationDelay=(Math.random()*4)+'s';
      s.style.fontSize=(8+Math.random()*14)+'px';
      stars.appendChild(s);
    }
    // Rahasia manis
    document.getElementById('btnRahasia').addEventListener('click', ()=>{
      alert('Rahasiaku: aku pengin menua bareng kamu. ❤️');
    });
  </script>
</body>
</html>
