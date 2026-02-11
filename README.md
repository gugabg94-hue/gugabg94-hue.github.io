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
