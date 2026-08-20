<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Para Ti ❤️</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            overflow: hidden;
            background: #000;
            font-family: Arial, sans-serif;
            color: white;
        }

        canvas {
            position: fixed;
            inset: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        /* ================================
           CONTENEDOR
        ================================= */

        .contenedor {
            position: relative;
            z-index: 10;

            width: 100%;
            height: 100vh;

            display: flex;
            justify-content: center;
            align-items: center;

            text-align: center;

            pointer-events: none;
        }

        /* ================================
           GALAXIA
        ================================= */

        .galaxia {
            position: absolute;

            width: 430px;
            height: 430px;

            top: 50%;
            left: 50%;

            transform: translate(-50%, -50%);

            border-radius: 50%;

            background:
                radial-gradient(
                    circle,
                    rgba(255,255,255,.95) 0%,
                    rgba(255,80,180,.7) 4%,
                    rgba(150,0,100,.5) 15%,
                    rgba(80,0,80,.2) 40%,
                    transparent 70%
                );

            box-shadow:
                0 0 30px #ff0099,
                0 0 80px #ff0088,
                0 0 150px rgba(255,0,150,.5);

            animation: girar 15s linear infinite;
        }

        @keyframes girar {
            from {
                transform: translate(-50%, -50%) rotate(0deg);
            }

            to {
                transform: translate(-50%, -50%) rotate(360deg);
            }
        }

        /* ================================
           LUNA
        ================================= */

        .luna {
            position: absolute;

            width: 120px;
            height: 120px;

            top: 50%;
            left: 50%;

            transform:
                translate(-50%, -50%)
                translate(150px, -120px);

            border-radius: 50%;

            background: #fff;

            box-shadow:
                0 0 20px white,
                0 0 50px #ffb6e6,
                0 0 100px #ff00aa;

            overflow: hidden;

            animation: lunaFlotando 4s ease-in-out infinite;
        }

        .luna::after {
            content: "";

            position: absolute;

            width: 132px;
            height: 132px;

            border-radius: 50%;

            background: #000;

            left: 42px;
            top: -16px;
        }

        @keyframes lunaFlotando {
            0%, 100% {
                transform:
                    translate(-50%, -50%)
                    translate(150px, -120px);
            }

            50% {
                transform:
                    translate(-50%, -50%)
                    translate(150px, -135px);
            }
        }

        /* ================================
           TEXTO
        ================================= */

        .texto {
            position: absolute;

            top: 16%;

            width: 100%;

            text-shadow:
                0 0 5px #fff,
                0 0 15px #ff00aa,
                0 0 30px #ff00aa;
        }

        .texto h1 {
            font-size: clamp(40px, 10vw, 85px);

            letter-spacing: 8px;

            animation:
                aparecer 2s ease,
                brillo 2s infinite alternate;
        }

        .texto h2 {
            margin-top: 10px;

            font-size: clamp(20px, 5vw, 35px);

            color: #ffd6f3;
        }

        @keyframes aparecer {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes brillo {
            from {
                text-shadow:
                    0 0 5px white,
                    0 0 15px #ff0099;
            }

            to {
                text-shadow:
                    0 0 10px white,
                    0 0 30px #ff0099,
                    0 0 60px #ff0099;
            }
        }

        /* ================================
           FOTO
        ================================= */

        .foto-container {
            position: absolute;

            top: 50%;
            left: 50%;

            transform: translate(-50%, -50%);

            width: 160px;
            height: 160px;

            border-radius: 50%;

            padding: 5px;

            background:
                linear-gradient(
                    45deg,
                    #ff00a8,
                    #fff,
                    #ff00a8
                );

            box-shadow:
                0 0 20px #ff00a8,
                0 0 50px #ff00a8;

            animation:
                fotoFlota 3s ease-in-out infinite;
        }

        .foto-container img {
            width: 100%;
            height: 100%;

            object-fit: cover;

            border-radius: 50%;

            background: #111;
        }

        @keyframes fotoFlota {
            0%, 100% {
                transform: translate(-50%, -50%) translateY(0);
            }

            50% {
                transform: translate(-50%, -50%) translateY(-12px);
            }
        }

        /* ================================
           MENSAJE
        ================================= */

        .mensaje {
            position: absolute;

            bottom: 13%;

            width: 90%;

            font-size: clamp(16px, 4vw, 24px);

            color: #fff;

            text-shadow:
                0 0 10px #ff00aa;

            animation: aparecer 3s ease;
        }

        /* ================================
           BOTONES
        ================================= */

        .controles {
            position: fixed;

            z-index: 30;

            bottom: 20px;

            left: 50%;

            transform: translateX(-50%);

            display: flex;

            gap: 10px;
        }

        button,
        label {
            border: none;

            padding: 12px 18px;

            border-radius: 30px;

            background: rgba(255,0,150,.25);

            border: 1px solid rgba(255,255,255,.4);

            color: white;

            cursor: pointer;

            backdrop-filter: blur(10px);

            transition: .3s;
        }

        button:hover,
        label:hover {
            transform: scale(1.08);

            background: rgba(255,0,150,.6);

            box-shadow:
                0 0 20px #ff0099;
        }

        /* ================================
           CORAZONES
        ================================= */

        .corazon {
            position: fixed;

            z-index: 20;

            color: #ff0099;

            font-size: 20px;

            pointer-events: none;

            animation:
                subir 4s linear forwards;

            text-shadow:
                0 0 10px #ff0099,
                0 0 20px #ff0099;
        }

        @keyframes subir {
            0% {
                transform:
                    translateY(0)
                    scale(.5);

                opacity: 1;
            }

            100% {
                transform:
                    translateY(-100vh)
                    translateX(var(--x))
                    scale(1.5);

                opacity: 0;
            }
        }

        /* ================================
           ESTRELLAS FUGACES
        ================================= */

        .estrella-fugaz {
            position: fixed;

            width: 100px;
            height: 2px;

            background:
                linear-gradient(
                    90deg,
                    white,
                    transparent
                );

            transform: rotate(-35deg);

            z-index: 5;

            pointer-events: none;

            animation:
                estrellaFugaz 1.5s linear forwards;
        }

        @keyframes estrellaFugaz {
            from {
                transform:
                    translate(0, 0)
                    rotate(-35deg);

                opacity: 1;
            }

            to {
                transform:
                    translate(-400px, 400px)
                    rotate(-35deg);

                opacity: 0;
            }
        }

        /* ================================
           RESPONSIVE
        ================================= */

        @media(max-width: 600px) {

            .galaxia {
                width: 330px;
                height: 330px;
            }

            .luna {
                width: 90px;
                height: 90px;

                transform:
                    translate(-50%, -50%)
                    translate(115px, -90px);
            }

            .luna::after {
                width: 99px;
                height: 99px;

                left: 31px;

                top: -12px;
            }

            .foto-container {
                width: 120px;
                height: 120px;
            }

            .texto {
                top: 13%;
            }

            .texto h1 {
                letter-spacing: 4px;
            }

            .mensaje {
                bottom: 13%;
            }

            .controles {
                bottom: 10px;
            }
        }
    </style>
</head>

<body>

    <!-- ================================
         CANVAS DEL UNIVERSO
    ================================= -->

    <canvas id="universo"></canvas>


    <div class="contenedor">

        <!-- GALAXIA -->

        <div class="galaxia"></div>


        <!-- LUNA -->

        <div class="luna"></div>


        <!-- TEXTO -->

        <div class="texto">

            <h1>TE AMO ❤️</h1>

            <h2 id="nombre">
                Sary
            </h2>

        </div>


        <!-- FOTO -->

        <div class="foto-container">

            <img
                id="foto"
                src="imagens/sary.jpeg"
                alt="Tu foto"
            >

        </div>


        <!-- MENSAJE -->

        <div class="mensaje">

            ✨ Feliz cumpleaños, Sary ✨

            <br>

            Que tu vida siempre esté llena
            de estrellas, felicidad y amor ❤️

        </div>

    </div>


    <!-- ================================
         CONTROLES
    ================================= -->

    <div class="controles">

        <button onclick="crearCorazones()">
            ❤️ Amor
        </button>

    </div>


    <script>

        /* =========================================
           CANVAS
        ========================================= */

        const canvas =
            document.getElementById("universo");

        const ctx =
            canvas.getContext("2d");


        let estrellas = [];

        let ancho;
        let alto;


        function ajustarCanvas() {

            ancho =
                canvas.width =
                window.innerWidth;

            alto =
                canvas.height =
                window.innerHeight;

        }


        ajustarCanvas();


        window.addEventListener(
            "resize",
            ajustarCanvas
        );


        /* =========================================
           CREAR ESTRELLAS
        ========================================= */

        for(let i = 0; i < 900; i++) {

            estrellas.push({

                x:
                    Math.random() * ancho,

                y:
                    Math.random() * alto,

                radio:
                    Math.random() * 1.8 + .2,

                velocidad:
                    Math.random() * .5 + .1,

                brillo:
                    Math.random(),

                cambio:
                    Math.random() * .03 + .01

            });

        }


        /* =========================================
           ANIMAR ESTRELLAS
        ========================================= */

        function animar() {

            ctx.fillStyle =
                "rgba(0,0,0,.25)";

            ctx.fillRect(
                0,
                0,
                ancho,
                alto
            );


            estrellas.forEach(
                estrella => {

                    estrella.y +=
                        estrella.velocidad;


                    if(estrella.y > alto) {

                        estrella.y = 0;

                        estrella.x =
                            Math.random() * ancho;

                    }


                    estrella.brillo +=
                        estrella.cambio;


                    const alpha =
                        .4 +
                        Math.abs(
                            Math.sin(
                                estrella.brillo
                            )
                        ) * .6;


                    ctx.beginPath();


                    ctx.arc(
                        estrella.x,
                        estrella.y,
                        estrella.radio,
                        0,
                        Math.PI * 2
                    );


                    /* CORRECCIÓN IMPORTANTE */

                    ctx.fillStyle =
                        `rgba(255,255,255,${alpha})`;


                    ctx.fill();

                }
            );


            requestAnimationFrame(animar);

        }


        animar();


        /* =========================================
           CREAR CORAZÓN
        ========================================= */

        function crearCorazon() {

            const corazon =
                document.createElement("div");


            corazon.className =
                "corazon";


            corazon.innerHTML =
                "❤️";


            corazon.style.left =
                Math.random() * 100 + "vw";


            corazon.style.bottom =
                "-30px";


            corazon.style.fontSize =
                (
                    15 +
                    Math.random() * 35
                ) + "px";


            corazon.style.setProperty(
                "--x",
                (
                    Math.random() * 200 -
                    100
                ) + "px"
            );


            document.body.appendChild(
                corazon
            );


            setTimeout(
                () => corazon.remove(),
                4000
            );

        }


        /* =========================================
           MUCHOS CORAZONES
        ========================================= */

        function crearCorazones() {

            for(let i = 0; i < 25; i++) {

                setTimeout(
                    crearCorazon,
                    i * 80
                );

            }

        }


        /* =========================================
           CORAZONES AUTOMÁTICOS
        ========================================= */

        setInterval(
            crearCorazon,
            800
        );


        /* =========================================
           ESTRELLAS FUGACES
        ========================================= */

        function crearEstrellaFugaz() {

            const estrella =
                document.createElement("div");


            estrella.className =
                "estrella-fugaz";


            estrella.style.left =
                Math.random() * 100 + "vw";


            estrella.style.top =
                Math.random() * 50 + "vh";


            document.body.appendChild(
                estrella
            );


            setTimeout(
                () => estrella.remove(),
                1500
            );

        }


        /* Una estrella fugaz cada cierto tiempo */

        setInterval(
            crearEstrellaFugaz,
            3500
        );


        /* =========================================
           CLICK EN LA PANTALLA
        ========================================= */

        document.addEventListener(
            "click",
            function(e) {

                if(
                    e.target.tagName === "BUTTON" ||
                    e.target.tagName === "LABEL"
                ) {
                    return;
                }


                for(let i = 0; i < 8; i++) {

                    const corazon =
                        document.createElement("div");


                    corazon.className =
                        "corazon";


                    corazon.innerHTML =
                        "💗";


                    corazon.style.left =
                        e.clientX + "px";


                    corazon.style.top =
                        e.clientY + "px";


                    corazon.style.setProperty(
                        "--x",
                        (
                            Math.random() * 200 -
                            100
                        ) + "px"
                    );


                    document.body.appendChild(
                        corazon
                    );


                    setTimeout(
                        () => corazon.remove(),
                        4000
                    );

                }

            }
        );

    </script>

</body>
</html>
