# HikariHikaru-daily-blog
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>HIKARI・HIKARU 日々のブログ</title>
  <link rel="stylesheet" href="style.css">
  <style>
    body {
      margin: 0;
      font-family: sans-serif;
      background-color: #fff8f0;
    }

    #blackout {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: black;
      z-index: 9999;
    }

    img {
      width: 300px;
      user-select: none;
      pointer-events: auto;
      -webkit-user-drag: none;
    }
  </style>
</head>
<body>
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>

  <main>
    <h2>HIKARI・HIKARUです。</h2>
    <p>
      いつも小説を読んでくださり<br>
      ありがとうございます。<br><br>

      皆様にご報告がございます。<br><br>

      本日より、ブログを不定期で更新することにしました。。<br><br>

      写真等も載せる予定です。<br>
      今後とも応援のほど、よろしくお願い申し上げます。
    </p>

    <!-- ▼ 写真コーナー（長押しで黒画面）▼ -->
    <h3>顔写真</h3>
    <p>※長押しすると黒画面になります。</p>
    <img src="your-image.jpg" alt="顔写真" id="protectedImage">

    <div id="blackout"></div>

    <!-- ▼ 日付別リンク ▼ -->
    <h2>ブログ一覧</h2>
    <ul>
      <li><a href="https://hikari-hikaru.github.io/dairy1/">2025年6月2日（dairy1ページ）</a></li>
    </ul>
  </main>

  <footer>
    <small>&copy; 1994 HIKARI HIKARU All rights reserved.</small>
  </footer>

  <script>
    const image = document.getElementById("protectedImage");
    const blackout = document.getElementById("blackout");

    let touchTimer;

    image.addEventListener("touchstart", () => {
      touchTimer = setTimeout(() => {
        blackout.style.display = "block";
      }, 500); // 0.5秒以上押すと黒くなる
    });

    image.addEventListener("touchend", () => {
      clearTimeout(touchTimer);
    });

    blackout.addEventListener("click", () => {
      blackout.style.display = "none";
    });
  </script>
</body>
</html>
