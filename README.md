<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Website</title>
    <style>
body {
    margin: 0;
    overflow: hidden;
    background-color: black; /* Set initial background color to black */
}

        #background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            object-fit: cover;
        }

        #content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            color: white;
        }

        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            z-index: 2;
            font-size: 20px;
            color: white;
            cursor: pointer;
        }

        #panel {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 492px;
    height: 331px;
    padding: 20px;
    background: rgb(20, 20, 23); /* Set the color using RGB values */
    color: white;
    text-align: center;
    z-index: 3;
    display: none;
    border-radius: 15px;
}

#profilePicture {
    width: 161px; /* Set the width to 161 pixels */
    height: 150px; /* Set the height to 150 pixels */
    border-radius: 50%;
    margin-bottom: 10px;
    position: absolute;
    top: -75px; /* Half of the height to position it halfway off the panel */
    left: 50%;
    transform: translateX(-50%);
}
#panel p {
    margin-top: 75px;
    font-size: 24px;
    font-weight: bold; /* Set the font weight to bold */
}

    </style>
</head>

<body>
    <audio id="myAudio" autoplay>
        <source src="your-video.mp4" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>

    <img id="background" src="main.gif" alt="Background Image">

    <div id="overlay" onclick="startAudio()">
        [+] Please click the screen to enter the website
    </div>

    <div id="panel">
        <img id="profilePicture" src="server icon.png" alt="Your Profile Picture">
        <p>Peruse Services</p>
        <!-- Add more profile information or content here as needed -->
    </div>

    <script>
        function startAudio() {
            var overlay = document.getElementById('overlay');
            var audio = document.getElementById('myAudio');
            var panel = document.getElementById('panel');
            var body = document.body;
            
            audio.play();
            overlay.style.display = 'none';
            panel.style.display = 'block';
            body.style.backgroundColor = 'transparent'; // Change the background color to transparent
        }
    </script>

<div id="panel">
    <a href="https://peruseservices.com" target="_blank">
        <img id="profilePicture" src="your-profile-picture.jpg" alt="Your Profile Picture">
        <p>Your Name</p>
    </a>
    <!-- Add more profile information or content here as needed -->
</div>
</body>

</html>
