<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sherif Elnayad - Java Backend Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #2c3e50;
            --secondary: #34495e;
            --accent: #3498db;
            --light: #ecf0f1;
            --text: #2c3e50;
            --text-light: #7f8c8d;
        }
        
        body {
            background-color: #f5f7fa;
            color: var(--text);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            display: flex;
            align-items: center;
            gap: 40px;
            position: relative;
            z-index: 2;
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .header-text h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
        }
        
        .header-text h2 {
            font-size: 1.5rem;
            font-weight: 400;
            margin-bottom: 20px;
            color: var(--light);
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 15px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.95rem;
        }
        
        .contact-item i {
            color: var(--accent);
        }
        
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            color: var(--primary);
            display: inline-block;
            padding-bottom: 10px;
            position: relative;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .timeline {
            position: relative;
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--accent);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        
        .timeline-content::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            right: -10px;
            background-color: white;
            top: 20px;
            border-radius: 50%;
            z-index: 1;
        }
        
        .timeline-item:nth-child(even) .timeline-content::after {
            left: -10px;
        }
        
        .timeline-date {
            font-weight: bold;
            color: var(--accent);
            margin-bottom: 5px;
        }
        
        .timeline-role {
            font-weight: 600;
            margin-bottom: 5px;
            color: var(--primary);
        }
        
        .timeline-company {
            font-style: italic;
            margin-bottom: 10px;
            color: var(--text-light);
        }
        
        .timeline-desc {
            margin-top: 10px;
        }
        
        .timeline-desc ul {
            padding-left: 20px;
        }
        
        .timeline-desc li {
            margin-bottom: 5px;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-desc {
            color: var(--text-light);
            margin-bottom: 15px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        .tech-tag {
            background-color: rgba(52, 152, 219, 0.1);
            color: var(--accent);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
        }
        
        .skill-category h3 {
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent);
        }
        
        .skill-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-item {
            background-color: rgba(52, 152, 219, 0.1);
            color: var(--accent);
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .education-card {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }
        
        .edu-degree {
            font-size: 1.4rem;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .edu-school {
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 10px;
        }
        
        .edu-details {
            color: var(--text-light);
        }
        
        .publication-card {
            background: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .pub-title {
            font-size: 1.2rem;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .pub-conference {
            color: var(--text-light);
            font-style: italic;
        }
        
        footer {
            background: var(--primary);
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--accent);
        }
        
        @media screen and (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            .contact-info {
                justify-content: center;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-content::after {
                left: -10px !important;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="header-text">
                    <h1>Sherif Abd El Khalek Ali</h1>
                    <h2>Java Backend Developer</h2>
                    <div class="contact-info">
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <span>Sherifali121@gmail.com</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <span>+201060512256</span>
                        </div>
                        <div class="contact-item">
                            <i class="fab fa-linkedin"></i>
                            <span>linkedin.com/in/sherif-el-nayad-96b9a4162</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
    
    <section id="experience">
        <div class="container">
            <div class="section-title">
                <h2>Work Experience</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">Nov 2024 - Present</div>
                        <div class="timeline-role">Java Backend Developer</div>
                        <div class="timeline-company">Etisalat& (e&), Cairo, Egypt</div>
                        <div class="timeline-desc">
                            <ul>
                                <li>Utilized PL/SQL to interact with the database, ensuring efficient data retrieval and manipulation</li>
                                <li>Worked with a team on multiple backend solutions using spring boot, JPA, hibernate</li>
                                <li>Designed and developed a new microservices architecture to replace legacy monolithic components</li>
                                <li>Utilized Kafka for efficient inter-service communication and real-time data streaming</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">Apr 2024 - Nov 2024</div>
                        <div class="timeline-role">Java Backend Developer</div>
                        <div class="timeline-company">Flairstech (Ciena Account), Cairo, Egypt</div>
                        <div class="timeline-desc">
                            <ul>
                                <li>Collaborated in sprint planning, providing accurate estimates for tasks</li>
                                <li>Developed and integrated new features based on evolving requirements</li>
                                <li>Worked closely with cross-squad teams to coordinate and integrate complex features</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">Mar 2023 - Mar 2024</div>
                        <div class="timeline-role">Java Backend Developer</div>
                        <div class="timeline-company">OPay Egypt, Cairo, Egypt</div>
                        <div class="timeline-desc">
                            <ul>
                                <li>Utilized SQL interact with the database, ensuring efficient data retrieval and manipulation</li>
                                <li>Worked with a team on multiple backend solutions using spring boot, JPA, hibernate</li>
                                <li>Played a key role in fixing production issues and maintaining high availability</li>
                                <li>Identifying & resolving issues in legacy APIs while improving overall system reliability</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">Jan 2022 - Mar 2023</div>
                        <div class="timeline-role">Java Backend Developer</div>
                        <div class="timeline-company">Silicon Expert, Cairo, Egypt</div>
                        <div class="timeline-desc">
                            <ul>
                                <li>Worked with a team on multiple backend solutions using spring boot, JPA, hibernate</li>
                                <li>Utilized SQL to interact with the database, ensuring efficient data retrieval and manipulation</li>
                                <li>Worked with cross-functional squads to understand and address customer needs</li>
                                <li>Worked on identifying & resolving issues in legacy APIs while improving system reliability</li>
                                <li>Adapted to agile development style, delivering high-quality software within tight deadlines</li>
                            </ul>
                        </div>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2>Projects</h2>
            </div>
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Wabtec CMT</h3>
                        <p class="project-desc">A web application that manages the information of parts and components to support the decision on buying certain parts from certain manufacturers.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Spring Boot</span>
                            <span class="tech-tag">Java</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Eshtri Aqar</h3>
                        <p class="project-desc">An Ecommerce web application that handles transactions regarding real estate, the website is responsible for selling and showing various units.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Spring Boot</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>Professional Skills</h2>
            </div>
            
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Languages</h3>
                    <div class="skill-list">
                        <span class="skill-item">Java</span>
                        <span class="skill-item">JavaScript</span>
                        <span class="skill-item">PHP</span>
                        <span class="skill-item">Python</span>
                        <span class="skill-item">Dart</span>
                        <span class="skill-item">SQL</span>
                        <span class="skill-item">C++</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Frameworks & Technologies</h3>
                    <div class="skill-list">
                        <span class="skill-item">Spring Boot</span>
                        <span class="skill-item">Hibernate</span>
                        <span class="skill-item">JPA</span>
                        <span class="skill-item">Flutter</span>
                        <span class="skill-item">Laravel</span>
                        <span class="skill-item">Hyperledger Fabric</span>
                        <span class="skill-item">Vue JS</span>
                        <span class="skill-item">Node JS</span>
                        <span class="skill-item">Ruby On Rails</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Tools & Databases</h3>
                    <div class="skill-list">
                        <span class="skill-item">PL/SQL</span>
                        <span class="skill-item">Kafka</span>
                        <span class="skill-item">Git</span>
                        <span class="skill-item">Docker</span>
                        <span class="skill-item">Microservices</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="education">
        <div class="container">
            <div class="section-title">
                <h2>Education</h2>
            </div>
            
            <div class="education-card">
                <h3 class="edu-degree">Bachelor of Computer Science</h3>
                <p class="edu-school">Misr International University</p>
                <p class="edu-details">2016-2020 | Cairo, Egypt | Good Grade</p>
            </div>
        </div>
    </section>
    
    <section id="publication">
        <div class="container">
            <div class="section-title">
                <h2>Publication</h2>
            </div>
            
            <div class="publication-card">
                <h3 class="pub-title">Egyptian Universities Digital Certificates Verification Model Using Blockchain</h3>
                <p class="pub-conference">Accepted for publication in: 2020 9th International Conference on Software and Information Engineering (ICSIE 2020)</p>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="mailto:Sherifali121@gmail.com"><i class="fas fa-envelope"></i></a>
            </div>
            <p>&copy; 2023 Sherif Elnayad. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
