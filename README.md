<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sherif Elnayad - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #64ffda;
            box-shadow: 0 0 20px rgba(100, 255, 218, 0.5);
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #64ffda, #00bcd4);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #8892b0;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-icons a {
            color: #ccd6f6;
            font-size: 1.8rem;
            transition: all 0.3s ease;
        }
        
        .social-icons a:hover {
            color: #64ffda;
            transform: translateY(-5px);
        }
        
        .tabs {
            display: flex;
            justify-content: center;
            margin: 30px 0;
            flex-wrap: wrap;
        }
        
        .tab-btn {
            padding: 12px 24px;
            background: transparent;
            border: none;
            color: #ccd6f6;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border-bottom: 2px solid transparent;
            margin: 0 10px;
        }
        
        .tab-btn:hover {
            color: #64ffda;
        }
        
        .tab-btn.active {
            color: #64ffda;
            border-bottom: 2px solid #64ffda;
        }
        
        .tab-content {
            display: none;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            backdrop-filter: blur(10px);
            margin-bottom: 30px;
            animation: fadeIn 0.5s ease;
        }
        
        .tab-content.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 20px;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .project-card h3 {
            color: #64ffda;
            margin-bottom: 10px;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        
        .skill {
            background: rgba(100, 255, 218, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }
        
        .skill:hover {
            background: rgba(100, 255, 218, 0.2);
            transform: scale(1.05);
        }
        
        .contact-form {
            display: grid;
            gap: 20px;
            margin-top: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group label {
            margin-bottom: 8px;
            color: #ccd6f6;
        }
        
        .form-group input, .form-group textarea {
            padding: 12px;
            border: none;
            border-radius: 5px;
            background: rgba(255, 255, 255, 0.1);
            color: #fff;
        }
        
        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        .btn {
            padding: 12px 30px;
            background: linear-gradient(45deg, #64ffda, #00bcd4);
            border: none;
            border-radius: 5px;
            color: #0a192f;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(100, 255, 218, 0.4);
        }
        
        footer {
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            color: #8892b0;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .mode-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.1);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            z-index: 100;
            transition: all 0.3s ease;
        }
        
        .mode-toggle:hover {
            transform: rotate(30deg);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .project-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="mode-toggle" id="modeToggle">
        <i class="fas fa-moon"></i>
    </div>
    
    <div class="container">
        <header>
            <img src="https://avatars.githubusercontent.com/u/123456789?v=4" alt="Sherif Elnayad" class="profile-img">
            <h1>Sherif Elnayad</h1>
            <p class="tagline">Full Stack Developer & UI/UX Enthusiast</p>
            
            <div class="social-icons">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-dev"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
            </div>
        </header>
        
        <div class="tabs">
            <button class="tab-btn active" data-tab="about">About</button>
            <button class="tab-btn" data-tab="projects">Projects</button>
            <button class="tab-btn" data-tab="skills">Skills</button>
            <button class="tab-btn" data-tab="contact">Contact</button>
        </div>
        
        <div class="tab-content active" id="about">
            <h2>Hello World! 👋</h2>
            <p>I'm Sherif, a passionate full-stack developer with a love for creating interactive and responsive web applications. With a background in computer science and several years of experience, I specialize in JavaScript technologies across the whole stack.</p>
            <br>
            <p>When I'm not coding, you can find me contributing to open source projects, writing technical blogs, or exploring new technologies in the ever-evolving world of web development.</p>
            <br>
            <p>I believe in writing clean, efficient code and creating user experiences that are both beautiful and functional.</p>
        </div>
        
        <div class="tab-content" id="projects">
            <h2>Featured Projects</h2>
            <p>Here are some of my recent projects that I'm particularly proud of:</p>
            
            <div class="project-grid">
                <div class="project-card">
                    <h3>E-Commerce Platform</h3>
                    <p>A full-stack e-commerce solution with React, Node.js, and MongoDB. Features user authentication, payment processing, and admin dashboard.</p>
                </div>
                <div class="project-card">
                    <h3>Task Management App</h3>
                    <p>A drag-and-drop task management application with real-time updates using Vue.js and Firebase.</p>
                </div>
                <div class="project-card">
                    <h3>Weather Dashboard</h3>
                    <p>An interactive weather application with data visualization using OpenWeather API and D3.js.</p>
                </div>
                <div class="project-card">
                    <h3>Fitness Tracker</h3>
                    <p>A mobile-friendly fitness tracking application with workout plans and progress analytics.</p>
                </div>
            </div>
        </div>
        
        <div class="tab-content" id="skills">
            <h2>Technical Skills</h2>
            <p>Here are some of the technologies and tools I work with:</p>
            
            <div class="skills-container">
                <span class="skill">JavaScript</span>
                <span class="skill">TypeScript</span>
                <span class="skill">React</span>
                <span class="skill">Vue.js</span>
                <span class="skill">Node.js</span>
                <span class="skill">Express</span>
                <span class="skill">MongoDB</span>
                <span class="skill">PostgreSQL</span>
                <span class="skill">Git</span>
                <span class="skill">Docker</span>
                <span class="skill">AWS</span>
                <span class="skill">CSS3</span>
                <span class="skill">SASS</span>
                <span class="skill">Python</span>
                <span class="skill">REST APIs</span>
                <span class="skill">GraphQL</span>
            </div>
        </div>
        
        <div class="tab-content" id="contact">
            <h2>Get In Touch</h2>
            <p>Feel free to reach out if you want to collaborate on something exciting. I'm always open to discussing new projects and ideas.</p>
            
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" placeholder="Your Name">
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" placeholder="Your Email">
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" placeholder="Your Message"></textarea>
                </div>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </div>
        
        <footer>
            <p>Made with ❤️ by Sherif Elnayad</p>
            <p>© 2023 - All rights reserved</p>
        </footer>
    </div>

    <script>
        // Tab functionality
        const tabBtns = document.querySelectorAll('.tab-btn');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                const tabId = btn.getAttribute('data-tab');
                
                // Remove active class from all buttons and contents
                tabBtns.forEach(b => b.classList.remove('active'));
                tabContents.forEach(c => c.classList.remove('active'));
                
                // Add active class to clicked button and corresponding content
                btn.classList.add('active');
                document.getElementById(tabId).classList.add('active');
            });
        });
        
        // Dark/Light mode toggle
        const modeToggle = document.getElementById('modeToggle');
        let isDarkMode = true;
        
        modeToggle.addEventListener('click', () => {
            isDarkMode = !isDarkMode;
            
            if (isDarkMode) {
                document.body.style.background = 'linear-gradient(135deg, #0f2027, #203a43, #2c5364)';
                modeToggle.innerHTML = '<i class="fas fa-moon"></i>';
            } else {
                document.body.style.background = 'linear-gradient(135deg, #8EC5FC, #E0C3FC)';
                document.body.style.color = '#333';
                modeToggle.innerHTML = '<i class="fas fa-sun"></i>';
            }
        });
        
        // Simple form validation
        const contactForm = document.querySelector('.contact-form');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thanks for your message! (This is a demo, no message was sent)');
            contactForm.reset();
        });
    </script>
</body>
</html>
