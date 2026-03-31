<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chameleon Coin | 3-Year Legacy | Pixel Power</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
    <style>
        body { background-color: #050505; color: #fff; font-family: sans-serif; overflow-x: hidden; position: relative; min-h-screen; }
        .pixel-font { font-family: 'Press Start 2P', cursive; }
        .neon-text { text-shadow: 0 0 10px #00FF7F, 0 0 20px #00FF7F; }
        .neon-border { border: 4px solid #00FF7F; box-shadow: 0 0 20px rgba(0, 255, 127, 0.5); }
        
        /* Estilo dos Camaleões Pixel Art */
        .chameleon-spirit {
            position: absolute;
            font-size: 2rem;
            cursor: pointer;
            transition: all 0.2s ease-out;
            user-select: none;
            z-index: 10;
            opacity: 0.6;
            filter: grayscale(100%); /* Começa cinza pixelizado */
            animation: float 4s ease-in-out infinite; /* Movimento flutuante */
        }
        
        /* Movimento flutuante (subir e descer) */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }

        /* Efeito ao passar o dedo/mouse */
        .chameleon-spirit:hover {
            opacity: 1;
            filter: grayscale(0%) hue-rotate(90deg) scale(1.8); /* Fica neon e cresce */
            animation-play-state: paused; /* Para de flutuar */
        }
        
        /* Balão de fala pixelizado */
        .speech-bubble {
            position: absolute;
            background: #00FF7F;
            color: #000;
            padding: 6px 10px;
            border-radius: 4px; /* Mais quadrado, cara de pixel */
            font-family: 'Press Start 2P', cursive;
            font-size: 0.5rem;
            bottom: 140%;
            left: 50%;
            transform: translateX(-50%) scale(0);
            transition: transform 0.2s ease-out;
            pointer-events: none;
            white-space: nowrap;
        }
        
        .chameleon-spirit:hover .speech-bubble {
            transform: translateX(-50%) scale(1);
        }
    </style>
</head>
<body class="p-6 flex flex-col items-center">

    <h1 class="text-3xl font-black mt-10 neon-text pixel-font italic z-20">CHAMELEON <span class="text-green-500">COIN</span></h1>
    
    <div class="my-10 text-center z-20">
        <img src="1774919945707.png" class="w-64 h-64 rounded-full neon-border object-cover border-4 mx-auto">
    </div>

    <div class="max-w-md text-center z-20">
        <p class="text-xl font-bold text-green-400 mb-4 uppercase tracking-widest pixel-font">3-Year Holder</p>
        <p class="text-gray-400 leading-relaxed italic pixel-font text-sm">Paciência de Camaleão, lucro de Diamante.</p>
    </div>

    <div class="mt-10 space-y-4 w-full max-w-xs z-20">
        <a href="https://t.me/Dev_Chameleon" target="_blank" class="block text-center bg-green-500 text-black font-black py-4 rounded-xl hover:bg-green-400 transition pixel-font text-xs">COMUNIDADE</a>
        <button class="block w-full text-center border-2 border-green-500 text-green-500 font-black py-4 rounded-xl pixel-font text-xs">COPIAR CA</button>
    </div>

    <footer class="mt-20 text-gray-700 text-xs z-20 pixel-font">
        © 2026 CHAMELEON COIN - CAXIAS TO THE WORLD.
    </footer>

    <script>
        const phrases = ["HODL!", "3 ANOS!", "💎!", "CAXIAS!", "PACIÊNCIA!"];
        const numberOfChameleons = 12; // Número de camaleões flutuantes

        for (let i = 0; i < numberOfChameleons; i++) {
            createChameleon();
        }

        function createChameleon() {
            const chameleon = document.createElement('div');
            chameleon.className = 'chameleon-spirit';
            // Usa o emoji, mas o CSS vai estilizar
            chameleon.innerHTML = '🦎';
            
            // Posição aleatória na tela, mas garantindo que não fiquem escondidos
            chameleon.style.top = Math.random() * 80 + 10 + '%'; 
            chameleon.style.left = Math.random() * 80 + 10 + '%';
            
            // Define um delay de animação diferente para cada um
            chameleon.style.animationDelay = Math.random() * -4 + 's';
            
            // Adiciona o balão de fala pixelizado
            const bubble = document.createElement('div');
            bubble.className = 'speech-bubble';
            bubble.innerText = phrases[Math.floor(Math.random() * phrases.length)];
            chameleon.appendChild(bubble);
            
            document.body.appendChild(chameleon);
        }
    </script>

</body>
</html>
