HTML




<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Laydy Magaly con todo mi corazón</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #ffe3e3 0%, #fbc2eb 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* Corazones flotantes de fondo */
        .heart-bg {
            position: absolute;
            color: rgba(255, 75, 110, 0.2);
            font-size: 24px;
            animation: float 6s linear infinite;
            bottom: -50px;
            z-index: 1;
        }

        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }

        /* Contenedor Principal */
        .container {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            text-align: center;
            max-width: 600px;
            width: 90%;
            z-index: 10;
            border: 2px solid rgba(255, 182, 193, 0.5);
            transition: transform 0.3s ease;
        }

        h1 {
            color: #d63384;
            font-size: 2.5rem;
            margin-bottom: 20px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .heart-icon {
            font-size: 50px;
            color: #ff4b6e;
            animation: pulse 1.5s infinite;
            margin-bottom: 20px;
            display: inline-block;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.15); }
            100% { transform: scale(1); }
        }

        /* Sobre y Carta animada */
        .envelope-wrapper {
            cursor: pointer;
            margin: 20px auto;
        }

        .btn-open {
            background: #ff4b6e;
            color: white;
            border: none;
            padding: 12px 30px;
            font-size: 1.1rem;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(255, 75, 110, 0.4);
            transition: all 0.3s ease;
        }

        .btn-open:hover {
            background: #e0395c;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 75, 110, 0.6);
        }

        .letter {
            display: none;
            text-align: left;
            line-height: 1.8;
            color: #4a4a4a;
            font-size: 1.1rem;
            margin-top: 20px;
            animation: fadeIn 1.5s ease forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .letter p {
            margin-bottom: 15px;
        }

        .highlight {
            color: #d63384;
            font-weight: bold;
        }

        .signature {
            text-align: right;
            font-style: italic;
            margin-top: 30px;
            font-size: 1.2rem;
            color: #ff4b6e;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="heart-icon">❤️</div>
        <h1>Para: Laydy Magaly</h1>
        
        <div class="envelope-wrapper" id="wrapper">
            <button class="btn-open" onclick="abrirCarta()">Abrir con amor 💌</button>
        </div>

        <!-- AQUÍ PUEDES EDITAR TU TEXTO -->
        <div class="letter" id="carta">
            <p>Querida <span class="highlight">Laydy Magaly</span>,</p>
            
            <p>Te escribo estas líneas porque a veces las palabras habladas no me alcanzan para expresar todo lo que siento, y hoy, más que nunca, necesito que me escuches desde el fondo de tu corazón.</p>
            
            <p>Primero que nada, <span class="highlight">quiero pedirte una disculpa sincera</span>. Sé que no he hecho las cosas bien últimamente y que mis errores han causado distancia entre nosotros. Lo que menos quiero en este mundo es lastimarte o hacerte sentir mal; tu sonrisa es mi parte favorita del día y saber que yo apagué un poco de esa alegría me duele profundamente.</p>
            
            <p>No soy perfecto, pero el amor que te tengo es real, inmenso y sincero. Eres una mujer increíble, llena de luz, y me duele pensar que por un impulso o un descuido pueda perder el lugar tan hermoso que tienes en mi vida.</p>
            
            <p>Por favor, perdóname. Quiero aprender de esto, ser mejor para ti y recordarte cada día lo importante que eres. Eres mi presente y la persona con la que quiero compartir mi futuro.</p>
            
            <p>Gracias por tu paciencia, por tu hermosa forma de ser y por existir.</p>
            
            <div class="signature">Con todo mi amor por siempre... Te amo. ✨</div>
        </div>
    </div>

    <script>
        // Función para abrir la carta
        function abrirCarta() {
            document.getElementById('wrapper').style.display = 'none';
            document.getElementById('carta').style.display = 'block';
        }

        // Generador de corazones flotantes de fondo
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart-bg');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 4 + 's'; // Entre 4 y 7 segundos
            heart.style.fontSize = Math.random() * 20 + 15 + 'px';
            
            document.body.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 7000);
        }

        // Crear corazones constantemente
        setInterval(createHeart, 400);
    </script>
</body>
</html>
