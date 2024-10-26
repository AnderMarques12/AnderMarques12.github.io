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
    display: none;
    position: fixed;
    top: 59%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgb(0, 0, 0);
    padding: 20px;
    border-radius: 10px;
    font-family: 'M PLUS 1 Code', sans-serif;
    color: #ffffff;
    z-index: 10000;
}

.context-options img {
    width: 84px;
    margin: 0 auto 20px;
    display: block;
    top: 12;
    left: 11;
    position: fixed;
}

.context-options .bot-title {
    font-size: 20px;
    text-align: center;
    position: fixed;
    margin-bottom: 20px;
    color: #000000;
    top: 33px;
    left: 103px;
}

.context-options .context-option {
    font-size: 14px;
    display: block;
    padding: 12px 20px;
    margin-bottom: 5px;
    background-color: rgb(25, 0, 255); 
    border-radius: 5px;
    color: #ffffff;
    cursor: pointer;
    text-align: center;
    transition: background-color 0.3s, transform 0.1s;

}

.context-options .context-option:hover {
    background-color: rgb(27 0 255 / 56%);
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
    overflow: hidden; /* Desativa o scroll */
    height: 100%;
}

    .login-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    height: auto;
    width: 101vw;
    position: absolute;
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
            background-color: #000000;
            color: #000;
            box-shadow: 0 0 30px rgba(255, 0, 0, 0.8);
            transform: scale(1.05);
        }
        .btn-primary2:hover {
            background-color: #000000;
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
    top: 0px;
    left: -12px;
    z-index: 9999;
}

    iframe {
        width: 100vw; 
        height: 150vh;
        border: none; 
    }
        

        #draggable-image {
    position: absolute;
    top: 50px;
    left: 33px;
    z-index: 10002;
    cursor: move;
}

        #draggable-image img {
            width: 100px;
            height: auto;
        }

        .black-background {
            display: none;
        }
        
        .white-square {
    width: 593px;
    height: 646px;
    background-color: #ff000000;
    border: 2px solid #00000000;
    position: absolute;
    top: 73px;
    left: 131px;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}
.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 95px);
    grid-template-rows: repeat(5, 103px);
    gap: 21px;
    height: 100%;
    width: 100%;
}
.grid-item {
    background-color: #ffffff00;
    border: 9px solid #00000000;
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


  .bot-title {
    color: #33ff33;
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: 20px;
    text-align: center;
    text-shadow: 0 0 8px #33ff33;
  }

  .input-group {
    width: 100%;
    position: relative;
    margin-bottom: 15px;
    top: 69px;
}

  .input-group label {
    color: #33ff33;
    font-size: 1em;
    margin-bottom: 5px;
    display: block;
    text-shadow: 0 0 5px #33ff33;
  }

  .input-group input {
    width: 100%;
    padding: 10px;
    border: 1px solid #33ff33;
    border-radius: 5px;
    background-color: #0d0d0d;
    color: #33ff33;
    font-family: 'Courier New', Courier, monospace;
  }
  .fa-cogs {
    color: #33ff33;
    margin-right: 27px;
    font-size: 1.2em;
    left: 249px;
    top: 364px;
    position: absolute;
    text-shadow: 0 0 5px #33ff33;
}
.toggle-button {
    width: 61px;
    height: 30px;
    background-color: #333;
    border-radius: 15px;
    position: relative;
    top: 30px;
    margin: 10px 0 20px;
    cursor: pointer;
    transition: background-color 0.4s ease;
    box-shadow: 0 0 10px #33ff33;
}

  /* Efeito ao Ativar */
  .toggle-button.active {
    background-color: #33ff33;
    box-shadow: 0 0 15px #33ff33;
  }

  .toggle-knob {
    width: 26px;
    height: 26px;
    background-color: #fff;
    border-radius: 50%;
    position: absolute;
    top: 2px;
    left: 2px;
    transition: left 0.3s ease;
  }

  /* Movimento do Knob quando ativo */
  .toggle-button.active .toggle-knob {
    left: 32px;
  }

  .status-text {
    color: #33ff33;
    font-size: 1em;
    margin-top: 10px;
    text-shadow: 0 0 5px #33ff33;
  }

  /* Spinner de Carregamento */
  .spinner {
    border: 4px solid rgba(51, 255, 51, 0.2);
    border-left-color: #33ff33;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    animation: spin 1s linear infinite;
  }

  @keyframes spin {
    100% {
      transform: rotate(360deg);
    }
  }

  #loading-animation {
    display: none;
    margin-top: 20px;
  }

  .loading-hidden {
    display: none;
  }
  #modo-automatico {
    font-size: 28px;
    vertical-align: middle;
}

#texto-automatico {
    font-size: 19px;
    margin-left: 10px;
    left: 8px;
    top: 68px;
    position: relative;
}

    </style>
</head>

<body>
    <div class="video-background">
        <video autoplay="" loop="" muted="">
          <source src="https://doublejonwhite.com/Video2.mp4" type="video/mp4">
          
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

<div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
    <img src="https://i.ibb.co/fpv7pmf/anonymous-8291223-1280.png" alt="Hacker">
  </div>
  
  <div class="context-options" id="contextOptions">
    <img id="myImage" src="https://i.ibb.co/8xfpYGj/fotor-20241011144526.png" alt="Imagem Atual">
    <span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquesz</span>
    
    <div class="input-group">
      <label>VALOR</label>
      <input type="text" placeholder="Valor das Entrada">
    </div>
    
    <div class="input-group">
      <label>APOSTAR</label>
      <input type="text" placeholder="% acima que deve aposta">
    </div>
    
    <div class="input-group">
      <label>META</label>
      <input type="text" placeholder="Meta para parar">
    </div>
    
    <div>
        <i class="fa fa-cogs" aria-hidden="true" id="modo-automatico"></i> <span id="texto-automatico">MODO AUTOMÁTICO</span>
       
      <div class="toggle-button" id="autoModeToggle" onclick="toggleAutoMode()">
        <div class="toggle-knob"></div>
      </div>
      <div class="status-text" id="statusText">Desativado</div>
    </div>
  
    <div id="loading-animation" class="loading-hidden">
        <!-- Spinner aqui -->
        <div class="spinner"></div>
    </div>
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
<div id="image-container"></div>
<div id="assertividade" class="assertivity-hidden"></div>
                        
</div>

    <div class="black-background"></div>
    <script>

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
    if (password === 'ALUNO1098') {
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

function toggleAutoMode() {
    const toggleButton = document.getElementById('autoModeToggle');
    const statusText = document.getElementById('statusText');

    toggleButton.classList.toggle('active');

    if (toggleButton.classList.contains('active')) {
      statusText.textContent = "Ativado";
      statusText.style.color = "#33ff33"; // Verde
    } else {
      statusText.textContent = "Desativado";
      statusText.style.color = "#ff3333"; // Vermelho
    }
  }
function closeContextOptions() {
    const loadingAnimation = document.getElementById('loading-animation');
    const contextOptions = document.getElementById('contextOptions');

    if (loadingAnimation) {
        loadingAnimation.classList.remove('loading-hidden');
        loadingAnimation.classList.add('loading-visible');
    }

    // Exibe a animação de carregamento por 5 segundos e depois atualiza o conteúdo
    setTimeout(() => {
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-visible');
            loadingAnimation.classList.add('loading-hidden');
        }

        if (contextOptions) {
            // Remove assertividade e imagem anteriores
            const existingAssertividade = contextOptions.querySelector('.assertividade');
            const existingImage = contextOptions.querySelector('.random-image');
            
            if (existingAssertividade) contextOptions.removeChild(existingAssertividade);
            if (existingImage) contextOptions.removeChild(existingImage);

            // Gera e exibe nova assertividade entre 1,00% e 100,00%
            const assertividadeValue = (Math.random() * 99 + 1).toFixed(2); // Gera um número entre 1.00 e 100.00
            const assertividade = `${assertividadeValue}%`;

            const assertividadeElement = document.createElement('div');
            assertividadeElement.textContent = `Assertividade: ${assertividade}`;
            assertividadeElement.className = 'assertividade';
            assertividadeElement.style.fontSize = '18px';
            assertividadeElement.style.marginBottom = '10px';
            assertividadeElement.style.color = assertividadeValue >= 90 ? 'green' : 'red'; // Verde se >= 90%, vermelho caso contrário
            contextOptions.appendChild(assertividadeElement);

            // Lista de URLs de imagens
            const imageUrls = [
                'https://i.ibb.co/WfX0bJ4/Captura-de-tela-2024-09-01-013829.png',
                'https://i.ibb.co/RDS5bK3/Captura-de-tela-2024-09-01-014104.png',
                'https://i.ibb.co/X2KPtR9/Captura-de-tela-2024-09-01-013952.png'
            ];

            // Escolhe e exibe uma imagem aleatória
            const imageUrl = imageUrls[Math.floor(Math.random() * imageUrls.length)];
            const imageElement = document.createElement('img');
            imageElement.src = imageUrl;
            imageElement.alt = 'Random Image';
            imageElement.style.width = '100px'; // Ajuste o tamanho conforme necessário
            imageElement.style.height = 'auto';
            imageElement.className = 'random-image';
            contextOptions.appendChild(imageElement);

            // Limpa a assertividade e a imagem após mais 5 segundos
            setTimeout(() => {
                if (contextOptions) {
                    const assertividadeElement = contextOptions.querySelector('.assertividade');
                    const randomImageElement = contextOptions.querySelector('.random-image');

                    if (assertividadeElement) contextOptions.removeChild(assertividadeElement);
                    if (randomImageElement) contextOptions.removeChild(randomImageElement);
                }
            }, 5000);
        }
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
       
        let autoModeInterval = null;

function toggleAutoMode() {
    const toggleButton = document.getElementById('autoModeToggle');
    const statusText = document.getElementById('statusText');

    toggleButton.classList.toggle('active');

    if (toggleButton.classList.contains('active')) {
        statusText.textContent = "Ativado";
        statusText.style.color = "#33ff33"; // Verde
        startAutoMode();  // Iniciar modo automático
    } else {
        statusText.textContent = "Desativado";
        statusText.style.color = "#ff3333"; // Vermelho
        stopAutoMode();  // Parar modo automático
    }
}
3
function startAutoMode() {
    autoModeInterval = setInterval(executeFunction, 15000); // Executa a cada 8 segundos
}

function stopAutoMode() {
    if (autoModeInterval) {
        clearInterval(autoModeInterval);
        autoModeInterval = null;
    }
}

function executeFunction() {
    // Função que será executada automaticamente a cada 8 segundos
    console.log('Executando função automática...');

    // Aqui você pode adicionar as ações que deseja realizar
    stopScroll(); // Executa a função stopScroll
}

function stopScroll() {
    const loadingAnimation = document.getElementById('loading-animation');
    
    // Exibir a animação de carregamento (spinner)
    if (loadingAnimation) {
        loadingAnimation.classList.remove('loading-hidden');
        loadingAnimation.classList.add('loading-visible');
    }

    // Esperar 5 segundos antes de mostrar os diamantes
    setTimeout(() => {
        // Após 5 segundos, remover a animação de carregamento
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-visible');
            loadingAnimation.classList.add('loading-hidden');
        }

        // Gera a assertividade aleatória
        const assertividade = (75 + Math.random() * 25).toFixed(2) + '%';


        const contextOptions = document.getElementById('contextOptions');
        if (contextOptions) {
            // Remover assertividade anterior (se existir)
            const existingAssertividade = contextOptions.querySelector('.assertividade');
            if (existingAssertividade) contextOptions.removeChild(existingAssertividade);

            // Criar o novo elemento de assertividade
            const assertividadeElement = document.createElement('div');
            assertividadeElement.textContent = `Assertividade: ${assertividade}`;
            assertividadeElement.className = 'assertividade';
            assertividadeElement.style.fontSize = '18px';
            assertividadeElement.style.marginBottom = '10px';

            // Definir cor com base no valor de assertividade
            const assertividadeValue = parseFloat(assertividade); // Converter para número
            assertividadeValue >= 90 ? assertividadeElement.style.color = 'green' : assertividadeElement.style.color = 'red';

            contextOptions.appendChild(assertividadeElement);

            // Limpar todos os itens do grid antes de adicionar os diamantes
            const gridItems = document.querySelectorAll('.grid-item');
            gridItems.forEach(item => item.innerHTML = '');

            // Sortear aleatoriamente os itens do grid e escolher de 1 a 6 itens para exibir diamantes
            const shuffledItems = Array.from(gridItems).sort(() => 0.5 - Math.random());
            const randomCount = Math.floor(Math.random() * 6) + 1;
            const itemsToChange = shuffledItems.slice(0, randomCount);
            const imageUrl = 'https://jon.bet/static/media/diamond.eac6e969.svg';
            const imageElement = `<img src="${imageUrl}" alt="Random Image" style="width: 100%; height: auto;">`;

            // Adicionar os diamantes aos itens sorteados
            itemsToChange.forEach(item => item.innerHTML += imageElement);
        }

        // Após 7 segundos, limpar a interface removendo a assertividade e os diamantes
        setTimeout(() => {
            const contextOptions = document.getElementById('contextOptions');
            if (contextOptions) {
                const assertividadeElement = contextOptions.querySelector('.assertividade');
                if (assertividadeElement) contextOptions.removeChild(assertividadeElement);

                const gridItems = document.querySelectorAll('.grid-item');
                gridItems.forEach(item => item.innerHTML = '');
            }
        }, 8000);

    }, 5000); // Aguardar 5 segundos para remover o spinner e mostrar os diamantes
}


</script>
