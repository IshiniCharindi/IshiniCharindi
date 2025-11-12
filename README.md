<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishini Dewamiththa | Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2C67F2;
            --secondary: #8A2BE2;
            --accent: #00D4AA;
            --dark: #0A0A14;
            --light: #F5F7FA;
            --gray: #6C757D;
            --card-bg: rgba(255, 255, 255, 0.05);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, var(--dark) 0%, #1a1a2e 50%, #16213e 100%);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        .header {
            padding: 80px 0 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(44, 103, 242, 0.1) 0%, rgba(138, 43, 226, 0.05) 30%, transparent 70%);
            z-index: -1;
        }

        .profile-image {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 20px;
            border: 4px solid var(--primary);
            box-shadow: 0 0 30px rgba(44, 103, 242, 0.5);
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 10px;
            background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -1px;
        }

        .tagline {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--light);
            font-weight: 300;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .badge {
            background: var(--card-bg);
            padding: 8px 16px;
            border-radius: 50px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: var(--transition);
        }

        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Section Styles */
        .section {
            margin: 60px 0;
            padding: 40px 0;
        }

        .section-title {
            font-size: 2.2rem;
            margin-bottom: 30px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .education-card {
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: var(--transition);
        }

        .education-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        .university {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--accent);
        }

        .degree {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }

        .gpa {
            font-size: 1rem;
            color: var(--gray);
        }

        .quote {
            font-style: italic;
            padding: 20px;
            border-left: 4px solid var(--primary);
            background: rgba(44, 103, 242, 0.1);
            border-radius: 0 10px 10px 0;
            margin-top: 20px;
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .tech-item {
            background: var(--card-bg);
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.05);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .tech-item:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            border-color: rgba(44, 103, 242, 0.3);
        }

        .tech-icon {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .tech-name {
            font-size: 0.8rem;
            color: var(--light);
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: var(--card-bg);
            border-radius: 15px;
            overflow: hidden;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .project-header {
            padding: 20px;
            background: rgba(44, 103, 242, 0.1);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .project-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 5px;
            color: var(--accent);
        }

        .project-desc {
            font-size: 0.95rem;
            color: var(--light);
            opacity: 0.9;
        }

        .project-body {
            padding: 20px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }

        .tech-tag {
            background: rgba(44, 103, 242, 0.2);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        /* Achievements */
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }

        .achievement-card {
            background: var(--card-bg);
            padding: 20px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            gap: 15px;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .achievement-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .achievement-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
        }

        .achievement-text h3 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }

        .achievement-text p {
            font-size: 0.9rem;
            color: var(--gray);
        }

        /* Contact */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .contact-link {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: var(--card-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .contact-link:hover {
            transform: translateY(-5px) scale(1.1);
            background: var(--primary);
            box-shadow: 0 10px 20px rgba(44, 103, 242, 0.3);
        }

        /* Stats */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .stat-card {
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 10px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .stat-label {
            font-size: 1rem;
            color: var(--gray);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 0;
            margin-top: 60px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }

        .floating {
            animation: float 5s ease-in-out infinite;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .name {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <div class="profile-image">
                <i class="fas fa-code"></i>
            </div>
            <h1 class="name">Ishini Dewamiththa</h1>
            <p class="tagline">Aspiring Full Stack Developer | Undergraduate at Uva Wellassa University of Sri Lanka</p>
            
            <div class="badges">
                <div class="badge">🚀 Full Stack Developer</div>
                <div class="badge">🎓 GPA: 3.83/4.00</div>
                <div class="badge">📍 Kandy, Sri Lanka</div>
            </div>
        </header>

        <!-- About Section -->
        <section class="section">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="education-card floating">
                    <h3 class="university">Uva Wellassa University of Sri Lanka</h3>
                    <p class="degree">B.Sc. (Hons) in Computer Science and Technology</p>
                    <p class="gpa">Current GPA: 3.83/4.00</p>
                    <div class="quote">
                        "Code is not just logic — it's creativity, empathy, and problem-solving blended together."
                    </div>
                </div>
                <div>
                    <p>I'm a passionate full-stack developer with a strong foundation in computer science and a drive to create innovative solutions. Currently exploring React Native and NestJS while building scalable applications.</p>
                    <div class="contact-links">
                        <a href="mailto:ishinidewamiththa@gmail.com" class="contact-link">
                            <i class="fas fa-envelope"></i>
                        </a>
                        <a href="https://linkedin.com/in/ishini-dewamiththa" class="contact-link">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="https://github.com/IshiniCharindi" class="contact-link">
                            <i class="fab fa-github"></i>
                        </a>
                        <a href="https://ishinidewamiththa.me" class="contact-link">
                            <i class="fas fa-globe"></i>
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Tech Stack Section -->
        <section class="section">
            <h2 class="section-title">Technical Stack</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <i class="fab fa-js tech-icon"></i>
                    <span class="tech-name">JavaScript</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-react tech-icon"></i>
                    <span class="tech-name">React</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-node-js tech-icon"></i>
                    <span class="tech-name">Node.js</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-python tech-icon"></i>
                    <span class="tech-name">Python</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-java tech-icon"></i>
                    <span class="tech-name">Java</span>
                </div>
                <div class="tech-item">
                    <i class="fas fa-database tech-icon"></i>
                    <span class="tech-name">MySQL</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-git-alt tech-icon"></i>
                    <span class="tech-name">Git</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-docker tech-icon"></i>
                    <span class="tech-name">Docker</span>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="section">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">Traffic Flow Optimization</h3>
                        <p class="project-desc">Reinforcement Learning-based traffic light control system</p>
                    </div>
                    <div class="project-body">
                        <p>AI-powered system to reduce congestion in Sri Lanka using TensorFlow and SUMO simulation.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">TensorFlow</span>
                            <span class="tech-tag">SUMO</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">Detroits ERP System</h3>
                        <p class="project-desc">Comprehensive ERP platform with biometric integration</p>
                    </div>
                    <div class="project-body">
                        <p>Integrated biometric attendance, payroll, and finance modules for enterprise management.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React.js</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MySQL</span>
                            <span class="tech-tag">Redis</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">COOP Digital</h3>
                        <p class="project-desc">Mobile app for cooperative banking</p>
                    </div>
                    <div class="project-body">
                        <p>Secure account management and banking services for cooperative societies.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React Native</span>
                            <span class="tech-tag">NestJS</span>
                            <span class="tech-tag">MySQL</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Achievements Section -->
        <section class="section">
            <h2 class="section-title">Achievements & Highlights</h2>
            <div class="achievements-grid">
                <div class="achievement-card">
                    <div class="achievement-icon">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <div class="achievement-text">
                        <h3>Champion – SheCoderess v6</h3>
                        <p>Hackathon & Design Showdown, 2025</p>
                    </div>
                </div>
                
                <div class="achievement-card">
                    <div class="achievement-icon">
                        <i class="fas fa-medal"></i>
                    </div>
                    <div class="achievement-text">
                        <h3>Participant – NBQSA</h3>
                        <p>National ICT Awards</p>
                    </div>
                </div>
                
                <div class="achievement-card">
                    <div class="achievement-icon">
                        <i class="fas fa-award"></i>
                    </div>
                    <div class="achievement-text">
                        <h3>Dean's List Recognition</h3>
                        <p>2022–2024</p>
                    </div>
                </div>
                
                <div class="achievement-card">
                    <div class="achievement-icon">
                        <i class="fas fa-microphone"></i>
                    </div>
                    <div class="achievement-text">
                        <h3>Champion – EngWrangle 2.0</h3>
                        <p>Debate Competition</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Stats Section -->
        <section class="section">
            <h2 class="section-title">GitHub Insights</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">150+</div>
                    <div class="stat-label">Contributions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">15</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">6</div>
                    <div class="stat-label">Languages</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">3.83</div>
                    <div class="stat-label">GPA Score</div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="footer">
            <p>Let's collaborate on impactful projects! Reach out at <a href="mailto:ishinidewamiththa@gmail.com" style="color: var(--accent);">ishinidewamiththa@gmail.com</a></p>
            <p style="margin-top: 20px; color: var(--gray);">"Turning ideas into interactive experiences — one commit at a time."</p>
        </footer>
    </div>

    <script>
        // Add floating animation to multiple elements
        document.addEventListener('DOMContentLoaded', function() {
            const floatingElements = document.querySelectorAll('.floating');
            floatingElements.forEach((el, index) => {
                el.style.animationDelay = `${index * 0.5}s`;
            });
            
            // Add scroll animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);
            
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.style.opacity = 0;
                section.style.transform = 'translateY(20px)';
                section.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
