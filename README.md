<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Udhayatharshini N | Data Science Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            color: #ffffff;
            overflow-x: hidden;
            min-height: 100vh;
        }

        /* Background Graphics */
        .bg-graphics {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .graphic-line {
            position: absolute;
            background: linear-gradient(90deg, transparent, #8b5cf6, transparent);
            opacity: 0.1;
            animation: lineMove 20s linear infinite;
        }

        .line-1 {
            top: 15%;
            left: -100px;
            width: 300px;
            height: 1px;
            animation-delay: 0s;
            transform: rotate(30deg);
        }

        .line-2 {
            top: 40%;
            right: -100px;
            width: 250px;
            height: 1px;
            animation-delay: 5s;
            transform: rotate(-45deg);
        }

        .graphic-dot {
            position: absolute;
            width: 3px;
            height: 3px;
            background: #8b5cf6;
            border-radius: 50%;
            opacity: 0.3;
            animation: pulse 2s infinite;
        }

        .dot-1 { top: 20%; left: 15%; animation-delay: 0s; }
        .dot-2 { top: 60%; right: 20%; animation-delay: 0.5s; }

        @keyframes lineMove {
            0% { transform: translateX(0) rotate(30deg); }
            100% { transform: translateX(500px) rotate(30deg); }
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.1; transform: scale(1); }
            50% { opacity: 0.3; transform: scale(1.5); }
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(139, 92, 246, 0.1);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5em;
            font-weight: 700;
            color: #8b5cf6;
            letter-spacing: 1px;
        }

        .nav-links {
            display: flex;
            gap: 40px;
        }

        .nav-links a {
            color: #ffffff;
            text-decoration: none;
            font-size: 1em;
            transition: color 0.3s;
            position: relative;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: #8b5cf6;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #8b5cf6;
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Main Hero Section */
        .hero-section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 40px 80px;
            max-width: 1400px;
            margin: 0 auto;
            gap: 80px;
        }

        .hero-content {
            flex: 1;
            opacity: 0;
            transform: translateX(-50px);
            animation: slideInLeft 1s ease-out forwards;
        }

        .hero-text {
            flex: 1;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            animation: fadeIn 1.5s ease-out forwards;
            animation-delay: 0.5s;
        }

        @keyframes slideInLeft {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }

        /* Typing Animation */
        .typing-container {
            margin-bottom: 30px;
        }

        .typing-text {
            font-size: 1.5rem;
            font-weight: 600;
            color: #8b5cf6;
            min-height: 60px;
        }

        .typing-line {
            display: block;
            font-size: 1.8rem;
            margin-bottom: 8px;
            color: #8b5cf6;
        }

        .typing-cursor {
            display: inline-block;
            width: 3px;
            height: 1.8rem;
            background: #8b5cf6;
            margin-left: 5px;
            animation: blink 1s infinite;
            vertical-align: bottom;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        /* Personal Intro */
        .greeting {
            font-size: 1.2rem;
            color: #8b5cf6;
            margin-bottom: 10px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #8b5cf6, #6d28d9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.2;
        }

        .title {
            font-size: 1.8rem;
            color: #e0e0e0;
            margin-bottom: 30px;
            font-weight: 500;
        }

        .intro-text {
            font-size: 1.1rem;
            color: #b0b0b0;
            line-height: 1.8;
            margin-bottom: 30px;
        }

        /* GIF Container */
        .gif-container {
            width: 100%;
            max-width: 500px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(139, 92, 246, 0.2);
            transition: transform 0.3s;
        }

        .gif-container:hover {
            transform: translateY(-5px);
            border-color: #8b5cf6;
        }

        .gif-container img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Professional Section */
        .section {
            padding: 80px 40px;
            max-width: 1400px;
            margin: 0 auto;
            opacity: 0;
            transform: translateX(-100px);
            transition: all 0.8s ease;
        }

        .section.visible {
            opacity: 1;
            transform: translateX(0);
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 50px;
            text-align: center;
            position: relative;
            color: #ffffff;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #8b5cf6, transparent);
        }

        .section-title span {
            color: #8b5cf6;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .skill-category {
            background: rgba(26, 26, 26, 0.8);
            backdrop-filter: blur(10px);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(139, 92, 246, 0.2);
            transition: all 0.3s;
        }

        .skill-category:hover {
            border-color: #8b5cf6;
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(139, 92, 246, 0.1);
        }

        .category-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(139, 92, 246, 0.1);
        }

        .category-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(139, 92, 246, 0.2));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #8b5cf6;
            font-size: 1.5rem;
        }

        .category-title {
            font-size: 1.4rem;
            font-weight: 600;
            color: #ffffff;
        }

        .skills-list {
            list-style: none;
        }

        .skill-item {
            padding: 12px 0;
            color: #b0b0b0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.05rem;
        }

        .skill-item:last-child {
            border-bottom: none;
        }

        .skill-item i {
            color: #8b5cf6;
            width: 24px;
            text-align: center;
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .contact-item {
            background: rgba(26, 26, 26, 0.8);
            backdrop-filter: blur(10px);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(139, 92, 246, 0.2);
            transition: all 0.3s;
            text-align: center;
        }

        .contact-item:hover {
            border-color: #8b5cf6;
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(139, 92, 246, 0.1);
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(139, 92, 246, 0.2));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            color: #8b5cf6;
            font-size: 1.8rem;
        }

        .contact-title {
            font-size: 1.2rem;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 10px;
        }

        .contact-link {
            color: #b0b0b0;
            text-decoration: none;
            font-size: 1.05rem;
            transition: color 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .contact-link:hover {
            color: #8b5cf6;
        }

        /* Philosophy Section */
        .philosophy-content {
            background: rgba(26, 26, 26, 0.8);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(139, 92, 246, 0.2);
            margin-top: 40px;
        }

        .philosophy-text {
            font-size: 1.2rem;
            color: #b0b0b0;
            line-height: 1.8;
            font-style: italic;
            text-align: center;
            position: relative;
            padding: 0 20px;
        }

        .philosophy-text::before,
        .philosophy-text::after {
            content: '"';
            font-size: 3rem;
            color: #8b5cf6;
            position: absolute;
            opacity: 0.5;
        }

        .philosophy-text::before {
            top: -10px;
            left: 0;
        }

        .philosophy-text::after {
            bottom: -30px;
            right: 0;
        }

        /* Footer */
        footer {
            background: rgba(10, 10, 10, 0.95);
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid rgba(139, 92, 246, 0.1);
            margin-top: 80px;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 40px;
        }

        .copyright {
            color: #808080;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero-section {
                gap: 40px;
            }
            
            .name {
                font-size: 3rem;
            }
            
            .title {
                font-size: 1.6rem;
            }
        }

        @media (max-width: 768px) {
            .hero-section {
                flex-direction: column;
                text-align: center;
                padding: 100px 20px 60px;
                gap: 60px;
            }
            
            .hero-content {
                order: 1;
            }
            
            .hero-image {
                order: 2;
            }
            
            .name {
                font-size: 2.5rem;
            }
            
            .title {
                font-size: 1.4rem;
            }
            
            .typing-text {
                font-size: 1.3rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .section {
                padding: 60px 20px;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .name {
                font-size: 2rem;
            }
            
            .title {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .skill-category,
            .contact-item {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Background Graphics -->
    <div class="bg-graphics">
        <div class="graphic-line line-1"></div>
        <div class="graphic-line line-2"></div>
        <div class="graphic-dot dot-1"></div>
        <div class="graphic-dot dot-2"></div>
    </div>

    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">Portfolio.</div>
            <div class="nav-links">
                <a href="#home">Home</a>
                <a href="#skills">Skills</a>
                <a href="#contact">Contact</a>
                <a href="#philosophy">Philosophy</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section" id="home">
        <div class="hero-content">
            <div class="hero-text">
                <div class="greeting">
                    <i class="fas fa-hand-wave"></i> Hi, I'm
                </div>
                
                <h1 class="name">Udhayatharshini N</h1>
                
                <div class="title">Data Science Developer & Software Engineer</div>
                
                <!-- Typing Animation -->
                <div class="typing-container">
                    <div class="typing-text" id="typingText">
                        <span class="typing-line"></span>
                        <span class="typing-cursor"></span>
                    </div>
                </div>
                
                <div class="intro-text">
                    Passionate about solving real-world problems through logical thinking, analytical reasoning, 
                    and practical implementation. With a strong interest in Data Science and Software Development, 
                    I focus on solving real-world problems through logical thinking, analytical reasoning, and 
                    practical implementation of concepts through hands-on work.
                </div>
                
                <div class="intro-text">
                    My journey has been shaped through project-based learning and practical implementation, 
                    where I concentrate on understanding problems deeply and refining solutions through iteration. 
                    I strongly believe that real learning happens when concepts are applied, tested, and improved over time.
                </div>
                
                <div class="intro-text">
                    I thrive in environments that encourage learning, adaptability, and thoughtful execution. 
                    With a disciplined mindset and a willingness to explore new technologies, I aim to build 
                    solutions that are not only technically sound but also meaningful and reliable in real-world scenarios.
                </div>
            </div>
        </div>
        
        <div class="hero-image">
            <div class="gif-container">
                <img src="https://cdn.dribbble.com/users/2704414/screenshots/7466903/media/b08ab576316bd4582fef189f471cd9e5.gif" 
                     alt="Developer Animation" 
                     onerror="this.onerror=null; this.src='https://img.itch.zone/aW1nLzQ2OTIwNTYuZ2lm/original/SbyK6b.gif'">
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <div class="container">
            <h2 class="section-title">Technical <span>Skills</span></h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <div class="category-header">
                        <div class="category-icon">
                            <i class="fas fa-code"></i>
                        </div>
                        <h3 class="category-title">Programming & Development</h3>
                    </div>
                    <ul class="skills-list">
                        <li class="skill-item">
                            <i class="fab fa-python"></i> Python
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-html5"></i> HTML5
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-css3-alt"></i> CSS3
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-js-square"></i> JavaScript
                        </li>
                    </ul>
                </div>

                <div class="skill-category">
                    <div class="category-header">
                        <div class="category-icon">
                            <i class="fas fa-database"></i>
                        </div>
                        <h3 class="category-title">Databases & Tools</h3>
                    </div>
                    <ul class="skills-list">
                        <li class="skill-item">
                            <i class="fas fa-database"></i> MySQL
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-table"></i> SQL
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-leaf"></i> MongoDB
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-chart-bar"></i> Power BI
                        </li>
                    </ul>
                </div>

                <div class="skill-category">
                    <div class="category-header">
                        <div class="category-icon">
                            <i class="fas fa-tools"></i>
                        </div>
                        <h3 class="category-title">Frameworks</h3>
                    </div>
                    <ul class="skills-list">
                        <li class="skill-item">
                            <i class="fas fa-flask"></i> Flask
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-stream"></i> Streamlit
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-github"></i> GitHub
                        </li>
                    </ul>
                </div>

                <div class="skill-category">
                    <div class="category-header">
                        <div class="category-icon">
                            <i class="fas fa-cogs"></i>
                        </div>
                        <h3 class="category-title">Core Competencies</h3>
                    </div>
                    <ul class="skills-list">
                        <li class="skill-item">
                            <i class="fas fa-puzzle-piece"></i> Problem Solving
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-exchange-alt"></i> Adaptability
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-users"></i> Team Collaboration
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-lightbulb"></i> Analytical Thinking
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Get In <span>Touch</span></h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <h3 class="contact-title">Email</h3>
                    <a href="mailto:udhayadharshini34@gmail.com" class="contact-link">
                        <i class="fas fa-envelope"></i> udhayadharshini34@gmail.com
                    </a>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fab fa-linkedin"></i>
                    </div>
                    <h3 class="contact-title">LinkedIn</h3>
                    <a href="https://www.linkedin.com/in/udhayadharshini-n-ab0560294/" target="_blank" class="contact-link">
                        <i class="fab fa-linkedin"></i> Connect on LinkedIn
                    </a>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    
                </div>
            </div>
        </div>
    </section>

    <!-- Philosophy Section -->
    <section id="philosophy" class="section">
        <div class="container">
            <h2 class="section-title">Professional <span>Philosophy</span></h2>
            <div class="philosophy-content">
                <p class="philosophy-text">
                    Real learning happens when concepts are applied, tested, and improved over time. 
                    I aim to build solutions that are not only technically sound but also meaningful 
                    and reliable in real-world scenarios.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <p class="copyright">
                <i class="far fa-copyright"></i> 2025 Udhayadharshini N. All rights reserved.
            </p>
        </div>
    </footer>

    <script>
        // Typing Animation
        const typingLines = [
            "Turning Data into Actionable Insights",
            "Building Solutions with Logic & Precision"
        ];
        
        let lineIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingSpeed = 100;
        const deletingSpeed = 50;
        const delayBetweenLines = 2000;
        
        const typingElement = document.querySelector('.typing-line');
        const cursorElement = document.querySelector('.typing-cursor');
        
        function typeText() {
            const currentLine = typingLines[lineIndex];
            
            if (!isDeleting) {
                typingElement.textContent = currentLine.substring(0, charIndex + 1);
                charIndex++;
                
                if (charIndex === currentLine.length) {
                    isDeleting = true;
                    setTimeout(typeText, delayBetweenLines);
                    return;
                }
            } else {
                typingElement.textContent = currentLine.substring(0, charIndex - 1);
                charIndex--;
                
                if (charIndex === 0) {
                    isDeleting = false;
                    lineIndex = (lineIndex + 1) % typingLines.length;
                }
            }
            
            setTimeout(typeText, isDeleting ? deletingSpeed : typingSpeed);
        }

        // Section Scroll Animations
        const sections = document.querySelectorAll('.section');
        
        function checkScroll() {
            sections.forEach(section => {
                const sectionTop = section.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (sectionTop < windowHeight * 0.75) {
                    section.classList.add('visible');
                }
            });
        }

        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            setTimeout(typeText, 1000);
            window.addEventListener('scroll', checkScroll);
            window.addEventListener('load', checkScroll);
            checkScroll(); // Initial check
        });
    </script>
</body>
</html>
