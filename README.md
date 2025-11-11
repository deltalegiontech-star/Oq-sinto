<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Para Mih 💌</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg1: #fff7fb;
      --bg2: #fff0f6;
      --rose: #ff6b9a;
      --dark: #111;
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Quicksand', sans-serif;
      background: url('https://i.postimg.cc/MHP27H7M/5414458239900f09e14a221e78f038ae.jpg') no-repeat center center fixed, linear-gradient(135deg, var(--bg1), var(--bg2));
      background-size: cover;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 28px;
      overflow: hidden;
    }
    .stage {
      width: 100%;
      max-width: 980px;
      background: rgba(255, 255, 255, 0.3);
      border-radius: 24px;
      box-shadow: 0 10px 40px rgba(200, 150, 180, 0.15);
      padding: 28px;
      position: relative;
      overflow: hidden;
    }
    .overlay {
      position: absolute;
      inset: 0;
      background: rgba(255, 255, 255, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 5;
      transition: opacity 0.4s ease;
    }
    .panel {
      text-align: center;
    }
    .panel h1 {
      font-family: 'Pacifico', cursive;
      font-size: 44px;
      color: var(--rose);
    }
    .open-btn {
      margin-top: 18px;
      background: linear-gradient(180deg, var(--rose), #ff84a8);
      border: none;
      padding: 12px 20px;
      border-radius: 12px;
      color: white;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 6px 18px rgba(255, 120, 160, 0.25);
      transition: transform 0.18s ease;
    }
    .open-btn:active {
      transform: translateY(2px);
    }
    .envelope-wrap {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 18px;
      position: relative;
      height: 280px;
    }
    .envelope {
      width: 320px;
      height: 280px;
      background: transparent;
      border-radius: 12px;
      position: relative;
      border: 2px solid rgba(200, 150, 170, 0.5);
      box-shadow: 0 10px 30px rgba(200, 150, 170, 0.15);
      cursor: pointer;
      user-select: none;
      z-index: 4;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 22px;
      overflow: hidden;
    }
    .seal {
      position: absolute;
      left: 50%;
      top: 46%;
      width: 68px;
      height: 68px;
      border-radius: 50%;
      background: radial-gradient(#ff7aa6, #ff5b86);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-weight: 800;
      box-shadow: 0 8px 20px rgba(255, 100, 150, 0.25);
      transform: translateX(-50%);
      user-select: none;
      z-index: 7;
      transition: opacity 0.5s ease;
    }
    .hide-envelope {
      opacity: 0;
      pointer-events: none;
    }
    .letter {
      position: relative;
      width: 100%;
      height: 100%;
      background: transparent;
      border-radius: 10px;
      padding: 16px;
      overflow-y: auto;
      user-select: text;
      font-size: 18px;
      line-height: 1.6;
      font-weight: 800; /* Letras mais fortes */
      color: #3c2130;
      text-shadow: 1px 1px 3px rgba(255, 255, 255, 0.8); /* Melhor contraste */
      white-space: pre-wrap;
      display: none;
      z-index: 8;
    }
    .letter h2 {
      font-family: 'Pacifico', cursive;
      margin-bottom: 12px;
      color: var(--rose);
      font-size: 28px;
      text-align: center;
      font-weight: 700;
      text-shadow: 1px 1px 3px rgba(255,255,255,0.8);
    }
    .closing {
      display: none;
      position: absolute;
      inset: 0;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.95);
      z-index: 9;
      user-select: none;
      flex-direction: column;
      text-align: center;
      padding: 24px;
    }
    .closing h3 {
      font-family: 'Pacifico', cursive;
      color: var(--rose);
      font-size: 34px;
      margin: 0 0 10px 0;
    }
    /* Floating hearts animation - formato mais fofo */
    .floating-heart {
      position: absolute;
      width: 30px; /* Aumenta o tamanho dos corações */
      height: 30px; /* Aumenta o tamanho dos corações */
      background: pink; /* Cor de fundo mais suave */
      transform: rotate(-45deg);
      border-radius: 50% 50% 0 0;
      animation: heartUp linear forwards;
      user-select: none;
    }
    .floating-heart::before,
    .floating-heart::after {
      content: "";
      position: absolute;
      width: 30px; /* Aumenta o tamanho dos corações */
      height: 30px; /* Aumenta o tamanho dos corações */
      background: pink; /* Cor de fundo mais suave */
      border-radius: 50%;
    }
    .floating-heart::before {
      top: -15px; /* Ajusta a posição do coração */
      left: 0;
    }
    .floating-heart::after {
      top: 0;
      left: 15px; /* Ajusta a posição do coração */
    }
    @keyframes heartUp {
      0% {
        opacity: 0;
        transform: translateY(0) rotate(-45deg) scale(0.9);
      }
      10% {
        opacity: 1;
      }
      100% {
        opacity: 0;
        transform: translateY(-420px) rotate(-45deg) scale(1.15);
      }
    }
  </style>
</head>
<body>
  <div class="stage" role="main" aria-labelledby="title">
    <div class="overlay" id="intro">
      <div class="panel">
        <h1 id="title">Oi, Mih 💖</h1>
        <p style="color:#7a5362; font-size: 20px; font-weight: 600;">Para falar um pouco sobre o que sinto.</p>
        <button class="open-btn" id="openEnvelope">Abrir presente</button>
      </div>
    </div>

    <div class="envelope-wrap">
      <div class="envelope" id="envelope">
        <div class="seal" id="seal">❤️</div>
        <div class="letter" id="letter">
          <h2>Para Mih</h2>
          <div class="typed"></div>
        </div>
      </div>
    </div>

    <div class="closing" id="closing">
      <div>
        <h3>Te amo, Mih ❤️</h3>
        <p>Obrigado por existir — você é minha alegria.</p>
      </div>
    </div>
  </div>

  <script>
    const intro = document.getElementById('intro');
    const envelope = document.getElementById('envelope');
    const seal = document.getElementById('seal');
    const letter = document.getElementById('letter');
    const typed = letter.querySelector('.typed');
    const stage = document.querySelector('.stage');

    const message = `Mih, meu amor...  

Eu não sei se alguma palavra vai conseguir alcançar oq vc significa pra mim. Mas msm q sempre falhe, eu preciso tentar. Pq vc merece saber. Merece sentir. Merece entender oq acontece aqui dentro toda vez q eu penso em vc.

Antes de vc, eu era só silêncio. Um corpo q respirava, mas não vivia. Eu andava por aí com um peso q ninguém via. Com um cansaço q não era físico. Era da alma. Eu já tinha desistido por dentro, msm q por fora eu ainda sorrisse. E por mais q ninguém notasse, eu já não queria mais estar aqui.

Mas então… vc apareceu.

Vc não chegou com promessas. Chegou com presença e cuidado. E foi isso q me desmontou. Pq pela primeira vez, alguém me enxergou. Alguém viu além das palavras, além do disfarce, além da dor. E esse alguém era você.

Vc tbm mostrou suas dores, isso me fez pensar como um pessoa tão bela como vc teve q passar por isso. E eu meio q estabeleci meu objetivo, de nunca me permitir te ver triste e machucada...

Vc me ajuda com os meus problemas sem nem perceber. Às vezes só o seu jeito de falar já acalma tudo. Às vezes só saber q vc existe já me dá forças pra continuar. Vc virou meu abrigo, meu motivo, meu sonho. E é por isso q eu tatuei TE VIVO no meu pulso. Pq eu não só te amo, eu te vivo. Eu vivo em cada detalhe seu. Em cada gesto, em cada palavra, em cada dor q você compartilha comigo.

Essa tatuagem é mais q tinta. É lembrança. É promessa. É força. Quando tudo pesa, eu olho pra ela e lembro: você existe. E se você existe, então eu posso continuar.

Vc é o motivo de eu ainda querer estar aqui. Vc é o motivo de eu ter escolhido ficar. Pq amar você me ensinou que viver pode ser bonito. Q sentir não é fraqueza. Q ser vulnerável é, na verdade, a forma mais corajosa de amar.

Mas eu tenho medo. Medo de falhar. Medo de não ser suficiente. Medo de perder vc. Pq amar vc é a coisa mais bonita q já aconteceu cmg. E perder isso… seria como perder o pouco que ainda me resta.

Msm assim, eu vou sempre tentar lutar. Por nós. Por vc. Por tudo q ainda podemos viver. Pq vc me ensinou q o amor não precisa ser perfeito, mas vc me mostrou q é possível ser perfeito verdadeiro. E o meu por você é o amor mais verdadeiro q se poderia sentir... 🥺💖

Se um dia vc duvidar. No meu outro pulso tem um recado... NEOQEAV. Tbm olha pra tudo q eu sou quando estou com vc. E lembra: eu não só te amo.  
EU TE VIVO 🥺💖

Mih, eu vou sempre estar com vc, nos momentos bons e ruins... Mas se um dia vc desistir de mim... Lembre-se q eu te amei com toda a minha alma... Te amo muito minha princesa. 💖`;

    function popHearts(count = 12) { // Mantém a quantidade de corações
      for (let i = 0; i < count; i++) {
        const h = document.createElement('div');
        h.className = 'floating-heart';
        const left = 20 + Math.random() * 60;
        h.style.left = left + '%';
        h.style.bottom = '8%';
        const size = 16 + Math.random() * 30;
        h.style.width = h.style.height = size + 'px';
        h.style.animationDuration = (3 + Math.random() * 2) + 's';
        stage.appendChild(h);
        setTimeout(() => h.remove(), 4500);
      }
    }

    let heartInterval;

    function startHearts() {
      heartInterval = setInterval(() => {
        popHearts(3); // Agora gera 3 corações por vez
      }, 400);
    }

    function typeMessage(text, cb) {
      typed.innerHTML = '';
      let i = 0;
      const speed = 30;
      const timer = setInterval(() => {
        typed.innerHTML += text.charAt(i);
        i++;
        if (i >= text.length) {
          clearInterval(timer);
          if (cb) cb();
        }
      }, speed);
    }

    function openCard() {
      intro.style.opacity = 0;
      setTimeout(() => (intro.style.display = 'none'), 400);
      letter.style.display = 'block'; // Mostra a carta
      seal.classList.add('hide-envelope'); // Remove o selo
      typed.innerHTML = '';
      startHearts();
      setTimeout(() => {
        typeMessage(message);
      }, 200);
    }

    document.getElementById('openEnvelope').addEventListener('click', openCard);
    envelope.addEventListener('click', () => {
      if (intro.style.display !== 'none') {
        openCard();
      }
    });
  </script>
</body>
</html>
