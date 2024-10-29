<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bet Spots</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: black; /* Fundo preto */
            overflow: hidden; /* Impede rolagem */
            height: 100vh; /* Garante que o corpo ocupe toda a altura da tela */
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            position: relative; /* Para posicionar o conteúdo sobre o vídeo */
            padding-bottom: 20px; /* Espaço para o botão e iframe */
        }
        .betSpots {
            display: flex;
            justify-content: space-between;
            width: 100%;
            max-width: 900px;
            margin-top: 20px; /* Espaço acima dos bet spots */
        }
        .betSpot1, .betSpot2, .betSpot3 {
            position: relative;
        }
        .fullSize {
            width: 100%;
            height: auto;
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
            z-index: 1; /* Garante que o botão esteja acima do overlay */
        }
        .pulsar {
            animation: pulsar 0.5s infinite;
        }
        @keyframes pulsar {
            0% { box-shadow: 0 0 0 rgba(255, 0, 0, 0.7); }
            50% { box-shadow: 0 0 20px rgba(255, 255, 255, 1); }
            100% { box-shadow: 0 0 0 rgba(255, 255, 255, 0.7); }
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
            z-index: 0; /* Fica abaixo do botão */
        }
        iframe {
        width: 100vw; 
        height: 150vh;
        border: none; 
    }
        @media (max-width: 600px) {
            .number-display {
                font-size: 20px; /* Reduz o tamanho da fonte para telas menores */
            }
            .button {
                font-size: 14px; /* Reduz o tamanho do botão para telas menores */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="betSpots">
            <div class="betSpot3 Player" data-role="bacbo-bet-spot-Player">
                <div class="fullSize">
                    <svg class="svg" width="300" height="228" viewBox="0 0 300 228" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.75 50C0.75 22.8 22.8 0.75 50 0.75H299.25V10.3315C254.184 12.294 218.25 49.4505 218.25 95V133C218.25 178.55 254.184 215.706 299.25 217.669V227.25H50C22.8 227.25 0.75 205.2 0.75 178V50Z" fill="#0038A5" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display3"></div>
                <div class="number-display" style="font-size: 20px; position: absolute; bottom: 10px; left: 25%; transform: translateX(-50%); color: white;">PLAYER</div>
            </div>

            <div class="betSpot2 Tie" data-role="bacbo-bet-spot-Tie">
                <div class="fullSize">
                    <svg class="svg" width="156" height="194" viewBox="0 0 156 194" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M78 193.25C35.336 193.25 0.75 158.664 0.75 116V78C0.75 35.336 35.336 0.75 78 0.75C120.664 0.75 155.25 35.336 155.25 78V116C155.25 158.664 120.664 193.25 78 193.25Z" fill="#CC8915" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display2"></div>
                <div class="number-display" style="font-size: 16px; position: absolute; bottom: 10px; left: 50%; transform: translateX(-50%); color: white;">TIE</div>
            </div>

            <div class="betSpot1 Banker" data-role="bacbo-bet-spot-Banker">
                <div class="fullSize">
                    <svg class="svg" width="300" height="228" viewBox="0 0 300 228" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M250 0.75C277.2 0.75 299.25 22.8 299.25 50V178C299.25 205.2 277.2 227.25 250 227.25H0.75V217.669C45.8164 215.706 81.75 178.55 81.75 133V95C81.75 49.4504 45.8164 12.294 0.75 10.3315V0.75H250Z" fill="#87200F" fill-opacity="0.95"></path>
                    </svg>
                </div>
                <div class="number-display" id="display1"></div>
                <div class="number-display" style="font-size: 20px; position: absolute; bottom: 18px; left: 75%; transform: translateX(-50%); color: white;">BANKER</div>
            </div>
        </div>
        
        <button class="button" onclick="generateRandomNumber()">Clique Aqui</button>

        <div id="hackingOverlay" class="hacking-effect" style="opacity: 0;">HACKEANDO DADOS...</div>
    </div>

    <iframe src="https://blaze.com/pt/games/bac-bo-ao-vivo"></iframe>

    <script>
        function generateRandomNumber() {
            const overlay = document.getElementById('hackingOverlay');
            overlay.style.opacity = '1'; // Mostra o overlay
            setTimeout(() => {
                overlay.style.opacity = '0'; // Esconde o overlay
                const randomNum = Math.floor(Math.random() * (12 - 7 + 1)) + 7;
                const betSpots = ['display1', 'display2', 'display3'];
                const randomSpot = betSpots[Math.floor(Math.random() * betSpots.length)];

                const displayElement = document.getElementById(randomSpot);
                displayElement.textContent = randomNum;

                // Adiciona a classe de animação
                const betSpotElement = displayElement.closest('.betSpot1') || displayElement.closest('.betSpot2') || displayElement.closest('.betSpot3');
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
