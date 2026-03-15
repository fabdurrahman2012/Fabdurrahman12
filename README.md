<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Faiz Abdurrahman | Shiroko Theme</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-blue: #56c2ff;
            --dark-bg: rgba(10, 10, 15, 0.85);
            --glass: rgba(255, 255, 255, 0.1);
            --glow: 0 0 15px rgba(86, 194, 255, 0.5);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #050505;
            font-family: 'Poppins', sans-serif;
            color: white;
            overflow-x: hidden;
            min-height: 100vh;
        }

        /* Latar Belakang Shiroko */
        .background-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://wallpapercave.com/wp/wp8951261.jpg') no-repeat center center/cover;
            z-index: -2;
            filter: brightness(0.4);
        }

        /* Cahaya Biru Bergerak (Animated Glow) */
        .ambient-light {
            position: fixed;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(86, 194, 255, 0.3) 0%, transparent 70%);
            border-radius: 50%;
            z-index: -1;
            filter: blur(50px);
            animation: float 10s infinite alternate;
        }

        @keyframes float {
            0% { transform: translate(0, 0); }
            50% { transform: translate(100vw, 50vh); }
            100% { transform: translate(50vw, 100vh); }
        }

        /* Intro Animation (Full Screen Profile) */
        #intro-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #000;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 100;
            transition: all 1s cubic-bezier(0.7, 0, 0.3, 1);
        }

        .intro-img {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            border: 4px solid var(--primary-blue);
            object-fit: cover;
            box-shadow: var(--glow);
            transition: 1s ease;
        }

        .shrink .intro-img {
            width: 100px;
            height: 100px;
            transform: translateY(-35vh);
        }

        .shrink#intro-screen {
            background: rgba(0,0,0,0);
            pointer-events: none;
        }

        /* Main Content */
        .container {
            max-width: 500px;
            margin: 0 auto;
            padding: 120px 20px 50px;
            opacity: 0;
            transform: translateY(20px);
            transition: 1s ease 0.5s;
        }

        .container.show {
            opacity: 1;
            transform: translateY(0);
        }

        header {
            text-align: center;
            margin-bottom: 30px;
        }

        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.5rem;
            color: var(--primary-blue);
            text-shadow: var(--glow);
            margin-bottom: 5px;
        }

        .subtitle {
            font-size: 0.9rem;
            opacity: 0.7;
            font-style: italic;
        }

        /* Card Links */
        .link-card {
            background: var(--dark-bg);
            border: 1px solid var(--glass);
            backdrop-filter: blur(10px);
            padding: 15px 20px;
            margin-bottom: 15px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            text-decoration: none;
            color: white;
            transition: 0.3s;
            position: relative;
            overflow: hidden;
        }

        .link-card:hover {
            background: rgba(86, 194, 255, 0.2);
            border-color: var(--primary-blue);
            transform: scale(1.03);
            box-shadow: var(--glow);
        }

        .link-card i {
            font-size: 1.5rem;
            margin-right: 15px;
            width: 30px;
            text-align: center;
            color: var(--primary-blue);
        }

        .link-card span {
            font-weight: 500;
            letter-spacing: 1px;
        }

        /* Donate Button Special */
        .donate-btn {
            background: linear-gradient(45deg, #0070ba, #56c2ff);
            border: none;
            margin-top: 10px;
            box-shadow: 0 4px 15px rgba(0, 112, 186, 0.4);
        }

        .donate-btn i { color: white; }

        /* Responsive */
        @media (max-width: 600px) {
            .container { padding-top: 100px; }
        }
    </style>
</head>
<body>

    <div class="background-overlay"></div>
    <div class="ambient-light"></div>

    <div id="intro-screen">
        <img src="https://lh3.googleusercontent.com/d/1TO3xlZjqgquFoGz-CHEibX4EdSmfl6LQ" alt="Profile" class="intro-img">
    </div>

    <div class="container" id="main-content">
        <header>
            <h1>FAIZ ABDURRAHMAN</h1>
            <p class="subtitle">Anime Lovers & Gamer | Shiroko Edition</p>
        </header>

        <a href="https://link.dana.id/minta?full_url=https://qr.dana.id/v1/281012012025101761838442" class="link-card donate-btn" target="_blank">
            <i class="fa-solid fa-wallet"></i>
            <span>DONATE VIA DANA</span>
        </a>

        <hr style="margin: 20px 0; border: 0; border-top: 1px solid var(--glass);">

        <a href="https://www.tiktok.com/@fabdurrahman2012" class="link-card" target="_blank">
            <i class="fa-brands fa-tiktok"></i>
            <span>TikTok Utama</span>
        </a>

        <a href="https://www.instagram.com/fabdurrahman2012/" class="link-card" target="_blank">
            <i class="fa-brands fa-instagram"></i>
            <span>Instagram</span>
        </a>

        <a href="https://www.youtube.com/@fabdurrahman2012" class="link-card" target="_blank">
            <i class="fa-brands fa-youtube"></i>
            <span>YouTube Channel</span>
        </a>

        <a href="https://www.facebook.com/faizabdurrahman2012" class="link-card" target="_blank">
            <i class="fa-brands fa-facebook"></i>
            <span>Facebook Personal</span>
        </a>

        <a href="https://www.facebook.com/profile.php?id=61558035861404&sk=sports" class="link-card" target="_blank">
            <i class="fa-brands fa-facebook-messenger"></i>
            <span>Facebook Sports</span>
        </a>

        <a href="https://chat.whatsapp.com/KMjImMIMG2K9D287847qmp" class="link-card" target="_blank">
            <i class="fa-brands fa-whatsapp"></i>
            <span>WhatsApp Anime Lovers</span>
        </a>

    </div>

    <script>
        // Animasi Intro
        window.addEventListener('load', () => {
            setTimeout(() => {
                const intro = document.getElementById('intro-screen');
                const content = document.getElementById('main-content');
                
                intro.classList.add('shrink');
                content.classList.add('show');
            }, 1500); // Intro muncul selama 1.5 detik
        });

        // Cahaya biru bergerak mengikuti kursor/acak
        const light = document.querySelector('.ambient-light');
        document.addEventListener('mousemove', (e) => {
            light.style.left = e.pageX - 150 + 'px';
            light.style.top = e.pageY - 150 + 'px';
        });
    </script>
</body>
</html>
