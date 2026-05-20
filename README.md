<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LibraryLand — Curated Digital Archives</title>
    
    <!-- Premium Typography: EB Garamond for Literary Headers, Inter for Clean UI -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400..700;1,400..700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">

    <style>
        /* --- Design System & CSS Variables --- */
        :root {
            --bg-color: #121413;       /* Deep, ink-black archive tone */
            --panel-bg: #1a1d1b;       /* Slightly lighter charcoal for cards */
            --text-primary: #e8e6e3;   /* Soft parchment white */
            --text-muted: #a3a09a;     /* Aged paper gray */
            --accent: #c5a880;         /* Muted archival gold */
            --accent-hover: #b3946b;   /* Deep gold for interactions */
            --border: #2a2e2b;         /* Subtle structural dividing lines */
            --font-serif: 'EB Garamond', serif;
            --font-sans: 'Inter', sans-serif;
            --max-width: 1100px;
        }

        /* --- Global Resets & Base Styles --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            font-family: var(--font-sans);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            padding: 0 1.5rem;
        }

        .container {
            max-width: var(--max-width);
            margin: 0 auto;
        }

        /* --- Header / Navigation --- */
        header {
            border-bottom: 1px solid var(--border);
            padding: 2rem 0;
            margin-bottom: 4rem;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: var(--font-serif);
            font-size: 1.75rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            color: var(--text-primary);
            text-decoration: none;
        }

        .logo span {
            color: var(--accent);
        }

        .tagline-badge {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.15em;
            color: var(--accent);
            border: 1px solid var(--accent);
            padding: 0.35rem 0.75rem;
            border-radius: 2px;
        }

        /* --- Hero Section --- */
        .hero {
            text-align: center;
            max-width: 800px;
            margin: 0 auto 6rem auto;
            padding: 2rem 0;
        }

        .hero h1 {
            font-family: var(--font-serif);
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: 400;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            letter-spacing: -0.01em;
        }

        .hero h1 em {
            font-family: var(--font-serif);
            color: var(--accent);
        }

        .hero p {
            font-size: clamp(1.1rem, 2vw, 1.35rem);
            color: var(--text-muted);
            margin-bottom: 2.5rem;
            font-weight: 300;
        }

        /* --- Interactive Form/CTA Elements --- */
        .cta-form {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
            max-width: 500px;
            margin: 0 auto;
            width: 100%;
        }

        @media (min-width: 600px) {
            .cta-form {
                flex-direction: row;
                background: var(--panel-bg);
                padding: 0.35rem;
                border: 1px solid var(--border);
                border-radius: 4px;
            }
            .cta-form input[type="email"] {
                background: transparent;
                border: none;
            }
        }

        input[type="email"] {
            flex: 1;
            padding: 1rem;
            background: var(--panel-bg);
            border: 1px solid var(--border);
            border-radius: 4px;
            color: var(--text-primary);
            font-family: var(--font-sans);
            font-size: 1rem;
            outline: none;
            transition: border-color 0.2s ease;
        }

        input[type="email"]:focus {
            border-color: var(--accent);
        }

        button[type="submit"] {
            background-color: var(--accent);
            color: #121413;
            border: none;
            padding: 1rem 2rem;
            font-family: var(--font-sans);
            font-size: 0.95rem;
            font-weight: 600;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.2s ease;
            white-space: nowrap;
        }

        button[type="submit"]:hover {
            background-color: var(--accent-hover);
        }

        /* --- Main Features / Value Proposition Grid --- */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 6rem;
            border-top: 1px solid var(--border);
            padding-top: 4rem;
        }

        .feature-card {
            background-color: var(--panel-bg);
            border: 1px solid var(--border);
            padding: 2.5rem;
            border-radius: 4px;
            transition: transform 0.2s ease, border-color 0.2s ease;
        }

        .feature-card:hover {
            border-color: rgba(197, 168, 128, 0.3);
        }

        .feature-card .number {
            font-family: var(--font-serif);
            font-size: 1.25rem;
            color: var(--accent);
            margin-bottom: 1rem;
            display: block;
        }

        .feature-card h3 {
            font-family: var(--font-serif);
            font-size: 1.5rem;
            font-weight: 500;
            margin-bottom: 0.75rem;
        }

        .feature-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            font-weight: 300;
        }

        /* --- Detailed Narrative/Concept Section --- */
        .manifesto {
            background: linear-gradient(180deg, var(--bg-color) 0%, var(--panel-bg) 100%);
            border: 1px solid var(--border);
            padding: 4rem 2rem;
            text-align: center;
            border-radius: 4px;
            margin-bottom: 6rem;
        }

        .manifesto-inner {
            max-width: 700px;
            margin: 0 auto;
        }

        .manifesto h2 {
            font-family: var(--font-serif);
            font-size: 2rem;
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .manifesto p {
            color: var(--text-muted);
            font-size: 1.1rem;
            font-style: italic;
            font-family: var(--font-serif);
            line-height: 1.8;
        }

        /* --- Footer --- */
        footer {
            border-top: 1px solid var(--border);
            padding: 3rem 0;
            text-align: center;
            font-size: 0.85rem;
            color: var(--text-muted);
            letter-spacing: 0.05em;
        }
    </style>
</head>
<body>

    <header class="container">
        <div class="nav-container">
            <a href="#" class="logo">Library<span>Land</span>.tv</a>
            <div class="tagline-badge">Archival Discovery</div>
        </div>
    </header>

    <main class="container">
        <!-- Hero Section: Direct Statement & Core Intent -->
        <section class="hero">
            <h1>Escape the algorithm. <br>Discover <em>curated</em> digital literature.</h1>
            <p>LibraryLand is a single, beautiful space dedicated to accessing highly organized, high-utility digital books and rare archival collections. No noise. Just reading.</p>
            
            <!-- Local submission fallback handling via standard HTML5 -->
            <form class="cta-form" action="#" method="POST" onsubmit="alert('Thank you for your interest! Your email has been saved to the waitlist loop.'); return false;">
                <input type="email" placeholder="Enter your email address" required aria-label="Email Address">
                <button type="submit">Join the Waitlist</button>
            </form>
        </section>

        <!-- Product Value Pillars -->
        <section class="features-grid">
            <div class="feature-card">
                <span class="number">01 / Focus</span>
                <h3>Curated Masterpieces</h3>
                <p>We skip the massive, unorganized text dumps. Every book in LibraryLand is verified for formatting, editorial value, and immediate readability.</p>
            </div>
            <div class="feature-card">
                <span class="number">02 / Utility</span>
                <h3>The Museumcore Aesthetic</h3>
                <p>A minimalist interface modeled after timeless physical archives. Built to let you study, read, and retain information without UI clutter.</p>
            </div>
            <div class="feature-card">
                <span class="number">03 / Intent</span>
                <h3>Smart Recommendations</h3>
                <p>Human-centered collection indexing designed to guide you toward your next profound read based on philosophical and literary depth, not clicks.</p>
            </div>
        </section>

        <!-- Manifesto / Concept Validation Layer -->
        <section class="manifesto">
            <div class="manifesto-inner">
                <h2>The LibraryLand Philosophy</h2>
                <p>"Modern platforms treat books like infinite content streams to endlessly scroll past. We believe a digital book asset should feel like an artifact—permanent, clear, and valuable."</p>
            </div>
        </section>
    </main>

    <footer class="container">
        <p>&copy; 2026 LibraryLand. All rights reserved. Designed for true readers.</p>
    </footer>

</body>
</html>
