<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Riya 🦕❤️</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
    body {
        margin: 0;
        padding: 0;
        font-family: 'Roboto', sans-serif;
        overflow: hidden;
        background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #fff;
    }

    /* Rose petals falling */
    .petal {
        position: absolute;
        width: 20px;
        height: 20px;
        background: url('https://i.imgur.com/7b5kI5C.png') no-repeat center center;
        background-size: contain;
        animation: fall linear infinite;
    }

    @keyframes fall {
        0% { transform: translateY(-50px) rotate(0deg); opacity: 1;}
        100% { transform: translateY(110vh) rotate(360deg); opacity: 0;}
    }

    .container {
        position: relative;
        background: rgba(0,0,0,0.5);
        padding: 40px;
        border-radius: 25px;
        text-align: center;
        box-shadow: 0 0 40px rgba(0,0,0,0.6);
        z-index: 10;
        max-width: 600px;
    }

    h1 {
        font-family: 'Pacifico', cursive;
        font-size: 3em;
        margin-bottom: 20px;
        color: #ff69b4;
        text-shadow: 0 0 10px #fff, 0 0 20px #ff69b4, 0 0 30px #ff69b4;
    }

    p {
        font-size: 1.3em;
        margin-bottom: 30px;
        line-height: 1.6;
        color: #fff;
        text-shadow: 0 0 5px #000;
    }

    .buttons {
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    button {
        padding: 15px 35px;
        font-size: 1.3em;
        border: none;
        border-radius: 15px;
        cursor: pointer;
        transition: 0.3s;
        font-weight: bold;
        box-shadow: 0 0 15px rgba(0,0,0,0.3);
    }

    #yesBtn {
        background: #ff4081;
        color: #fff;
        text-shadow: 0 0 5px #fff;
    }

    #noBtn {
        background: #ffe135;
        color: #000;
        position: absolute;
        text-shadow: 0 0 5px #000;
    }

    .message {
        display: none;
        font-size: 1.4em;
        margin-top: 20px;
        line-height: 1.5;
        font-weight: bold;
        color: #ffd700;
        text-shadow: 0 0 10px #fff, 0 0 20px #ff69b4;
        animation: glow 1.5s infinite alternate;
    }

    @keyframes glow {
        0% { text-shadow: 0 0 10px #fff, 0 0 20px #ff69b4;}
        100% { text-shadow: 0 0 20px #fff, 0 0 40px #ff69b4;}
    }

    /* Floating hearts */
    .heart {
        position: absolute;
        font-size: 24px;
        animation: float 5s linear infinite;
    }

    @keyframes float {
        0% {transform: translateY(0) scale(1);}
        50% {transform: translateY(-20px) scale(1.2);}
        100% {transform: translateY(0) scale(1);}
    }

</style>
</head>
<body>

<div class="container">
    <h1>Riya 🦕❤️</h1>
    <p>Will you be my Valentine? 😌❤️</p>
    <div class="buttons">
        <button id="yesBtn">Yes 🥰</button>
        <button id="noBtn">No 😏</button>
    </div>
    <div class="message" id="loveMsg">
        <p>
        I love you more! In every universe my precious girl, your boy is my love and my best memories until I die 🧿❤️<br>
        Meeting you and looking into your beautiful eyes 🌹 my home, my safest place 😌❤️<br>
        Your Lambu - 🦍❤️
        </p>
    </div>
</div>

<script>
    // Function to create rose petals
    function createPetals() {
        for (let i = 0; i < 30; i++) {
            const petal = document.createElement('div');
            petal.classList.add('petal');
            petal.style.left = Math.random() * window.innerWidth + 'px';
            petal.style.animationDuration = 3 + Math.random() * 5 + 's';
            document.body.appendChild(petal);
        }
    }

    // Floating hearts
    function createHearts() {
        const emojis = ['💖','💘','💞','❤️'];
        for (let i = 0; i < 20; i++) {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerText = emojis[Math.floor(Math.random()*emojis.length)];
            heart.style.left = Math.random() * window.innerWidth + 'px';
            heart.style.animationDuration = 3 + Math.random()*3 + 's';
            heart.style.fontSize = 15 + Math.random()*20 + 'px';
            document.body.appendChild(heart);
        }
    }

    createPetals();
    createHearts();

    // No button moving logic
    const noBtn = document.getElementById('noBtn');
    noBtn.addEventListener('mouseover', () => {
        const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
        const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
        noBtn.style.left = x + 'px';
        noBtn.style.top = y + 'px';
    });

    // Yes button logic
    const yesBtn = document.getElementById('yesBtn');
    const loveMsg = document.getElementById('loveMsg');

    yesBtn.addEventListener('click', () => {
        loveMsg.style.display = 'block';
        yesBtn.style.display = 'none';
        noBtn.style.display = 'none';
    });

</script>
</body>
</html>
