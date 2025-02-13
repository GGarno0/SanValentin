<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
            text-align: center;
            overflow: hidden;
            position: relative;
        }

        .container {
            z-index: 1;
            max-width: 90%;
        }

        h1 {
            color: white;
            font-size: 2em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .botones {
            margin-top: 20px;
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 100%;
            max-width: 300px;
        }

        button {
            padding: 15px;
            font-size: 1.2em;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
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

        /* 📱 Ajustes para imágenes en móviles */
        .imagenes {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-bottom: 20px;
            max-width: 90%;
        }

        .imagen {
            width: 80px;
            height: 80px;
            border-radius: 10px;
            object-fit: cover;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s;
        }

        .imagen:hover {
            transform: scale(1.1);
        }

        @media (min-width: 600px) {
            .botones {
                flex-direction: row;
            }
        }
    </style>
</head>

<body>

    <!-- 📸 Sección de imágenes decorativas -->
    <div class="imagenes">
        <img src="NoEntrar/imagen1.jpeg" alt="Foto nuestra" class="imagen">
        <img src="NoEntrar/imagen2.jpg" alt="Regalo para ti" class="imagen">
        <img src="NoEntrar/imagen3.jpeg" alt="Doggo" class="imagen">
        <img src="NoEntrar/imagen4.jpeg" alt="Otra foto nuestra" class="imagen">
        <img src="NoEntrar/imagen5.jpg" alt="Flores para ti" class="imagen">
        <img src="NoEntrar/imagen6.jpeg" alt="Chocolates" class="imagen">
    </div>

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

            if (escala > 5) {
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
            btnNo.style.left = Math.random() * (window.innerWidth - 100) + 'px';
            btnNo.style.top = Math.random() * (window.innerHeight - 50) + 'px';
        }
    </script>

</body>

</html>
