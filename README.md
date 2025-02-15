# Jitsuzon
Jitsuzon – A responsive author platform for Covenant in Pandemonium, featuring dynamic typewriter effects, smooth scroll navigation, interactive newsletter subscription, and author updates. Built with HTML, CSS, and JavaScript, designed with a dark, dystopian aesthetic inspired by the novel’s themes.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Novelist | Author Platform</title>
    <style>
        :root {
            --primary-red: #c62b28;
            --dark-bg: #0a0a0a;
            --light-text: #f5f5f5;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Helvetica Neue', sans-serif;
        }

        body {
            background-color: var(--dark-bg);
            color: var(--light-text);
            line-height: 1.6;
        }

        .nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            padding: 1.5rem;
            z-index: 1000;
            border-bottom: 2px solid var(--primary-red);
        }

        .nav a {
            color: var(--light-text);
            text-decoration: none;
            margin: 0 2rem;
            font-size: 1.1rem;
            transition: color 0.3s;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(rgba(10, 10, 10, 0.7), rgba(10, 10, 10, 0.7)),
                        url('your-cover-image.jpg') center/cover;
            text-align: center;
        }

        .hero h1 {
            font-family: 'Times New Roman', serif;
            font-size: 4rem;
            letter-spacing: 0.3rem;
            margin-bottom: 2rem;
            text-transform: uppercase;
            color: var(--primary-red);
        }

        .typewriter {
            border-right: 3px solid var(--primary-red);
            white-space: nowrap;
            overflow: hidden;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }

        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--primary-red) }
        }

        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .newsletter {
            background: rgba(198, 43, 40, 0.1);
            padding: 3rem;
            text-align: center;
            border: 1px solid var(--primary-red);
        }

        .buy-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            margin: 2rem 0;
            transition: transform 0.3s;
            cursor: pointer;
        }

        .buy-card:hover {
            transform: translateY(-5px);
            border: 1px solid var(--primary-red);
        }

    </style>
</head>
<body>
    <nav class="nav">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#buy">Buy</a>
        <a href="#contact">Contact</a>
    </nav>

    <section class="hero" id="home">
        <div>
            <h1>NOVEL TITLE</h1>
            <div class="typewriter">A gripping tale of adventure and destiny</div>
        </div>
    </section>

    <section class="section" id="updates">
        <h2>Author's Updates</h2>
        <div class="update-feed" id="updateContainer"></div>
    </section>

    <section class="section" id="buy">
        <h2>Where to Buy</h2>
        <div class="buy-card">
            <h3>Amazon</h3>
            <p>Available in Paperback & Kindle</p>
            <button class="buy-btn">Purchase Now</button>
        </div>
        <!-- Add more retailers -->
    </section>

    <section class="newsletter">
        <h3>Join My Newsletter</h3>
        <form id="newsletterForm">
            <input type="email" placeholder="Enter your email" required>
            <button type="submit">Subscribe</button>
        </form>
    </section>

    <script>
        // Typewriter Effect
        document.addEventListener('DOMContentLoaded', () => {
            const phrases = ["A gripping tale...", "New chapter releases...", "Available now..."];
            let index = 0;
            const typewriter = document.querySelector('.typewriter');

            setInterval(() => {
                typewriter.style.animation = 'none';
                setTimeout(() => {
                    typewriter.textContent = phrases[index];
                    typewriter.style.animation = 'typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite';
                    index = (index + 1) % phrases.length;
                }, 100);
            }, 4000);
        });

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Newsletter Submission
        document.getElementById('newsletterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thanks for subscribing!');
            this.reset();
        });

        // Dynamic Updates
        const updates = [
            { date: '2023-10-15', content: 'New chapter preview available next week!' },
            { date: '2023-10-10', content: 'Upcoming book signing event announced' }
        ];

        const updateContainer = document.getElementById('updateContainer');
        updates.forEach(update => {
            const div = document.createElement('div');
            div.innerHTML = `<h4>${update.date}</h4><p>${update.content}</p>`;
            updateContainer.appendChild(div);
        });

        // Scroll Progress
        window.addEventListener('scroll', () => {
            const scrollTop = document.documentElement.scrollTop;
            const scrollHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const progress = (scrollTop / scrollHeight) * 100;
            document.documentElement.style.setProperty('--scroll-progress', `${progress}%`);
        });
    </script>
</body>
</html>
