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
    border: 8px solid #222;
    border-radius: 50%;
    border-top: 8px solid #ff0000;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
    box-shadow: 0 0 20px rgba(255, 0, 0, 0.7);
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
    top: 81%;
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
    TOP: 7PX;
    POSITION: RELATIVE;
}


.context-options .bot-title {
    font-size: 14px;
    text-align: center;
    margin-bottom: 20px;
    position: relative;
    color: #ffffff;
    top: -10px;
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
    display: flex;
    align-items: center;
    justify-content: center;
    height: auto;
    width: 101vw;
    position: fixed;
    top: 39px;
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
        
        .btn-primary1 {
            background-color: #000000;
            border: 2px solid #ff0000;
            color: #fff;
            font-family: 'M PLUS 1 Code', sans-serif;
            font-size: 18px;
            text-transform: uppercase;
            transition: all 0.2s ease-in-out;
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.5), 0 0 20px rgba(255, 0, 0, 0.3);
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
            background: rgba(255, 0, 0, 0.5);
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
            background: rgba(0, 255, 42, 0.541);
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
            box-shadow: 0 0 30px rgb(44 255 0 / 80%);
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
    left: -12px;
    z-index: 9999;
}

    iframe {
        width: 100vw; 
        height: 150vh;
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
    width: 79px;
    top: 0px;
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
 
.white-square {
    width: 352px;
    height: 408px;
    border: 2px solid #ff000000;
    position: absolute;
    top: 47px;
    left: 19px;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}
.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 64px);
    grid-template-rows: repeat(5, 71px);
    gap: 6px;
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00;
    border: 6px solid #00000000;
}
    </style>
</head>

<body>
    <div class="video-background">
        <video autoplay="" loop="" muted="">
          <source src="https://app.doublewhiteapp.com/build/assets/3585079191-preview.mp4_1728018529513-_uhUTxz9.mp4" type="video/mp4">
          
        </video>
      </div>
      

    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
                <p id="studentCount" class="mb-0" style="font-size: 39px; color: #00ff40; text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);">
                    <i class="fas fa-user-graduate" style="margin-right: 5px;"></i>
                    <span style="font-weight: bold;">1000 ALUNOS</span> 
                    <span style="color: #ff0000; font-weight: bold;">LIMITE: 1000</span>
                </p>
                
                <img class="login-intro-img" src="https://i.ibb.co/8xfpYGj/fotor-20241011144526.png" alt="Perfil">
            </div>
            
            <div class="register-form mt-4">
                <p class="text-center mb-4">Digite sua senha e clique na Plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group mb-4">
                        <input type="password" id="password" placeholder="Digite sua senha" class="form-control" required>
                    </div>
                    <div class="row">
                        <div class="col">
                            <button class="btn btn-primary1 w-100" type="button" onclick="login('https://blaze1.space/pt/games/mines')" style="height: 60px;">
                                <img src="https://blaze1.space/static/media/logo.cf45d2ad.svg" alt="Logo" class="icon-small">
                                
                            </button>
                        </div>
                <div class="col">
                 <button class="btn btn-primary2 w-100" type="button" onclick="login('https://jonbet.com/pt/games/mines')" style="height: 60px;">
                         <img src="https://jon.bet/static/media/logo.3af9f796.svg" alt="Logo" class="large-icon">
                          
                        </button>
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
<img src="https://i.ibb.co/fpv7pmf/anonymous-8291223-1280.png" alt="Hacker"></div>

<div class="context-options" id="contextOptions">
    <video autoplay muted loop class="background-video" playsinline>
        <source src="https://app.doublewhiteapp.com/build/assets/3585079191-preview.mp4_1728018529513-_uhUTxz9.mp4" type="video/mp4">
        Seu navegador não suporta a reprodução de vídeos.
    </video>
    <span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquez [2.0]</span>
    <img id="myImage" src="https://i.ibb.co/8xfpYGj/fotor-20241011144526.png" alt="Imagem Atual">
    <div id="result"></div>
    <span class="context-option" onclick="stopScroll();"><i class="fa fa-bomb" aria-hidden="true"></i> Hackear Mines</span>
    <span class="context-option closeContextOptions" onclick="closeContextOptions();"><i class="fa fa-play" aria-hidden="true"></i> Hackear Double</span>
    <div id="loading-animation" class="loading-hidden">
        <div class="spinner"></div>
    </div>
</div>


                              

        
<div id="image-container"></div>
<div id="assertividade" class="assertivity-hidden"></div>
                        
</div>
                                    
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
    <script>

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
    const password = document.getElementById('password').value;
    if (password === 'ALUNO11') {
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


function closeContextOptions() { 
    const loadingAnimation = document.getElementById('loading-animation');
    const contextOptions = document.getElementById('contextOptions');
    const loadingOverlay = document.getElementById('loading-overlay');

    // Exibe o overlay (se aplicável) como no stopScroll
    if (loadingOverlay) {
        loadingOverlay.style.display = 'flex';
    }

    setTimeout(() => {
        // Após exibir o overlay, removê-lo
        if (loadingOverlay) {
            loadingOverlay.style.display = 'none';
        }

        // Exibe a animação de carregamento
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-hidden');
            loadingAnimation.classList.add('loading-visible');
        }

        // Aguarda a animação de carregamento terminar
        setTimeout(() => {
            if (loadingAnimation) {
                loadingAnimation.classList.remove('loading-visible');
                loadingAnimation.classList.add('loading-hidden');
            }

            // Remove conteúdo existente e atualiza com novo conteúdo
            if (contextOptions) {
                const existingAssertividade = contextOptions.querySelector('.assertividade');
                const existingImage = contextOptions.querySelector('.random-image');
                
                if (existingAssertividade) contextOptions.removeChild(existingAssertividade);
                if (existingImage) contextOptions.removeChild(existingImage);

                // Gera assertividade entre 90% e 100%
                const assertividadeValue = (90 + Math.random() * 10).toFixed(2);
                const assertividade = `${assertividadeValue}%`;

                const assertividadeElement = document.createElement('div');
                assertividadeElement.textContent = `Assertividade: ${assertividade}`;
                assertividadeElement.className = 'assertividade';
                assertividadeElement.style.fontSize = '18px';
                assertividadeElement.style.marginBottom = '10px';
                assertividadeElement.style.color = 'green'; // Sempre verde

                contextOptions.appendChild(assertividadeElement);

                // Lista de URLs de imagens
                const imageUrls = [
                    'https://i.ibb.co/WfX0bJ4/Captura-de-tela-2024-09-01-013829.png',
                    'https://i.ibb.co/RDS5bK3/Captura-de-tela-2024-09-01-014104.png',
                    'https://i.ibb.co/X2KPtR9/Captura-de-tela-2024-09-01-013952.png'
                ];

                const imageUrl = imageUrls[Math.floor(Math.random() * imageUrls.length)];
                const imageElement = document.createElement('img');
                imageElement.src = imageUrl;
                imageElement.alt = 'Random Image';
                imageElement.style.width = '100px';
                imageElement.style.height = 'auto';
                imageElement.className = 'random-image';

                contextOptions.appendChild(imageElement);

                // Remove conteúdo após 7 segundos
                setTimeout(() => {
                    if (contextOptions) {
                        const assertividadeElement = contextOptions.querySelector('.assertividade');
                        const randomImageElement = contextOptions.querySelector('.random-image');
                        if (assertividadeElement) contextOptions.removeChild(assertividadeElement);
                        if (randomImageElement) contextOptions.removeChild(randomImageElement);
                    }
                }, 7000);
            }
        }, 1000);
    }, 4000);
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
       
        function stopScroll() {
    // Exibe a animação do overlay (risco verde)
    const loadingOverlay = document.getElementById('loading-overlay');
    if (loadingOverlay) {
        loadingOverlay.style.display = 'flex'; // Torna o overlay visível
    }

    // A animação do "sniper" vai durar 2 segundos para cada ciclo de movimento
    // Aqui vamos fazer a animação durar 4 segundos para ser repetida 2 vezes (com efeito completo)
    setTimeout(() => {
        // Após 4 segundos, esconde o overlay
        if (loadingOverlay) {
            loadingOverlay.style.display = 'none'; // Esconde o overlay
        }

        // Exibe a animação de carregamento
        const loadingAnimation = document.getElementById('loading-animation');
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-hidden');
            loadingAnimation.classList.add('loading-visible');
        }

        // Aguarda a animação de carregamento terminar (por exemplo, 1 segundo)
        setTimeout(() => {
            if (loadingAnimation) {
                // Oculta a animação de carregamento
                loadingAnimation.classList.remove('loading-visible');
                loadingAnimation.classList.add('loading-hidden');
            }

            // Gera um valor percentual fixo acima de 90
            const assertividade = (90 + Math.random() * 10).toFixed(2) + '%'; // Valor entre 90% e 100%

            // Seleciona o menu contextOptions
            const contextOptions = document.getElementById('contextOptions');

            if (contextOptions) {
                // Remove qualquer assertividade anterior
                const existingAssertividade = contextOptions.querySelector('.assertividade');
                if (existingAssertividade) {
                    contextOptions.removeChild(existingAssertividade);
                }

                // Cria um elemento para exibir a assertividade
                const assertividadeElement = document.createElement('div');
                assertividadeElement.textContent = `Assertividade: ${assertividade}`;
                assertividadeElement.className = 'assertividade';
                assertividadeElement.style.fontSize = '14px';
                assertividadeElement.style.marginBottom = '0px';
                assertividadeElement.style.color = 'green'; // Sempre verde porque assertividade é >= 90%

                // Adiciona a assertividade ao menu contextOptions
                contextOptions.appendChild(assertividadeElement);

                // Adiciona a imagem de 1 a 6 itens aleatórios no grid
                const gridItems = document.querySelectorAll('.grid-item');
                gridItems.forEach(item => item.innerHTML = ''); // Limpa o conteúdo atual
                const shuffledItems = Array.from(gridItems).sort(() => 0.5 - Math.random());
                const randomCount = Math.floor(Math.random() * 6) + 3; // Número aleatório de 1 a 6
                const itemsToChange = shuffledItems.slice(0, randomCount);
                const imageUrl = 'https://jon.bet/static/media/diamond.eac6e969.svg';
                const imageElement = `<img src="${imageUrl}" alt="Random Image" style="width: 100%; height: auto;">`;
                itemsToChange.forEach(item => item.innerHTML += imageElement);
            }

            // Aguarda 5 segundos e então reverte as mudanças
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
            }, 8000); // Tempo de espera para reverter as mudanças (5 segundos)
        }, 1000); // Tempo de espera para a animação de carregamento (1 segundo)
    }, 8000); // Tempo de espera para a animação do "sniper" (4 segundos)
}



    </script>
