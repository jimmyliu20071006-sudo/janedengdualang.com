<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <title>年齡驗證網站</title>
  <style>
    body { text-align: center; font-family: Arial, sans-serif; background: #f8f8f8; }
    #gate, #content { display: none; }
    #gate { margin-top: 15%; }
    button {
      margin: 10px; padding: 10px 20px; font-size: 16px;
      cursor: pointer; border: none; border-radius: 5px;
    }
    button.enter { background: #4CAF50; color: white; }
    button.exit { background: #f44336; color: white; }
    img { max-width: 90%; height: auto; margin-top: 20px; border-radius: 8px; }
  </style>
</head>
<body>

  <!-- 年齡確認畫面 -->
  <div id="gate">
    <p>
      该网站包含有年龄限制的内容。<br>
      登录即表示您确认您已年满 18 岁，或在您访问本网站时所在的司法管辖区已是成年人。
    </p>
    <button class="enter" onclick="enterSite()">我年满 18 岁 - 进入</button>
    <button class="exit" onclick="exitSite()">我未满 18 岁 - 退出</button>
  </div>

  <!-- 網站內容 -->
  <div id="content">
    <h1>歡迎</h1>
    <img src="photo.jpg" alt="你的照片">
  </div>

  <script>
    // 預設顯示年齡驗證
    document.getElementById("gate").style.display = "block";

    function enterSite() {
      document.getElementById("gate").style.display = "none";
      document.getElementById("content").style.display = "block";
    }

    function exitSite() {
      window.location.href = "https://google.com"; // 未成年轉跳
    }
  </script>

</body>
</html>
