<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdulrahman - Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #34495e;
            --text-color: #333;
            --border-radius: 8px;
            --box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f9f9f9;
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 60px 0;
            text-align: center;
            border-radius: 0 0 20px 20px;
            margin-bottom: 40px;
        }

        .profile-header {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }

        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid white;
            box-shadow: var(--box-shadow);
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: var(--primary-color);
        }

        .title {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 20px;
        }

        .cta-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 24px;
            background-color: var(--secondary-color);
            color: white;
            text-decoration: none;
            border-radius: var(--border-radius);
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: var(--box-shadow);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--primary-color);
        }

        section {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: var(--box-shadow);
        }

        h2 {
            color: var(--primary-color);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        h2 i {
            color: var(--secondary-color);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background-color: var(--light-color);
            padding: 20px;
            border-radius: var(--border-radius);
        }

        .skill-category h3 {
            margin-bottom: 15px;
            color: var(--dark-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-category h3 i {
            color: var(--secondary-color);
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-tag {
            background-color: white;
            padding: 8px 15px;
            border-radius: 30px;
            font-size: 0.9rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            border: 1px solid #e0e0e0;
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .stat-card {
            background-color: var(--light-color);
            padding: 20px;
            border-radius: var(--border-radius);
            text-align: center;
        }

        .stat-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--secondary-color);
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--dark-color);
        }

        .languages-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .language-bar {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .language-name {
            min-width: 100px;
            font-weight: 600;
        }

        .language-progress {
            flex-grow: 1;
            height: 12px;
            background-color: #e0e0e0;
            border-radius: 6px;
            overflow: hidden;
        }

        .language-progress-fill {
            height: 100%;
            background-color: var(--secondary-color);
            border-radius: 6px;
        }

        .language-percent {
            min-width: 50px;
            text-align: right;
            font-weight: 600;
        }

        footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            color: var(--dark-color);
            border-top: 1px solid var(--light-color);
        }

        @media (max-width: 768px) {
            .title {
                font-size: 2rem;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                justify-content: center;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="profile-header">
                <div class="avatar">
                    <i class="fas fa-user"></i>
                </div>
                <h1 class="title">Mouad </h1>
                <p class="subtitle">Full Stack Developer </p>
                <div class="cta-buttons">
                    <a href="#" class="btn btn-outline"><i class="fab fa-github"></i> GitHub</a>
                    <a href="#" class="btn btn-outline"><i class="fab fa-linkedin"></i> LinkedIn</a>
                    <a href="#" class="btn btn-outline"><i class="fas fa-envelope"></i> Contact</a>
                </div>
            </div>
        </div>
    </header>

    <div class="container">
        <section class="about">
            <h2><i class="fas fa-user"></i> About Me</h2>
            <p>I'm a passionate software developer specializing in full-stack web development with a focus on creating efficient, scalable, and user-friendly applications. I believe in continuous learning, clean code, and contributing to the open-source community.</p>
            
            <h3 style="margin-top: 20px;">Current Focus</h3>
            <ul style="margin-left: 20px; margin-top: 10px;">
                <li>Building modern, responsive web applications</li>
                <li>Developing developer tools and productivity software</li>
                <li>Contributing to open-source projects</li>
                <li>Continuous learning and skill enhancement</li>
            </ul>
        </section>

        <section class="skills">
            <h2><i class="fas fa-code"></i> Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fab fa-html5"></i> Frontend Development</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">HTML5</span>
                        <span class="skill-tag">CSS3</span>
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">React</span>
                        <span class="skill-tag">Tailwind CSS</span>
                        <span class="skill-tag">jQuery</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-server"></i> Backend Development</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Node.js</span>
                        <span class="skill-tag">PHP</span>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">MySQL</span>
                        <span class="skill-tag">SQLite</span>
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">Vite</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-database"></i> Databases & Tools</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">MySQL</span>
                        <span class="skill-tag">SQLite</span>
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">GitHub</span>
                        <span class="skill-tag">Vite</span>
                    </div>
                </div>
            </div>
        </section>

        <section class="github-stats">
            <h2><i class="fab fa-github"></i> GitHub Statistics</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-value">10</div>
                    <div class="stat-label">Total Stars Earned</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">833</div>
                    <div class="stat-label">Total Commits (Last Year)</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">4</div>
                    <div class="stat-label">Total Pull Requests</div>
                </div>
            </div>
            
            <h3 style="margin-top: 30px;">Most Used Languages</h3>
            <div class="languages-container">
                <div class="language-bar">
                    <span class="language-name">JavaScript</span>
                    <div class="language-progress">
                        <div class="language-progress-fill" style="width: 34.93%"></div>
                    </div>
                    <span class="language-percent">34.93%</span>
                </div>
                <div class="language-bar">
                    <span class="language-name">HTML</span>
                    <div class="language-progress">
                        <div class="language-progress-fill" style="width: 24.86%"></div>
                    </div>
                    <span class="language-percent">24.86%</span>
                </div>
                <div class="language-bar">
                    <span class="language-name">PHP</span>
                    <div class="language-progress">
                        <div class="language-progress-fill" style="width: 15.81%"></div>
                    </div>
                    <span class="language-percent">15.81%</span>
                </div>
                <div class="language-bar">
                    <span class="language-name">RCS</span>
                    <div class="language-progress">
                        <div class="language-progress-fill" style="width: 9.08%"></div>
                    </div>
                    <span class="language-percent">9.08%</span>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <div class="container">
            <p>&copy; 2023 Abdulrahman. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
