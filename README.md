<!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>suraksha shield: your guide to cyber safety</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=poppins:wght@400;600;700&display=swap');

        :root {
            --primary-color: #004b9e; /* professional blue */
            --secondary-color: #f0f4f8; /* light grey */
            --text-color: #2c3e50; /* dark charcoal */
            --accent-color: #ffc107; /* vibrant gold */
            --danger-color: #e74c3c; /* red for alerts */
            --success-color: #2ecc71; /* green for success/helpline */
            --font-family: 'poppins', sans-serif;
            --shadow-light: 0 4px 15px rgba(0, 0, 0, 0.1);
            --shadow-medium: 0 8px 25px rgba(0, 0, 0, 0.2);
        }

        body {
            font-family: var(--font-family);
            color: var(--text-color);
            background-color: var(--secondary-color);
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        header {
            background-color: #fff;
            padding: 1rem 0;
            box-shadow: var(--shadow-light);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
            display: flex;
            align-items: center;
        }

        .logo-icon {
            font-size: 2.5rem;
            margin-right: 10px;
        }

        .logo img { /* new style for the new logo */
            height: 50px; /* Adjust size as needed */
            margin-right: 10px;
        }

        nav ul {
            list-style: none;
            display: flex;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--primary-color);
            font-weight: 600;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: var(--accent-color);
        }

        .hero {
            background: linear-gradient(rgba(0, 75, 158, 0.8), rgba(0, 45, 90, 0.8)), url('https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-4.0.3&ixid=m3wxmja3fdb8mhxwag90by1wywdlfhx8fgvufdb8fhx8fa%3d%3d&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            color: #fff;
            padding: 6rem 2rem;
            text-align: center;
            border-bottom-left-radius: 50px;
            border-bottom-right-radius: 50px;
        }

        .hero h1 {
            font-size: clamp(2rem, 5vw, 3.5rem);
            margin-bottom: 1rem;
            font-weight: 700;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
        }

        .hero p {
            font-size: clamp(1rem, 2vw, 1.25rem);
            max-width: 800px;
            margin: 0 auto 2rem auto;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--text-color);
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }

        .about-section, .features, .demographics, .resources, .image-showcase, .gallery-section {
            padding: 4rem 0;
            text-align: center;
        }

        .about-section {
            background-color: #fff;
        }

        .features h2, .demographics h2, .resources h2, .about-section h2, .image-showcase h2, .gallery-section h2 {
            font-size: clamp(2rem, 4vw, 2.8rem);
            color: var(--primary-color);
            margin-bottom: 3rem;
            position: relative;
        }

        .features h2::after, .demographics h2::after, .resources h2::after, .about-section h2::after, .image-showcase h2::after, .gallery-section h2::after {
            content: '';
            width: 100px;
            height: 5px;
            background-color: var(--accent-color);
            display: block;
            margin: 15px auto 0;
            border-radius: 5px;
        }

        .about-section p {
            max-width: 900px;
            margin: 0 auto;
            font-size: 1.1rem;
            line-height: 1.8;
            text-align: left;
        }

        .feature-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            justify-content: center;
        }

        .card {
            background-color: #fff;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: var(--shadow-light);
            text-align: left;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
        }

        .card:hover {
            transform: translateY(-10px) rotate(1deg);
            box-shadow: var(--shadow-medium);
        }

        .card-icon {
            font-size: 3.5rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
        }

        .card h3 {
            font-size: 1.8rem;
            color: var(--text-color);
            margin-bottom: 0.5rem;
        }

        .demographics {
            padding: 4rem 0;
            background-color: #fff;
            text-align: center;
        }

        .demographic-sections {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
        }

        .demographic-section {
            background-color: var(--secondary-color);
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }

        .demographic-section:hover {
            transform: scale(1.02);
        }

        .demographic-section h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .demographic-section ul {
            list-style-type: '👉 ';
            padding-left: 1.5rem;
            text-align: left;
        }

        .demographic-section ul li {
            margin-bottom: 0.75rem;
        }

        .resources {
            padding: 4rem 0;
            text-align: center;
        }

        .resources .button-group {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .resources .cta-button {
            background-color: var(--danger-color);
            color: #fff;
        }

        .resources .cta-button.helpline {
            background-color: var(--success-color);
        }

        .image-showcase .image-container {
            max-width: 500px;
            margin: 0 auto;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow-medium);
        }

        .image-showcase img {
            display: block;
            width: 100%;
            height: auto;
        }

        .gallery-section .upload-form {
            background-color: #fff;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow-light);
            max-width: 500px;
            margin: 2rem auto;
        }

        .gallery-section .upload-form label {
            display: block;
            margin-bottom: 1rem;
            font-weight: 600;
            color: var(--text-color);
        }

        .gallery-section .upload-form input {
            display: block;
            width: 100%;
            padding: 0.75rem;
            margin-bottom: 1.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }

        .gallery-section .upload-form button {
            background-color: var(--primary-color);
            color: #fff;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s ease;
        }

        .gallery-section .upload-form button:hover {
            background-color: #003370;
        }

        .gallery-section .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 2rem;
        }

        .gallery-section .gallery img,
        .gallery-section .gallery video {
            width: 100%;
            height: auto;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            .navbar {
                flex-direction: column;
            }
            .logo {
                margin-bottom: 1rem;
            }
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            nav ul li {
                margin: 0.5rem 1rem;
            }
            .hero {
                padding: 4rem 1rem;
            }
            .resources .button-group {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container navbar">
            <a href="#" class="logo">
                <img src="logosu.png" >Suraksha Shield 
            </a>
            <nav>
                <ul>
                    <li><a href="#about">about</a></li>
                    <li><a href="#features">features</a></li>
                    <li><a href="#demographics">for you</a></li>
                    <li><a href="#resources">resources</a></li>
                    <li><a href="#image-showcase">image</a></li>
                    <li><a href="#gallery">gallery</a></li>
                    <li><a href="#contact">contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero" id="home">
            <div class="container">
                <h1>secure your digital life. stay one step ahead of scams.</h1>
                <p>from phishing to upi fraud, cyber threats are on the rise. suraksha shield is your personal shield, providing simple, trustworthy guidance to protect yourself and your loved ones.</p>
                <a href="#features" class="cta-button">start your safety journey now</a>
            </div>
        </section>

        <section class="about-section" id="about">
            <div class="container">
                <h2>our mission</h2>
                <p>
                    suraksha shield is more than just a website; it's a nationwide movement to build a safer digital environment for all. our mission is to demystify cyber security and make it accessible to everyone, regardless of their background or technical expertise. we believe that with the right knowledge, every citizen can become their own first line of defense against online threats. from preventing phishing scams to safeguarding personal data, we provide actionable, easy-to-understand advice. our platform is built on the principles of **trust, simplicity, and adaptability to serve diverse needs. we are committed to empowering students, homemakers, professionals, and senior citizens with tailored information. by staying vigilant and informed, you can protect your finances, privacy, and peace of mind. suraksha shield provides a reliable source of information, free from jargon and complex technicalities. we are constantly updating our resources to address the latest cyber threats and fraud techniques. join us in our journey to **create a digitally secure india, one user at a time.
                </p>
            </div>
        </section>

        <section class="features" id="features">
            <div class="container">
                <h2>why suraksha shield?</h2>
                <div class="feature-cards">
                    <div class="card">
                        <div class="card-icon">🧠</div>
                        <h3>smart education</h3>
                        <p>learn to spot scams with interactive quizzes, real-life examples, and simple, visual guides. understand how cybercriminals operate.</p>
                    </div>
                    <div class="card">
                        <div class="card-icon">🛠</div>
                        <h3>practical tools</h3>
                        <p>get instant access to a scam identifier, secure password generator, and a 'what to do if...' checklist for emergencies.</p>
                    </div>
                    <div class="card">
                        <div class="card-icon">👥</div>
                        <h3>customized for you</h3>
                        <p>whether you're a student, senior citizen, or professional, our content adapts to the threats you face, making it relevant and relatable.</p>
                    </div>
                    <div class="card">
                        <div class="card-icon">🌐</div>
                        <h3>multilingual content</h3>
                        <p>information is available in multiple regional languages to ensure no one is left behind in the fight against cyber fraud.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="demographics" id="demographics">
            <div class="container">
                <h2>cyber safety guides for every indian</h2>
                <div class="demographic-sections">
                    <div class="demographic-section">
                        <h3>students 🎓</h3>
                        <ul>
                            <li>protecting your social media profiles</li>
                            <li>avoiding online gaming and academic scams</li>
                            <li>recognizing fake job offers and internship fraud</li>
                        </ul>
                    </div>
                    <div class="demographic-section">
                        <h3>professionals 👔</h3>
                        <ul>
                            <li>securing your work-from-home setup</li>
                            <li>recognizing business email compromise (bec)</li>
                            <li>safeguarding professional and financial data</li>
                        </ul>
                    </div>
                    <div class="demographic-section">
                        <h3>homemakers & rural users 🏡</h3>
                        <ul>
                            <li>spotting fake offers and lottery scams</li>
                            <li>identifying fraudulent calls and sms</li>
                            <li>safe use of digital wallets and online shopping</li>
                        </ul>
                    </div>
                    <div class="demographic-section">
                        <h3>senior citizens 👵👴</h3>
                        <ul>
                            <li>recognizing calls from fake 'relatives' or 'officials'</li>
                            <li>protecting personal details from identity theft</li>
                            <li>safe management of pension and banking information</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section class="resources" id="resources">
            <div class="container">
                <h2>quick resources & help 🆘</h2>
                <p style="font-size: 1.1rem; max-width: 800px; margin: 1rem auto;">in case you have been a victim of cyber fraud, here are the immediate steps you must take. remember, acting fast is crucial.</p>
                <div class="button-group">
                    <a href="https://cybercrime.gov.in/" target="_blank" class="cta-button">
                        report a cyber crime
                    </a>
                    <a href="tel:1930" class="cta-button helpline">
                        call the national helpline (1930)
                    </a>
                </div>
            </div>
        </section>

        <section class="image-showcase" id="image-showcase">
            <div class="container">
                <h2>Image Showcase</h2>
                <div class="image-container">
                    <img src="https://th.bing.com/th/id/OIP.2tCUVQZyGNn3ecQDuKa-egHaEK?w=308&h=180&c=7&r=0&o=7&dpr=1.3&pid=1.7&rm=3" alt="Safety Illustration">
                    </div>
            </div>
        </section>

       

                <h3>Our Media</h3>
                <div class="gallery">
                    <img src="https://th.bing.com/th/id/OIP.ynUnCXzmTLQcv9AxdRWZEAHaFj?w=263&h=197&c=7&r=0&o=5&dpr=1.3&pid=1.7" alt="Gallery Image 1">
                    <img src="https://th.bing.com/th/id/OIP.tnQK95LHEc5X59OSFvy-JAHaDm?w=345&h=169&c=7&r=0&o=5&dpr=1.3&pid=1.7" alt="Gallery Image 2">
                    <img src="https://th.bing.com/th/id/OIP.q3MwC93CdLin63_ncZ3oMAHaKe?w=129&h=183&c=7&r=0&o=7&dpr=1.3&pid=1.7&rm=3" alt="Gallery Image 3">
                 <video controls width="150" height="100" poster="https://via.placeholder.com/150/dddddd/333333?Text=Video">
                        <source src="VID-20250823-WA0009.mp4" type="video/mp4">
                        Your browser does not support HTML video.
                    </video>
                    <img src="https://th.bing.com/th/id/OIP.mNc1iNx5dwAorWW-C_F6yAHaFj?w=243&h=182&c=7&r=0&o=5&dpr=1.3&pid=1.7" alt="Gallery Image 4">
                    </div>
            </div>
        </section>

    </main>

    <footer>
        <div class="container">
            <div class="social-links" style="margin-bottom: 1rem;">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
            </div>
            <p>&copy; 2025 suraksha shield. all rights reserved. | an initiative for a safer digital india.</p>
        </div>
    </footer>

    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <script src="new.js"></script>

</body>
</html>
<footer>
        <div class="container">
            <div class="social-links" style="margin-bottom: 1rem;">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
            </div>
            <p>&copy; 2025 suraksha shield. all rights reserved. | an initiative for a safer digital india.</p>
        </div>
    </footer>

    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <script src="new.js"></script>
    <section class="features" id="features">
    <div class="container">
        <h2>why suraksha shield?</h2>
        <div class="feature-cards">
            <div class="card">
                <div class="card-icon">🧠</div>
                <h3>smart education</h3>
                <p>learn to spot scams with interactive quizzes, real-life examples, and simple, visual guides. understand how cybercriminals operate.
