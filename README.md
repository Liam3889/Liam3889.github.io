<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #ffe6e6;
            color: #333;
            padding: 20px;
        }
        h1 {
            font-size: 3em;
            color: #ff1a75;
            margin-bottom: 20px;
        }
        img {
            width: 150px;
            margin: 20px 0;
        }
        button {
            font-size: 1.2em;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .yes {
            background-color: #ff4d4d;
            color: white;
            transition: transform 0.2s ease-in-out;
        }
        .yes:hover {
            transform: scale(1.1);
        }
        .no {
            background-color: #333;
            color: white;
            position: absolute;
        }
        .message {
            margin-top: 20px;
            font-size: 1.5em;
            color: darkblue;
        }
        .hidden {
            display: none;
        }
        footer {
            margin-top: 40px;
            font-size: 1em;
            color: #555;
        }
    </style>
    <script>
        function showInvitation() {
            const mainContent = document.getElementById("main-content");
            const invitationContent = document.getElementById("invitation-content");

            // Hide the main content and show the invitation
            mainContent.classList.add("hidden");
            invitationContent.classList.remove("hidden");
        }

        function moveNoButton() {
            const noButton = document.querySelector('.no');
            noButton.style.top = Math.random() * (window.innerHeight - 50) + 'px';
            noButton.style.left = Math.random() * (window.innerWidth - 100) + 'px';
        }
    </script>
</head>
<body>
    <div id="main-content">
        <h1>Will you be my Valentine?</h1>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e9/Heart_corazón.svg/1024px-Heart_corazón.svg.png" alt="Heart">
        <button class="yes" onclick="showInvitation()">Yes</button>
        <button class="no" onmouseover="moveNoButton()">No</button>
    </div>

    <div id="invitation-content" class="hidden">
        <h1>Congratulations!</h1>
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/33/Hyatt_logo.png" alt="Hyatt Place" style="width: 300px;">
        <p>You are invited to stay at <strong>Hyatt Place</strong> for a romantic getaway this Valentine's Day (14th February).</p>
        <p>Looking forward to celebrating this special day with you!</p>
    </div>

    <footer>
        Made with ❤️ for Valentine's Day!
    </footer>
</body>
</html>
