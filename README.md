<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Lotto Recommender</title>
</head>
<body>
  <h1>로또 번호 추천기</h1>
  <button onclick="generateNumbers()">추천 번호 받기</button>
  <p id="numbers"></p>

  <script>
    function generateNumbers() {
      const numbers = [];
      while (numbers.length < 6) {
        const num = Math.floor(Math.random() * 45) + 1;
        if (!numbers.includes(num)) numbers.push(num);
      }
      document.getElementById('numbers').innerText = '추천 번호: ' + numbers.join(', ');
    }
  </script>
</body>
</html>
