# random-survey
Simple scripts for random survey assignment and experiment flow control.
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <title>問卷分流中</title>
  <script>
    window.onload = function () {

      // 👉 在這裡放你的問卷連結
      const surveys = [
        "https://www.surveycake.com/s/zp7YY?version=A", // 情境 A
        "https://www.surveycake.com/s/wpWdM?version=B", // 情境 B
      ];

      // 隨機抽一個
      const randomIndex = Math.floor(Math.random() * surveys.length);

      // 導向問卷
      window.location.href = surveys[randomIndex];
    };
  </script>
</head>
<body>
  <p>問卷載入中，請稍候…</p>
</body>
</html>
