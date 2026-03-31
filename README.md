<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chameleon Coin | 3-Year Legacy Interativo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { background-color: #050505; color: #fff; font-family: sans-serif; overflow-x: hidden; }
        .neon-text { text-shadow: 0 0 10px #00FF7F; }
        .neon-border { border: 2px solid #00FF7F; box-shadow: 0 0 15px rgba(0, 255, 127, 0.3); }
        
        /* Estilo dos Camaleões Interativos */
        .chameleon-spirit {
            position: absolute;
            font-size: 1.5rem;
            cursor: pointer;
            transition: all 0.3s ease-out;
            user-select: none;
            z-index: 10;
            opacity: 0.7;
        }
        
        /* Efeito ao passar o dedo/mouse */
        .chameleon-spirit:hover {
            transform: scale(1.8) rotate(15deg);
            opacity: 1;
            filter: hue-rotate(90deg); /* Muda a cor! */
        }
        
        /* Balão de fala */
        .speech-bubble {
            position: absolute;
            background: #00FF7F;
            color: #000;
            padding: 5px 10px;
            border-radius: 10px;
            font-size: 0.75rem;
            font-weight: bold;
            white-space: nowrap;
            bottom: 130%;
            left: 50%;
            transform: translateX(-50%) scale(0);
            transition: transform 0.2s ease-out;
            pointer-events: none;
        }
        
        .chameleon-spirit:hover .speech-bubble {
            transform: translateX(-50%) scale(1);
        }
    </style>
</head>
<body class="p-6 flex flex-col items-center min-h-screen relative">

    <h1 class="text-4xl font-black mt-10 neon-text italic z-20">CHAMELEON <span class="text-green-500">COIN</span></h1>
    
    <div class="my-10 text-center z-20">
        <img src="1774919945707.png" class="w-64 h-64 rounded-full neon-border object-cover border-4 mx-auto">
    </div>

    <div class="max-w-md text-center z-20">
        <p class="text-xl font-bold text-green-400 mb-4 uppercase tracking-widest">3-Year Holder Ecosystem 💎</p>
        <p class="text-gray-400 leading-relaxed italic">"Paciência de Camaleão, lucro de Diamante."</p>
    </div>

    <div class="mt-10 space-y-4 w-full max-w-xs z-20">
        <a href="https://t.me/Dev_Chameleon" target="_blank" class="block text-center bg-green-500 text-black font-black py-4 rounded-xl hover:bg-green-400 transition">ENTRAR NO TELEGRAM</a>
        <button class="block w-full text-center border-2 border-green-500 text-green-500 font-black py-4 rounded-xl">COPIAR CONTRATO (CA)</button>
    </div>

    <footer class="mt-20 text-gray-600 text-xs z-20">
        © 2026 Chameleon Coin - Duque de Caxias para o Mundo.
    </footer>

    <script>
        const phrases = ["HODL!", "3 ANOS!", "💎!", "CAXIAS!", "LUCRO!", "🚀!", "PACIÊNCIA!"];
        const numberOfChameleons = 15; // Quantos camaleões você quer?

        for (let i = 0; i < numberOfChameleons; i++) {
            createChameleon();
        }

        function createChameleon() {
            const chameleon = document.createElement('div');
            chameleon.className = 'chameleon-spirit';
            chameleon.innerHTML = '🦎';
            
            // Posição aleatória na tela
            chameleon.style.top = Math.random() * 80 + 10 + '%'; // Entre 10% e 90% da altura
            chameleon.style.left = Math.random() * 80 + 10 + '%'; // Entre 10% e 90% da largura
            
            // Adiciona o balão de fala
            const bubble = document.createElement('div');
            bubble.className = 'speech-bubble';
            bubble.innerText = phrases[Math.floor(Math.random() * phrases.length)];
            chameleon.appendChild(bubble);
            
            document.body.appendChild(chameleon);
        }
    </script>

</body>
</html>
