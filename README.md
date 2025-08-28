<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CalonWibu GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/nparticles.js/2.0.0/particles.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&family=Roboto+Mono:wght@300;400;500&display=swap');
        
        :root {
            --primary: #8a2be2;
            --secondary: #ff6ec7;
            --accent: #43cbff;
            --dark: #1a1a2e;
            --darker: #0d0d1a;
            --light: #f0f0f0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
            min-height: 100vh;
        }
        
        #particles-js {
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: 0;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 1;
        }
        
        header {
            text-align: center;
            padding: 3rem 1rem;
            position: relative;
            animation: fadeIn 1.5s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .profile-pic {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            box-shadow: 0 0 30px var(--accent);
            animation: float 6s ease-in-out infinite;
            margin-bottom: 1.5rem;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: shine 5s infinite linear;
        }
        
        @keyframes shine {
            0% { background-position: -200% center; }
            100% { background-position: 200% center; }
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--secondary);
            font-weight: 300;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: var(--light);
            font-size: 1.5rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-links a:hover {
            transform: translateY(-5px);
            background: var(--primary);
            box-shadow: 0 5px 15px rgba(142, 45, 226, 0.4);
        }
        
        section {
            background: rgba(26, 26, 46, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2.5rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            animation: slideUp 1s ease-out;
            border: 1px solid rgba(255, 110, 199, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
        }
        
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        h2 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--secondary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        h2 i {
            color: var(--accent);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }
        
        @media (max-width: 768px) {
            .about-content {
                grid-template-columns: 1fr;
            }
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .skill-category {
            background: rgba(255, 255, 255, 0.05);
            padding: 1.5rem;
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .skill-category h3 {
            color: var(--accent);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }
        
        .skill-list {
            list-style: none;
        }
        
        .skill-list li {
            margin-bottom: 0.8rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .skill-list li::before {
            content: '▶';
            color: var(--primary);
            font-size: 0.8rem;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s ease;
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .project-img {
            height: 180px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .project-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .project-content h3 {
            color: var(--accent);
            margin-bottom: 0.8rem;
        }
        
        .project-content p {
            margin-bottom: 1.5rem;
            flex-grow: 1;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }
        
        .project-tech span {
            background: rgba(67, 203, 255, 0.2);
            color: var(--accent);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-links {
            display: flex;
            gap: 1rem;
        }
        
        .project-links a {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--light);
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            background: rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        
        .project-links a:hover {
            background: var(--primary);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            text-align: center;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 1.5rem;
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: scale(1.05);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            color: var(--accent);
            font-size: 1.1rem;
        }
        
        footer {
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            animation: fadeIn 1.5s ease-out;
        }
        
        .quote {
            font-style: italic;
            color: var(--secondary);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .highlight {
            color: var(--accent);
            font-weight: 700;
        }
        
        .typewriter {
            overflow: hidden;
            border-right: 0.15em solid var(--accent);
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 0.15em;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--accent) }
        }
        
        .scroll-animation {
            opacity: 0;
            transform: translateY(50px);
            transition: opacity 1s ease, transform 1s ease;
        }
        
        .is-visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .neon-text {
            text-shadow: 0 0 5px var(--primary), 0 0 10px var(--primary), 0 0 15px var(--primary), 0 0 20px var(--secondary);
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>
    
    <div class="container">
        <header>
            <img src="https://avatars.githubusercontent.com/u/583231?v=4" alt="CalonWibu" class="profile-pic">
            <h1 class="neon-text">CalonWibu</h1>
            <p class="tagline typewriter">Frontend Developer & Anime Enthusiast</p>
            
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
            </div>
        </header>
        
        <section class="scroll-animation">
            <h2><i class="fas fa-user"></i> Tentang Saya</h2>
            <div class="about-content">
                <div>
                    <p>Halo! Saya adalah seorang <span class="highlight">Frontend Developer</span> dengan passion menciptakan pengalaman web yang menarik dan interaktif. Saya sangat menyukai anime dan budaya Jepang, yang sering menjadi inspirasi dalam project-project saya.</p>
                    <p>Dengan lebih dari 3 tahun pengalaman dalam pengembangan web, saya telah menguasai berbagai teknologi frontend dan selalu bersemangat untuk mempelajari hal-hal baru.</p>
                </div>
                <div>
                    <p>Selain coding, saya juga menikmati menggambar karakter anime, bermain game, dan tentu saja menonton anime terbaru. Filosogi saya dalam coding adalah "Clean code is like a good anime plot - it should be engaging and easy to follow".</p>
                </div>
            </div>
        </section>
        
        <section class="scroll-animation">
            <h2><i class="fas fa-code"></i> Skills & Technologies</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Frontend Development</h3>
                    <ul class="skill-list">
                        <li>HTML5 & CSS3</li>
                        <li>JavaScript (ES6+)</li>
                        <li>React.js</li>
                        <li>Vue.js</li>
                        <li>TypeScript</li>
                        <li>SASS/SCSS</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Backend Development</h3>
                    <ul class="skill-list">
                        <li>Node.js</li>
                        <li>Express.js</li>
                        <li>PHP</li>
                        <li>MySQL</li>
                        <li>MongoDB</li>
                        <li>RESTful APIs</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Tools & Utilities</h3>
                    <ul class="skill-list">
                        <li>Git & GitHub</li>
                        <li>Webpack</li>
                        <li>Figma</li>
                        <li>Adobe XD</li>
                        <li>VS Code</li>
                        <li>Netlify & Vercel</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section class="scroll-animation">
            <h2><i class="fas fa-star"></i> Proyek Unggulan</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-film"></i>
                    </div>
                    <div class="project-content">
                        <h3>Anime Discovery</h3>
                        <p>Platform untuk menemukan anime terbaik dengan UI yang memukau dan animasi fluid. Terintegrasi dengan API MyAnimeList.</p>
                        <div class="project-tech">
                            <span>React</span>
                            <span>CSS3</span>
                            <span>Anime.js</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Code</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-palette"></i>
                    </div>
                    <div class="project-content">
                        <h3>CSS Art Gallery</h3>
                        <p>Koleksi seni CSS yang menakjubkan dengan animasi yang halus dan kreatif. Semua artwork dibuat murni dengan HTML dan CSS.</p>
                        <div class="project-tech">
                            <span>HTML5</span>
                            <span>CSS3</span>
                            <span>GSAP</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Code</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img">
                        <i class="fab fa-discord"></i>
                    </div>
                    <div class="project-content">
                        <h3>Wibu Bot</h3>
                        <p>Bot Discord dengan fitur anime, kuis, dan entertainment yang lengkap. Sudah digunakan oleh lebih dari 500 server.</p>
                        <div class="project-tech">
                            <span>Node.js</span>
                            <span>Discord.js</span>
                            <span>MongoDB</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Code</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="scroll-animation">
            <h2><i class="fas fa-chart-line"></i> GitHub Stats</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">150+</div>
                    <div class="stat-label">Repositories</div>
                </div>
                
                <div class="stat-card">
                    <div class="stat-number">5.8k</div>
                    <div class="stat-label">Commits</div>
                </div>
                
                <div class="stat-card">
                    <div class="stat-number">320+</div>
                    <div class="stat-label">Contributions</div>
                </div>
                
                <div class="stat-card">
                    <div class="stat-number">42</div>
                    <div class="stat-label">Projects</div>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 2rem;">
                <img src="https://github-readme-stats.vercel.app/api?username=CalonWibu&show_icons=true&theme=radical" alt="GitHub Stats" style="max-width: 100%; border-radius: 10px;">
            </div>
        </section>
        
        <footer>
            <p class="quote">"コードは詩のようであるべきだ - Code should be like poetry" ~ Anonymous Wibu Programmer</p>
            <p>© 2023 CalonWibu. Dibuat dengan <i class="fas fa-heart" style="color: #ff6ec7;"></i> dan banyak <i class="fas fa-coffee" style="color: #8a2be2;"></i></p>
        </footer>
    </div>

    <script>
        // Inisialisasi particles.js
        document.addEventListener('DOMContentLoaded', function() {
            particlesJS('particles-js', {
                particles: {
                    number: { value: 80, density: { enable: true, value_area: 800 } },
                    color: { value: "#8a2be2" },
                    shape: { type: "circle" },
                    opacity: { value: 0.5, random: true },
                    size: { value: 3, random: true },
                    line_linked: {
                        enable: true,
                        distance: 150,
                        color: "#43cbff",
                        opacity: 0.4,
                        width: 1
                    },
                    move: {
                        enable: true,
                        speed: 2,
                        direction: "none",
                        random: true,
                        out_mode: "out",
                        bounce: false
                    }
                },
                interactivity: {
                    detect_on: "canvas",
                    events: {
                        onhover: { enable: true, mode: "grab" },
                        onclick: { enable: true, mode: "push" },
                        resize: true
                    }
                },
                retina_detect: true
            });
            
            // Scroll animation
            const scrollElements = document.querySelectorAll('.scroll-animation');
            
            const elementInView = (el, dividend = 1) => {
                const elementTop = el.getBoundingClientRect().top;
                return (elementTop <= (window.innerHeight || document.documentElement.clientHeight) / dividend);
            };
            
            const displayScrollElement = (element) => {
                element.classList.add('is-visible');
            };
            
            const hideScrollElement = (element) => {
                element.classList.remove('is-visible');
            };
            
            const handleScrollAnimation = () => {
                scrollElements.forEach((el) => {
                    if (elementInView(el, 1.2)) {
                        displayScrollElement(el);
                    } else {
                        hideScrollElement(el);
                    }
                });
            };
            
            window.addEventListener('scroll', () => {
                handleScrollAnimation();
            });
            
            // Initial check
            handleScrollAnimation();
        });
    </script>
</body>
</html>
