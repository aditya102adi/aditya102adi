<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aditya Kumar Sharma - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 15s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 60px;
            font-weight: bold;
            border: 5px solid rgba(255, 255, 255, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .tagline {
            font-size: 1.2em;
            opacity: 0.95;
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .social-btn {
            padding: 10px 25px;
            background: rgba(255, 255, 255, 0.2);
            border: 2px solid rgba(255, 255, 255, 0.5);
            border-radius: 25px;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .social-btn:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .content {
            padding: 40px;
        }

        .section {
            margin-bottom: 50px;
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 25px;
            color: #667eea;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-icon {
            font-size: 1.2em;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .about-card {
            padding: 20px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-radius: 15px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .about-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .about-card strong {
            color: #667eea;
            display: block;
            margin-bottom: 5px;
        }

        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
        }

        .tech-category {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 15px;
            border-left: 4px solid #667eea;
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }

        .tech-category h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        .tech-list {
            list-style: none;
        }

        .tech-list li {
            padding: 8px 0;
            color: #555;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .tech-list li::before {
            content: '▹';
            color: #667eea;
            font-weight: bold;
        }

        .project-card {
            background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 25px;
            border: 1px solid #e9ecef;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.2);
            transform: translateY(-3px);
        }

        .project-title {
            font-size: 1.5em;
            color: #667eea;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .project-features {
            list-style: none;
            margin-top: 15px;
        }

        .project-features li {
            padding: 5px 0;
            color: #555;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .project-features li::before {
            content: '✓';
            color: #28a745;
            font-weight: bold;
        }

        .goals-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .goal-item {
            padding: 20px;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            border-radius: 15px;
            color: #333;
            transition: transform 0.3s ease;
        }

        .goal-item:hover {
            transform: scale(1.05);
        }

        .footer {
            background: #2d3748;
            color: white;
            text-align: center;
            padding: 30px;
        }

        .footer p {
            margin: 10px 0;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }

            .tagline {
                font-size: 1em;
            }

            .content {
                padding: 20px;
            }

            .section h2 {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="header-content">
                <div class="avatar">AK</div>
                <h1>👋 Hi, I'm Aditya Kumar Sharma</h1>
                <p class="tagline">🚀 Software Engineer | Java & Spring Boot Developer | ML Enthusiast</p>
                <div class="social-links">
                    <a href="#" class="social-btn">📧 Email</a>
                    <a href="#" class="social-btn">💼 GitHub</a>
                    <a href="#" class="social-btn">💬 Connect</a>
                </div>
            </div>
        </header>

        <div class="content">
            <section class="section">
                <h2><span class="section-icon">🧠</span>About Me</h2>
                <p style="margin-bottom: 20px; font-size: 1.1em; color: #555;">
                    I'm a passionate software engineer with a strong foundation in Computer Science, focused on building scalable, clean, and real-world applications. I enjoy solving complex problems, writing maintainable code, and continuously improving my technical depth.
                </p>
                <div class="about-grid">
                    <div class="about-card">
                        <strong>🎓 Education</strong>
                        M.Tech Graduate in Computer Science
                    </div>
                    <div class="about-card">
                        <strong>💻 Focus</strong>
                        Backend-focused with strong Java fundamentals
                    </div>
                    <div class="about-card">
                        <strong>🔍 Interests</strong>
                        System design and real-world architectures
                    </div>
                    <div class="about-card">
                        <strong>📈 Philosophy</strong>
                        Consistent learning and long-term growth
                    </div>
                </div>
            </section>

            <section class="section">
                <h2><span class="section-icon">🛠️</span>Tech Stack</h2>
                <div class="tech-stack">
                    <div class="tech-category">
                        <h3>💡 Languages</h3>
                        <ul class="tech-list">
                            <li>Java</li>
                            <li>Python</li>
                            <li>SQL</li>
                        </ul>
                    </div>
                    <div class="tech-category">
                        <h3>⚙️ Frameworks & Tools</h3>
                        <ul class="tech-list">
                            <li>Spring Boot</li>
                            <li>Git & GitHub</li>
                            <li>Maven</li>
                        </ul>
                    </div>
                    <div class="tech-category">
                        <h3>🧩 Core Concepts</h3>
                        <ul class="tech-list">
                            <li>Object-Oriented Programming</li>
                            <li>SOLID Principles</li>
                            <li>Data Structures & Algorithms</li>
                            <li>RESTful APIs</li>
                            <li>Multithreading</li>
                            <li>Database Design</li>
                        </ul>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2><span class="section-icon">🚀</span>Featured Projects</h2>
                
                <div class="project-card">
                    <div class="project-title">
                        🌿 ML-Based Tomato Plant Disease Detection
                    </div>
                    <p>Built a CNN-based image classification system focused on real-world agricultural problem solving.</p>
                    <ul class="project-features">
                        <li>Achieved 96% accuracy</li>
                        <li>Comprehensive data preprocessing pipeline</li>
                        <li>Model training and evaluation</li>
                        <li>Real-world agricultural impact</li>
                    </ul>
                </div>

                <div class="project-card">
                    <div class="project-title">
                        🚗 Spring Boot Backend Application
                    </div>
                    <p>Industry-level backend application inspired by real-world booking platforms.</p>
                    <ul class="project-features">
                        <li>Layered architecture design</li>
                        <li>RESTful API implementation</li>
                        <li>Comprehensive validations</li>
                        <li>Production-ready code quality</li>
                    </ul>
                </div>
            </section>

            <section class="section">
                <h2><span class="section-icon">📚</span>Currently Working On</h2>
                <div class="goals-list">
                    <div class="goal-item">
                        Mastering <strong>Java + Spring Boot</strong>
                    </div>
                    <div class="goal-item">
                        Practicing <strong>DSA</strong> with structured approaches
                    </div>
                    <div class="goal-item">
                        Learning <strong>System Design</strong> fundamentals
                    </div>
                    <div class="goal-item">
                        Improving <strong>Backend Performance</strong>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2><span class="section-icon">🎯</span>Goals</h2>
                <div class="about-grid">
                    <div class="about-card">
                        <strong>💼 Career</strong>
                        Become a strong Software Development Engineer (SDE)
                    </div>
                    <div class="about-card">
                        <strong>🏗️ Impact</strong>
                        Work on large-scale systems that matter
                    </div>
                    <div class="about-card">
                        <strong>🌍 Community</strong>
                        Contribute to meaningful open-source projects
                    </div>
                    <div class="about-card">
                        <strong>📈 Growth</strong>
                        Keep learning and building every day
                    </div>
                </div>
            </section>
        </div>

        <footer class="footer">
            <p><strong>⭐ If you like my work, consider giving a star — it motivates me to build more!</strong></p>
            <p>💬 Always open to discussions, collaborations, and learning opportunities</p>
            <p style="margin-top: 20px; opacity: 0.8;">© 2026 Aditya Kumar Sharma. Keep Building, Keep Growing.</p>
        </footer>
    </div>
</body>
</html>
