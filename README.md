<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ashraful Islam Akash | Web Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1.1rem;
        }

        nav ul li a:hover {
            color: var(--secondary-color);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            text-align: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary-color);
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        .hero h2 {
            font-size: 1.8rem;
            color: var(--secondary-color);
            margin-bottom: 20px;
            font-weight: 500;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
        }

        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        /* Sections */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color);
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .about-text p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .about-image {
            flex: 1;
            text-align: center;
        }

        .about-image img {
            width: 100%;
            max-width: 400px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-10px);
        }

        .skill-card i {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }

        .skill-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        /* Links Section */
        .links-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .link-card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            width: 300px;
            transition: transform 0.3s;
        }

        .link-card:hover {
            transform: translateY(-10px);
        }

        .link-card i {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--secondary-color);
        }

        .link-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .link-card a {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s;
            margin-top: 10px;
        }

        .link-card a:hover {
            background-color: var(--secondary-color);
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: white;
            padding: 40px 0;
            text-align: center;
        }

        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .social-links {
            display: flex;
            gap: 20px;
            margin: 20px 0;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--secondary-color);
        }

        .copyright {
            margin-top: 20px;
            opacity: 0.8;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .about-image {
                order: -1;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero h2 {
                font-size: 1.5rem;
            }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--primary-color);
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            }
            
            nav ul.active {
                display: flex;
            }
            
            nav ul li {
                margin: 10px 0;
                margin-left: 0;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            section {
                padding: 60px 0;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero h2 {
                font-size: 1.3rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .link-card {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">Ashraful<span>Akash</span></a>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#links">Links</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <img src="./akash.jpg" alt="Ashraful Islam Akash" class="profile-img">
            <h1>Ashraful Islam Akash</h1>
            <h2>Web Developer & Student</h2>
            <p>I'm a passionate web developer and a student at IUBAT. I love solving problems and have competitive programming experience on Codeforces. Currently expanding my skills in full-stack web development.</p>
            <a href="#links" class="btn">Connect With Me</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Web Developer & Problem Solver</h3>
                    <p>Hello! I'm Ashraful Islam Akash, a dedicated web development student at IUBAT with a strong passion for creating functional and beautiful web applications.</p>
                    <p>When I'm not studying or working on web projects, you can find me solving algorithmic problems on Codeforces. Competitive programming has helped me develop strong problem-solving skills and a logical approach to coding challenges.</p>
                    <p>I'm constantly learning new technologies and frameworks to stay up-to-date with the ever-evolving web development landscape. My goal is to become a full-stack developer who can create comprehensive digital solutions.</p>
                    <p>I believe in writing clean, efficient, and maintainable code. I enjoy collaborating with others and am always open to new opportunities to learn and grow as a developer.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1517077304055-6e89abbf09b0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Web Development">
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" style="background-color: #f5f7fa;">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill-card">
                    <i class="fas fa-code"></i>
                    <h3>Web Development</h3>
                    <p>Proficient in HTML5, CSS3, JavaScript, and responsive web design. Experience with modern frameworks and libraries to create dynamic web applications.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-laptop-code"></i>
                    <h3>Problem Solving</h3>
                    <p>Regular participant in Codeforces contests. Strong algorithmic thinking and ability to solve complex programming problems efficiently.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-graduation-cap"></i>
                    <h3>Continuous Learning</h3>
                    <p>Currently pursuing studies in Computer Science at IUBAT. Constantly updating skills with new technologies and best practices in software development.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Links Section -->
    <section id="links">
        <div class="container">
            <div class="section-title">
                <h2>Connect With Me</h2>
            </div>
            <div class="links-container">
                <div class="link-card">
                    <i class="fab fa-github"></i>
                    <h3>GitHub</h3>
                    <p>Check out my projects, contributions, and code repositories on GitHub.</p>
                    <a href="https://github.com/Ashraful-akash467" target="_blank">Visit GitHub</a>
                </div>
                <div class="link-card">
                    <i class="fab fa-facebook"></i>
                    <h3>Facebook</h3>
                    <p>Connect with me on Facebook to stay updated with my latest activities.</p>
                    <a href="https://www.facebook.com/share/1Ar2XKt6it/" target="_blank">Visit Facebook</a>
                </div>
                <div class="link-card">
                    <i class="fab fa-linkedin"></i>
                    <h3>LinkedIn</h3>
                    <p>View my professional profile and connect with me on LinkedIn.</p>
                    <a href="https://www.linkedin.com/in/ashraful-islam-akash-387906253?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">Visit LinkedIn</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <a href="#" class="logo">Ashraful<span>.</span></a>
                <p>Web Developer & Student at IUBAT</p>
                <div class="social-links">
                    <a href="https://github.com/Ashraful-akash467" target="_blank"><i class="fab fa-github"></i></a>
                    <a href="https://www.facebook.com/share/1Ar2XKt6it/" target="_blank"><i class="fab fa-facebook"></i></a>
                    <a href="https://www.linkedin.com/in/ashraful-islam-akash-387906253?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank"><i class="fab fa-linkedin"></i></a>
                </div>
                <p class="copyright">&copy; 2023 Ashraful Islam Akash. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('nav ul').classList.toggle('active');
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('nav ul li a').forEach(link => {
            link.addEventListener('click', function() {
                document.querySelector('nav ul').classList.remove('active');
            });
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>

