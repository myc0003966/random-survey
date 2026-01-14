<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Survey Redirect</title>
  </head>
  <body>
    <p>Redirecting to survey…</p>

    <script>
      const params = new URLSearchParams(window.location.search);
      const version = params.get("version");

      let surveyBase = "";
      if (version === "A") {
        surveyBase = "https://www.surveycake.com/s/zp7YY";
      } else if (version === "B") {
        surveyBase = "https://www.surveycake.com/s/wpWdM";
      } 

      const finalUrl = surveyBase + "?" + params.toString();
      window.location.replace(finalUrl);
    </script>
  </body>
</html>
