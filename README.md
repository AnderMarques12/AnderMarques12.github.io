<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>




    <style>
        @import url('https://fonts.googleapis.com/css2?family=M+PLUS+1+Code&display=swap');
       

  

/* Estilo da animação de carregamento */
.loading-hidden {
    display: none;
}

.loading-visible {
    display: block;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
}

.spinner {
    border: 8px solid #f3f3f3;
    border-radius: 50%;
    border-top: 8px solid #3498db;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* Estilo do container de imagem */
#image-container img {
    max-width: 100%;
    height: auto;
}
.context-options {
    display: none; /* Inicialmente escondido */
    position: fixed;
    top: 75%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgb(0, 0, 0);
    padding: 20px;
    border-radius: 10px;
    font-family: 'M PLUS 1 Code', sans-serif;
    color: #ffffff;
    z-index: 10000; /* Garante que fique sobre outros elementos */
}



        .context-options img {
            width: 100px;
            margin: 0 auto 20px;
            display: block;
        }

        .context-options .bot-title {
            font-size: 20px;
            text-align: center;
            margin-bottom: 20px;
            color: #ffffff;
        }

        .context-options .context-option {
            display: block;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(255, 0, 0);
            /* Preto transparente */
            border-radius: 5px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }

        .context-options .context-option:last-child {
            margin-bottom: 0;
        }

        .context-options .closeContextOptions:hover {
    background-color: rgba(255, 0, 0, 1);
}

        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1);
            /* Fundo vermelho mais opaco ao passar o mouse */
        }

        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            /* Texto branco */
            margin-top: 20px;
        }

        .time {
            font-size: 14px;
            /* Tamanho da fonte reduzido */
            color: #ffffff;
            position: fixed;
            top: 10px;
            /* Distância do topo */
            right: 10px;
            /* Distância da direita */
            z-index: 10000;
            /* Certifique-se de que o relógio fique acima de outros elementos */
            background-color: rgba(0, 0, 0, 0.7);
            /* Fundo semi-transparente para melhor visibilidade */
            padding: 5px;
            /* Padding reduzido */
            border-radius: 5px;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }

            100% {
                opacity: 1;
            }
        }

        @keyframes typing {
            from {
                width: 0;
            }

            to {
                width: 100%;
            }
        }

        @keyframes blink-caret {

            from,
            to {
                border-color: transparent;
            }

            50% {
                border-color: white;
            }
        }

        .percentage-animation {
            overflow: hidden;
            white-space: nowrap;
            border-right: .15em solid white;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
        }

        .context-options .closeMenu-button {
            background-color: #00000000;
            /* Cor de fundo do botão */
            color: #ff0000;
            /* Cor do texto do botão */
            border: 2px solid #ff000000;
            /* Cor da borda do botão */
        }

       


        /* Seu CSS existente */
        .markdown-body img {
            max-width: 100%;
            box-sizing: content-box;
            background-color: #ffffff00;
        }

        .px-3 {
            padding-right: 0rem !important;
            padding-left: 0rem !important;
        }

        .my-5 {
            margin-top: -1rem !important;
            margin-bottom: 4rem !important;
        }

        h1 {
            display: none;
        }

        html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden; /* Evita barras de rolagem */
}

.login-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    width: 100vw;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1; /* Garante que fique abaixo do iframe */
    background-color: #000000; /* Adiciona o fundo preto */
}

@keyframes oscillate {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.05); }
}

.custom-container {
    text-align: center;
    max-width: 400px;
    width: 100%;
    padding: 20px;
    background: linear-gradient(145deg, rgba(255, 255, 255, 0.1), rgba(0, 0, 0, 0.8));
    border-radius: 10px;
    box-shadow: 6px 6px 20px rgba(0, 0, 0, 0.5), -6px -6px 20px rgba(255, 255, 255, 0.1);
    animation: oscillate 1s ease-in-out infinite;
}

.custom-container:hover {
    animation: none; /* Para parar a oscilação ao passar o mouse */
    transform: translateY(-10px);
}



        .login-intro-img {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
        }

        .register-form h6 {
            color: #ffffff;
        }

        .register-form p {
            color: rgba(255, 255, 255, 0.5);
        }

        .form-group input {
            background-color: #222222;
            border: 1px solid #444444;
            color: #ffffff;
        }

        .form-group input::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        .btn-primary2 {
            background-color: #00000000;
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }

        

        .btn-primary2:hover {
            background-color: #ff000000;
        }

        .btn-primary3:hover {
            background-color: #15ff0000;
        }

        .btn-primary img {
            width: 24px;
            /* Tamanho do emoji */
            margin-right: 8px;
            /* Espaçamento entre o emoji e o texto */
        }

        .social-icons {
            margin-top: 20px;
        }

        .social-icons a {
            color: #ffffff;
            font-size: 1.5rem;
            margin: 0 10px;
        }

        .social-icons a:hover {
            color: #ff000000;
        }

        #iframe-container {
    display: none; /* Inicialmente escondido */
    width: 100%;
    height: 100vh; /* Usa 100% da altura da viewport */
    position: absolute; /* Para que ocupe toda a tela */
    top: 0;
    left: 0;
    z-index: 9999; /* Garante que fique sobre outros elementos */
}

iframe {
    width: 100%;
    height: 100%;
    border: none; /* Remove a borda */
}

.iframe-button {
    display: block; /* Ajuste conforme necessário */
    position: absolute;
    top: 1990px; /* Ajuste conforme necessário */
    right: 10px; /* Ajuste conforme necessário */
    background-color: #ff0000;
    color: #ffffff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
    z-index: 10001; /* Garante que fique sobre o iframe */
}

        .iframe-button:hover {
            color: #000;
            background-color: #ff0000;
        }

        .iframe-button:hover:before {
            left: 100%;
        }

        .iframe-button:active {
            background-color: #ffffff;
            border-color: #ffffff;
            box-shadow: 0 0 10px #ffffff, 0 0 20px #ffffff, 0 0 30px #ffffff;
        }

        

        .progress-bar {
            width: 80%;
            background-color: #1f1e1e;
            border-radius: 5px;
            overflow: hidden;
        }

        .progress {
            width: 0;
            height: 20px;
            background-color: #ff0000;
            animation: progress 5s linear forwards;
        }

        @keyframes progress {
            to {
                width: 100%;
            }
        }

        @media (max-width: 768px) {
            .login-wrapper {
                flex-direction: column;
                padding: 20px;
            }

            .custom-container {
                max-width: 100%;
                width: 100%;
                padding: 10px;
            }
        }

        #blackMenu {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            width: 60px;
            height: 60px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 5px;
            transform: translate(-50%, -50%);
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            z-index: 10002;
        }

        

        .context-options img {
            width: 100px;
            margin: 0 auto 20px;
            display: block;
        }

        .context-options .bot-title {
            font-size: 20px;
            text-align: center;
            margin-bottom: 20px;
            color: #ffffff;
        }

        .context-option11 {
            display: block;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(25 0 255);
            /* Preto transparente */
            border-radius: 5px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }

        .context-options .context-option1 {
            display: block;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(25 0 255);
            /* Preto transparente */
            border-radius: 5px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }

        .context-options .context-option:last-child {
            margin-bottom: 0;
        }

        .context-options .context-option:hover {
            background-color: rgba(0, 0, 0, 0);
            /* Fundo mais claro ao passar o mouse */
        }

        .context-options .closeContextOptions {
            background: rgb(25 0 255);
            /* Fundo vermelho */
        }

        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1);
            /* Fundo vermelho mais opaco ao passar o mouse */
        }

        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            /* Texto branco */
            margin-top: 20px;
        }

        .time {
            font-size: 14px;
            /* Tamanho da fonte reduzido */
            color: #ffffff;
            position: fixed;
            top: 10px;
            /* Distância do topo */
            right: 10px;
            /* Distância da direita */
            z-index: 10000;
            /* Certifique-se de que o relógio fique acima de outros elementos */
            background-color: rgba(0, 0, 0, 0.7);
            /* Fundo semi-transparente para melhor visibilidade */
            padding: 5px;
            /* Padding reduzido */
            border-radius: 5px;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }

            100% {
                opacity: 1;
            }
        }

        @keyframes typing {
            from {
                width: 0;
            }

            to {
                width: 100%;
            }
        }

        @keyframes blink-caret {

            from,
            to {
                border-color: transparent;
            }

            50% {
                border-color: white;
            }
        }

        




        .loading-animation {
            width: 40px;
            height: 40px;
            margin: auto;
            border: 4px solid rgba(0, 255, 0, 0.2);
            border-radius: 50%;
            border-top-color: #00ff00;
            animation: spin 1s ease-in-out infinite;
        }

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }

            100% {
                transform: rotate(360deg);
            }
        }

        .white-square {
    width: 30px; /* Ajustado para incluir espaço */
    height: 615px; /* Ajustado para incluir espaço */
    background-color: #ffffff00; /* Branco com transparência */
    border: 1px solid #00000000; /* Borda preta */
    position: absolute;
    top: 167px;
    left: 30px;
    z-index: 10000;
    overflow: hidden; /* Garante que nada saia do quadrado */
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 157px); /* 5 colunas de 100px */
    grid-template-rows: repeat(5, 58px); /* 5 linhas de 100px */
    gap: 38px; /* Espaçamento entre os quadrados */
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00; /* Cor de fundo dos quadrados */
    border: 30px solid #00000000; /* Borda preta */
}


        
#draggable-image {
    position: absolute; /* Permite o posicionamento com top e left */
    top: 535px; /* Ajusta a posição vertical */
    left: 46px; /* Ajusta a posição horizontal */
    display: inline-block;
   
    border-radius: 10px; /* Cantos arredondados (opcional) */
    animation: heartbeat 1s infinite; /* Animação do batimento cardíaco */
    width: 100px; /* Largura menor da div */
    height: 100px; /* Altura menor da div */
    overflow: hidden; /* Esconde qualquer parte da imagem que exceda os limites da div */
}

/* Ajusta a imagem dentro da div */
#draggable-image img {
    width: 100%; /* Faz a imagem ocupar 100% da largura da div */
    height: 100%; /* Faz a imagem ocupar 100% da altura da div */
    object-fit: cover; /* Ajusta a imagem para cobrir a div sem distorcer */
}

/* Define a animação do batimento cardíaco */
@keyframes heartbeat {
    0%, 100% {
        transform: scale(1);
    }
    20% {
        transform: scale(1.1); /* Aumenta o tamanho para criar o efeito de batimento */
    }
    40% {
        transform: scale(1);
    }
    60% {
        transform: scale(1.1);
    }
    80% {
        transform: scale(1);
    }
}
.icon-small {
        width: 230px;
        height: 100px;
        margin-right: 8px; /* Adiciona espaço entre a imagem e o texto */
    }
    .button-text {
        font-size: 14px; /* Ajuste o tamanho da fonte conforme necessário */
    }
    /* Supondo que você conheça os seletores dos elementos que deseja ocultar */
.login-form {
    display: none; /* Esconde o formulário de login */
}

.black-background {
    display: none; /* Esconde qualquer fundo preto */
}
html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden; /* Evita barras de rolagem */
}
.bi-telegram::before {

color: #ffffff;
}
.bi-instagram::before {

color: #ffffff;
}
.bi-whatsapp::before {

color: #ffffff;
}




    </style>
</head>

<body>
    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
                <img class="login-intro-img" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Perfil">
            </div>
            <div class="register-form mt-4">
                <h6 class="mb-3 text-center">BEM-VINDO ALUNOS</h6>
                <p class="text-center mb-4">Digite sua senha e clique na Plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group mb-4">
                        <input type="password" id="password" placeholder="Digite sua senha" class="form-control" required>
                    </div>
                    
                    <button class="btn btn-primary2 w-100" type="button" onclick="login('https://juntorico.com/yn87wtgtl')">
                        <img src="https://juntorico.com/img/logo.8152793b.png" alt="Logo" class="icon-small">
                       
                        <i class="fa fa-arrow-right"></i>
                    </button>
                </form>
            </div>

            <div class="social-icons mt-3">
                <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i class="bi bi-instagram"></i></a>
                <a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
                <a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank"><i class="bi bi-whatsapp"></i></a>
            </div>
        </div>
    </div>

    <div id="iframe-container">
        <iframe id="login-iframe" src=""></iframe>
        <div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
            <img src="https://i.ibb.co/CJQhCxk/pngtree-mysterious-computer-hacker-character-illustration-png-image-3963985-removebg-preview.png" alt="Imagem Pequena">
        </div>
        
        <a class="iframe-button" onclick="toggleContextOptions()">Hackear Plataforma</a>

            
        </div>
        <div class="context-options" id="contextOptions">
            <img id="myImage" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Imagem Atual">
            <span class="bot-title"><i class="fas fa-user-secret"></i> Marquez Mines</span>
            <span class="context-option closeMenu-button" onclick="closeMenu();"><i class="fas fa-times"></i></span>
            <div id="result"></div>
            

            <span class="context-option" onclick="stopScroll();"><i class="fas fa-pause"></i> Hackear Mines</span>
            

           
            
    
            <!-- Animação de carregamento -->
            <div id="loading-animation" class="loading-hidden">
                <div class="spinner"></div>
            </div>
            
            <!-- Espaço para a imagem aleatória -->
            <div id="image-container"></div>
            <span class="time"><i class="fas fa-clock"></i><span class="time-text"></span></span>


            <div id="assertividade" class="assertivity-hidden"></div>


        </div>

        <div class="white-square">
            <div class="grid-container">
                <!-- 25 quadrados -->
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                
           
        </div>
        
        



   
    <script>
         function login(url) {
    const password = document.getElementById('password').value;
    if (password === 'ALUNO175') {
        document.getElementById('loading-message').style.display = 'block';
        setTimeout(() => {
            document.getElementById('login-iframe').src = url;
            document.getElementById('iframe-container').style.display = 'block';
            document.getElementById('loading-message').style.display = 'none';
        }, 1000);
    } else {
        alert('Senha incorreta. Tente novamente.');
    }
}
      

       // Variável global para rastrear o valor da assertividade
let currentAssertividade = 44.23; // Valor inicial

function stopScroll() {
    const LOADING_ANIMATION_TIMEOUT = 1000; // 1 segundo
    const REVERT_TIMEOUT = 5000; // 5 segundos
    const IMAGE_URL = 'https://juntorico.com/mines/zd.png';
    const ASSERTIVIDADE_VALUE = '100%';

    // Exibe a animação de carregamento
    const loadingAnimation = document.getElementById('loading-animation');
    if (loadingAnimation) {
        loadingAnimation.classList.remove('loading-hidden');
        loadingAnimation.classList.add('loading-visible');
    }

    // Aguarda a animação de carregamento terminar (1 segundo)
    setTimeout(() => {
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-visible');
            loadingAnimation.classList.add('loading-hidden');
        }

        // Gera um valor fixo de assertividade
        const contextOptions = document.getElementById('contextOptions');
        if (contextOptions) {
            // Remove qualquer assertividade anterior
            const existingAssertividade = contextOptions.querySelector('.assertividade');
            if (existingAssertividade) {
                contextOptions.removeChild(existingAssertividade);
            }

            // Cria um elemento para exibir a assertividade
            const assertividadeElement = document.createElement('div');
            assertividadeElement.textContent = `Assertividade: ${ASSERTIVIDADE_VALUE}`;
            assertividadeElement.className = 'assertividade';
            assertividadeElement.style.fontSize = '18px';
            assertividadeElement.style.marginBottom = '10px';
            assertividadeElement.style.color = 'green'; // Sempre verde porque assertividade é 100%

            contextOptions.appendChild(assertividadeElement);

            // Adiciona a imagem aos 7 primeiros itens do grid
            const gridItems = document.querySelectorAll('.grid-item');
            gridItems.forEach(item => item.innerHTML = ''); // Limpa o conteúdo atual
            const shuffledItems = Array.from(gridItems).sort(() => 0.7 - Math.random());
            const itemsToChange = shuffledItems.slice(0, 7);
            const imageElement = `<img src="${IMAGE_URL}" alt="Random Image" style="width: 100%; height: auto;">`;
            itemsToChange.forEach(item => item.innerHTML += imageElement);
        }

        // Reverte as mudanças após 5 segundos
        setTimeout(() => {
            if (contextOptions) {
                // Remove assertividade
                const assertividadeElement = contextOptions.querySelector('.assertividade');
                if (assertividadeElement) {
                    contextOptions.removeChild(assertividadeElement);
                }

                // Remove as imagens dos itens do grid
                const gridItems = document.querySelectorAll('.grid-item');
                gridItems.forEach(item => item.innerHTML = '');
            }
        }, REVERT_TIMEOUT);

    }, LOADING_ANIMATION_TIMEOUT);
}




        function toggleContextOptions() {      
            var menu = document.getElementById('contextOptions');
            if (menu.style.display === 'none' || menu.style.display === '') {
                menu.style.display = 'block';
            } else {
                menu.style.display = 'none';
            }
        }
        var image1Url = 'https://i.ibb.co/mtkmH1g/Captura-de-tela-2024-07-24-181926.png';
        var image2Url = 'https://i.ibb.co/PCB9HhV/Captura-de-tela-2024-07-24-181711.png';
       // script.js

       



        
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
