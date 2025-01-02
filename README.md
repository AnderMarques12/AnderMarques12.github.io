<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

    <style>

        @import url('https://fonts.googleapis.com/css2?family=M+PLUS+1+Code&display=swap');
        .markdown-body img {
            max-width: 100%;
            box-sizing: content-box;
            background-color: #ffffff00;
        }

        .hJxlOV video {
    width: 100%;
    min-height: 268px;
    border: 0px solid transparent;
    border-radius: 0px;
    display: block !important;
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
    border: 8px solid #000000;
    border-radius: 50%;
    border-top: 8px solid #ff0000;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
    box-shadow: 0 0 20px rgb(255 0 0);
}

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }

            100% {
                transform: rotate(360deg);
            }
        }

        #image-container img {
            max-width: 100%;
            height: auto;
        }

        .feedback-hidden {
    display: none;
    color: #ffffff;
    font-family: 'M PLUS 1 Code', monospace;
    margin-top: 10px;
}

#hack-feedback {
    font-size: 14px;
    text-align: center;
    margin-top: 20px;
    color: #00ff3d;
    background-color: rgba(0, 0, 0, 0.8);
    padding: 10px;
    border-radius: 5px;
    width: 100%;
    display: none; 
}

.context-options {
    position: fixed;
    top: 77%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0, 0, 0, 0.8);
    padding: 15px;
    border-radius: 10px;
    font-family: 'M PLUS 1 Code', sans-serif;
    color: #ffffff;
    z-index: 10000;
    overflow: hidden;
}
.context-options .context-option {
    display: inline-flex
;
    align-items: center;
    justify-content: center;
    padding: 10px 20px;
    border-radius: 30px;
    cursor: pointer;
    transition: all 0.3s ease;
    border: none;
    background: linear-gradient(45deg, #c50505, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
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


.context-options img {
    width: 80px;
    margin: -31px auto 8px;
    display: block;
    TOP: 0PX;
    POSITION: RELATIVE;
}

img, svg {
    vertical-align: middle;
    WIDTH: 100%;
 
    TOP: -3PX;
    LEFT: 0PX;
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



.context-options .context-option.ativo {
    background-color: green;
}

.context-options .context-option.desativado {
    background-color: red;
}


        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            margin-top: 20px;
        }

        html, body {
        margin: 0;
        padding: 0;
        overflow-x: hidden; 
        overflow-y: auto; 
        height: 100%; 
    }
    .login-wrapper {
    display: flex
;
    align-items: center;
    justify-content: center;
    height: auto;
    width: 101vw;
    position: fixed;
    top: 60%;
    left: 0;
    background-color: rgba(0, 0, 0, 0);
}
    .custom-container {
    text-align: center;
    max-width: 388px;
    width: 100%;
    padding: 0px;
    background-color: rgba(0, 0, 0, 0);
    border-radius: 23px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0);
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

.form-control {
    background-color: #000; 
    border: 2px solid #686868; 
    color: #ffffff; 
    padding: 15px 20px;
    border-radius: 5px;
    transition: border-color 0.3s ease, box-shadow 0.3s ease;
    font-size: 16px;
    box-shadow: 0 0 10px rgba(0, 255, 68, 0); 
}

.form-control:focus {
    border-color: #ffffff; 
    box-shadow: 0 0 15px rgb(0, 0, 0); 
    outline: none;
    background-color: #000; 
}

.form-control::placeholder {
    color: rgb(247, 247, 247); 
}


.btn-primary2 {
    background-color: #000000;
    border: 2px solid #7a00ff;
    color: #fff;
    font-family: 'M PLUS 1 Code', sans-serif;
    font-size: 18px;
    text-transform: uppercase;
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 10px rgb(184 0 255 / 50%), 0 0 20px rgb(169 0 255 / 30%);
    position: relative;
    overflow: hidden;
}
        
        .btn-primary1 {
    background-color: #000000;
    border: 2px solid #ff7a00;
    color: #fff;
    font-family: 'M PLUS 1 Code', sans-serif;
    font-size: 18px;
    text-transform: uppercase;
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 10px rgb(255 137 0 / 50%), 0 0 20px rgba(255, 0, 0, 0.3);
    position: relative;
    overflow: hidden;
}
        
        
.btn-primary1::before {
    content: '';
    position: absolute;
    top: -200%;
    left: 0;
    width: 100%;
    height: 200%;
    background: rgb(255 106 0 / 50%);
    transform: rotate(45deg);
    transition: all 0.5s ease;
}
.btn-primary2::before {
    content: '';
    position: absolute;
    top: -200%;
    left: 0;
    width: 100%;
    height: 200%;
    background: rgb(140 0 255 / 54%);
    transform: rotate(45deg);
    transition: all 0.5s ease;
}
        
        .btn-primary1:hover::before {
            top: 0;
        }
        .btn-primary2:hover::before {
            top: 0;
        }
        
        .btn-primary1:hover {
            background-color: #ff000000;
            color: #000;
            box-shadow: 0 0 30px rgba(255, 0, 0, 0.8);
            transform: scale(1.05);
        }
        .btn-primary2:hover {
            background-color: #37ff0000;
            color: #000;
            box-shadow: 0 0 30px rgba(111, 0, 255, 0.8);
            transform: scale(1.05);
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

#iframe-container {
    display: none;
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0px;
    z-index: 9999;
}

    iframe {
        width: 100vw; 
        height: 100vh;
        border: none; 
    }
    .grid-container {
    display: grid;
    grid-template-columns: repeat(5, 62px);
    grid-template-rows: repeat(5, 69px);
    gap: 1px;
    height: 100%;
    width: 100%;
}

        .grid-item {
            background-color: #00000000;
            border: 6px solid #00000000;
        }

  

        #draggable-image img {
    width: 137px;
    top: 24px;
    left: 36px;
    height: auto;
    position: fixed;
}
        .black-background {
            display: none;
        }
        
      

.loading-hidden {
    display: none; 
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
h1 {
    display: none;
}


h1 a[href="https://aplicativomarquez.github.io/"] {
    display: none;
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
    background-color: rgba(0, 0, 0, 0.795);
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
 
.white-square {
    width: 593px;
    height: 646px;
    background-color: #ffffff00;
    border: 2px solid #00000000;
    position: absolute;
    top: 36PX;
    left: 108PX;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}
.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 95px);
    grid-template-rows: repeat(5, 101px);
    gap: 21px;
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00;
    border: 7px solid #00000000;
}
#modoAutomatico {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 10px 20px;
    border-radius: 30px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: all 0.3s ease;
    border: none;
}

#modoAutomatico.ativo {
    background: linear-gradient(172deg, #229c05, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

#modoAutomatico.desativado {
    background: linear-gradient(45deg, #000000, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

#modoAutomatico:hover {
    transform: scale(1.05); /* Leve aumento no tamanho */
}

#modoAutomatico:active {
    transform: scale(0.95); /* Leve redução no tamanho */
}
.context-option.hack-mines {
    background: linear-gradient(45deg, #000000, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    border: 2px solid white; /* Adiciona uma "porta branca" na forma de borda */
    border-radius: 5px; /* Suaviza os cantos para um visual mais elegante */
}

.context-option.hack-mines:hover {
    background: linear-gradient(45deg, #0041a5, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

.context-option.hack-mines:active {
    transform: scale(0.95); /* Leve redução no clique */
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.2);
}

.context-option.hack-double {
    background: linear-gradient(45deg, #000000, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    border: 2px solid white; /* Adiciona uma "porta branca" na forma de borda */
    border-radius: 5px; /* Suaviza os cantos para um visual mais elegante */
}

.context-option.hack-double:hover {
    background: linear-gradient(45deg, #0041a5, #000000);
    color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

.context-option.hack-double:active {
    transform: scale(0.95); /* Leve redução no clique */
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.2);
}

/* Ícones */
.context-option i {
    margin-right: 8px;
    font-size: 18px;
}
.video-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    z-index: -1;
  }

  .video-background video {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 100%;
    min-height: 100%;
    object-fit: cover;
  }
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: none; /* Não exibir inicialmente */
    justify-content: center;
    align-items: center;
    z-index: 1000; /* Certifique-se de que está acima de outros elementos */
}

.aviso {
    position: relative;
    width: 400px;
    padding: 25px;
    background-color: rgba(0, 0, 0, 0.6); /* Fundo semitransparente */
    border: 3px solid #285ff4;
    text-align: center;
    color: white;
    font-family: Arial, sans-serif;
}

.aviso p {
    margin: 10px 0;
}

.aviso .atencao {
    color: red;
}

.close-btn {
    position: absolute;
    top: -17px;
    right: 5px;
    background: none;
    border: none;
    color: white;
    font-size: 50px;
    cursor: pointer;
    pointer-events: auto; /* Permite cliques no botão */
}
.white-square {
    width: 402px;
    height: 448px;
    position: absolute;
    top: 150px;
    left: 7px;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 76px);
    grid-template-rows: repeat(5, 76px);
    gap: 5px;
    height: 100%;
    width: 100%;
}
.grid-item {
    background-color: #ffffff00;
    border: 15px solid #00000000;
}

    </style>
</head>

<body>
    <div class="video-background">
        <video autoplay loop muted>
          <source src="https://doublejonwhite.com/Video2.mp4" type="video/mp4">
          Seu navegador não suporta vídeos em HTML5.
        </video>
      </div>
      

    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
            
                
          
            <div class="register-form mt-4">
                <p class="text-center mb-4">Digite sua senha e clique na Plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group mb-4">
                       
                    </div>
                    <div class="row">
                        <div class="col">
                            <button 
                                class="btn btn-primary1 w-100" 
                                type="button" 
                                onclick="login('https://brganho.com/y83y2dom4')" 
                                style="height: 60px;">
                                <img src="https://brganho.com/img/logo.b41ad7a4.png" alt="Logo" class="icon-small">
                            </button>
                        </div>
                        <div class="col">
                            <button 
                                class="btn btn-primary2 w-100" 
                                type="button" 
                                onclick="login('https://jogar.win/y829fn1qx')" 
                                style="height: 60px;">
                                <img src="https://jogar.win/img/logo.e6258434.png" alt="Logo" class="large-icon">
                            </button>
                        </div>
                    </div>
                    
                   
                    
                  <div class="social-icons mt-3">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank" class="instagram"><i class="bi bi-instagram"></i></a>
                    <a href="https://t.me/hackermarquesz" target="_blank" class="telegram"><i class="bi bi-telegram"></i></a>
                    <a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank" class="whatsapp"><i class="bi bi-whatsapp"></i></a>
                </div>
                
                    
<div id="iframe-container">
<iframe id="login-iframe" src=""></iframe>
<div id="loading-overlay" class="loading-overlay"></div>

<div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
<img src="https://i.ibb.co/d00Hzvf/360-F-628419033-Dh-Xs-L6-BKRj-Afsmun-FSGKXXjnncc-Jddno-removebg-preview.png" alt="Hacker"></div>

<div class="white-square">
    <div class="grid-container">
      
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
<div class="overlay" id="overlay">
    <div class="aviso">
       
        <p>O HACKER ESTA BLOQUEANDO NENHUMA ENTRADA FEITA </p>
        <p class="atencao">Atenção: DEPOSITE 30 PARA DESBLOQUEAR O HACKER E FAÇA UMA ENTRADA.</p>
        
    </div>
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

        let modoAutomaticoAtivado = false;
let intervaloMudarIframe;


function login(url) {
    // Esconde o wrapper de login
    document.getElementById('login-wrapper').style.display = 'none';

    // Mostra o contêiner do iframe
    document.getElementById('iframe-container').style.display = 'block';

    // Atualiza a URL do iframe
    document.getElementById('login-iframe').src = url;
}


function stopScroll() { 
    const loadingOverlay = document.getElementById('loading-overlay');
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
            // Limpa os itens
            gridItems.forEach(item => item.innerHTML = '');

            // Seleciona aleatoriamente um item
            const shuffledItems = Array.from(gridItems).sort(() => Math.random() - 0.5);
            const selectedItem = shuffledItems[0]; // Seleciona o primeiro do embaralhamento

            // Adiciona a imagem do diamante
            const imageUrl = 'https://brwinner.net/mines/zs.png';
            const imageElement = `<img src="${imageUrl}" alt="Diamante" style="width: 100%; height: auto;">`;
            if (selectedItem) {
                selectedItem.innerHTML = imageElement;
            }
        }

        // Remove a assertividade e limpa os itens após 8 segundos
        setTimeout(() => {
            if (contextOptions) {
                const assertividadeElement = contextOptions.querySelector('.assertividade');
                if (assertividadeElement) {
                    contextOptions.removeChild(assertividadeElement);
                }
            }

            const gridItems = document.querySelectorAll('.grid-item');
            gridItems.forEach(item => item.innerHTML = '');
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
 
