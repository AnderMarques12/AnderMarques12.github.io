<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Bac Bo</title>
    <style>
        body {
            background-color: black;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            overflow: hidden;
            height: 100vh;
            position: relative;
        }
        video {
            position: fixed;
            top: 7%;
            min-width: 34%;
            min-height: 14%;
            z-index: 0;
            transform: translate(-50%, -50%);
            object-fit: cover;
        }
        .left-video { left: 9%; }
        .right-video { right: -66%; }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            position: relative;
            padding-bottom: 20px;
            z-index: 1;
        }
        .betSpots {
            display: flex;
            justify-content: space-between;
            width: 100%;
            max-width: 900px;
            margin-top: 20px;
        }
        .betSpot {
            position: relative;
            transition: transform 0.5s;
            flex: 1;
            max-width: 250px;
            margin: 0 10px;
            text-align: center;
        }
        .button {
            margin: 20px 0;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            z-index: 1;
            border: none;
            border-radius: 12px;
            background: linear-gradient(45deg, #00f, #00d);
            color: white;
            text-shadow: 0 0 5px rgba(0, 255, 255, 0.8);
            box-shadow: 0 0 20px rgba(0, 0, 255, 0.8);
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .button:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 30px rgba(0, 0, 255, 1);
        }
        .number-display {
            font-size: 24px;
            color: white;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-shadow: 1px 1px 2px black;
            padding: 5px;
            border-radius: 5px;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        .pulsate {
            animation: pulse 1.5s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <video class="left-video" autoplay muted loop>
        <source src="https://static.vecteezy.com/system/resources/previews/024/148/810/artificial-intelligence-network-ai-line-circuit-technology-data-transfer-abstract-5g-background-free-video.webm" type="video/webm">
        Seu navegador não suporta o elemento de vídeo.
    </video>
    
    <video class="right-video" autoplay muted loop>
        <source src="https://static.vecteezy.com/system/resources/previews/024/148/810/artificial-intelligence-network-ai-line-circuit-technology-data-transfer-abstract-5g-background-free-video.webm" type="video/webm">
        Seu navegador não suporta o elemento de vídeo.
    </video>

    <div class="container">
        <div class="betSpots">
            <!-- Bet Spots Code (as you have it) -->
        </div>
        <button class="button" onclick="generateRandomNumber()">HACKEAR BACBO</button>
    </div>

    <audio id="hackSound" src="hack_sound.mp3" preload="auto"></audio>

    <script>
        function generateRandomNumber() {
            const button = document.querySelector('.button');
            button.textContent = "CARREGANDO...";
            button.disabled = true;

            setTimeout(() => {
                const randomNum = Math.floor(Math.random() * (12 - 7 + 1)) + 7;
                const betSpots = ['display1', 'display2', 'display3'];
                const randomSpot = betSpots[Math.floor(Math.random() * betSpots.length)];

                const displayElement = document.getElementById(randomSpot);
                displayElement.textContent = randomNum;

                // Gera dados
                const die1 = Math.floor(Math.random() * 6) + 1;
                const die2 = Math.floor(Math.random() * 6) + 1;

                // Atualiza dados correspondentes
                const diceContainer = document.getElementById(`dice${randomSpot.charAt(randomSpot.length - 1)}`);
                const diceColor = getDiceColor(randomSpot);

                diceContainer.innerHTML = `
                    <div class="dice" style="border-color: ${diceColor};">
                        ${createDots(die1, diceColor)}
                        <div class="number-display" style="color: ${diceColor}; font-weight: bold;">${die1}</div>
                    </div>
                    <div class="dice" style="border-color: ${diceColor};">
                        ${createDots(die2, diceColor)}
                        <div class="number-display" style="color: ${diceColor}; font-weight: bold;">${die2}</div>
                    </div>
                `;

                displayElement.classList.add('pulsate');

                const betSpotElement = document.getElementById(randomSpot).closest('.betSpot');
                betSpotElement.classList.add('pulsate');

                setTimeout(() => {
                    displayElement.classList.remove('pulsate');
                    betSpotElement.classList.remove('pulsate');
                    setTimeout(() => {
                        displayElement.textContent = '';
                        diceContainer.innerHTML = '';
                    }, 1000);
                }, 4000);

                button.textContent = "HACKEAR BACBO";
                button.disabled = false;
            }, 2000);
        }

        function getDiceColor(spot) {
            if (spot === 'display1') return '#ff5722';
            if (spot === 'display2') return '#fbc02d';
            return '#00bcd4';
        }

        function createDots(num, color) {
            const dotPositions = [
                [], [[1, 1]], [[0, 0], [2, 2]], [[0, 0], [1, 1], [2, 2]],
                [[0, 0], [0, 2], [2, 0], [2, 2]], [[0, 0], [0, 2], [1, 1], [2, 0], [2, 2]],
                [[0, 0], [0, 2], [1, 1], [2, 0], [2, 1], [2, 2]]
            ];

            return dotPositions[num - 1].map(pos => {
                return `<div class="dot" style="top: ${pos[0] * 10 + 8}px; left: ${pos[1] * 10 + 8}px; background-color: ${color};"></div>`;
            }).join('');
        }
    </script>
</body>
</html>
