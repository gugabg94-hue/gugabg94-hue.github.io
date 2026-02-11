<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Raquel</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: radial-gradient(circle, #ffafbd, #ffc3a0); /* Fundo degradê suave */
            overflow: hidden; /* Evita barras de rolagem */
            font-family: 'Georgia', serif;
        }

        h1 {
            color: #d63384;
            font-size: 3rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            z-index: 10; /* Garante que o texto fique na frente dos corações */
            text-align: center;
            background: rgba(255, 255, 255, 0.4);
            padding: 20px 40px;
            border-radius: 50px;
            backdrop-filter: blur(5px);
        }

        /* Configuração dos Corações */
        .coracao {
            position: absolute;
            color: #ff4d6d;
            font-size: 20px;
            user-select: none;
            animation: flutuar linear infinite;
        }

        @keyframes flutuar {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

    <h1>Eu amo você, Raquel, pra todo sempre! ❤️</h1>

    <script>
        function criarCoracao() {
            const coracao = document.createElement('div');
            coracao.classList.add('coracao');
            coracao.innerHTML = '❤️';
            
            // Posição aleatória na largura da tela
            coracao.style.left = Math.random() * 100 + "vw";
            
            // Tamanhos aleatórios
            coracao.style.fontSize = Math.random() * 20 + 20 + "px";
            
            // Velocidade aleatória (entre 3 e 8 segundos)
            coracao.style.animationDuration = Math.random() * 5 + 3 + "s";
            
            document.body.appendChild(coracao);

            // Remove o coração depois que a animação acaba para não travar o PC
            setTimeout(() => {
                coracao.remove();
            }, 8000);
        }

        // Cria um novo coração a cada 300 milissegundos
        setInterval(criarCoracao, 300);
    </script>

</body>
</html>
