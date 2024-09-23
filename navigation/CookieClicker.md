---
layout: page
title: Cookie Clicker
permalink: /cookieclicker/
---

{% include nav/home.html %}

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 200vh;
            background-color: #F0F0F0;
        }
        #cookie {
            width: 250px; /* Increase the cookie size */
            cursor: pointer;
            margin-bottom: 20px;
        }
        #score {
            font-size: 32px; /* Increase score text size */
            color: black;
        }
        .game-container {
            background-color: #333; /* Add a background color */
            padding: 30px; /* Increase padding for a bigger box */
            border-radius: 10px; /* Rounded corners for a smoother look */
            width: 350px; /* Increase container width */
            text-align: center;
        }
    </style>
</head>
<body>
    <h1><b style="font-family: 'Fredericka the Great'; color: #9e2a2b; font-size:25px;">Cookie Clicker</b></h1>
     <img id="cookie" src="https://prettysimplesweet.com/wp-content/uploads/2020/07/Big-Chocolate-Chip-Cookies-150x150.jpg" alt="Cookie">
    <div id="score">Score: 0</div>
    <audio id="clickSound" src="{{site.baseurl}}/assets/js/click-151673.mp3"></audio>
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

