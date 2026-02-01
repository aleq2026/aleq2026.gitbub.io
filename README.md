<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Para la dueña de mi corazón ❤️</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            overflow: hidden;
        }

        .card {
            background: white;
            padding: 35px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.25);
            max-width: 420px;
            position: relative;
        }

        h1 {
            color: #ff4d6d;
        }

        p {
            color: #555;
            font-size: 17px;
        }

        img {
            width: 150px;
            border-radius: 15px;
            margin: 15px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .buttons {
            margin-top: 25px;
            position: relative;
            height: 80px;
        }

        button {
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            font-size: 16px;
            cursor: pointer;
            position: absolute;
            transition: 0.3s ease;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
            left: 20%;
        }

        #noBtn {
            background-color: #ccc;
            color: #333;
            left: 55%;
        }

        .heart {
            position: absolute;
            font-size: 24px;
            animation: float 4s infinite ease-in;
            color: #ff4d6d;
        }

        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-800px); opacity: 0; }
        }
    </style>
</head>
<body>

<!-- 🎵 MÚSICA (cambia "musica.mp3" por la canción que quieras) -->
<audio autoplay loop>
    <source src="musica.mp3" type="audio/mpeg">
</audio>

<div class="card">
    <h1>Para ti, mi amor 💖</h1>

    <!-- 📸 FOTO (pon aquí una foto de ustedes y nómbrala "foto.jpg") -->
    <img src="foto.jpg" alt="Nosotros">

    <p>De todas las personas del mundo…</p>
    <p>Eres mi lugar favorito, mi paz, y la mejor abogada de mi corazón 🥹⚖️❤️</p>
    <p><strong>¿Quieres ser mi San Valentín? 🌹</strong></p>

    <div class="buttons">
        <button id="yesBtn">Sí 💘</button>
        <button id="noBtn">No 😢</button>
    </div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");

    noBtn.addEventListener("mouseover", () => {
        const x = Math.random() * 300 - 150;
        const y = Math.random() * 200 - 100;
        noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    yesBtn.addEventListener("click", () => {
        document.body.innerHTML = `
            <div style="display:flex;flex-direction:column;justify-content:center;align-items:center;height:100vh;background:linear-gradient(135deg,#ff758c,#ff7eb3);font-family:Arial;text-align:center;">
                <h1 style="color:white;font-size:42px;">Sabía que dirías que sí 😍</h1>
                <p style="color:white;font-size:22px;">Prometo hacerte feliz todos los días ❤️</p>
                <h2 style="color:white;">Este San Valentín es solo el inicio 🌹✨</h2>
            </div>
        `;
    });

    setInterval(() => {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.top = "100vh";
        heart.style.fontSize = Math.random() * 20 + 15 + "px";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 4000);
    }, 300);
</script>

</body>
</html>
