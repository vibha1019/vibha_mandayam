<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cookie Clicker Game</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        #cookie {
            width: 150px;
            cursor: pointer;
            margin-bottom: 20px;
        }
        #score {
            font-size: 24px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Cookie Clicker</h1>
    <img src="https://i.imgur.com/bvCoIjo.png" alt="Cookie" id="cookie">
    <div id="score">Score: 0</div>
    
    <audio id="clickSound" src="https://www.soundjay.com/button/button-1.mp3"></audio>

    <script>
        let score = 0;
        const cookie = document.getElementById('cookie');
        const scoreDisplay = document.getElementById('score');
        const clickSound = document.getElementById('clickSound');

        cookie.addEventListener('click', function() {
            score++;
            scoreDisplay.textContent = 'Score: ' + score;
            clickSound.play();
        });
    </script>
</body>
</html>
