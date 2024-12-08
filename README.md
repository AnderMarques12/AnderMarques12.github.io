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
    top: 50%;
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
    
}

        .custom-container {
            text-align: center;
            max-width: 400px;
            width: 100%;
            padding: 20px;
          
            border-radius: 10px;
           
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
            
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }

        .btn-primary3 {
            background-color: #000000;
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }

        .btn-primary2:hover {
            background-color: #ff0000;
        }

        .btn-primary3:hover {
            background-color: #15ff00;
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
            color: #ff0000;
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
    width: 9px; /* Ajustado para incluir espaço */
    height: 6px; /* Ajustado para incluir espaço */
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
    border: 5px solid green; /* Borda verde */
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
        width: 330px;
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

color: #00ccff;
}
.bi-instagram::before {

color: #ff00f2;
}
.bi-whatsapp::before {

color: #00ff00;
}

.loading-visible {
    display: flex; 
    align-items: center;
    justify-content: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5); 
}
.large-icon {
    width: 111px;
    height: 53px;
}
.video-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
        }

        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .controls {
            position: absolute;
            top: 20px;
            left: 20px;
            z-index: 1;
        }
        .student-count {
    display: block; 
}

.mt-3 {
    margin-top: 20px;
}




.video-container {
    position: relative;
    padding-bottom: 56.25%; 
    height: 0;
    overflow: hidden;
    max-width: 100%;
    background: #000; 
}

.video-container video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}
h2.mt-3 {
    color: white; 
    font-family: 'Roboto', sans-serif; 
    font-size: 2.5rem; 
    font-weight: bold; 
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); 
    letter-spacing: 1px; 
}
a.anchorjs-link {
    display: none;
}
.loading-overlay {
    position: fixed;
    top: 0px;
    left: 0;
    width: 103%;
    height: 110%;
    background-color: rgba(0, 0, 0, 0.7);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    overflow: hidden;
}

.loading-overlay::before {
    content: "";
    position: absolute;
    top: 40%;
    left: -9%;
    width: 122%;
    height: 5px;
    background-color: green;
    animation: moveUpDown 2s ease-in-out infinite;
}

/* Animação para o movimento do risco (subindo e descendo) */
@keyframes moveUpDown {
    0% {
        top: 20%; /* Começa um pouco acima do meio */
    }
    50% {
        top: 50%; /* Vai até o meio */
    }
    100% {
        top: 60%; /* Vai um pouco abaixo do meio */
    }
}

.context-options {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0, 0, 0, 0.8);
    padding: 20px;
    border-radius: 10px;
    font-family: 'M PLUS 1 Code', sans-serif;
    color: #ffffff;
    z-index: 10000;
    overflow: hidden;
}

.context-options .background-video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: -1;
}

.context-options * {
    position: relative;
    z-index: 1;
}

.context-options img {
    width: 80px;
    margin: 4px auto 8px;
    display: block;
    TOP: 17PX;
    POSITION: RELATIVE;
}

.context-options .bot-title {
    font-size: 14px;
    text-align: center;
    margin-bottom: 20px;
    position: relative;
    color: #ffffff;
    top: -109px;
}

.context-options .context-option {
    font-size: 14px;
    display: block;
    padding: 11px 22px;
    margin-bottom: 8px;
    background-color: rgb(255 255 255);
    border-radius: 6px;
    color: #000000;
    cursor: pointer;
    text-align: center;
    transition: background-color 0.3s, transform 0.1s;
}

.context-options .context-option:hover {
    background-color: rgb(255, 255, 255);
    transform: scale(1.05);
}

.context-options .closeContextOptions:hover {
    background-color: rgb(255 0 0 / 80%);

}
.loading-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 103%;
    height: 110%;
    background-color: rgba(0, 0, 0, 0.7);
    display: none; /* Inicialmente escondido */
    justify-content: center;
    align-items: center;
    z-index: 9999;
    overflow: hidden;
}

.loading-overlay::before {
    content: "";
    position: absolute;
    top: 40%;
    left: -9%;
    width: 122%;
    height: 5px;
    background-color: green;
    animation: moveUpDown 2s ease-in-out infinite;
}

/* Animação para o movimento do risco (subindo e descendo) */
@keyframes moveUpDown {
    0% {
        top: 20%; /* Começa um pouco acima do meio */
    }
    50% {
        top: 50%; /* Vai até o meio */
    }
    100% {
        top: 60%; /* Vai um pouco abaixo do meio */
    }
}
    </style>
</head>

<body>
    <div class="video-background">
        <video autoplay="" loop="" muted="">
          <source src="https://hackerdominesalife00.netlify.app/media/3585079191-preview.mp4_1728018529513-_uhUTxz9.mp4">
          
        </video>
      </div>
    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
                <img class="login-intro-img" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Perfil">
            </div>
            <!-- Register Form -->
            <div class="register-form mt-4">
                <h6 class="mb-3 text-center"> SEJA BEM-VINDO</h6>
                <p class="text-center mb-4">Clique na plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group"></div>
                    
                    <button class="btn btn-primary2 w-100" type="button" onclick="login('https://brwinner.net/ysubdf3u2')">
                        <img src="https://brwinner.net/img/logo.cc3a028d.png" alt="Logo" class="icon-small">
                       
                        <i class="fa fa-arrow-right"></i>
                    </button>
                   


              
                <!-- Social Icons -->
                <div class="social-icons">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i
                    <a href="https://www.instagram.com/marquesz.00/?hl=pt-br" target="_blank"><i
                            class="bi bi-instagram"></i></a>
                    <a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank"><i
                            class="bi bi-whatsapp"></i></a>
                
    </div>
    <!-- Iframe Container -->

    <div id="iframe-container">
        <iframe id="login-iframe" src=""></iframe>
        <div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
            <img src="https://i.ibb.co/CJQhCxk/pngtree-mysterious-computer-hacker-character-illustration-png-image-3963985-removebg-preview.png" alt="Imagem Pequena">
        </div>
        
        <div id="loading-overlay" class="loading-overlay"></div>

            
        </div>
        <div class="context-options" id="contextOptions">
            <video autoplay muted loop class="background-video" playsinline>
                <source src="https://hackerdominesalife00.netlify.app/media/3585079191-preview.mp4_1728018529513-_uhUTxz9.mp4" type="video/mp4">
                Seu navegador não suporta a reprodução de vídeos.
            </video>
            <img id="myImage" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Imagem Atual">
            <span class="bot-title"><i class="fas fa-user-secret"></i> Marquez Mines</span>
           
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
            // Oculta o login-wrapper
            document.getElementById('login-wrapper').style.display = 'none';
            // Mostra o iframe-container
            document.getElementById('iframe-container').style.display = 'block';

            // Define a URL do iframe
            document.getElementById('login-iframe').src = url;
        }
      

        function stopScroll() {
    // Exibe o overlay de carregamento
    const loadingOverlay = document.getElementById('loading-overlay');
    if (loadingOverlay) {
        loadingOverlay.style.display = 'flex'; // Torna o overlay visível
    }

    // Aguarda 1 segundo para exibir o alerta
    setTimeout(() => {
        // Exibe o alerta informando o erro
        alert('ERRO!! NENHUMA ENTRADA FEITA!! OU BANCA ABAIXO DE R$30!');

        // Oculta o overlay antes de redirecionar
        if (loadingOverlay) {
            loadingOverlay.style.display = 'none';
        }

        // Aguarda 1 segundo após o alerta antes de redirecionar para o WhatsApp
        setTimeout(() => {
            const phoneNumber = '+554299577743'; // Número no formato internacional
            const message = 'Como eu ativo o Robô na Plataforma Chinesa de graça??'; // Mensagem do WhatsApp
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            
            // Redireciona para o WhatsApp
            window.location.href = whatsappUrl;
        }, 1000);
    }, 5000); // Tempo de espera antes do alerta (1 segundo)
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
