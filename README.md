# PEDRO-JOTA
Pra garota que eu gosto 
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedido Especial</title>
    <style>
        /* Estilos da Intro */
        #intro {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-color: #ff85a2; /* Rosa bonito */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            color: white;
            font-family: 'Arial', sans-serif;
            transition: opacity 1s ease;
        }

        .heart {
            font-size: 50px;
            animation: pulse 1.5s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        /* Estilo do Corpo e Fundo */
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
            font-family: 'Arial', sans-serif;
            background-image: url('https://r.jina.ai/i/67be9269550346d0a79a5be43f44358a'); /* Sua foto de fundo */
            background-size: cover;
            background-position: center;
        }

        /* Overlay para escurecer um pouco o fundo e destacar o texto */
        .overlay {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.4);
            z-index: 1;
        }

        .container {
            position: relative;
            z-index: 2;
            background: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            max-width: 350px;
        }

        h1 { color: #d63384; margin-bottom: 30px; }

        .botoes {
            display: flex;
            justify-content: center;
            gap: 20px;
            height: 50px;
        }

        button {
            padding: 10px 25px;
            font-size: 1.1em;
            font-weight: bold;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        #sim { background-color: #2ecc71; color: white; }

        #nao {
            background-color: #e74c3c;
            color: white;
            position: relative;
            transition: all 0.2s ease;
        }

        .footer {
            margin-top: 20px;
            font-size: 0.8em;
            color: #555;
        }
    </style>
</head>
<body>

    <div id="intro">
        <div class="heart">❤️</div>
        <h1 style="color: white;">GERFESON</h1>
        <p>Preparou algo especial para você Nanay😍...</p>
        <button onclick="iniciar()" style="background: white; color: #ff85a2; margin-top: 20px;">CLIQUE PARA VER</button>
    </div>

    <div class="overlay"></div>

    <div class="container">
        <h1>TO MUITO APEGADO A TU OQUE TU ACHA 😅 
desculpa fazer tu perder tempo com isso kkkk acha bom ?❤️</h1>
        <div class="botoes">
            <button id="sim" onclick="aceitou()">SIM</button>
            <button id="nao" onmouseover="fugir()" onclick="fugir()">NÃO</button>
        </div>
        <div class="footer">
            CEO: Pedro Jota | Insta: @p.jota
        </div>
    </div>

    <script>
        function iniciar() {
            document.getElementById('intro').style.opacity = '0';
            setTimeout(() => {
                document.getElementById('intro').style.display = 'none';
            }, 1000);
        }

        function aceitou() {
            window.location.href = "https://vt.tiktok.com/ZSms299K4/";
        }

        var fugiu = false;
        function fugir() {
            var btnNao = document.getElementById("nao");
            
            if (!fugiu) {
                btnNao.style.position = 'fixed';
                fugiu = true;
            }

            // Calcula posições aleatórias
            var x = Math.random() * (window.innerWidth - btnNao.offsetWidth);
            var y = Math.random() * (window.innerHeight - btnNao.offsetHeight);

            // Garante que o botão fique visível
            x = Math.max(10, Math.min(x, window.innerWidth - 100));
            y = Math.max(10, Math.min(y, window.innerHeight - 50));

            btnNao.style.left = x + "px";
            btnNao.style.top = y + "px";
        }
    </script>
</body>
</html>