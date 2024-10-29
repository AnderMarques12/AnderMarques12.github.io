<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Bac Bo</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: black;
            overflow: hidden;
            height: 100vh;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            position: relative;
            padding-bottom: 20px;
        }

        .betSpots {
            display: flex;
            justify-content: space-between; /* Distribui os itens */
            width: 100%;
            max-width: 900px;
            margin-top: 20px;
        }

        .betSpot1 {
    position: relative;
    transition: transform 0.5s;
    flex: 1;
    left: 116px;
    max-width: 300px;
    top: 0px;
}
.betSpot2 {
    position: absolute;
    transition: transform 0.5s;
    flex: 1;
    left: 347px;
    max-width: 300px;
    top: 39px;
}
                  
.betSpot3 {
    position: absolute;
    transition: transform 0.5s;
    flex: 1;
    left: 432px;
    max-width: 300px;
    top: 21px;
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

        .pulsar {
            animation: pulsar 1s infinite; /* Alterado para animação de pulsar */
        }

        @keyframes pulsar {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); } /* Crescendo */
        }

        .number-display {
            font-size: 24px;
            color: white;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-shadow: 1px 1px 2px black;
        }

        .hacking-effect {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 48px;
            opacity: 0;
            transition: opacity 0.5s ease;
            z-index: 0;
        }

        .hack-message {
            font-size: 24px;
            animation: blink 1s infinite; /* Animação de piscar */
            color: #00ff00;
            margin-top: 20px;
        }

        @keyframes blink {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        .light-effect {
            position: absolute;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            animation: light 1s infinite alternate; /* Efeito de luz */
            z-index: -1;
        }

        @keyframes light {
            0% { transform: scale(1); }
            100% { transform: scale(1.05); }
        }

        .data-loading {
            color: #00ff00;
            font-size: 20px;
            position: absolute;
            bottom: 30px;
            opacity: 0;
            animation: dataBlink 1s infinite;
        }

        @keyframes dataBlink {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        iframe {
            border: none;
            width: 100%; 
            height: 150vh;
            margin-top: 20px;
            z-index: 0;
            position: relative;
        }

        @media (max-width: 600px) {
            .number-display {
                font-size: 20px;
            }
            .button {
                font-size: 14px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="betSpots">
            <div class="betSpot1" id="betSpot3">
                <div class="fullSize">
                    <svg class="svg" width="300" height="228" viewBox="0 0 300 228" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.75 50C0.75 22.8 22.8 0.75 50 0.75H299.25V10.3315C254.184 12.294 218.25 49.4505 218.25 95V133C218.25 178.55 254.184 215.706 299.25 217.669V227.25H50C22.8 227.25 0.75 205.2 0.75 178V50Z" fill="#0038A5" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display3"></div>
                <div class="number-display" style="font-size: 20px; position: absolute; bottom: 10px; left: 25%; transform: translateX(-50%); color: white;">PLAYER</div>
            </div>

            <div class="betSpot2" id="betSpot2">
                <div class="fullSize">
                    <svg class="svg" width="156" height="194" viewBox="0 0 156 194" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M78 193.25C35.336 193.25 0.75 158.664 0.75 116V78C0.75 35.336 35.336 0.75 78 0.75C120.664 0.75 155.25 35.336 155.25 78V116C155.25 158.664 120.664 193.25 78 193.25Z" fill="#CC8915" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display2"></div>
                <div class="number-display" style="font-size: 16px; position: absolute; bottom: 10px; left: 50%; transform: translateX(-50%); color: white;">TIE</div>
            </div>

            <div class="betSpot3" id="betSpot1">
                <div class="fullSize">
                    <svg class="svg" width="300" height="228" viewBox="0 0 300 228" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M250 0.75C277.2 0.75 299.25 22.8 299.25 50V178C299.25 205.2 277.2 227.25 250 227.25H0.75V217.669C45.8164 215.706 81.75 178.55 81.75 133V95C81.75 49.4504 45.8164 12.294 0.75 10.3315V0.75H250Z" fill="#87200F" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display1"></div>
                <div class="number-display" style="font-size: 20px; position: absolute; bottom: 18px; left: 75%; transform: translateX(-50%); color: white;">BANKER</div>
            </div>
        </div>

        <button class="button" onclick="generateRandomNumber()">HACKEAR BACBO</button>

        <div id="hackingOverlay" class="hacking-effect">
            <div class="light-effect"></div>
            <div class="hack-message">HACKING...</div>
            <div class="data-loading">CARREGANDO DADOS...</div>
        </div>
    </div>

    <iframe src="https://blaze.com/pt/games/bac-bo-ao-vivo"></iframe>

    <audio id="hackSound" src="hack_sound.mp3" preload="auto"></audio>

    <script>
        function generateRandomNumber() {
            const overlay = document.getElementById('hackingOverlay');
            const hackMessage = document.querySelector('.hack-message');
            const lightEffect = document.querySelector('.light-effect');
            const dataLoading = document.querySelector('.data-loading');
            const hackSound = document.getElementById('hackSound');

            overlay.style.opacity = '1'; // Mostra o overlay
            hackMessage.style.opacity = '1'; // Mostra a mensagem de hacking
            lightEffect.style.animationPlayState = 'running'; // Inicia o efeito de luz
            dataLoading.style.opacity = '1'; // Mostra o texto de carregando
            hackSound.play(); // Toca o som de hacking

            setTimeout(() => {
                overlay.style.opacity = '0'; // Esconde o overlay
                hackMessage.style.opacity = '0'; // Esconde a mensagem de hacking
                lightEffect.style.animationPlayState = 'paused'; // Para o efeito de luz
                dataLoading.style.opacity = '0'; // Esconde o texto de carregando
                hackSound.pause(); // Para o som de hacking

                const randomNum = Math.floor(Math.random() * (12 - 7 + 1)) + 7;
                const betSpots = ['display1', 'display2', 'display3'];
                const randomSpot = betSpots[Math.floor(Math.random() * betSpots.length)];

                const displayElement = document.getElementById(randomSpot);
                displayElement.textContent = randomNum;

                // Adiciona a classe de animação de pulsar
                const betSpotElement = displayElement.closest('.betSpot');
                betSpotElement.classList.add('pulsar');

                setTimeout(() => {
                    displayElement.textContent = '';
                    // Remove a classe de animação
                    betSpotElement.classList.remove('pulsar');
                }, 4000);
            }, 2000); // Duração do efeito de hackeando (2 segundos)
        }
    </script>
</body>
</html>
