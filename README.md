# random-survey
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Survey Redirect</title>
  </head>
  <body>
    <p>Redirecting to survey…</p>

    <script>
      // 1. 取得所有網址參數（保留 Connect IDs）
      const params = new URLSearchParams(window.location.search);

      // 2. 讀取 version（A / B）
      const version = params.get("version");

      // 3. SurveyCake 問卷網址（請換成你自己的）
      let surveyBase = "";

      if (version === "A") {
        surveyBase = "https://www.surveycake.com/s/zp7YY"; // A 問卷
      } else if (version === "B") {
        surveyBase = "https://www.surveycake.com/s/wpWdM"; // B 問卷
      } 

      // 4. 組合最終網址（所有參數原封不動帶過去）
      const finalUrl = surveyBase + "?" + params.toString();

      // 5. 導向
      window.location.replace(finalUrl);
    </script>
  </body>
</html>
