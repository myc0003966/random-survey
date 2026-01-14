<script>
  // 1. 取得原始查詢字串（包含 ?）
  const queryString = window.location.search;

  // 2. 讀取 version
  const params = new URLSearchParams(queryString);
  const version = params.get("version");

  // 3. 設定 SurveyCake 問卷網址
  let surveyBase = "";

  if (version === "A") {
    surveyBase = "https://www.surveycake.com/s/zp7YY";
  } else if (version === "B") {
    surveyBase = "https://www.surveycake.com/s/wpWdM";
  } else {
    surveyBase = "https://www.surveycake.com/s/zp7YY"; // 保底
  }

  // 4. 正確組合網址（重點：不要再加 ?）
  const finalUrl = surveyBase + queryString;

  // 5. 導向
  window.location.replace(finalUrl);
</script>
