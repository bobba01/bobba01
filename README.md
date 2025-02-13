<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
            background-color: #f5f5f5;
            position: relative;
            height: 100vh;
            overflow: hidden;
        }
        h1 {
            font-size: 36px;
            color: #ff69b4;
        }
        .btn {
            padding: 15px 30px;
            font-size: 18px;
            margin: 10px;
            cursor: pointer;
            border-radius: 5px;
            border: 2px solid #ff69b4;
            background-color: #ffb6c1;
            color: white;
            transition: all 0.3s ease;
        }
        .btn:hover {
            background-color: #ff69b4;
        }
        .message {
            font-size: 24px;
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>

    <h1>Will you be my Valentine?</h1>

    <button class="btn" id="yesButton" onclick="yesClicked()">Yes</button>
    <button class="btn" id="noButton" onclick="noClicked()">No</button>

    <div class="message" id="response"></div>

    <script>
        function yesClicked() {
            // Hide both buttons and show the message
            document.getElementById('yesButton').style.display = 'none';
            document.getElementById('noButton').style.display = 'none';
            document.getElementById('response').style.display = 'block';
            document.getElementById('response').innerText = "I love you my munchkin, my Valentine always and forever ❤️";
        }

        function noClicked() {
            // Make the "No" button move randomly on the screen
            const noButton = document.getElementById('noButton');
            noButton.style.position = 'absolute';
            noButton.style.left = Math.random() * (window.innerWidth - noButton.offsetWidth) + 'px';
            noButton.style.top = Math.random() * (window.innerHeight - noButton.offsetHeight) + 'px';
            
            // Grow the "Yes" button gradually
            const yesButton = document.getElementById('yesButton');
            yesButton.style.transform = 'scale(' + (1 + Math.random() * 0.2) + ')';
            yesButton.style.transition = 'transform 0.5s ease';
        }
    </script>

</body>
</html>
