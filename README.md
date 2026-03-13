<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asmae Hasker - Modern Profile</title>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #7c3aed;
            --secondary: #a78bfa;
            --accent: #c084fc;
            --dark-bg: #0f0c29;
            --card-bg: rgba(255, 255, 255, 0.05);
            --card-border: rgba(255, 255, 255, 0.1);
            --text-main: #ffffff;
            --text-muted: #c4b5fd;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, var(--dark-bg) 0%, #302b63 50%, #24243e 100%);
            color: var(--text-main);
            display: flex;
            justify-content: center;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .poster-container {
            width: 720px;
            min-height: 1280px;
            background: radial-gradient(circle at 50% 10%, rgba(124, 58, 237, 0.2) 0%, transparent 60%),
                        linear-gradient(180deg, #0f0c29 0%, #1a163a 100%);
            position: relative;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 24px;
            box-shadow: 0 0 50px rgba(0,0,0,0.5);
        }

        /* Decorative Background Elements */
        .bg-orb {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            z-index: 0;
            animation: float 10s infinite ease-in-out;
        }
        .orb-1 { width: 300px; height: 300px; background: rgba(124, 58, 237, 0.3); top: -50px; left: -50px; }
        .orb-2 { width: 400px; height: 400px; background: rgba(56, 189, 248, 0.15); bottom: 100px; right: -100px; animation-delay: 2s; }
        .orb-3 { width: 200px; height: 200px; background: rgba(236, 72, 153, 0.2); top: 40%; left: 20%; animation-delay: 4s; }

        @keyframes float {
            0%, 100% { transform: translateY(0) scale(1); }
            50% { transform: translateY(-20px) scale(1.05); }
        }

        /* Content Wrapper */
        .content-wrapper {
            position: relative;
            z-index: 1;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* Header */
        .header-container {
            width: 100%;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            background: rgba(255,255,255,0.02);
            border: 1px solid var(--card-border);
        }
        
        .header-img {
            width: 100%;
            height: auto;
            display: block;
            object-fit: cover;
        }

        .typing-container {
            width: 100%;
            display: flex;
            justify-content: center;
            margin-bottom: 10px;
        }
        .typing-img {
            width: 100%;
            max-width: 600px;
            height: auto;
        }

        /* Badges */
        .badges-row {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 8px;
        }
        .badge-item {
            padding: 4px 12px;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.15);
            font-size: 12px;
            display: flex;
            align-items: center;
            gap: 6px;
            color: #fff;
        }

        /* Glass Card Style */
        .glass-card {
            background: var(--card-bg);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid var(--card-border);
            border-radius: 24px;
            padding: 24px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
        }

        .section-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 20px;
            font-weight: 700;
            color: var(--text-main);
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .section-title i {
            color: var(--accent);
        }

        /* About & Stats Layout */
        .top-section {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 20px;
        }

        .about-content {
            font-family: 'Space Grotesk', monospace;
            font-size: 14px;
            color: var(--text-muted);
            line-height: 1.6;
            background: rgba(0,0,0,0.2);
            padding: 16px;
            border-radius: 12px;
            border-left: 3px solid var(--primary);
        }

        .stats-img-container {
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        .stats-img {
            width: 100%;
            height: auto;
            border-radius: 12px;
            filter: brightness(0.9) contrast(1.1);
        }

        /* Tech Stack */
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: flex-start;
        }
        .tech-badge {
            display: flex;
            align-items: center;
            height: 32px;
            border-radius: 6px;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            padding: 0 10px;
            font-size: 13px;
            transition: transform 0.2s;
        }
        .tech-badge:hover {
            transform: translateY(-2px);
            background: rgba(255,255,255,0.1);
            border-color: var(--secondary);
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 16px;
        }

        .project-card {
            background: linear-gradient(90deg, rgba(124, 58, 237, 0.1) 0%, rgba(255, 255, 255, 0.02) 100%);
            border: 1px solid var(--card-border);
            border-radius: 20px;
            padding: 16px;
            display: flex;
            gap: 16px;
            align-items: center;
            transition: all 0.3s ease;
        }
        .project-card:hover {
            transform: scale(1.02);
            background: linear-gradient(90deg, rgba(124, 58, 237, 0.2) 0%, rgba(255, 255, 255, 0.05) 100%);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .project-img {
            width: 100px;
            height: 100px;
            border-radius: 16px;
            object-fit: cover;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .project-info h3 {
            font-size: 18px;
            color: #fff;
            margin-bottom: 4px;
        }
        .project-info p {
            font-size: 12px;
            color: var(--text-muted);
            margin-bottom: 8px;
            line-height: 1.4;
        }
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }
        .mini-tag {
            font-size: 10px;
            padding: 2px 8px;
            border-radius: 4px;
            background: rgba(0,0,0,0.3);
            color: #ccc;
        }

        /* Activity Section */
        .activity-section {
            display: flex;
            flex-direction: column;
            gap: 16px;
        }
        .snake-container {
            width: 100%;
            height: 200px;
            background: #0d1117;
            border-radius: 16px;
            overflow: hidden;
            position: relative;
            border: 1px solid var(--card-border);
        }
        .snake-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.9;
        }
        
        .lang-stats {
            display: flex;
            justify-content: center;
        }
        .lang-img {
            width: 200px;
            height: auto;
        }

        /* Footer */
        .footer {
            text-align: center;
            margin-top: auto;
            padding-top: 20px;
        }
        .connect-badges {
            display: flex;
            justify-content: center;
            gap: 16px;
            margin-bottom: 20px;
        }
        .footer-note {
            font-size: 12px;
            color: var(--text-muted);
            margin-bottom: 10px;
        }
        .footer-img {
            width: 100%;
            height: auto;
            border-radius: 0 0 20px 20px;
        }

    </style>
</head>
<body>

<div class="poster-container">
    <!-- Background Orbs -->
    <div class="bg-orb orb-1"></div>
    <div class="bg-orb orb-2"></div>
    <div class="bg-orb orb-3"></div>

    <div class="content-wrapper">
        
        <!-- Header Section -->
        <div class="header-container">
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=250&section=header&text=Asmae%20Hasker&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Full-Stack%20%E2%80%A2%20Flutter%20%E2%80%A2%20AI%20Maker&descAlignY=55&descSize=20&descColor=c4b5fd" alt="Header" class="header-img">
        </div>

        <div class="typing-container">
            <img src="https://readme-typing-svg.demolab.com?font=Space+Grotesk&weight=700&size=24&pause=800&color=A78BFA&center=true&vCenter=true&width=600&height=60&lines=Building+AI-Powered+Experiences+%E2%9C%A8;Flutter+%2B+Spring+Boot+Enthusiast+%F0%9F%9A%80;Open+to+PFE+Internship+%E2%80%94+April+2026+%F0%9F%8C%9F" alt="Typing SVG" class="typing-img">
        </div>

        <!-- Status Badges -->
        <div class="badges-row">
            <div class="badge-item"><i class="material-icons" style="font-size:14px;">place</i> Settat, Morocco</div>
            <div class="badge-item"><i class="material-icons" style="font-size:14px;">school</i> FST Settat</div>
            <div class="badge-item" style="background: rgba(74, 222, 128, 0.2); border-color: rgba(74, 222, 128, 0.3); color: #4ade80;">
                <i class="material-icons" style="font-size:14px;">work</i> Open to Internship
            </div>
        </div>

        <!-- Top Grid: About & Stats -->
        <div class="top-section">
            <div class="glass-card">
                <div class="section-title">
                    <i class="material-icons">person</i> About Me
                </div>
                <div class="about-content">
                    <div><strong>name:</strong> Asmae Hasker</div>
                    <div><strong>role:</strong> Junior Full-Stack Dev</div>
                    <div><strong>education:</strong> Licence ST – SI (2026)</div>
                    <div><strong>building:</strong> SmartWallet, AI Agent</div>
                    <div><strong>passions:</strong> Clean Arch, AI, UI/UX</div>
                </div>
            </div>

            <div class="stats-img-container">
                <img src="https://github-readme-stats.vercel.app/api?username=asmaeHaskar&show_icons=true&theme=transparent&hide_border=true&title_color=a78bfa&text_color=c4b5fd&icon_color=7c3aed&bg_color=0d0d1a&ring_color=7c3aed" alt="Stats" class="stats-img">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=asmaeHaskar&theme=transparent&hide_border=true&stroke=7c3aed&ring=a78bfa&fire=c084fc&currStreakNum=c4b5fd&sideNums=c4b5fd&currStreakLabel=a78bfa&sideLabels=a78bfa&background=0d0d1a" alt="Streak" class="stats-img">
            </div>
        </div>

        <!-- Tech Stack -->
        <div class="glass-card">
            <div class="section-title">
                <i class="material-icons">code</i> Tech Stack
            </div>
            <div class="tech-stack">
                <!-- Mobile & Frontend -->
                <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" class="tech-badge">
                <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" class="tech-badge">
                <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" class="tech-badge">
                <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" class="tech-badge">
                <!-- Backend & Database -->
                <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" alt="Spring Boot" class="tech-badge">
                <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" class="tech-badge">
                <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" class="tech-badge">
                <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" class="tech-badge">
                <!-- AI & DevOps -->
                <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" class="tech-badge">
                <img src="https://img.shields.io/badge/n8n-FF6B00?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n" class="tech-badge">
                <img src="https://img.shields.io/badge/Groq_API-FF4B4B?style=for-the-badge&logoColor=white" alt="Groq" class="tech-badge">
                <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" class="tech-badge">
                <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" alt="Figma" class="tech-badge">
            </div>
        </div>

        <!-- Featured Projects -->
        <div class="glass-card">
            <div class="section-title">
                <i class="material-icons">rocket_launch</i> Featured Projects
            </div>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <img src="https://sfile.chatglm.cn/images-ppt/f0758228cfbe.jpg" alt="SmartWallet" class="project-img">
                    <div class="project-info">
                        <h3>💰 SmartWallet</h3>
                        <p>Modern cross-platform finance tracker with real-time analytics.</p>
                        <div class="project-tags">
                            <span class="mini-tag">Flutter</span>
                            <span class="mini-tag">Spring Boot</span>
                            <span class="mini-tag">Docker</span>
                        </div>
                    </div>
                </div>
                <!-- Project 2 -->
                <div class="project-card">
                    <img src="https://sfile.chatglm.cn/images-ppt/bea248a9e071.png" alt="AI Agent" class="project-img">
                    <div class="project-info">
                        <h3>🤖 AI Recruitment Agent</h3>
                        <p>Autonomous agent automating job applications & cover letters.</p>
                        <div class="project-tags">
                            <span class="mini-tag">n8n</span>
                            <span class="mini-tag">Groq LLaMA 3</span>
                            <span class="mini-tag">Telegram</span>
                        </div>
                    </div>
                </div>
                <!-- Project 3 -->
                <div class="project-card">
                    <img src="https://sfile.chatglm.cn/images-ppt/206aa7f762db.jpg" alt="UniqueLearn" class="project-img">
                    <div class="project-info">
                        <h3>🎓 UniqueLearn</h3>
                        <p>Full-stack e-learning platform with course management.</p>
                        <div class="project-tags">
                            <span class="mini-tag">PHP</span>
                            <span class="mini-tag">JavaScript</span>
                            <span class="mini-tag">MySQL</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Activity & Languages -->
        <div class="glass-card activity-section">
            <div class="section-title">
                <i class="material-icons">insights</i> Activity
            </div>
            <div class="snake-container">
                <img src="https://sfile.chatglm.cn/images-ppt/20ada2514143.jpg" alt="Snake Animation" class="snake-img">
                <div style="position:absolute; top:10px; right:10px; background:rgba(0,0,0,0.6); padding:4px 8px; border-radius:4px; font-size:10px; color:#fff;">Contribution Snake</div>
            </div>
            <div class="lang-stats">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=asmaeHaskar&layout=donut&bg_color=0d0d1a&title_color=a78bfa&text_color=c4b5fd&hide_border=true&langs_count=6&size_weight=0.5&count_weight=0.5" alt="Languages" class="lang-img">
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="connect-badges">
                <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" style="height:28px;">
                <img src="https://img.shields.io/badge/Gmail-hasker.asm%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" style="height:28px;">
                <img src="https://img.shields.io/badge/GitHub-asmaeHaskar-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" style="height:28px;">
            </div>
            <p class="footer-note">Available for PFE internship starting April 2026</p>
            <img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer&animation=fadeIn" alt="Footer" class="footer-img">
        </div>

    </div>
</div>

</body>
</html>
