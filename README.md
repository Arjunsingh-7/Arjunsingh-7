<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arjun Singh - Tech Stack</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Fira Code', 'Monaco', monospace;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .container {
            max-width: 1000px;
            width: 100%;
        }

        .header {
            text-align: center;
            margin-bottom: 60px;
            animation: slideDown 0.8s ease-out;
        }

        .header h1 {
            color: #00ff88;
            font-size: 48px;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(0, 255, 136, 0.5);
            letter-spacing: 2px;
        }

        .header p {
            color: #b0b0b0;
            font-size: 18px;
            margin-bottom: 5px;
        }

        .header .subtitle {
            color: #00ffff;
            font-size: 14px;
            margin-top: 10px;
            animation: pulse 2s infinite;
        }

        .tech-section {
            margin-bottom: 50px;
            animation: slideUp 0.8s ease-out;
        }

        .section-title {
            color: #00ff88;
            font-size: 20px;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #00ff88;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 15px;
            margin-bottom: 40px;
        }

        .key {
            position: relative;
            perspective: 1000px;
        }

        .key-content {
            background: linear-gradient(145deg, #1a1a2e, #16213e);
            border: 2px solid #00ff88;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.1), inset 0 0 20px rgba(0, 255, 136, 0.05);
            animation: fadeInUp 0.6s ease-out backwards;
            transform-style: preserve-3d;
        }

        .key-content:nth-child(1) { animation-delay: 0.1s; }
        .key-content:nth-child(2) { animation-delay: 0.15s; }
        .key-content:nth-child(3) { animation-delay: 0.2s; }
        .key-content:nth-child(4) { animation-delay: 0.25s; }
        .key-content:nth-child(5) { animation-delay: 0.3s; }
        .key-content:nth-child(6) { animation-delay: 0.35s; }

        .key-content:hover {
            border-color: #00ffff;
            box-shadow: 0 0 30px rgba(0, 255, 255, 0.5), 
                        inset 0 0 20px rgba(0, 255, 136, 0.1),
                        0 10px 30px rgba(0, 255, 136, 0.3);
            transform: translateY(-5px) rotateX(10deg);
        }

        .key-icon {
            font-size: 24px;
            margin-bottom: 8px;
            display: block;
        }

        .key-label {
            color: #00ff88;
            font-size: 14px;
            font-weight: bold;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }

        .key-content:hover .key-label {
            color: #00ffff;
            text-shadow: 0 0 10px rgba(0, 255, 255, 0.8);
        }

        /* Animated glow effect */
        .key-content::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 30% 30%, rgba(0, 255, 136, 0.1), transparent);
            border-radius: 8px;
            opacity: 0;
            animation: glow 3s ease-in-out infinite;
        }

        .key-content:hover::before {
            animation: glowHover 0.5s ease-out forwards;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px) rotateX(-90deg);
            }
            to {
                opacity: 1;
                transform: translateY(0) rotateX(0);
            }
        }

        @keyframes glow {
            0%, 100% {
                opacity: 0;
                box-shadow: 0 0 0px rgba(0, 255, 136, 0);
            }
            50% {
                opacity: 1;
                box-shadow: 0 0 20px rgba(0, 255, 136, 0.3);
            }
        }

        @keyframes glowHover {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.7;
            }
        }

        .stats-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 50px;
            text-align: center;
        }

        .stat-card {
            background: linear-gradient(145deg, #1a1a2e, #16213e);
            border: 2px solid #00ff88;
            border-radius: 8px;
            padding: 20px;
            color: #00ff88;
            font-size: 14px;
            animation: slideUp 0.8s ease-out 0.5s backwards;
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.1);
        }

        .stat-card:hover {
            box-shadow: 0 0 30px rgba(0, 255, 255, 0.5);
            border-color: #00ffff;
        }

        .stat-number {
            font-size: 28px;
            font-weight: bold;
            color: #00ffff;
            margin-bottom: 5px;
        }

        .code-block {
            background: #0f0c29;
            border: 1px solid #00ff88;
            border-radius: 8px;
            padding: 20px;
            margin: 30px 0;
            color: #00ff88;
            font-size: 14px;
            overflow-x: auto;
            animation: slideUp 0.8s ease-out;
            line-height: 1.6;
        }

        .code-block .comment {
            color: #666;
        }

        .code-block .string {
            color: #00ffff;
        }

        .footer {
            text-align: center;
            margin-top: 60px;
            color: #b0b0b0;
            animation: slideUp 0.8s ease-out 0.8s backwards;
        }

        .footer a {
            color: #00ff88;
            text-decoration: none;
            transition: all 0.3s ease;
            margin: 0 10px;
        }

        .footer a:hover {
            color: #00ffff;
            text-shadow: 0 0 10px rgba(0, 255, 255, 0.8);
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 36px;
            }

            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            }

            .key-label {
                font-size: 12px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>$ ARJUN SINGH</h1>
            <p>AI & Data Science Enthusiast</p>
            <p>Full Stack Developer | IoT Explorer</p>
            <p class="subtitle">Building innovative tech solutions 🚀</p>
        </div>

        <div class="code-block">
<span class="comment"># Quick intro</span>
arjun = {
    <span class="string">"location"</span>: <span class="string">"Kanpur, UP 🇮🇳"</span>,
    <span class="string">"passion"</span>: <span class="string">"Building innovative solutions"</span>,
    <span class="string">"current_focus"</span>: <span class="string">"Cloud Computing & ML"</span>
}
        </div>

        <div class="tech-section">
            <div class="section-title">💻 Languages</div>
            <div class="tech-grid">
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🐍</span>
                        <span class="key-label">Python</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">⚡</span>
                        <span class="key-label">JavaScript</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">☕</span>
                        <span class="key-label">Java</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="tech-section">
            <div class="section-title">🎨 Frontend</div>
            <div class="tech-grid">
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">⚛️</span>
                        <span class="key-label">React</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">▲</span>
                        <span class="key-label">Next.js</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🏗️</span>
                        <span class="key-label">HTML5</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🎨</span>
                        <span class="key-label">CSS3</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="tech-section">
            <div class="section-title">⚙️ Backend & Database</div>
            <div class="tech-grid">
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🔧</span>
                        <span class="key-label">Django</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🗄️</span>
                        <span class="key-label">MySQL</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="tech-section">
            <div class="section-title">📊 Data Science & AI</div>
            <div class="tech-grid">
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">📈</span>
                        <span class="key-label">NumPy</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🐼</span>
                        <span class="key-label">Pandas</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">📊</span>
                        <span class="key-label">Matplotlib</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="tech-section">
            <div class="section-title">🛠️ Tools & Platforms</div>
            <div class="tech-grid">
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🔀</span>
                        <span class="key-label">Git</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">🐙</span>
                        <span class="key-label">GitHub</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">💾</span>
                        <span class="key-label">VS Code</span>
                    </div>
                </div>
                <div class="key">
                    <div class="key-content">
                        <span class="key-icon">▲</span>
                        <span class="key-label">Vercel</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="stats-section">
            <div class="stat-card">
                <div class="stat-number">10+</div>
                <div>Projects Completed</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">5</div>
                <div>Technologies Mastered</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">4</div>
                <div>Live Deployments</div>
            </div>
        </div>

        <div class="footer">
            <p style="margin-top: 40px; margin-bottom: 20px;">
                <strong>Let's Connect!</strong>
            </p>
            <a href="https://github.com/Arjunsingh-7" target="_blank">GitHub</a>
            <a href="https://www.linkedin.com/in/arjun-singh-2519ab280/" target="_blank">LinkedIn</a>
            <a href="https://arjunsingh-omega.vercel.app/" target="_blank">Portfolio</a>
            <a href="mailto:arjunsingh792002@gmail.com">Email</a>
            <p style="margin-top: 30px; color: #666;">
                ⭐ Star my repositories if you find them useful!
            </p>
            <p style="color: #666;">
                🤝 Open to collaborations and exciting projects!
            </p>
        </div>
    </div>

    <script>
        // Add click animation
        document.querySelectorAll('.key-content').forEach(key => {
            key.addEventListener('click', function() {
                this.style.animation = 'none';
                setTimeout(() => {
                    this.style.animation = '';
                }, 10);
            });
        });

        // Randomize animation start
        document.querySelectorAll('.key-content').forEach((key, index) => {
            key.style.animationDelay = (index * 0.08) + 's';
        });
    </script>
</body>
</html>
