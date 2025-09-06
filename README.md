<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tauseeb Ahmed Siddiqui - GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #f0f6fc;
            line-height: 1.6;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            animation: fadeIn 1s ease-out;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #58a6ff;
            margin-bottom: 20px;
            animation: float 6s ease-in-out infinite;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #58a6ff, #8cb6ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: slideIn 1s ease-out;
        }
        
        h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #c9d1d9;
        }
        
        h3 {
            font-size: 1.5rem;
            margin: 30px 0 15px;
            color: #58a6ff;
            display: flex;
            align-items: center;
        }
        
        h3 i {
            margin-right: 10px;
        }
        
        .section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            animation: slideUp 0.8s ease-out;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.12);
        }
        
        .stat-value {
            font-size: 2.5rem;
            font-weight: 700;
            margin: 10px 0;
            color: #58a6ff;
        }
        
        .stat-label {
            font-size: 1rem;
            color: #8b949e;
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .skill-item {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 10px;
            padding: 15px 10px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            transform: scale(1.05);
            background: rgba(255, 255, 255, 0.12);
            box-shadow: 0 5px 15px rgba(88, 166, 255, 0.2);
        }
        
        .skill-icon {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #58a6ff;
        }
        
        .skill-name {
            font-size: 0.9rem;
            color: #c9d1d9;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.08);
            color: #c9d1d9;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-btn:hover {
            background: #58a6ff;
            color: #0d1117;
            transform: translateY(-3px);
        }
        
        .chart-container {
            position: relative;
            height: 300px;
            margin-top: 20px;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }
        
        .badge {
            background: linear-gradient(45deg, #238636, #2ea043);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }
        
        .badge i {
            font-size: 0.8rem;
        }
        
        .activity-container {
            margin-top: 20px;
        }
        
        .activity-bar {
            height: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            overflow: hidden;
            margin: 5px 0;
        }
        
        .activity-fill {
            height: 100%;
            background: linear-gradient(90deg, #238636, #2ea043);
            border-radius: 5px;
            width: 0;
            transition: width 2s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideIn {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        @keyframes slideUp {
            from { transform: translateY(30px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        @media (max-width: 768px) {
            .stats-container {
                grid-template-columns: 1fr;
            }
            
            .skills-container {
                grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img src="https://avatars.githubusercontent.com/u/583231?v=4" alt="Profile Image" class="profile-img">
            <h1>Tauseeb Ahmed Siddiqui</h1>
            <h2>Web & Android Developer from India</h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/siddiqui-tauseef-ahmed" class="social-btn" target="_blank">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://leetcode.com/u/sidtauseef/" class="social-btn" target="_blank">
                    <i class="fab fa-python"></i>
                </a>
                <a href="https://github.com/sidtauseef" class="social-btn" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
                <a href="mailto:tauseefahmed.siddiqui@gmail.com" class="social-btn">
                    <i class="far fa-envelope"></i>
                </a>
            </div>
        </div>
        
        <div class="stats-container">
            <div class="stat-card">
                <i class="fas fa-code-branch fa-2x"></i>
                <div class="stat-value">42</div>
                <div class="stat-label">Repositories</div>
            </div>
            <div class="stat-card">
                <i class="fas fa-star fa-2x"></i>
                <div class="stat-value">128</div>
                <div class="stat-label">Stars Earned</div>
            </div>
            <div class="stat-card">
                <i class="fas fa-code-commit fa-2x"></i>
                <div class="stat-value">576</div>
                <div class="stat-label">Commits</div>
            </div>
            <div class="stat-card">
                <i class="fas fa-project-diagram fa-2x"></i>
                <div class="stat-value">15</div>
                <div class="stat-label">Projects</div>
            </div>
        </div>
        
        <div class="section">
            <h3><i class="fas fa-user-circle"></i> About Me</h3>
            <p>I'm a passionate full-stack developer with expertise in Web and Android development. I enjoy building innovative solutions and learning new technologies. With a strong foundation in programming principles and experience across multiple platforms, I write clean, efficient, and maintainable code.</p>
            
            <div class="badges">
                <div class="badge"><i class="fas fa-medal"></i> Full-Stack Developer</div>
                <div class="badge"><i class="fas fa-medal"></i> Android Specialist</div>
                <div class="badge"><i class="fas fa-medal"></i> Problem Solver</div>
            </div>
        </div>
        
        <div class="section">
            <h3><i class="fas fa-code"></i> Technologies & Skills</h3>
            <p>Here are some of the technologies I work with:</p>
            
            <div class="skills-container">
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-android"></i></div>
                    <div class="skill-name">Android</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-react"></i></div>
                    <div class="skill-name">React</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-node-js"></i></div>
                    <div class="skill-name">Node.js</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-python"></i></div>
                    <div class="skill-name">Python</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-js"></i></div>
                    <div class="skill-name">JavaScript</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-database"></i></div>
                    <div class="skill-name">MongoDB</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-database"></i></div>
                    <div class="skill-name">MySQL</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-docker"></i></div>
                    <div class="skill-name">Docker</div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h3><i class="fas fa-chart-line"></i> Coding Activity</h3>
            <p>My weekly development activity:</p>
            
            <div class="activity-container">
                <div>Monday <span class="activity-percent">70%</span></div>
                <div class="activity-bar">
                    <div class="activity-fill" style="width: 70%"></div>
                </div>
                
                <div>Tuesday <span class="activity-percent">90%</span></div>
                <div class="activity-bar">
                    <div class="activity-fill" style="width: 90%"></div>
                </div>
                
                <div>Wednesday <span class="activity-percent">85%</span></div>
                <div class="activity-bar">
                    <div class="activity-fill" style="width: 85%"></div>
                </div>
                
                <div>Thursday <span class="activity-percent">60%</span></div>
                <div class="activity-bar">
                    <div class="activity-fill" style="width: 60%"></div>
                </div>
                
                <div>Friday <span class="activity-percent">95%</span></div>
                <div class="activity-bar">
                    <div class="activity-fill" style="width: 95%"></div>
                </div>
                
                <div>Weekend <span class="activity-percent">40%</span></div>
                <div class="activity-bar">
                    <div class="activity-fill" style="width: 40%"></div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h3><i class="fas fa-trophy"></i> GitHub Stats</h3>
            <div class="chart-container">
                <canvas id="statsChart"></canvas>
            </div>
        </div>
    </div>

    <script>
        // Animate activity bars on page load
        document.addEventListener('DOMContentLoaded', function() {
            // Animate activity bars
            const activityBars = document.querySelectorAll('.activity-fill');
            activityBars.forEach(bar => {
                const width = bar.style.width;
                bar.style.width = '0';
                setTimeout(() => {
                    bar.style.width = width;
                }, 500);
            });
            
            // Initialize chart
            const ctx = document.getElementById('statsChart').getContext('2d');
            const chart = new Chart(ctx, {
                type: 'radar',
                data: {
                    labels: ['Web Development', 'Android', 'Backend', 'Databases', 'DevOps', 'UI/UX'],
                    datasets: [{
                        label: 'Skill Level',
                        data: [85, 90, 75, 70, 65, 80],
                        backgroundColor: 'rgba(88, 166, 255, 0.2)',
                        borderColor: 'rgba(88, 166, 255, 1)',
                        pointBackgroundColor: 'rgba(88, 166, 255, 1)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgba(88, 166, 255, 1)'
                    }]
                },
                options: {
                    scales: {
                        r: {
                            angleLines: {
                                display: true
                            },
                            suggestedMin: 0,
                            suggestedMax: 100
                        }
                    },
                    animation: {
                        duration: 2000,
                        easing: 'easeOutQuart'
                    }
                }
            });
        });
    </script>
</body>
</html>
