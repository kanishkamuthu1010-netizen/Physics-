<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PhyVisuals | Master 11th & 12th Physics</title>
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --accent-green: #10b981;
            --accent-blue: #3b82f6;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 5%;
            background-color: rgba(15, 23, 42, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid #334155;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(to right, var(--accent-blue), var(--accent-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        nav a {
            color: var(--text-main);
            text-decoration: none;
            margin-left: 2rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--accent-green);
        }

        .hero {
            text-align: center;
            padding: 5rem 1rem;
            background: radial-gradient(circle at center, #1e3a8a 0%, var(--bg-color) 70%);
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            color: var(--text-muted);
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 2rem auto;
        }

        .cta-btn {
            background: linear-gradient(to right, var(--accent-blue), var(--accent-green));
            color: white;
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .cta-btn:hover {
            transform: scale(1.05);
        }

        .section-title {
            text-align: center;
            margin: 4rem 0 2rem 0;
            font-size: 2rem;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 0 5%;
        }

        .card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 2rem;
            border: 1px solid #334155;
            transition: border-color 0.3s;
        }

        .card:hover {
            border-color: var(--accent-green);
        }

        .badge {
            background-color: #3b82f6;
            color: white;
            padding: 0.2rem 0.6rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Interactive Simulation Box Demo */
        .simulation-box {
            background: #020617;
            border: 2px dashed #334155;
            height: 250px;
            border-radius: 8px;
            margin-top: 1.5rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .projectile-demo {
            width: 20px;
            height: 20px;
            background-color: var(--accent-green);
            border-radius: 50%;
            position: absolute;
            bottom: 20px;
            left: 20px;
            animation: fly 4s infinite ease-in-out;
        }

        @keyframes fly {
            0% { bottom: 20px; left: 20px; }
            50% { bottom: 180px; left: 50%; }
            100% { bottom: 20px; left: calc(100% - 40px); }
        }

        .pricing-card {
            text-align: center;
            border: 2px solid var(--accent-green);
        }

        .price {
            font-size: 2.5rem;
            font-weight: bold;
            margin: 1rem 0;
            color: var(--accent-green);
        }

        footer {
            text-align: center;
            padding: 3rem;
            margin-top: 5rem;
            border-top: 1px solid #334155;
            color: var(--text-muted);
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">PhyVisuals</div>
        <nav>
            <a href="#modules">Modules</a>
            <a href="#demo">Live Demo</a>
            <a href="#pricing">Premium Access</a>
        </nav>
    </header>

    <section class="hero">
        <h1>Stop Memorizing Physics. <br>Start Seeing It.</h1>
        <p>Interactive 2D & 3D animations designed specifically for 11th and 12th-grade students to ace boards, JEE, and NEET.</p>
        <button class="cta-btn" onclick="document.getElementById('pricing').scrollIntoView({behavior: 'smooth'});">Get Premium Access</button>
    </section>

    <h2 class="section-title" id="modules">Explore Class Modules</h2>
    <div class="grid">
        <div class="card">
            <span class="badge" style="background-color: var(--accent-blue);">Class 11th</span>
            <h3>Mechanics & Waves</h3>
            <p>Visualize changing vectors in Projectile Motion, Torque in Rotational Mechanics, and particle movement in Sound Waves.</p>
        </div>
        <div class="card">
            <span class="badge" style="background-color: #8b5cf6;">Class 12th</span>
            <h3>Electrostatics & Optics</h3>
            <p>See invisible magnetic fields, trace light rays through complex lenses, and watch electrons jump energy levels in Modern Physics.</p>
        </div>
    </div>

    <h2 class="section-title" id="demo">Interactive Simulation Preview</h2>
    <div style="padding: 0 5%; max-width: 800px; margin: 0 auto;">
        <div class="card">
            <h3>Module: Kinematics (Projectile Motion)</h3>
            <p style="color: var(--text-muted)">Live preview of trajectory curves based on velocity and launch angle vectors.</p>
            <div class="simulation-box">
                <div class="projectile-demo"></div>
                <span style="color: #475569; font-size: 0.9rem; z-index: 10;">[ Interactive Canvas Animation Area ]</span>
            </div>
        </div>
    </div>

    <h2 class="section-title" id="pricing">Choose Your Learning Plan</h2>
    <div class="grid" style="max-width: 900px; margin: 0 auto;">
        <div class="card">
            <h3>Free Plan</h3>
            <div class="price">$0</div>
            <p>Access to basic text notes and 3 entry-level animations per chapter.</p>
            <button class="cta-btn" style="background: #334155; width: 100%;">Get Started</button>
        </div>
        <div class="card pricing-card">
            <h3>Pro Pass (All-Access)</h3>
            <div class="price">$9<span style="font-size: 1rem; color: var(--text-muted)">/month</span></div>
            <p>Unlock all 100+ interactive 3D simulations, formula cheat sheets, and exam review guides.</p>
            <button class="cta-btn" style="width: 100%;">Go Pro Now</button>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 PhyVisuals. Making Physics crystal clear.</p>
    </footer>

</body>
</html>
