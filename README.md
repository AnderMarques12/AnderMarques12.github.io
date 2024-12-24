<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">




    <style>
        @import url('https://fonts.googleapis.com/css2?family=M+PLUS+1+Code&display=swap');
       

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


#image-container img {
    max-width: 100%;
    height: auto;
}



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
    overflow: hidden; 
}


.custom-container {
    position: fixed;
    top: 150px;
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
            background-color: #000000;
            border: 2px solid #00ff37;
            color: #fff;
            font-family: 'M PLUS 1 Code', sans-serif;
            font-size: 18px;
            text-transform: uppercase;
            transition: all 0.2s ease-in-out;
            box-shadow: 0 0 10px rgba(0, 255, 13, 0.5), 0 0 20px rgba(255, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
 
       
        .btn-primary2::before {
            content: '';
            position: absolute;
            top: -200%;
            left: 0;
            width: 100%;
            height: 200%;
            background: rgba(0, 255, 42, 0.541);
            transform: rotate(45deg);
            transition: all 0.5s ease;
        }
        
      
        
      
        .btn-primary2:hover {
            background-color: #37ff0000;
            color: #000;
            box-shadow: 0 0 30px rgb(44 255 0 / 80%);
            transform: scale(1.05);
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
    display: none; 
    width: 100%;
    height: 100vh; 
    z-index: 9999;
}


iframe {
    
  position: fixed;
  top: 0;
  left: 0;
  width: 100%; /* Ocupa a largura total */
  height: 100%; /* Ocupa a altura total */
  z-index: 999; /* Fica acima de outros elementos */
  background-color: #fff; /* Ajuste conforme necessário */
  overflow: hidden; /* Impede rolagem interna */
  touch-action: none; /* Impede interações indesejadas */
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
    display: flex
;
    align-items: center;
    justify-content: center;
    height: 135vh;
    width: 100vw;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
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

        
        .context-options {
    position: fixed;
    top: 71%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0, 0, 0, 0.8);
    padding: 20px;
    border-radius: 10px;
    
    color: #ffffff;
    z-index: 10000;
    overflow: hidden;
    display: none; 
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
    TOP: 7PX;
    POSITION: RELATIVE;
}


.context-options .bot-title {
    font-size: 19px;
    text-align: center;
    margin-bottom: 20px;
    position: relative;
    color: #ffffff;
    top: -10px;
    /* width: 31px; */
    margin: 91px auto 20px;
    display: block;
    TOP: -103PX;
    POSITION: RELATIVE;
}
.context-options .context-option {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 10px 20px;
    border-radius: 30px;
    font-size: 12px;
    font-weight: bold;
    cursor: pointer;
    transition: all 0.3s ease;
    border: none;
    background: linear-gradient(45deg, #c50505, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

.context-options .context-option:hover {
    transform: scale(1.05);
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

      

        
        #draggable-image {
    position: absolute;
    top: 19PX;
    left: 11px;
    z-index: 10002;
    cursor: move;
}


#draggable-image img {
    width: 105px;
    height: auto;
    TOP: 512PX;
    POSITION: FIXED;
}
.icon-small {
    width: 414PX;
    height: 228PX;
    position: relative;
    top: 6px;
    
}
    .button-text {
        font-size: 14px; 
    }
   
.login-form {
    display: none; 
}

.black-background {
    display: none; 
}
html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden; 
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
        .social-icons a.instagram {
    color: #C13584; 

}

.social-icons a.instagram:hover {
    color: #e1306c; 
    text-shadow: 0 0 15px rgba(225, 48, 108, 0.8);
}

.social-icons a.telegram {
    color: #0088cc; 

}

.social-icons a.telegram:hover {
    color: #00acee; 
    text-shadow: 0 0 15px rgba(0, 172, 238, 0.8);
}

.social-icons a.whatsapp {
    color: #25D366; 

}

.social-icons a.whatsapp:hover {
    color: #128C7E; 
    text-shadow: 0 0 15px rgba(18, 140, 126, 0.8);
}


.social-icons {
    margin-top: 20px;
    text-align: center;
    POSITION: RELATIVE;
}

.social-icons a {
    color: #ffffff;
    font-size: 2.5rem;
    margin: 0 15px;
    position: relative;
    transition: color 0.3s ease, transform 0.3s ease;

}
.social-icons a:hover {
    color: #ff0000; 
    transform: scale(1.2); 
    text-shadow: 0 0 15px rgba(255, 0, 0, 0.8), 0 0 30px rgba(255, 0, 51, 0.5); 
}


.social-icons a::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    background-color: #ffffff; 
    bottom: -5px;
    left: 0;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.4s ease, background-color 0.4s ease;
}

.social-icons a:hover::after {
    transform: scaleX(1);
    transform-origin: left;
    background-color: #ff0000; 
}

.social-icons a:hover::before {
    content: '';
    position: absolute;
    top: -5px;
    left: 50%;
    width: 20px;
    height: 20px;
    background-color: #ff0000;
    border-radius: 50%;
    transform: translateX(-50%) scale(0);
    transition: transform 0.4s ease;
}

.social-icons a:hover::before {
    transform: translateX(-50%) scale(1);
}


        .login-intro-img {
            max-width: 100%;
            height: auto;
            margin-bottom: 7px;
        }

        .register-form h6 {
            color: #ffffff;
        }

        .register-form p {
            color: rgb(255, 255, 255);
        }
        .form-group {
    position: relative;
    margin-bottom: 30px;
}
.white-square {
    width: 497px;
    height: 615px;
    position: absolute;
    top: 181px;
    left: 198px;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}

.grid-container {
    display: grid
;
    grid-template-columns: repeat(5, 52px);
    grid-template-rows: repeat(5, 50px);
    gap: 40px;
    height: 100%;
    width: 100%;
}
.grid-item {
    background-color: #ffffff00;
    border: 0px solid #00000000;
}


        
    </style>
</head>

<body>
    <div class="video-background">
        <video autoplay loop muted playsinline>
            <source src="https://doublejonwhite.com/Video2.mp4" type="video/mp4">
            Seu navegador não suporta o vídeo.
        </video>
    </div>
    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
           
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
                    <button class="btn btn-primary1 w-100" type="button" onclick="login('https://tudo.win/y8eqmzssp')" style="height: 250px;">
                        <img src="https://minespro.oficialvenda.com.br/wp-content/uploads/2023/02/Mines-Pro-Logo.png" alt="Logo" class="icon-small">
                        
                    </button>
            
                <div class="social-icons">
                    <a href="https://www.instagram.com/hack.da.blaze_/?hl=pt-br" target="_blank"><i
                            class="bi bi-instagram"></i></a>
                    <a href="https://t.me/hackermarquesz" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://wa.me/5542998134733?text=Boa%20tarde%20estou%20com%20problema%20no%20hack3r,%20pode%20me%20ajuda?" target="_blank"><i
                            class="bi bi-whatsapp"></i></a>
                
    </div>
 

    <div id="iframe-container">
        <iframe id="login-iframe" src=""></iframe>
        <div id="loading-overlay" class="loading-overlay"></div>
        <div id="draggable-image" class="iframe-button" onclick="toggleContextOptions()">
           
            <img src="https://i.ibb.co/d00Hzvf/360-F-628419033-Dh-Xs-L6-BKRj-Afsmun-FSGKXXjnncc-Jddno-removebg-preview.png" alt="Imagem Pequena">
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
        
            
        </div>
        <div class="context-options" id="contextOptions">
            <video autoplay muted loop class="background-video" playsinline>
                <source src="https://hackerdominesalife00.netlify.app/media/3585079191-preview.mp4_1728018529513-_uhUTxz9.mp4" type="video/mp4">
                Seu navegador não suporta a reprodução de vídeos.
            </video>
            <span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquez </span>
            
            <div id="result"></div>
            <span class="context-option" onclick="stopScroll();"><i class="fa fa-bomb" aria-hidden="true"></i> HACKEAR MINES</span>
        
            <div id="loading-animation" class="loading-hidden">
                <div class="spinner"></div>
            </div>
        

       
        



   
    <script>
           // Função para abrir o contexto ao dar dois cliques
    function openContextOptions() {
        const contextOptions = document.getElementById('contextOptions');
        contextOptions.style.display = 'block'; // Mostra o elemento
    }

    // Adiciona o evento de dois cliques para mouse
    document.addEventListener('dblclick', (event) => {
        const target = event.target;
        if (target.closest('.background-video') || target.closest('.context-options')) {
            openContextOptions();
        }
    });

    // Adiciona suporte para toque duplo em dispositivos móveis
    let lastTouchTime = 0;

    document.addEventListener('touchstart', (event) => {
        const currentTime = new Date().getTime();
        const timeSinceLastTouch = currentTime - lastTouchTime;

        if (timeSinceLastTouch < 300 && timeSinceLastTouch > 0) { // Intervalo para toque duplo
            const target = event.target;
            if (target.closest('.background-video') || target.closest('.context-options')) {
                openContextOptions();
            }
        }

        lastTouchTime = currentTime;
    });
const video = document.querySelector('.background-video');
video.addEventListener('ended', () => {
    video.play(); // Força o replay caso o loop falhe
});


document.addEventListener('DOMContentLoaded', function () {
            var video = document.getElementById('background-video');

            // Tenta reproduzir o vídeo quando a página é carregada
            video.play().then(() => {
                // Sucesso, o vídeo está sendo reproduzido
            }).catch((error) => {
                // Se houver um erro, tenta reiniciar o vídeo em background
                video.muted = true;
                video.play();
            });
        });
       function login(url) {
        
            document.getElementById('login-wrapper').style.display = 'none';
         
            document.getElementById('iframe-container').style.display = 'block';
        
            document.querySelector('.iframe-button').style.display = 'block';
          
            document.getElementById('login-iframe').src = url;
        }
      

let currentAssertividade = 44.23; 
function stopScroll() {
        const loadingOverlay = document.getElementById('loading-overlay');
        const loadingAnimation = document.getElementById('loading-animation');
        const contextOptions = document.getElementById('contextOptions');

        // Mostrar o overlay de carregamento
        if (loadingOverlay) {
            loadingOverlay.style.display = 'flex';
        }

        setTimeout(() => {
            // Esconder o overlay de carregamento
            if (loadingOverlay) {
                loadingOverlay.style.display = 'none';
            }

            // Lógica principal após o carregamento
            const assertividade = '100%';

            if (contextOptions) {
                const existingAssertividade = contextOptions.querySelector('.assertividade');
                if (existingAssertividade) {
                    contextOptions.removeChild(existingAssertividade);
                }

                const assertividadeElement = document.createElement('div');
                assertividadeElement.textContent = `Assertividade: ${assertividade}`;
                assertividadeElement.className = 'assertividade';
                assertividadeElement.style.fontSize = '18px';
                assertividadeElement.style.marginBottom = '10px';
                assertividadeElement.style.color = 'green';

                contextOptions.appendChild(assertividadeElement);

                const gridItems = document.querySelectorAll('.grid-item');
                gridItems.forEach(item => item.innerHTML = '');
                const shuffledItems = Array.from(gridItems).sort(() => 0.7 - Math.random());
                const itemsToChange = shuffledItems.slice(0, 7);
                const imageUrl = 'https://brwinner.net/mines/zs.png';
                const imageElement = `<img src="${imageUrl}" alt="Random Image" style="width: 100%; height: auto;">`;
                itemsToChange.forEach(item => item.innerHTML += imageElement);
            }

            setTimeout(() => {
                if (contextOptions) {
                    const assertividadeElement = contextOptions.querySelector('.assertividade');
                    if (assertividadeElement) {
                        contextOptions.removeChild(assertividadeElement);
                    }

                    const gridItems = document.querySelectorAll('.grid-item');
                    gridItems.forEach(item => item.innerHTML = '');
                }
            }, 8000);
        }, 5000);
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
   

       



        
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
