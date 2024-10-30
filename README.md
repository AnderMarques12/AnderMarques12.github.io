<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Bac Bo</title>
    <style>
        body {
            background-color: black; /* Fundo preto */
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
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            object-fit: cover;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            max-width: 900px; /* Tamanho máximo */
            position: relative;
            z-index: 1;
        }

        .betSpots {
            display: flex;
            justify-content: space-between;
            width: 100%;
            max-width: 900px;
            margin: 20px 0;
        }

        .betSpot {
            position: relative;
            transition: transform 0.5s;
            flex: 1;
            margin: 0 10px; /* Margem entre os betSpots */
            overflow: hidden; /* Para esconder bordas */
        }

        .betSpot svg {
            filter: drop-shadow(0 0 20px rgba(0, 255, 255, 0.8)); /* Efeito de sombra */
        }

        .betSpot:hover {
            transform: scale(1.05); /* Aumenta ao passar o mouse */
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

        iframe {
            width: 100%;
            height: 500px; /* Altura fixa para o iframe */
            margin-top: 20px;
            z-index: 0;
            border: none; /* Remove a borda padrão */
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
    <video autoplay muted loop>
        <source src="https://static.vecteezy.com/system/resources/previews/024/148/810/artificial-intelligence-network-ai-line-circuit-technology-data-transfer-abstract-5g-background-free-video.webm" type="video/webm">
        Seu navegador não suporta o elemento de vídeo.
    </video>

    <div class="container">
        <div class="betSpots">
            <div class="betSpot" id="betSpot3">
                <div class="fullSize">
                    <svg class="svg" width="300" height="228" viewBox="0 0 300 228" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.75 50C0.75 22.8 22.8 0.75 50 0.75H299.25V10.3315C254.184 12.294 218.25 49.4505 218.25 95V133C218.25 178.55 254.184 215.706 299.25 217.669V227.25H50C22.8 227.25 0.75 205.2 0.75 178V50Z" fill="#0038A5" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display3"></div>
                <div class="number-display" style="font-size: 20px; position: absolute; bottom: 10px; left: 25%; transform: translateX(-50%); color: white;">PLAYER</div>
            </div>

            <div class="betSpot" id="betSpot2">
                <div class="fullSize">
                    <svg class="svg" width="156" height="194" viewBox="0 0 156 194" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M78 193.25C35.336 193.25 0.75 158.664 0.75 116V78C0.75 35.336 35.336 0.75 78 0.75C120.664 0.75 155.25 35.336 155.25 78V116C155.25 158.664 120.664 193.25 78 193.25Z" fill="#CC8915" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display2"></div>
                <div class="number-display" style="font-size: 16px; position: absolute; bottom: 10px; left: 50%; transform: translateX(-50%); color: white;">TIE</div>
            </div>

            <div class="betSpot" id="betSpot1">
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
    </div>

    <iframe src="https://blaze.com/pt/games/bac-bo-ao-vivo"></iframe>

    <audio id="hackSound" src="hack_sound.mp3" preload="auto"></audio>

    <script>
        function generateRandomNumber() {
            const randomNum = Math.floor(Math.random() * (12 - 7 + 1)) + 7;
            const betSpots = ['display1', 'display2', 'display3'];
            const randomSpot = betSpots[Math.floor(Math.random() * betSpots.length)];

            const displayElement = document.getElementById(randomSpot);
            displayElement.textContent = randomNum;

            setTimeout(() => {
                displayElement.textContent = '';
            }, 4000);
        }
    </script>
</body>
</html>
