<h1 class="jitsuzon-title">JITSUZON</h1>
<div class="site-branding">
    <h1 class="jitsuzon-title">JITSUZON</h1>
    <div class="jitsuzon-subtitle">Nexus of Fractured Realities</div>
    <p class="jitsuzon-description">
        A responsive author platform for <em>Covenant in Pandemonium</em>, where psychological thrillers 
        bleed into reality. Explore fragmented narratives, hidden omens, and the mind of 
        Adinath Prakashan – where engineering logic collides with apocalyptic storytelling.
    </p>
</div>

<style>
    /* Add these styles to your existing CSS */
    .site-branding {
        text-align: center;
        padding: 4rem 2rem 0;
        max-width: 1200px;
        margin: 0 auto;
    }

    .jitsuzon-title {
        font-family: 'Orbitron', sans-serif;
        font-size: 4.5rem;
        font-weight: 700;
        background: linear-gradient(45deg, var(--neon-pink), var(--blood-pink));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        text-transform: uppercase;
        letter-spacing: 8px;
        margin-bottom: 1rem;
        animation: hologram 3s infinite alternate;
    }

    @keyframes hologram {
        0% { 
            opacity: 0.9;
            text-shadow: 0 0 10px var(--neon-pink);
        }
        100% { 
            opacity: 1;
            text-shadow: 0 0 25px var(--neon-pink),
                       0 0 35px var(--blood-pink);
        }
    }

    .jitsuzon-subtitle {
        font-family: 'Zen Tokyo Zoo', cursive;
        font-size: 2rem;
        color: var(--neon-pink);
        margin-bottom: 2rem;
        text-shadow: 0 0 15px rgba(255, 0, 255, 0.5);
    }

    .jitsuzon-description {
        font-family: 'Oswald', sans-serif;
        font-size: 1.25rem;
        line-height: 1.6;
        color: rgba(255, 255, 255, 0.9);
        max-width: 800px;
        margin: 0 auto;
        padding: 1rem;
        border-top: 2px solid var(--neon-pink);
        border-bottom: 2px solid var(--neon-pink);
        position: relative;
    }

    .jitsuzon-description::before {
        content: "◈";
        position: absolute;
        left: -30px;
        top: -15px;
        color: var(--neon-pink);
        font-size: 1.5rem;
        text-shadow: 0 0 10px var(--neon-pink);
    }

    .jitsuzon-description::after {
        content: "◈";
        position: absolute;
        right: -30px;
        bottom: -15px;
        color: var(--neon-pink);
        font-size: 1.5rem;
        text-shadow: 0 0 10px var(--neon-pink);
    }
</style>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jitsuzon | A Covenant in Pandemonium</title>
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;500&family=Zen+Tokyo+Zoo&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon-pink: #FF00FF;
            --deep-black: #000000;
            --blood-pink: #FF1493;
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
        }

        .side-nav {
            position: fixed;
            right: 2%;
            top: 50%;
            transform: translateY(-50%);
            z-index: 1000;
        }

        .side-nav a {
            display: block;
            writing-mode: vertical-rl;
            transform: rotate(180deg);
            color: white;
            text-decoration: none;
            margin: 1.5rem 0;
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .side-nav a:hover {
            color: var(--neon-pink);
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: radial-gradient(circle, rgba(255,0,255,0.1) 0%, rgba(0,0,0,1) 70%);
            position: relative;
        }

        .title {
            font-family: 'Zen Tokyo Zoo', cursive;
            font-size: 4.5rem;
            text-align: center;
            text-transform: uppercase;
            background: linear-gradient(45deg, var(--neon-pink), var(--blood-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: glitch 2s infinite;
        }

        @keyframes glitch {
            0%, 100% { text-shadow: 0.05em 0 0 rgba(255,0,0,.75), -0.025em -0.05em 0 rgba(0,255,0,.75), 0.025em 0.05em 0 rgba(0,0,255,.75); }
            14%, 49% { text-shadow: -0.05em -0.025em 0 rgba(255,0,0,.75), 0.025em 0.025em 0 rgba(0,255,0,.75), -0.05em -0.05em 0 rgba(0,0,255,.75); }
            50%, 99% { text-shadow: 0.025em 0.05em 0 rgba(255,0,0,.75), 0.05em 0 0 rgba(0,255,0,.75), 0 -0.05em 0 rgba(0,0,255,.75); }
        }

        .update-container {
            padding: 4rem;
            border: 3px solid var(--neon-pink);
            margin: 5rem auto;
            max-width: 800px;
            position: relative;
            background: rgba(0,0,0,0.7);
            clip-path: polygon(0 0, 100% 0, 100% 75%, 95% 75%, 95% 100%, 85% 75%, 0 75%);
        }

        .chat-bubble {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background: var(--neon-pink);
            width: 60px;
            height: 60px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        .cursor {
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        .fancy-button {
            padding: 12px 24px;
            font-size: 18px;
            font-family: 'Oswald', sans-serif;
            color: var(--neon-pink);
            background: transparent;
            border: 2px solid var(--neon-pink);
            border-radius: 8px;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 0 10px var(--neon-pink), 0 0 20px var(--neon-pink), 0 0 40px var(--neon-pink);
            margin-top: 20px;
        }

        .fancy-button:hover {
            color: var(--deep-black);
            background: var(--neon-pink);
            box-shadow: 0 0 20px var(--neon-pink), 0 0 40px var(--neon-pink), 0 0 80px var(--neon-pink);
        }

        #aboutMe {
            display: none;
            margin-top: 20px;
            font-family: Arial, sans-serif;
            line-height: 1.6;
            font-size: 18px;
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid var(--neon-pink);
            border-radius: 8px;
        }
    </style>
</head>
<body>
    <nav class="side-nav">
        <a href="#updates">Manifest</a>
        <a href="#events">Omens</a>
        <a href="https://instagram.com/adinath_prakashan" target="_blank" rel="noopener noreferrer">Contact</a>
    </nav>

    <section class="hero">
        <div>
            <h1 class="title">A Covenant<br>in<br>Pandemonium</h1>
            <div class="type-text" style="text-align: center; margin-top: 2rem; font-size: 1.5rem;">
                <span id="typewriter"></span><span class="cursor">|</span>
            </div>
        </div>
    </section>

    <section class="update-container" id="updates">
        <h2 style="color: var(--neon-pink); margin-bottom: 2rem;">Author's Transmission</h2>
        <p style="font-size: 1.8rem;">Are you ready for a psychological thriller?</p>
        <p style="margin-top: 2rem; opacity: 0.8;">The veil will lift soon...</p>
    </section>

    <section class="update-container" id="events">
        <h2 style="color: var(--neon-pink); margin-bottom: 2rem;">Coming Shadows</h2>
        <p style="font-size: 1.5rem;">The stars whisper of impending revelations...</p>
    </section>

    <div style="text-align: center; margin: 40px 0;">
        <button id="whoAmIButton" class="fancy-button">Who Am I?</button>
    </div>

    <div id="aboutMe">
        <p>I’m <strong>Adinath Prakashan</strong>, a mechanical engineering student with a passion for storytelling. While my academic life revolves around engineering, my mind is constantly building worlds, crafting characters, and exploring the depths of post-apocalyptic fiction.</p>
        <p>My love for movies, anime, and TV series (<em>Friends, The Big Bang Theory, One Piece, The Walking Dead</em>) has shaped the way I think about stories. Now, I’m creating my own.</p>
        <p>One of my favorite storytelling techniques is foreshadowing. I love weaving hidden clues that only make sense later. For example, in <em>Covenant in Pandemonium</em>, the man with four arms and the thousands of rats? They aren’t hallucinations. They are real. But my protagonist, Richard, doesn’t react as most people would. Why? Because his mind can no longer process reality as it should. I don’t just want to tell a thrilling story—I want to create an experience that makes people think.</p>
    </div>

    <div class="chat-bubble" onclick="window.location.href='mailto:adinathprakashan@gmail.com'">
        💬
    </div>

    <script>
        // Typewriter Effect
        const messages = [
            "Where reality fractures...",
            "A mind-bending journey awaits...",
            "The pandemonium approaches..."
        ];
        let messageIndex = 0;
        let charIndex = 0;
        const typewriter = document.getElementById('typewriter');
        
        function typeMessage() {
            if (charIndex < messages[messageIndex].length) {
                typewriter.textContent += messages[messageIndex].charAt(charIndex);
                charIndex++;
                setTimeout(typeMessage, 100);
            } else {
                setTimeout(eraseMessage, 2000);
            }
        }

        function eraseMessage() {
            if (charIndex > 0) {
                typewriter.textContent = messages[messageIndex].substring(0, charIndex - 1);
                charIndex--;
                setTimeout(eraseMessage, 50);
            } else {
                messageIndex = (messageIndex + 1) % messages.length;
                setTimeout(typeMessage, 500);
            }
        }

        typeMessage();

        // Who Am I? Button Functionality
        document.getElementById('whoAmIButton').addEventListener('click', function() {
            const aboutMe = document.getElementById('aboutMe');
            aboutMe.style.display = aboutMe.style.display === 'none' ? 'block' : 'none';
        });

        // Dynamic Background
        document.addEventListener('mousemove', (e) => {
            const x = e.clientX / window.innerWidth;
            const y = e.clientY / window.innerHeight;
            document.body.style.background = `radial-gradient(at ${x * 100}% ${y * 100}%, 
                rgba(255,0,255,0.1) 0%, 
                rgba(0,0,0,1) 70%)`;
        });
    </script>
</body>
</html>
            
