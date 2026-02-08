<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hershey Annelio - Content Editor & Writer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Newsreader:wght@300;400;500;600&family=DM+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --off-white: #F5F5F5;
            --pure-white: #FFFFFF;
            --charcoal: #1A1A1A;
            --dark-gray: #2D2D2D;
            --medium-gray: #6B6B6B;
            --light-gray: #D4D4D4;
            --accent-gray: #4A4A4A;
        }

```
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        font-family: 'DM Sans', sans-serif;
        background-color: var(--off-white);
        color: var(--charcoal);
        line-height: 1.6;
        overflow-x: hidden;
    }

    html {
        scroll-behavior: smooth;
    }

    /* Navigation */
    nav {
        position: fixed;
        top: 0;
        width: 100%;
        background: rgba(255, 255, 255, 0.98);
        backdrop-filter: blur(10px);
        z-index: 1000;
        border-bottom: 1px solid var(--light-gray);
        padding: 1.2rem 0;
        animation: slideDown 0.6s ease-out;
    }

    @keyframes slideDown {
        from {
            transform: translateY(-100%);
            opacity: 0;
        }
        to {
            transform: translateY(0);
            opacity: 1;
        }
    }

    nav .container {
        max-width: 1100px;
        margin: 0 auto;
        padding: 0 2rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        font-family: 'Newsreader', serif;
        font-size: 1.3rem;
        font-weight: 500;
        color: var(--charcoal);
        text-decoration: none;
        letter-spacing: -0.3px;
    }

    .nav-links {
        display: flex;
        gap: 2.5rem;
        list-style: none;
    }

    .nav-links a {
        color: var(--medium-gray);
        text-decoration: none;
        font-weight: 500;
        font-size: 0.9rem;
        position: relative;
        transition: color 0.3s ease;
        letter-spacing: 0.3px;
    }

    .nav-links a::after {
        content: '';
        position: absolute;
        bottom: -5px;
        left: 0;
        width: 0;
        height: 1px;
        background: var(--charcoal);
        transition: width 0.3s ease;
    }

    .nav-links a:hover {
        color: var(--charcoal);
    }

    .nav-links a:hover::after {
        width: 100%;
    }

    /* Hero Section */
    .hero {
        min-height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 8rem 2rem 4rem;
        position: relative;
        background: linear-gradient(135deg, #FAFAFA 0%, #F0F0F0 100%);
    }

    .hero-content {
        max-width: 700px;
        text-align: center;
        animation: fadeInUp 0.8s ease-out 0.2s both;
    }

    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .hero-name {
        font-family: 'Newsreader', serif;
        font-size: 5rem;
        font-weight: 400;
        line-height: 1;
        margin-bottom: 2rem;
        color: var(--charcoal);
        letter-spacing: -2px;
        animation: fadeInUp 0.8s ease-out 0.3s both;
    }

    .hero-tagline {
        font-size: 1.1rem;
        color: var(--medium-gray);
        margin-bottom: 4rem;
        font-weight: 400;
        letter-spacing: 0.5px;
        animation: fadeInUp 0.8s ease-out 0.4s both;
    }

    .hero-buttons {
        display: flex;
        gap: 1.5rem;
        justify-content: center;
        flex-wrap: wrap;
        animation: fadeInUp 0.8s ease-out 0.5s both;
    }

    .btn {
        padding: 1.1rem 3rem;
        font-size: 0.95rem;
        font-weight: 600;
        text-decoration: none;
        transition: all 0.3s ease;
        cursor: pointer;
        display: inline-block;
        font-family: 'DM Sans', sans-serif;
        letter-spacing: 0.5px;
        border: none;
    }

    .btn-primary {
        background: var(--charcoal);
        color: var(--pure-white);
    }

    .btn-primary:hover {
        background: var(--dark-gray);
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
    }

    .btn-secondary {
        background: transparent;
        color: var(--charcoal);
        border: 2px solid var(--charcoal);
    }

    .btn-secondary:hover {
        background: var(--charcoal);
        color: var(--pure-white);
        transform: translateY(-2px);
    }

    /* Section Base Styles */
    section {
        padding: 6rem 2rem;
        max-width: 1100px;
        margin: 0 auto;
    }

    .section-header {
        text-align: center;
        margin-bottom: 4rem;
        animation: fadeInUp 0.8s ease-out both;
    }

    .section-title {
        font-family: 'Newsreader', serif;
        font-size: 3rem;
        font-weight: 400;
        color: var(--charcoal);
        margin-bottom: 1rem;
        letter-spacing: -1px;
    }

    .section-subtitle {
        font-size: 1.1rem;
        color: var(--medium-gray);
        max-width: 600px;
        margin: 0 auto;
        line-height: 1.7;
    }

    /* About Section */
    #about {
        background: var(--pure-white);
        border-top: 1px solid var(--light-gray);
        border-bottom: 1px solid var(--light-gray);
    }

    .about-content {
        max-width: 750px;
        margin: 0 auto;
    }

    .about-intro {
        font-size: 1.3rem;
        font-weight: 500;
        color: var(--charcoal);
        margin-bottom: 2rem;
        line-height: 1.6;
        animation: fadeInUp 0.8s ease-out 0.2s both;
    }

    .about-text {
        font-size: 1.05rem;
        color: var(--medium-gray);
        line-height: 1.8;
        margin-bottom: 1.5rem;
        animation: fadeInUp 0.8s ease-out 0.3s both;
    }

    .about-cta {
        font-size: 1.05rem;
        color: var(--charcoal);
        font-weight: 500;
        margin-top: 2.5rem;
        animation: fadeInUp 0.8s ease-out 0.4s both;
    }

    /* Portfolio Section */
    .portfolio-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        gap: 3rem;
        margin-top: 3rem;
    }

    .portfolio-item {
        background: var(--pure-white);
        border: 1px solid var(--light-gray);
        overflow: hidden;
        transition: all 0.3s ease;
        cursor: pointer;
        animation: fadeInUp 0.6s ease-out both;
    }

    .portfolio-item:nth-child(1) { animation-delay: 0.1s; }
    .portfolio-item:nth-child(2) { animation-delay: 0.2s; }
    .portfolio-item:nth-child(3) { animation-delay: 0.3s; }
    .portfolio-item:nth-child(4) { animation-delay: 0.4s; }
    .portfolio-item:nth-child(5) { animation-delay: 0.5s; }
    .portfolio-item:nth-child(6) { animation-delay: 0.6s; }

    .portfolio-item:hover {
        transform: translateY(-5px);
        box-shadow: 0 12px 30px rgba(0, 0, 0, 0.08);
        border-color: var(--medium-gray);
    }

    .portfolio-image {
        width: 100%;
        height: 200px;
        background: linear-gradient(135deg, #E8E8E8 0%, #D4D4D4 100%);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 3rem;
        color: var(--medium-gray);
        transition: all 0.3s ease;
    }

    .portfolio-item:hover .portfolio-image {
        background: linear-gradient(135deg, #D4D4D4 0%, #C0C0C0 100%);
    }

    .portfolio-content {
        padding: 2rem;
    }

    .portfolio-date {
        font-size: 0.85rem;
        color: var(--medium-gray);
        margin-bottom: 0.8rem;
        letter-spacing: 0.5px;
    }

    .portfolio-title {
        font-family: 'Newsreader', serif;
        font-size: 1.4rem;
        font-weight: 500;
        color: var(--charcoal);
        margin-bottom: 0.8rem;
        line-height: 1.3;
        letter-spacing: -0.3px;
    }

    .portfolio-excerpt {
        font-size: 0.95rem;
        color: var(--medium-gray);
        line-height: 1.6;
    }

    /* Contact Section */
    #contact {
        background: var(--charcoal);
        color: var(--pure-white);
        text-align: center;
        padding: 5rem 2rem;
    }

    #contact .section-title {
        color: var(--pure-white);
    }

    #contact .section-subtitle {
        color: var(--light-gray);
    }

    .contact-btn {
        margin-top: 2rem;
        background: var(--pure-white);
        color: var(--charcoal);
        padding: 1.1rem 3rem;
        font-size: 0.95rem;
        font-weight: 600;
        text-decoration: none;
        display: inline-block;
        transition: all 0.3s ease;
        letter-spacing: 0.5px;
    }

    .contact-btn:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(255, 255, 255, 0.2);
    }

    /* Footer */
    footer {
        background: var(--dark-gray);
        color: var(--light-gray);
        text-align: center;
        padding: 2.5rem 2rem;
        font-size: 0.9rem;
    }

    footer a {
        color: var(--pure-white);
        text-decoration: none;
        transition: opacity 0.3s ease;
    }

    footer a:hover {
        opacity: 0.7;
    }

    /* Scroll Reveal Animation */
    .reveal {
        opacity: 0;
        transform: translateY(30px);
    }

    .reveal.active {
        opacity: 1;
        transform: translateY(0);
        transition: all 0.8s ease-out;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .hero-name {
            font-size: 3.5rem;
        }

        .section-title {
            font-size: 2.2rem;
        }

        .nav-links {
            gap: 1.5rem;
        }

        .nav-links a {
            font-size: 0.85rem;
        }

        .hero-buttons {
            flex-direction: column;
            align-items: center;
        }

        .btn {
            width: 100%;
            max-width: 300px;
        }

        .portfolio-grid {
            grid-template-columns: 1fr;
            gap: 2rem;
        }
    }

    @media (max-width: 480px) {
        .hero-name {
            font-size: 2.5rem;
        }

        .logo {
            font-size: 1.1rem;
        }

        nav .container {
            padding: 0 1.2rem;
        }

        section {
            padding: 4rem 1.2rem;
        }
    }
</style>
```

</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <a href="#" class="logo">Hershey Annelio</a>
            <ul class="nav-links">
                <li><a href="#works">My Work</a></li>
                <li><a href="#about">About Me</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

```
<!-- Hero Section -->
<section class="hero" id="home">
    <div class="hero-content">
        <h1 class="hero-name">Hershey Annelio</h1>
        <p class="hero-tagline">Content Editor & Writer</p>
        <div class="hero-buttons">
            <a href="#works" class="btn btn-primary">My Work</a>
            <a href="#about" class="btn btn-secondary">About Me</a>
        </div>
    </div>
</section>

<!-- Portfolio Section -->
<section id="works">
    <div class="section-header reveal">
        <h2 class="section-title">My Work</h2>
        <p class="section-subtitle">A collection of writing that explores everyday moments, creative insights, and things worth noticing.</p>
    </div>

    <div class="portfolio-grid">
        <div class="portfolio-item reveal">
            <div class="portfolio-image">🌅</div>
            <div class="portfolio-content">
                <p class="portfolio-date">Recent</p>
                <h3 class="portfolio-title">Why Sunsets Over the Ocean Calm Me Down</h3>
                <p class="portfolio-excerpt">A reflection on the simple power of natural beauty and why some moments just make us stop and breathe.</p>
            </div>
        </div>

        <div class="portfolio-item reveal">
            <div class="portfolio-image">🎨</div>
            <div class="portfolio-content">
                <p class="portfolio-date">Featured</p>
                <h3 class="portfolio-title">The Arts in Baguio City: Why I Can't Walk Past a Mural Without Stopping</h3>
                <p class="portfolio-excerpt">Exploring the vibrant street art scene and what it says about creativity in everyday spaces.</p>
            </div>
        </div>

        <div class="portfolio-item reveal">
            <div class="portfolio-image">⚠️</div>
            <div class="portfolio-content">
                <p class="portfolio-date">Analysis</p>
                <h3 class="portfolio-title">Scams Aren't Obvious Anymore, and That's the Problem</h3>
                <p class="portfolio-excerpt">A deep dive into how modern scams have evolved and what makes them so convincing today.</p>
            </div>
        </div>

        <div class="portfolio-item reveal">
            <div class="portfolio-image">📸</div>
            <div class="portfolio-content">
                <p class="portfolio-date">09 May, 2026</p>
                <h3 class="portfolio-title">The Art of Noticing Through Your Camera</h3>
                <p class="portfolio-excerpt">How photography changes the way we see the world around us, one frame at a time.</p>
            </div>
        </div>

        <div class="portfolio-item reveal">
            <div class="portfolio-image">🛡️</div>
            <div class="portfolio-content">
                <p class="portfolio-date">Consumer Insight</p>
                <h3 class="portfolio-title">Product Recalls & Consumer Safety: What Actually Matters (and What We Tend to Miss)</h3>
                <p class="portfolio-excerpt">Breaking down the important details about product safety that often get lost in the headlines.</p>
            </div>
        </div>

        <div class="portfolio-item reveal">
            <div class="portfolio-image">✍️</div>
            <div class="portfolio-content">
                <p class="portfolio-date">Coming Soon</p>
                <h3 class="portfolio-title">More Stories in Progress</h3>
                <p class="portfolio-excerpt">Currently working on new pieces about everyday observations, cultural moments, and things that make us think.</p>
            </div>
        </div>
    </div>
</section>

<!-- About Section -->
<section id="about">
    <div class="section-header reveal">
        <h2 class="section-title">About Hershey</h2>
    </div>

    <div class="about-content">
        <p class="about-intro reveal">Hi, I'm Hershey! I'm a writer with a background in customer service and inside sales.</p>
        
        <p class="about-text reveal">I help shape content that feels clear, natural, and easy to trust—so people stay engaged instead of tuning out.</p>
        
        <p class="about-text reveal">I understand the reader's point of view because I'm often the reader myself. I care about straightforward messages, real connection, and content that respects people's time. That's how I approach editing—cutting the noise, fixing the awkward parts, and keeping the voice warm and real.</p>
        
        <p class="about-cta reveal">If this matches what you're looking for, send me a message. I'd love to learn more about what you're working on.</p>
    </div>
</section>

<!-- Contact Section -->
<section id="contact">
    <div class="section-header">
        <h2 class="section-title">Let's Work Together</h2>
        <p class="section-subtitle">Have a project in mind? I'd love to hear about it.</p>
    </div>
    <a href="mailto:your.email@example.com" class="contact-btn">Get in Touch</a>
</section>

<!-- Footer -->
<footer>
    <p>&copy; 2026 Hershey Annelio. All rights reserved.</p>
</footer>

<script>
    // Smooth scroll reveal animation
    const reveals = document.querySelectorAll('.reveal');

    function checkReveal() {
        const windowHeight = window.innerHeight;
        const revealPoint = 100;

        reveals.forEach(reveal => {
            const revealTop = reveal.getBoundingClientRect().top;
            
            if (revealTop < windowHeight - revealPoint) {
                reveal.classList.add('active');
            }
        });
    }

    window.addEventListener('scroll', checkReveal);
    checkReveal(); // Check on load

    // Smooth scroll for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        });
    });
</script>
```

</body>
</html>
