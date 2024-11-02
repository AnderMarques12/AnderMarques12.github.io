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
        .left-video {
            left: 9%;
        }
        .right-video {
            right: -66%;
        }
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
        .betSpot1 {
            top: 12px;
            left: 128px;
        }
        .betSpot2 {
            position: absolute;
            top: 48px;
            left: 584px;
        }
        .betSpot3 {
            position: absolute;
            top: 32px;
            left: 670px;
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
        .button:active {
            transform: translateY(1px);
            box-shadow: 0 0 15px rgba(0, 0, 255, 0.5);
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
        .dice-container {
            display: flex;
            justify-content: center;
            margin-top: 10px;
        }
        .dice {
            width: 40px;
            height: 40px;
            border: 4px solid;
            border-radius: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            margin: 0 5px;
        }
        .dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            position: absolute;
        }
        .dots {
            position: relative;
            width: 100%;
            height: 100%;
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
            <div class="betSpot betSpot1" id="betSpot3">
                <svg class="svg" width="300" height="228" viewBox="0 0 300 228" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <filter id="f3" x="-20%" y="-20%" width="140%" height="140%">
                            <feGaussianBlur in="SourceAlpha" stdDeviation="5" />
                            <feOffset dx="0" dy="0" result="offsetblur" />
                            <feFlood flood-color="rgba(0, 255, 255, 0.8)" />
                            <feComposite in2="offsetblur" operator="in" />
                            <feMerge>
                                <feMergeNode />
                                <feMergeNode in="SourceGraphic" />
                            </feMerge>
                     
                    </defs>
                    <path d="M0.75 50C0.75 22.8 22.8 0.75 50 0.75H299.25V10.3315C254.184 12.294 218.25 49.4505 218.25 95V133C218.25 178.55 254.184 215.706 299.25 217.669V227.25H50C22.8 227.25 0.75 205.2 0.75 178V50Z" fill="none" stroke="url(#grad3)" stroke-width="3" />
                    <defs>
                        <linearGradient id="grad3" x1="0%" y1="0%" x2="100%" y2="100%">
                            <stop offset="0%" style="stop-color:#00bcd4; stop-opacity:1" />
                            <stop offset="100%" style="stop-color:#009688; stop-opacity:1" />
                        </linearGradient>
                    </defs>
                </svg>
                <div class="number-display" id="display3"></div>
                <div class="dice-container" id="dice3"></div>
                <div class="number-display" style="font-size: 16px; position: absolute; top: 5px; left: 50%; transform: translateX(-50%); color: white;">PLAYER</div>
            </div>

            <div class="betSpot betSpot2" id="betSpot2">
                <svg class="svg" width="156" height="194" viewBox="0 0 156 194" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <filter id="f2" x="-20%" y="-20%" width="140%" height="140%">
                            <feGaussianBlur in="SourceAlpha" stdDeviation="5" />
                            <feOffset dx="0" dy="0" result="offsetblur" />
                            <feFlood flood-color="rgba(255, 193, 7, 0.8)" />
                            <feComposite in2="offsetblur" operator="in" />
                            <feMerge>
                                <feMergeNode />
                                <feMergeNode in="SourceGraphic" />
                            </feMerge>
                        
                    </defs>
                    <path d="M78 193.25C35.336 193.25 0.75 158.664 0.75 116V78C0.75 35.336 35.336 0.75 78 0.75C120.664 0.75 155.25 35.336 155.25 78V116C155.25 158.664 120.664 193.25 78 193.25Z" fill="none" stroke="url(#grad2)" stroke-width="3" />
                    <defs>
                        <linearGradient id="grad2" x1="0%" y1="0%" x2="100%" y2="100%">
                            <stop offset="0%" style="stop-color:#fbc02d; stop-opacity:1" />
                            <stop offset="100%" style="stop-color:#f9a825; stop-opacity:1" />
                        </linearGradient>
                    </defs>
                </svg>
                <div class="number-display" id="display2"></div>
                <div class="dice-container" id="dice2"></div>
                <div class="number-display" style="font-size: 16px; position: absolute; top: 5px; left: 50%; transform: translateX(-50%); color: white;">TIE</div>
            </div>

            <div class="betSpot betSpot3" id="betSpot1">
                <svg class="svg" width="300" height="228" viewBox="0 0 300 228" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <filter id="f1" x="-20%" y="-20%" width="140%" height="140%">
                            <feGaussianBlur in="SourceAlpha" stdDeviation="5" />
                            <feOffset dx="0" dy="0" result="offsetblur" />
                            <feFlood flood-color="rgba(255, 82, 82, 0.8)" />
                            <feComposite in2="offsetblur" operator="in" />
                            <feMerge>
                                <feMergeNode />
                                <feMergeNode in="SourceGraphic" />
                            </feMerge>
                       
                    </defs>
                    <path d="M250 0.75C277.2 0.75 299.25 22.8 299.25 50V178C299.25 205.2 277.2 227.25 250 227.25H0.75V217.669C45.8164 215.706 81.75 178.55 81.75 133V95C81.75 49.4504 45.8164 12.294 0.75 10.3315V0.75H250Z" fill="none" stroke="url(#grad1)" stroke-width="3" />
                    <defs>
                        <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="100%">
                            <stop offset="0%" style="stop-color:#ff5722; stop-opacity:1" />
                            <stop offset="100%" style="stop-color:#f44336; stop-opacity:1" />
                        </linearGradient>
                    </defs>
                </svg>
                <div class="number-display" id="display1"></div>
                <div class="dice-container" id="dice1"></div>
                <div class="number-display" style="font-size: 16px; position: absolute; top: 5px; left: 50%; transform: translateX(-50%); color: white;">BANKER</div>
            </div>
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

                // Gera dois números aleatórios para os dados
                const die1 = Math.floor(Math.random() * 6) + 1;
                const die2 = Math.floor(Math.random() * 6) + 1;

                // Atualiza os dados correspondentes
                const diceContainer = document.getElementById(`dice${randomSpot.charAt(randomSpot.length - 1)}`);
                const diceColor = getDiceColor(randomSpot);

                diceContainer.innerHTML = `
                    <div class="dice" style="border-color: ${diceColor};">
                        <div class="dots">${createDots(die1, diceColor)}</div>
                        <div class="number-display" style="color: ${diceColor}; font-weight: bold; font-size: 16px; position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);">${die1}</div>
                    </div>
                    <div class="dice" style="border-color: ${diceColor};">
                        <div class="dots">${createDots(die2, diceColor)}</div>
                        <div class="number-display" style="color: ${diceColor}; font-weight: bold; font-size: 16px; position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);">${die2}</div>
                    </div>
                `;

                // Adiciona pulsação ao número gerado
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
            if (spot === 'display1') return '#ff5722'; // Cor do BANKER
            if (spot === 'display2') return '#fbc02d'; // Cor do TIE
            return '#00bcd4'; // Cor do PLAYER
        }

        function createDots(num, color) {
            const dotPositions = [
                [],
                [[1, 1]], // 1 ponto
                [[0, 0], [2, 2]], // 2 pontos
                [[0, 0], [1, 1], [2, 2]], // 3 pontos
                [[0, 0], [0, 2], [2, 0], [2, 2]], // 4 pontos
                [[0, 0], [0, 2], [1, 1], [2, 0], [2, 2]], // 5 pontos
                [[0, 0], [0, 2], [1, 1], [2, 0], [2, 1], [2, 2]] // 6 pontos
            ];

            return dotPositions[num - 1].map(pos => {
                const dotStyle = {
                    top: `${pos[0] * 10 + 8}px`,
                    left: `${pos[1] * 10 + 8}px`,
                    backgroundColor: color,
                    visibility: 'visible'
                };
                return `<div class="dot" style="position: absolute; ${Object.entries(dotStyle).map(([k, v]) => `${k}: ${v};`).join(' ')}"></div>`;
            }).join('');
        }
    </script>
</body>
</html>
