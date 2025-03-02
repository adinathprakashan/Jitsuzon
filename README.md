<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JITSUZON | Covenant in Pandemonium</title>
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;500&family=Zen+Tokyo+Zoo&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon-pink: #FF00FF;
            --deep-black: #000000;
            --blood-pink: #FF1493;
            --cyber-teal: #00fff9;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: var(--deep-black);
            color: white;
            font-family: 'Oswald', sans-serif;
            overflow-x: hidden;
            cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><circle cx="12" cy="12" r="8" fill="none" stroke="%23FF00FF" stroke-width="2"/></svg>') 12 12, auto;
        }

        /* Cyber Matrix Background */
        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
            pointer-events: none;
        }

        /* Neuromorphic Navigation */
        .neuro-nav {
            position: fixed;
            top: 2rem;
            right: 2rem;
            display: flex;
            gap: 1.5rem;
            z-index: 1000;
        }

        .neuro-nav a {
            padding: 1rem;
            border-radius: 15px;
            background: var(--deep-black);
            box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5),
                       -5px -5px 10px rgba(255, 0, 255, 0.1);
            transition: all 0.3s ease;
            text-decoration: none;
            color: var(--neon-pink);
        }

        .neuro-nav a:hover {
            box-shadow: inset 5px 5px 10px rgba(0, 0, 0, 0.5),
                       inset -5px -5px 10px rgba(255, 0, 255, 0.1);
        }

        /* Holographic Title */
        .hologram-title {
            font-family: 'Zen Tokyo Zoo', cursive;
            font-size: 5vw;
            text-align: center;
            text-transform: uppercase;
            position: relative;
            margin: 15vh 0;
            perspective: 1000px;
        }

        .hologram-title span {
            display: inline-block;
            background: linear-gradient(45deg, var(--neon-pink), var(--cyber-teal));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: hologram-float 6s infinite ease-in-out;
        }

        @keyframes hologram-float {
            0%, 100% { transform: translateY(0) rotateX(0deg) rotateY(0deg); }
            25% { transform: translateY(-10px) rotateX(15deg) rotateY(15deg); }
            50% { transform: translateY(0) rotateX(0deg) rotateY(-15deg); }
            75% { transform: translateY(10px) rotateX(-15deg) rotateY(0deg); }
        }

        /* Content Sections */
        .cyber-section {
            max-width: 1200px;
            margin: 10rem auto;
            padding: 2rem;
            border: 2px solid var(--neon-pink);
            position: relative;
            background: rgba(0, 0, 0, 0.9);
            clip-path: polygon(0 0, 100% 0, 100% 90%, 98% 100%, 0 100%);
        }

        .cyber-section::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--neon-pink), var(--cyber-teal));
            z-index: -1;
            animation: border-glow 3s infinite alternate;
        }

        @keyframes border-glow {
            0% { opacity: 0.3; }
            100% { opacity: 0.7; }
        }

        /* Quantum Interface */
        .quantum-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
        }

        .quantum-card {
            padding: 2rem;
            background: rgba(255, 0, 255, 0.05);
            border: 1px solid var(--neon-pink);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .quantum-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 0 30px var(--neon-pink);
        }

        /* Contact Section */
        .contact-section {
            text-align: center;
            margin: 5rem 0;
        }

        .contact-section a {
            display: inline-block;
            margin: 1rem;
            padding: 1rem 2rem;
            border: 2px solid var(--neon-pink);
            color: var(--neon-pink);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .contact-section a:hover {
            background: var(--neon-pink);
            color: var(--deep-black);
            box-shadow: 0 0 20px var(--neon-pink);
        }

        /* Mobile-Friendly Scrolling */
        @media (max-width: 768px) {
            .hologram-title {
                font-size: 10vw;
                margin: 10vh 0;
            }

            .neuro-nav {
                top: 1rem;
                right: 1rem;
                gap: 1rem;
            }

            .neuro-nav a {
                padding: 0.5rem;
                font-size: 0.9rem;
            }

            .cyber-section {
                margin: 5rem auto;
                padding: 1rem;
            }

            .quantum-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <canvas id="neural-canvas"></canvas>
    <div class="time-distortion"></div>
    <div class="matrix-bg"></div>

    <nav class="neuro-nav">
        <a href="#world">The World</a>
        <a href="#king">The Cannibal King</a>
        <a href="#truth">The Truth</a>
    </nav>

    <h1 class="hologram-title">
        <span>Covenant</span>
        <span style="animation-delay: -2s">in</span>
        <span style="animation-delay: -4s">Pandemonium</span>
    </h1>

    <section class="cyber-section" id="world">
        <h2>The World of Pandemonium</h2>
        <div class="quantum-grid">
            <div class="quantum-card">
                <h3>Survival Through Intellect</h3>
                <p>In a world ravaged by Catastrophe, brute strength is no longer enough. The factions that thrive are those that master deception, strategy, and the ever-shifting power dynamics of a broken world.</p>
            </div>
            <div class="quantum-card">
                <h3>Warring Factions</h3>
                <p>From the shadowy Syndicates to the nomadic Free Cities, alliances are fragile, and betrayal is the only constant. Who will outwit whom in this deadly game of survival?</p>
            </div>
        </div>
    </section>

    <section class="cyber-section" id="king">
        <h2>The Cannibal King</h2>
        <div class="quantum-grid">
            <div class="quantum-card">
                <h3>Villain or Visionary?</h3>
                <p>The King of Guanjuato is a figure shrouded in mystery. Is he a ruthless tyrant, or a pragmatic leader willing to do whatever it takes to unite a fractured world?</p>
            </div>
            <div class="quantum-card">
                <h3>Layers of Deception</h3>
                <p>Beneath the propaganda and the tales of his brutality lies a mind as sharp as a blade. What is his true endgame, and who will survive long enough to uncover it?</p>
            </div>
        </div>
    </section>

    <section class="cyber-section" id="truth">
        <h2>The Greatest Revelation</h2>
        <div class="quantum-grid">
            <div class="quantum-card">
                <h3>Understanding the World</h3>
                <p>In the end, the question is not who controls the world, but who truly understands it. And in a world of chaos, is understanding a blessing—or a curse?</p>
            </div>
            <div class="quantum-card">
                <h3>The Price of Knowledge</h3>
                <p>For those who seek the truth, the cost may be more than they can bear. Will the pursuit of understanding lead to salvation—or destruction?</p>
            </div>
        </div>
    </section>

    <section class="contact-section">
        <h2>Connect With Me</h2>
        <a href="https://instagram.com/adinath_prakashan" target="_blank">Instagram</a>
        <a href="mailto:adinathprakashan@gmail.com">Email Me</a>
    </section>

    <script>
        // Neural Network Visualization
        const canvas = document.getElementById('neural-canvas');
        const ctx = canvas.getContext('2d');
        let nodes = [];

        function initNeural() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            
            for(let i = 0; i < 50; i++) {
                nodes.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    radius: Math.random() * 3 + 1,
                    dx: (Math.random() - 0.5) * 0.5,
                    dy: (Math.random() - 0.5) * 0.5
                });
            }

            animate();
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            nodes.forEach(node => {
                // Update positions
                node.x += node.dx;
                node.y += node.dy;
                
                // Draw nodes
                ctx.beginPath();
                ctx.arc(node.x, node.y, node.radius, 0, Math.PI * 2);
                ctx.fillStyle = `rgba(255, 0, 255, ${node.radius/4})`;
                ctx.fill();
                
                // Draw connections
                nodes.forEach(other => {
                    const distance = Math.hypot(node.x - other.x, node.y - other.y);
                    if(distance < 150) {
                        ctx.beginPath();
                        ctx.moveTo(node.x, node.y);
                        ctx.lineTo(other.x, other.y);
                        ctx.strokeStyle = `rgba(255, 0, 255, ${0.3 - distance/500})`;
                        ctx.lineWidth = 0.5;
                        ctx.stroke();
                    }
                });
            });
            
            requestAnimationFrame(animate);
        }

        // Initialize effects
        initNeural();

        // Smooth Scrolling for Mobile
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
            
