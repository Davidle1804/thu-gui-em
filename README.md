

<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Thư Gửi Em Yêu 💌</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(145deg, #ffdce0, #ffe9f0);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .container {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    .envelope {
      width: 400px;
      height: 350px;
      background: #fff0f5;
      border: 2px solid #e91e63;
      border-radius: 10px;
      position: relative;
      cursor: pointer;
      transition: all 1s ease-in-out;
      box-shadow: 0 10px 30px rgba(255, 105, 135, 0.3);
    }

    .flap {
      position: absolute;
      top: 0;
      left: 0;
      width: 300px;
      height: 100px;
      background: #f8bbd0;
      clip-path: polygon(0 0, 50% 100%, 100% 0);
      transform-origin: top;
      transition: transform 1s ease-in-out;
      z-index: 2;
    }

    .letter {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      padding: 20px;
      box-sizing: border-box;
      background: #fff;
      border-radius: 10px;
      opacity: 0;
      transform: scale(0.9);
      transition: all 1s ease-in-out;
      z-index: 1;
      overflow-y: auto;
    }

    .open .flap {
      transform: rotateX(180deg);
    }

    .open .letter {
      opacity: 1;
      transform: scale(1);
    }

    .letter h1 {
      color: #e91e63;
      text-align: center;
      font-size: 24px;
    }

    .typing-text {
      white-space: pre-line;
      font-size: 16px;
      line-height: 1.6;
      color: #444;
      min-height: 180px;
    }

    .heart {
      text-align: center;
      font-size: 24px;
      margin-top: 10px;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }

    .instruction {
      margin-top: 20px;
      font-size: 16px;
      color: #e91e63;
      animation: fadeIn 3s ease-in-out infinite alternate;
    }

    @keyframes fadeIn {
      from { opacity: 0.5; }
      to { opacity: 1; }
    }

    audio {
      display: none;
    }
  </style>
</head>
<body>

 <audio autoplay loop>
  <source src="https://soundcloud.com/interscope/maroon-5-sugar?in=ixt3r/sets/m5&utm_source=clipboard&utm_medium=text&utm_campaign=social_sharing?ex=67f2e3fc&is=67f1927c&hm=732e3b9c4862a38d51ebda9aa031df52456ff73012e631695df61eef02cf5cd1&" type="audio/mpeg">
</audio>

function openEnvelope() {
  const envelope = document.getElementById("envelope");
  const audio = document.getElementById("loveSong");  // Lấy phần tử audio

  if (!envelope.classList.contains("open")) {
    envelope.classList.add("open");
    audio.play();  // Phát nhạc khi mở thư
    setTimeout(typeLine, 1000); // delay sau khi mở để bắt đầu typing
  }
}



  <div class="container">
    <div class="envelope" onclick="openEnvelope()" id="envelope">
      <div class="flap"></div>
      <div class="letter">
        <h1>Gửi Em Yêu 💌</h1>
        <div class="typing-text" id="typingText"></div>
        <img src="https://cdn.discordapp.com/attachments/1278039895155413143/1358174754636431672/z6388253717704_06dffb124ccd253f8a6f55f06b2c0458.jpg?ex=67f2e24f&is=67f190cf&hm=b8c16ff015d38979a9db92802c97bf45cb8cab898490002dee8ae87a9c7ecd0a&" alt="Ảnh kỷ niệm" style="width: 100%; border-radius: 10px; margin-top: 10px;">

       <div class="heart">💖💖💖</div>
      </div>
    </div>
    <div class="instruction">✨ Nhấp vào để mở thư ✨</div>
  </div>

  <script>
    const text = `
Em yêu ơi,

Khi em đọc những dòng này, là lúc mà anh đang buồn vì không có em bên cạnh, anh muốn được gặp em lắm.

Mấy nay có nhiều chuyện xảy ra, thật lòng anh không muốn em buồn, nhưng anh cũng sợ em phải chịu khổ cùng anh. Em là người anh yêu nên anh mới vậy á.

Chỉ cần còn được gặp em là ngày đó anh còn thấy vui, không được gặp em người anh bất rứt lắm luôn á, đúng kiểu bị khó chịu trong người. Anh cảm thấy nhớ em lắm rồi.

Anh yêu em lắm,

Anh yêu emmmmm 🥰    `;

    let index = 0;
    let typingText = document.getElementById("typingText");

    function typeLine() {
      if (index < text.length) {
        typingText.innerHTML += text[index];
        index++;
        setTimeout(typeLine, 30); // tốc độ gõ từng ký tự
      }
    }

    function openEnvelope() {
      const envelope = document.getElementById("envelope");
      if (!envelope.classList.contains("open")) {
        envelope.classList.add("open");
        setTimeout(typeLine, 1000); // delay sau khi mở để bắt đầu typing
      }
    }
  </script>

</body>
</html>
