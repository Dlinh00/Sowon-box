<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <title>소원 상자 (Wish Box)</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      background: radial-gradient(circle at center, #1a0b12 0%, #050505 100%);
      color: #e6d5b8;
      font-family: 'Apple SD Gothic Neo', 'Malgun Gothic', sans-serif;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }
    .app-container {
      width: 100%;
      max-width: 400px;
      height: 100%;
      max-height: 750px;
      padding: 30px 24px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      text-align: center;
      border: 1px solid #3a1c24;
      background: rgba(10, 8, 10, 0.85);
      box-shadow: 0 0 40px rgba(139, 0, 0, 0.25);
    }
    .header { margin-top: 20px; }
    .symbol {
      font-size: 42px;
      color: #b8860b;
      text-shadow: 0 0 15px rgba(184, 134, 11, 0.6);
      margin-bottom: 10px;
      transition: transform 2s ease;
    }
    .spinning { transform: rotate(360deg); }
    h1 {
      font-size: 22px;
      letter-spacing: 3px;
      font-weight: 400;
      color: #d4af37;
    }
    .counter {
      margin-top: 12px;
      font-size: 13px;
      color: #9e4747;
      letter-spacing: 1px;
    }
    .wish-area {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }
    textarea {
      width: 100%;
      height: 110px;
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid #4a252c;
      border-radius: 8px;
      padding: 14px;
      color: #f5ebd6;
      font-size: 15px;
      resize: none;
      outline: none;
    }
    textarea::placeholder { color: #6e5d5d; }
    textarea:focus { border-color: #b8860b; }
    button {
      background: linear-gradient(135deg, #4a0e17 0%, #240509 100%);
      color: #e6d5b8;
      border: 1px solid #8a2be2;
      border-color: #8b3a3a;
      padding: 15px;
      border-radius: 8px;
      font-size: 16px;
      letter-spacing: 2px;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    button:active { transform: scale(0.98); }
    button:disabled { opacity: 0.4; cursor: not-allowed; }
    .status-box {
      min-height: 70px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      line-height: 1.5;
      color: #c93b3b;
      opacity: 0;
      transition: opacity 0.8s ease;
    }
    .status-box.visible { opacity: 1; }
    .footer {
      font-size: 11px;
      color: #5c4b4b;
      letter-spacing: 1px;
    }
  </style>
</head>
<body>
  <div class="app-container">
    <div class="header">
      <div class="symbol" id="symbol">❖</div>
      <h1>소원 상자</h1>
      <div class="counter" id="counter">남은 소원: 7 / 7</div>
    </div>

    <div class="wish-area">
      <textarea id="wishInput" placeholder="당신의 소원을 입력하세요...&#10;모든 소원에는 대가가 따릅니다."></textarea>
      <button id="wishBtn" onclick="makeWish()">소원 빌기</button>
    </div>

    <div class="status-box" id="statusBox"></div>

    <div class="footer">7번째 소원이 끝나면, 모든 것을 잃게 됩니다.</div>
  </div>

  <script>
    let wishesLeft = 7;
    const warnings = [
      "첫 번째 소원이 접수되었습니다. 곧 이루어집니다...",
      "두 번째 소원이 이루어졌습니다. 주변을 조심하세요.",
      "세 번째 소원. 대가가 이미 시작되었습니다.",
      "네 번째 소원. 돌이킬 수 없습니다.",
      "다섯 번째 소원. 누군가 당신의 곁을 떠날 것입니다.",
      "여섯 번째 소원. 마지막 기회가 다가오고 있습니다.",
      "일곱 번째 소원 완료. 이제 상자가 당신의 영혼을 거둡니다."
    ];

    function playMusicBox() {
      const ctx = new (window.AudioContext || window.webkitAudioContext)();
      const notes = [523.25, 659.25, 783.99, 622.25, 523.25, 493.88];
      notes.forEach((freq, i) => {
        const osc = ctx.createOscillator();
        const gain = ctx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(freq, ctx.currentTime + i * 0.45);
        gain.gain.setValueAtTime(0.15, ctx.currentTime + i * 0.45);
        gain.gain.exponentialRampToValueAtTime(0.0001, ctx.currentTime + i * 0.45 + 1.2);
        osc.connect(gain);
        gain.connect(ctx.destination);
        osc.start(ctx.currentTime + i * 0.45);
        osc.stop(ctx.currentTime + i * 0.45 + 1.3);
      });
    }

    function makeWish() {
      const input = document.getElementById('wishInput');
      const statusBox = document.getElementById('statusBox');
      const symbol = document.getElementById('symbol');
      const btn = document.getElementById('wishBtn');

      if (!input.value.trim() || wishesLeft <= 0) return;

      playMusicBox();
      symbol.classList.toggle('spinning');

      const index = 7 - wishesLeft;
      wishesLeft--;

      document.getElementById('counter').innerText = `남은 소원: ${wishesLeft} / 7`;
      statusBox.classList.remove('visible');

      setTimeout(() => {
        statusBox.innerText = warnings[index];
        statusBox.classList.add('visible');
        input.value = "";
        if (wishesLeft === 0) {
          btn.disabled = true;
          input.disabled = true;
          input.placeholder = "더 이상 소원을 빌 수 없습니다.";
        }
      }, 600);
    }
  </script>
</body>
</html>
