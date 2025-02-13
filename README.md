<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        body {
            margin: 0;
            padding: 20px;
            background: linear-gradient(45deg, #ff007f, #ff69b4);
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            position: relative;
        }

        .container {
            text-align: center;
            z-index: 1;
        }

        h1 {
            color: white;
            font-size: 3em;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .botones {
            margin-top: 30px;
        }

        button {
            padding: 15px 30px;
            margin: 0 10px;
            font-size: 1.2em;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        #btnSi {
            background-color: #4CAF50;
            color: white;
        }

        #btnNo {
            background-color: #f44336;
            color: white;
            position: relative;
        }

        .imagen {
            position: absolute;
            width: 150px;
            height: 150px;
            border-radius: 10px;
            object-fit: cover;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
        }

        #imagen1 { top: 10px; left: 10px; }
        #imagen2 { top: 10px; right: 10px; }
        #imagen3 { bottom: 10px; left: 10px; }
        #imagen4 { bottom: 10px; right: 10px; }
        #imagen5 { left: 10px; top: 50%; transform: translateY(-50%); }
        #imagen6 { right: 10px; top: 50%; transform: translateY(-50%); }

    </style>
</head>
<body>
    <img src="NoEntrar/imagen1.jpeg" alt="Foto nuestra" class="imagen" id="imagen1">
    <img src="NoEntrar/imagen2.jpg" alt="Regalo para ti" class="imagen" id="imagen2">
    <img src="NoEntrar/imagen3.jpeg" alt="Doggo" class="imagen" id="imagen3">
    <img src="NoEntrar/imagen4.jpeg" alt="Otra foto nuestra" class="imagen" id="imagen4">
    <img src="NoEntrar/imagen5.jpg" alt="Flores para ti" class="imagen" id="imagen5">
    <img src="NoEntrar/imagen6.jpeg" alt="Chocolates" class="imagen" id="imagen6">

    <div class="container">
        <h1>¿Quieres ser mi San Valentín? 💖</h1>
        <div class="botones">
            <button id="btnSi" onclick="aceptar()">¡Sí!</button>
            <button id="btnNo" onmouseover="moverBoton()" onclick="negar()">No</button>
        </div>
    </div>

    <script>
        let escala = 1;

        function negar() {
            escala *= 1.2;
            document.getElementById('btnSi').style.transform = `scale(${escala})`;

            if(escala > 5) {
                document.getElementById('btnSi').style.fontSize = '3em';
                document.getElementById('btnSi').style.position = 'fixed';
                document.getElementById('btnSi').style.width = '100%';
                document.getElementById('btnSi').style.height = '100%';
                document.getElementById('btnSi').style.top = '0';
                document.getElementById('btnSi').style.left = '0';
                document.getElementById('btnSi').style.borderRadius = '0';
            }
        }

        function aceptar() {
            alert('¡Sabía que dirías que sí! 💝');
        }

        function moverBoton() {
            const btnNo = document.getElementById('btnNo');
            btnNo.style.position = 'absolute';
            btnNo.style.left = Math.random() * (window.innerWidth - 200) + 'px';
            btnNo.style.top = Math.random() * (window.innerHeight - 100) + 'px';
        }
    </script>
</body>
</html>
