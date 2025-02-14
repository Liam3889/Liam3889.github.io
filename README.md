<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Dancing+Script:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Dancing Script', cursive;
            text-align: center;
            background: linear-gradient(to right, #ff9a9e, #fecfef, #ff758c);
            color: #333;
            padding: 20px;
            overflow: hidden;
            margin: 0;
        }
        h1 {
            font-size: 3.5em;
            color: #ff1a75;
            margin-bottom: 20px;
            font-family: 'Great Vibes', cursive;
        }
        img {
            width: 150px;
            margin: 20px 0;
        }
        button {
            font-size: 1.5em;
            padding: 12px 25px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 30px;
            font-family: 'Dancing Script', cursive;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
        }
        .yes {
            background-color: #ff4d4d;
            color: white;
            transition: transform 0.2s ease-in-out, background 0.3s ease-in-out, font-size 0.3s ease-in-out;
        }
        .yes:hover {
            transform: scale(1.1);
            background-color: #ff1a1a;
        }
        .no {
            background-color: #333;
            color: white;
            position: absolute;
        }
        .message-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: none;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }
        .message-container video {
            position: absolute;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .message {
            position: relative;
            z-index: 2;
            font-size: 2.5em;
            background: rgba(0, 0, 0, 0.5);
            padding: 30px;
            border-radius: 15px;
            font-family: 'Great Vibes', cursive;
        }
        .hidden {
            display: none;
        }
        footer {
            margin-top: 40px;
            font-size: 1.2em;
            color: #555;
            font-family: 'Dancing Script', cursive;
        }
    </style>
    <script>
        let yesSize = 1.5; // Initial font size in em

        function showMessage() {
            document.getElementById("main-content").classList.add("hidden");
            document.getElementById("message-container").style.display = "flex";
        }

        function moveNoButton() {
            const noButton = document.querySelector('.no');
            noButton.style.top = Math.random() * (window.innerHeight - 50) + 'px';
            noButton.style.left = Math.random() * (window.innerWidth - 100) + 'px';

            // Make the "Yes" button grow
            const yesButton = document.querySelector('.yes');
            yesSize += 0.3; // Increase size
            yesButton.style.fontSize = yesSize + "em";
            yesButton.style.padding = (yesSize * 8) + "px " + (yesSize * 16) + "px"; // Adjust padding
        }
    </script>
</head>
<body>
    <div id="main-content">
        <h1>Will you be my Valentine?</h1>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e9/Heart_corazón.svg/1024px-Heart_corazón.svg.png" alt="Heart">
        <button class="yes" onclick="showMessage()">Yes</button>
        <button class="no" onmouseover="moveNoButton()" onclick="moveNoButton()">No</button>
    </div>

    <div id="message-container" class="message-container">
        <video autoplay loop muted>
            <source src="your-video.mp4" type="video/mp4">
        </video>
        <div class="message">
            ❤️ Yay! I have a gift for you, one for today (food) and another for your shopping! ❤️<br>
            I can't wait to celebrate this beautiful day with you!<br><br>
            Love, your BF ❤️
        </div>
    </div>
</body>
</html>
