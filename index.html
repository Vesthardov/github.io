<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PyClient — Лучший Minecraft клиент</title>
    
    <!-- Google Fonts - Poppins -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    
    <!-- Font Awesome для иконок -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        /* ===== БАЗОВЫЕ СТИЛИ ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #121212;
            --bg-secondary: #1a1a1a;
            --bg-card: #1e1e1e;
            --text-primary: #FFFFFF;
            --text-secondary: #b0b0b0;
            --accent: #8A2BE2;
            --accent-hover: #9b4ced;
            --accent-glow: rgba(138, 43, 226, 0.4);
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* ===== ШАПКА (HEADER) ===== */
        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 1rem 2rem;
            background: rgba(18, 18, 18, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--accent), #c77dff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            cursor: pointer;
        }

        .logo i {
            -webkit-text-fill-color: var(--accent);
            margin-right: 0.3rem;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav ul li a {
            font-weight: 500;
            font-size: 1rem;
            transition: color 0.3s ease;
            position: relative;
        }

        nav ul li a:hover {
            color: var(--accent);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-primary);
        }

        /* ===== HERO СЕКЦИЯ ===== */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            overflow: hidden;
        }

        /* Видео фон - замените placeholder.mp4 на реальное видео */
        .hero-video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            transform: translate(-50%, -50%);
            z-index: -2;
            object-fit: cover;
        }

        /* Затемнение поверх видео */
        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(
                180deg,
                rgba(18, 18, 18, 0.7) 0%,
                rgba(18, 18, 18, 0.85) 50%,
                rgba(18, 18, 18, 1) 100%
            );
            z-index: -1;
        }

        /* Плейсхолдер для видео (если видео не загрузилось) */
        .hero-placeholder {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(ellipse at center, rgba(138, 43, 226, 0.15) 0%, transparent 70%),
                var(--bg-primary);
            z-index: -3;
        }

        .hero-content {
            z-index: 1;
            padding: 2rem;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-content h1 {
            font-size: clamp(3rem, 10vw, 7rem);
            font-weight: 900;
            letter-spacing: -2px;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #fff 0%, #c77dff 50%, var(--accent) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 60px var(--accent-glow);
        }

        .hero-content h2 {
            font-size: clamp(1rem, 3vw, 1.5rem);
            font-weight: 400;
            color: var(--text-secondary);
            margin-bottom: 2.5rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            font-size: 1.1rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            font-family: 'Poppins', sans-serif;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent), #6a1fb8);
            color: var(--text-primary);
            border: none;
            box-shadow: 0 4px 30px var(--accent-glow);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 40px var(--accent-glow);
            background: linear-gradient(135deg, var(--accent-hover), #7b24d6);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-primary);
            border: 2px solid var(--accent);
        }

        .btn-secondary:hover {
            background: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 8px 40px var(--accent-glow);
        }

        /* ===== СЕКЦИЯ ПРЕИМУЩЕСТВ ===== */
        .features {
            padding: 6rem 2rem;
            background: var(--bg-secondary);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: clamp(2rem, 5vw, 3rem);
            font-weight: 700;
            margin-bottom: 4rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--accent), #c77dff);
            margin: 1rem auto 0;
            border-radius: 2px;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: var(--bg-card);
            padding: 2.5rem;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--accent), #c77dff);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        .feature-card:hover::before {
            transform: scaleX(1);
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, var(--accent), #6a1fb8);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 10px 30px var(--accent-glow);
        }

        .feature-card h3 {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .feature-card p {
            color: var(--text-secondary);
            font-size: 1rem;
            line-height: 1.7;
        }

        /* ===== CTA СЕКЦИЯ ===== */
        .cta {
            padding: 8rem 2rem;
            text-align: center;
            background: 
                radial-gradient(ellipse at center, rgba(138, 43, 226, 0.2) 0%, transparent 60%),
                var(--bg-primary);
            position: relative;
        }

        .cta h2 {
            font-size: clamp(1.8rem, 5vw, 3rem);
            font-weight: 700;
            margin-bottom: 2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta .btn-primary {
            padding: 1.2rem 3rem;
            font-size: 1.2rem;
        }

        /* ===== ПОДВАЛ (FOOTER) ===== */
        footer {
            background: var(--bg-card);
            padding: 3rem 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .footer-copyright {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        .footer-socials {
            display: flex;
            gap: 1.5rem;
        }

        .footer-socials a {
            color: var(--text-secondary);
            font-size: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: color 0.3s ease;
        }

        .footer-socials a:hover {
            color: var(--accent);
        }

        .footer-socials a i {
            font-size: 1.3rem;
        }

        /* ===== АДАПТИВНОСТЬ ===== */
        @media (max-width: 768px) {
            header {
                padding: 1rem;
            }

            nav ul {
                position: fixed;
                top: 70px;
                left: 0;
                right: 0;
                background: rgba(18, 18, 18, 0.98);
                flex-direction: column;
                align-items: center;
                padding: 2rem;
                gap: 1.5rem;
                transform: translateY(-150%);
                transition: transform 0.3s ease;
            }

            nav ul.active {
                transform: translateY(0);
            }

            .mobile-menu-btn {
                display: block;
            }

            .hero-content h1 {
                letter-spacing: -1px;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn {
                width: 100%;
                max-width: 280px;
                justify-content: center;
            }

            .features {
                padding: 4rem 1rem;
            }

            .feature-card {
                padding: 2rem;
            }

            .cta {
                padding: 5rem 1rem;
            }

            .footer-content {
                flex-direction: column;
                text-align: center;
            }
        }

        /* ===== АНИМАЦИИ ПРИ СКРОЛЛЕ ===== */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease-out;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- ===== ШАПКА ===== -->
    <header>
        <div class="logo">
            <i class="fab fa-python"></i>PyClient
        </div>
        <nav>
            <ul id="nav-menu">
                <li><a href="#hero">Главная</a></li>
                <li><a href="#features">Преимущества</a></li>
                <li><a href="#cta">Скачать</a></li>
            </ul>
        </nav>
        <div class="mobile-menu-btn" onclick="toggleMenu()">
            <i class="fas fa-bars"></i>
        </div>
    </header>

    <!-- ===== ГЛАВНЫЙ ЭКРАН (HERO) ===== -->
    <section class="hero" id="hero">
        <!-- Плейсхолдер фона (если видео не загрузится) -->
        <div class="hero-placeholder"></div>
        
        <!-- 
            TODO: Замените src на путь к вашему видео.
            Рекомендуемый формат: MP4, разрешение 1920x1080, 
            сжатый для веба (10-20 МБ).
        -->
        <video class="hero-video" autoplay muted loop playsinline poster="">
            <source src="placeholder.mp4" type="video/mp4">
            <!-- Если видео не поддерживается, будет показан плейсхолдер -->
        </video>
        
        <!-- Затемнение видео -->
        <div class="hero-overlay"></div>
        
        <div class="hero-content">
            <h1>PyClient</h1>
            <h2>Лучший клиент для твоих побед в Майнкрафт.</h2>
            <div class="hero-buttons">
                <!-- TODO: Замените # на реальную ссылку на скачивание -->
                <a href="#cta" class="btn btn-primary">
                    <i class="fas fa-download"></i> Скачать
                </a>
                <!-- TODO: Замените # на ссылку на ваш Discord-сервер -->
                <a href="#" class="btn btn-secondary" target="_blank">
                    <i class="fab fa-discord"></i> Наш Discord
                </a>
            </div>
        </div>
    </section>

    <!-- ===== СЕКЦИЯ ПРЕИМУЩЕСТВ ===== -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">Наши преимущества</h2>
            <div class="features-grid">
                <!-- Карточка 1 -->
                <div class="feature-card fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>FPS Boost</h3>
                    <p>Увеличьте производительность игры в несколько раз. Наши оптимизации позволяют играть даже на слабых ПК.</p>
                </div>
                
                <!-- Карточка 2 -->
                <div class="feature-card fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-puzzle-piece"></i>
                    </div>
                    <h3>Лучшие моды</h3>
                    <p>Встроенная коллекция самых популярных модов для PvP и не только. Всё работает из коробки.</p>
                </div>
                
                <!-- Карточка 3 -->
                <div class="feature-card fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3>Кастомизация</h3>
                    <p>Полностью настраиваемый интерфейс. Создайте клиент своей мечты с помощью гибких настроек.</p>
                </div>
                
                <!-- Карточка 4 -->
                <div class="feature-card fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-shield-halved"></i>
                    </div>
                    <h3>Безопасность</h3>
                    <p>100% безопасный клиент без вирусов и майнеров. Открытый исходный код и регулярные обновления.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== CTA СЕКЦИЯ ===== -->
    <section class="cta" id="cta">
        <h2>Готов начать игру с PyClient?</h2>
        <!-- TODO: Замените # на реальную ссылку на скачивание -->
        <a href="#" class="btn btn-primary">
            <i class="fas fa-download"></i> Скачать сейчас
        </a>
    </section>

    <!-- ===== ПОДВАЛ (FOOTER) ===== -->
    <footer>
        <div class="footer-content">
            <p class="footer-copyright">© 2026 PyClient. Все права защищены.</p>
            <div class="footer-socials">
                <!-- TODO: Замените # на реальные ссылки -->
                <a href="#" target="_blank">
                    <i class="fab fa-discord"></i> Discord
                </a>
                <a href="#" target="_blank">
                    <i class="fab fa-telegram"></i> Telegram
                </a>
                <a href="#" target="_blank">
                    <i class="fab fa-youtube"></i> YouTube
                </a>
            </div>
        </div>
    </footer>

    <!-- ===== JAVASCRIPT ===== -->
    <script>
        // Мобильное меню
        function toggleMenu() {
            const menu = document.getElementById('nav-menu');
            menu.classList.toggle('active');
        }

        // Закрытие меню при клике на ссылку
        document.querySelectorAll('#nav-menu a').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('nav-menu').classList.remove('active');
            });
        });

        // Анимация появления элементов при скролле
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Плавный скролл для старых браузеров
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
