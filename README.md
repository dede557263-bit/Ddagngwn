```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dede Agung Gunawan - Profil Pribadi</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header dengan Anime Chibi */
        .header {
            text-align: center;
            padding: 50px 20px;
            position: relative;
            animation: fadeInDown 1s ease-out;
        }

        .chibi-hero {
            width: 250px;
            height: 250px;
            margin: 0 auto 30px;
            border-radius: 50%;
            border: 8px solid rgba(255,255,255,0.3);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            background: url('https://i.imgur.com/8zKzL8k.png') center/cover; /* Chibi anime boy */
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-title {
            color: white;
            font-size: 3.5em;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            margin-bottom: 10px;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .hero-subtitle {
            font-size: 1.5em;
            color: rgba(255,255,255,0.9);
            font-weight: 300;
            animation: fadeInUp 1s ease-out 0.8s both;
        }

        /* Section Cards */
        .sections {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            padding: 50px 0;
        }

        .card {
            background: rgba(255,255,255,0.95);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1);
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }

        .card-icon {
            font-size: 4em;
            color: #667eea;
            margin-bottom: 20px;
        }

        .card h3 {
            font-size: 1.8em;
            color: #333;
            margin-bottom: 15px;
        }

        .card p {
            color: #666;
            line-height: 1.6;
            font-size: 1.1em;
        }

        /* Chibi Friends */
        .chibi-friends {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .chibi-friend {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            border: 4px solid rgba(255,255,255,0.5);
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .chibi-friend:hover {
            transform: scale(1.1) rotate(10deg);
        }

        .chibi-friend:nth-child(1) { background: url('https://i.imgur.com/Qwertyu.png') center/cover; }
        .chibi-friend:nth-child(2) { background: url('https://i.imgur.com/AbcdeFg.png') center/cover; }
        .chibi-friend:nth-child(3) { background: url('https://i.imgur.com/Xyz1234.png') center/cover; }

        /* Social Media */
        .social {
            margin-top: 40px;
        }

        .social a {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            color: white;
            text-decoration: none;
            background: rgba(255,255,255,0.2);
            padding: 12px 25px;
            border-radius: 50px;
            margin: 0 10px;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .social a:hover {
            background: white;
            color: #667eea;
            transform: translateY(-3px);
        }

        /* Animations */
        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-title { font-size: 2.5em; }
            .hero-subtitle { font-size: 1.2em; }
            .sections { grid-template-columns: 1fr; }
            .chibi-hero { width: 200px; height: 200px; }
        }

        /* Floating particles */
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: white;
            border-radius: 50%;
            animation: floatParticle 6s infinite linear;
        }

        @keyframes floatParticle {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>
    <!-- Floating Particles -->
    <div class="particle" style="left: 10%; animation-delay: 0s;"></div>
    <div class="particle" style="left: 20%; animation-delay: 1s;"></div>
    <div class="particle" style="left: 80%; animation-delay: 2s;"></div>
    <div class="particle" style="left: 90%; animation-delay: 3s;"></div>

    <div class="container">
        <header class="header">
            <div class="chibi-hero"></div>
            <h1 class="hero-title">Dede Agung Gunawan</h1>
            <p class="hero-subtitle">Lahir 1 July 2007 | Subang, Jawa Barat</p>
            
            <div class="chibi-friends">
                <div class="chibi-friend"></div>
                <div class="chibi-friend"></div>
                <div class="chibi-friend"></div>
            </div>

            <div class="social">
                <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
                <a href="#"><i class="fab fa-tiktok"></i> TikTok</a>
                <a href="#"><i class="fab fa-discord"></i> Discord</a>
            </div>
        </header>

        <section class="sections">
            <div class="card" style="animation: fadeInUp 1s ease-out 1.2s both;">
                <div class="card-icon">
                    <i class="fas fa-home"></i>
                </div>
                <h3>Tempat Tinggal</h3>
                <p>🏠 Tinggal di kota Subang, Jawa Barat. Kota yang nyaman dengan suasana yang tenang dan penuh kenangan indah! 🌾</p>
            </div>

            <div class="card" style="animation: fadeInUp 1s ease-out 1.4s both;">
                <div class="card-icon">
                    <i class="fas fa-birthday-cake"></i>
                </div>
                <h3>Tanggal Lahir</h3>
                <p>🎂 Lahir pada 1 July 2007. Cancer ♋️ - Penuh emosi tapi setia kawan! Saat ini berusia 17 tahun dan siap menaklukkan dunia! 🚀</p>
            </div>

            <div class="card" style="animation: fadeInUp 1s ease-out 1.6s both;">
                <div class="card-icon">
                    <i class="fas fa-heart"></i>
                </div>
                <h3>Hobi & Minat</h3>
                <p>❤️ Anime lover, gaming addict, dan foodie! Selalu excited dengan hal-hal baru dan petualangan seru bersama teman-teman! 🎮✨</p>
            </div>

            <div class="card" style="animation: fadeInUp 1s ease-out 1.8s both;">
                <div class="card-icon">
                    <i class="fas fa-star"></i>
                </div>
                <h3>Impian</h3>
                <p>⭐ Ingin menjadi developer keren yang bisa bikin website se-wow ini! Juga traveling ke Jepang untuk ketemu waifu impian! 🌸✈️</p>
            </div>
        </section>
    </div>

    <script>
        // Tambah efek klik pada chibi friends
        document.querySelectorAll('.chibi-friend').forEach((friend, index) => {
            friend.addEventListener('click', () => {
                friend.style.transform = 'scale(1.3) rotate(360deg)';
                setTimeout(() => {
                    friend.style.transform = 'scale(1.1) rotate(10deg)';
                }, 500);
            });
        });

        // Parallax effect
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('.header');
            parallax.style.transform = `translateY(${scrolled * 0.5}px)`;
        });
    </script>
</body>
</html>
```

