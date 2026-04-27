<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ria Auto House | Quality Cars in Windhoek, Namibia</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: #0a0a0a;
        }

        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            border-bottom: 2px solid #FFD700;
            padding: 1rem 0;
            box-shadow: 0 2px 15px rgba(255, 215, 0, 0.15);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo img {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #FFD700;
            background: #222;
        }

        .logo-text h1 {
            font-size: 1.8rem;
            margin-bottom: 0.2rem;
            color: #FFD700;
        }

        .logo-text p {
            font-size: 0.9rem;
            color: #cccccc;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #ffffff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a:hover {
            color: #FFD700;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #FFD700;
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.85), rgba(10, 10, 10, 0.9)),
                        url('https://images.unsplash.com/photo-1449965408869-eaa3f722e40d?w=1920&h=800&fit=crop') center/cover no-repeat;
            color: white;
            padding: 120px 0;
            text-align: center;
            border-bottom: 3px solid #FFD700;
        }

        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
            color: #FFD700;
            text-shadow: 0 2px 10px rgba(255, 215, 0, 0.3);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
            color: #cccccc;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%);
            color: #0a0a0a;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255, 215, 0, 0.5);
        }

        .cta-button.secondary {
            background: transparent;
            border: 2px solid #FFD700;
            color: #FFD700;
        }

        .cta-button.secondary:hover {
            background: #FFD700;
            color: #0a0a0a;
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background: linear-gradient(180deg, #111111 0%, #0a0a0a 100%);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #FFD700;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, #FFD700, #D4AF37);
            margin: 15px auto 0;
            border-radius: 2px;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-image img {
            width: 100%;
            border-radius: 15px;
            border: 2px solid #FFD700;
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.15);
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #FFD700;
        }

        .about-text p {
            margin-bottom: 1rem;
            font-size: 1.1rem;
            line-height: 1.8;
            color: #cccccc;
        }

        .about-text ul {
            color: #cccccc;
        }

        .about-text ul li {
            margin-bottom: 0.5rem;
        }

        .about-text strong {
            color: #FFD700;
        }

        /* Import Section */
        .import-section {
            padding: 80px 0;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 50%, #0a0a0a 100%);
            color: white;
            border-top: 2px solid #333;
            border-bottom: 2px solid #333;
        }

        .import-section .section-title {
            color: #FFD700;
        }

        .import-section .section-title::after {
            background: linear-gradient(90deg, #FFD700, #D4AF37);
        }

        .import-section p {
            color: #cccccc;
        }

        .import-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-top: 40px;
        }

        .import-card {
            background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%);
            padding: 40px 30px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid #333;
            transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
        }

        .import-card:hover {
            transform: translateY(-10px);
            border-color: #FFD700;
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.15);
        }

        .import-card i {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: #FFD700;
        }

        .import-card h4 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #FFD700;
        }

        .import-card p {
            opacity: 0.95;
            line-height: 1.7;
        }

        .countries {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 50px;
            flex-wrap: wrap;
        }

        .country-badge {
            background: linear-gradient(135deg, #222222 0%, #1a1a1a 100%);
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            border: 1px solid #444;
            color: #FFD700;
            transition: border-color 0.3s, box-shadow 0.3s;
        }

        .country-badge:hover {
            border-color: #FFD700;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.2);
        }

        /* Services Section */
        .services {
            padding: 80px 0;
            background: linear-gradient(180deg, #0a0a0a 0%, #111111 100%);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .service-card {
            background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%);
            padding: 35px 25px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid #333;
            transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: #FFD700;
            box-shadow: 0 10px 25px rgba(255, 215, 0, 0.1);
        }

        .service-card i {
            font-size: 3rem;
            color: #FFD700;
            margin-bottom: 15px;
        }

        .service-card h4 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #FFD700;
        }

        .service-card p {
            color: #cccccc;
        }

        /* Contact Section */
        .contact {
            padding: 80px 0;
            background: linear-gradient(135deg, #0a0a0a 0%, #111111 100%);
            color: white;
            border-top: 3px solid #FFD700;
        }

        .contact .section-title {
            color: #FFD700;
        }

        .contact .section-title::after {
            background: linear-gradient(90deg, #FFD700, #D4AF37);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info {
            background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid #333;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 30px;
            gap: 15px;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: #FFD700;
            min-width: 30px;
        }

        .contact-item h4 {
            font-size: 1.2rem;
            margin-bottom: 5px;
            color: #FFD700;
        }

        .contact-item p {
            color: #cccccc;
            line-height: 1.6;
        }

        .contact-item a {
            color: #cccccc;
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-item a:hover {
            color: #FFD700;
        }

        .map-container {
            background: #1a1a1a;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #333;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .map-container iframe {
            width: 100%;
            height: 350px;
            border: none;
            border-radius: 10px;
            filter: grayscale(50%) brightness(0.8);
        }

        .hours-badge {
            display: inline-block;
            background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%);
            color: #0a0a0a;
            padding: 10px 20px;
            border-radius: 25px;
            margin-top: 10px;
            font-weight: bold;
        }

        /* Footer */
        footer {
            background: #000000;
            color: #cccccc;
            text-align: center;
            padding: 30px 0;
            border-top: 2px solid #FFD700;
        }

        footer p {
            opacity: 0.8;
        }

        .social-links {
            margin: 20px 0;
        }

        .social-links a {
            color: #FFD700;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s, transform 0.3s;
            display: inline-block;
        }

        .social-links a:hover {
            color: #D4AF37;
            transform: scale(1.2);
        }

        /* Animations */
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

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .import-grid,
            .services-grid {
                grid-template-columns: 1fr;
            }

            .logo-text h1 {
                font-size: 1.3rem;
            }

            .countries {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">
                <img src="https://images.unsplash.com/photo-1560179707-f14e90ef3623?w=200&h=200&fit=crop" alt="Ria Auto House Logo">
                <div class="logo-text">
                    <h1>Ria Auto House</h1>
                    <p>Quality Cars in Windhoek</p>
                </div>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#import">Imports</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Your Trusted Car Dealer in Namibia</h2>
            <p>Quality vehicles imported directly from Asia at competitive prices</p>
            <div class="cta-buttons">
                <a href="tel:+264817131637" class="cta-button"><i class="fas fa-phone"></i> Call: +264 81 713 1637</a>
                <a href="https://wa.me/264817131637" class="cta-button secondary"><i class="fab fa-whatsapp"></i> WhatsApp Us</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Ria Auto House</h2>
            <div class="about-content">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1449965408869-eaa3f722e40d?w=600&h=400&fit=crop" alt="Ria Auto House Showroom">
                </div>
                <div class="about-text">
                    <h3>Bringing Quality Cars from Asia to Namibia</h3>
                    <p>Ria Auto House is your premier destination for quality used and new vehicles in Windhoek, Namibia. We specialize in importing cars directly from trusted suppliers in Asia, ensuring you get the best value for your money.</p>
                    <p>With years of experience in the automotive industry, we understand what Namibian drivers need. Our commitment is to provide reliable, well-maintained vehicles at competitive prices, backed by excellent customer service.</p>
                    <p>Whether you're looking for a family sedan, a rugged bakkie, or a reliable taxi, we source the best options from Japan, Korea, China, and other Asian markets to meet your needs and budget.</p>
                    <p><strong>Why Choose Us?</strong></p>
                    <ul style="margin-left: 20px; margin-top: 10px;">
                        <li>Direct imports from Asia - No middlemen</li>
                        <li>Competitive pricing</li>
                        <li>Verified vehicle history</li>
                        <li>Complete documentation support</li>
                        <li>After-sales support</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Import Section -->
    <section class="import-section" id="import">
        <div class="container">
            <h2 class="section-title">Direct Imports from Asia</h2>
            <p style="text-align: center; font-size: 1.2rem; max-width: 800px; margin: 0 auto 40px;">
                We source our vehicles directly from trusted suppliers across Asia, ensuring quality, competitive pricing, and the latest models for the Namibian market.
            </p>
            
            <div class="import-grid">
                <div class="import-card">
                    <i class="fas fa-ship"></i>
                    <h4>Direct Shipping</h4>
                    <p>Vehicles shipped directly from Asian ports to Walvis Bay, eliminating middlemen and reducing costs. Full container and RORO shipping options available.</p>
                </div>
                <div class="import-card">
                    <i class="fas fa-check-circle"></i>
                    <h4>Quality Verified</h4>
                    <p>Every vehicle undergoes rigorous inspection before purchase. We work with certified auction houses and dealers in Japan, Korea, and China.</p>
                </div>
                <div class="import-card">
                    <i class="fas fa-file-contract"></i>
                    <h4>Complete Documentation</h4>
                    <p>We handle all import paperwork, customs clearance, and registration. NATIS documents, roadworthiness certificates, and full legal compliance guaranteed.</p>
                </div>
            </div>

            <div class="countries">
                <div class="country-badge">
                    <i class="fas fa-flag"></i> Japan
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> South Korea
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> China
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> Thailand
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> UAE
                </div>
            </div>

            <div style="margin-top: 50px; background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%); padding: 40px; border-radius: 15px; text-align: center; border: 1px solid #333;">
                <h3 style="margin-bottom: 20px; font-size: 1.8rem; color: #FFD700;"><i class="fas fa-sync-alt" style="color: #FFD700;"></i> How Our Import Process Works</h3>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 30px; margin-top: 30px;">
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">1</div>
                        <h4 style="color: #FFD700;">Tell Us What You Need</h4>
                        <p>Contact us with your preferred make, model & budget</p>
                    </div>
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">2</div>
                        <h4 style="color: #FFD700;">We Source It</h4>
                        <p>We purchase and inspect from our Asian partners</p>
                    </div>
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">3</div>
                        <h4 style="color: #FFD700;">Shipping</h4>
                        <p>Vehicle shipped to Walvis Bay (4-6 weeks)</p>
                    </div>
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">4</div>
                        <h4 style="color: #FFD700;">Clear & Deliver</h4>
                        <p>Customs clearance and delivery to Windhoek</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <i class="fas fa-car"></i>
                    <h4>Car Sales</h4>
                    <p>Quality used and new vehicles at competitive prices</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-ship"></i>
                    <h4>Import Services</h4>
                    <p>Custom car import from Asia with full documentation</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-file-alt"></i>
                    <h4>Documentation</h4>
                    <p>Complete NATIS, registration, and customs clearance</p>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 50px; background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%); padding: 40px; border-radius: 15px; color: white; border: 1px solid #333;">
                <h3 style="margin-bottom: 20px; color: #FFD700;"><i class="fas fa-search" style="color: #FFD700;"></i> Looking for a Specific Car?</h3>
                <p style="font-size: 1.1rem; margin-bottom: 25px; max-width: 700px; margin-left: auto; margin-right: auto; color: #cccccc;">
                    Don't see what you need? We can source any vehicle from our Asian partners. 
                    Just tell us your requirements and we'll find the perfect car for you!
                </p>
                <a href="https://wa.me/264817131637?text=I'm looking for a specific car" class="cta-button"><i class="fab fa-whatsapp"></i> Request a Car via WhatsApp</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Visit Our Showroom</h4>
                            <p>Windhoek, Namibia<br>(Exact location provided upon appointment)</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div>
                            <h4>Phone / WhatsApp</h4>
                            <p><a href="tel:+264817131637" style="color: #cccccc; text-decoration: none;">+264 81 713 1637</a></p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <h4>Email</h4>
                            <p><a href="mailto:gwaantewainvestment23@gmail.com" style="color: #cccccc; text-decoration: none;">gwaantewainvestment23@gmail.com</a></p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <h4>Business Hours</h4>
                            <p>Monday - Sunday<br>08:00 AM - 5:00 PM</p>
                            <span class="hours-badge"><i class="fas fa-check-circle"></i> Open Daily 8AM - 5PM</span>
                        </div>
                    </div>
                    <div style="margin-top: 30px; padding: 20px; background: rgba(255, 215, 0, 0.1); border-radius: 10px; border: 1px solid #333;">
                        <h4 style="margin-bottom: 10px; color: #FFD700;"><i class="fab fa-whatsapp" style="color: #FFD700;"></i> Quick Contact via WhatsApp</h4>
                        <p style="color: #cccccc;">For fastest response, message us on WhatsApp. We usually reply within 1 hour during business hours.</p>
                        <a href="https://wa.me/264817131637" class="cta-button" style="margin-top: 15px; display: inline-block;"><i class="fab fa-whatsapp"></i> Chat on WhatsApp</a>
                    </div>
                </div>

                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d114684.12345678901!2d17.0697!3d-22.5597!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjLCsDMzJzM0LjkiUyAxN8KwMDQnMTAuOSJF!5e0!3m2!1sen!2sna!4v1234567890123!5m2!1sen!2sna"
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade">
                    </iframe>
                    <p style="margin-top: 15px; text-align: center; color: #999; font-size: 0.9rem;">
                        <i class="fas fa-info-circle" style="color: #FFD700;"></i> Windhoek, Namibia<br>
                        <a href="https://www.google.com/maps/place/Windhoek" target="_blank" style="color: #FFD700; text-decoration: none;">
                            Get Directions
                        </a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-whatsapp"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2026 Ria Auto House. All Rights Reserved.</p>
            <p style="margin-top: 10px; font-size: 0.9rem;">
                <i class="fas fa-map-marker-alt" style="color: #FFD700;"></i> Windhoek, Namibia | 
                <i class="fas fa-phone" style="color: #FFD700;"></i> +264 81 713 1637 | 
                <i class="fas fa-envelope" style="color: #FFD700;"></i> gwaantewainvestment23@gmail.com
            </p>
            <p style="margin-top: 15px; font-size: 0.85rem; opacity: 0.7;">
                Quality vehicles imported from Japan, Korea, China & UAE | Open Daily 8AM - 5PM
            </p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
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

        // Add scroll effect to header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 2px 20px rgba(255, 215, 0, 0.2)';
            } else {
                header.style.boxShadow = '0 2px 15px rgba(255, 215, 0, 0.15)';
            }
        });
    </script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ria Auto House | Quality Cars in Windhoek, Namibia</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: #0a0a0a;
        }

        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            border-bottom: 2px solid #FFD700;
            padding: 1rem 0;
            box-shadow: 0 2px 15px rgba(255, 215, 0, 0.15);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo img {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #FFD700;
            background: #222;
        }

        .logo-text h1 {
            font-size: 1.8rem;
            margin-bottom: 0.2rem;
            color: #FFD700;
        }

        .logo-text p {
            font-size: 0.9rem;
            color: #cccccc;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #ffffff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a:hover {
            color: #FFD700;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #FFD700;
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.85), rgba(10, 10, 10, 0.9)),
                        url('https://images.unsplash.com/photo-1449965408869-eaa3f722e40d?w=1920&h=800&fit=crop') center/cover no-repeat;
            color: white;
            padding: 120px 0;
            text-align: center;
            border-bottom: 3px solid #FFD700;
        }

        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
            color: #FFD700;
            text-shadow: 0 2px 10px rgba(255, 215, 0, 0.3);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
            color: #cccccc;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%);
            color: #0a0a0a;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255, 215, 0, 0.5);
        }

        .cta-button.secondary {
            background: transparent;
            border: 2px solid #FFD700;
            color: #FFD700;
        }

        .cta-button.secondary:hover {
            background: #FFD700;
            color: #0a0a0a;
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background: linear-gradient(180deg, #111111 0%, #0a0a0a 100%);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #FFD700;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, #FFD700, #D4AF37);
            margin: 15px auto 0;
            border-radius: 2px;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-image img {
            width: 100%;
            border-radius: 15px;
            border: 2px solid #FFD700;
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.15);
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #FFD700;
        }

        .about-text p {
            margin-bottom: 1rem;
            font-size: 1.1rem;
            line-height: 1.8;
            color: #cccccc;
        }

        .about-text ul {
            color: #cccccc;
        }

        .about-text ul li {
            margin-bottom: 0.5rem;
        }

        .about-text strong {
            color: #FFD700;
        }

        /* Import Section */
        .import-section {
            padding: 80px 0;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 50%, #0a0a0a 100%);
            color: white;
            border-top: 2px solid #333;
            border-bottom: 2px solid #333;
        }

        .import-section .section-title {
            color: #FFD700;
        }

        .import-section .section-title::after {
            background: linear-gradient(90deg, #FFD700, #D4AF37);
        }

        .import-section p {
            color: #cccccc;
        }

        .import-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-top: 40px;
        }

        .import-card {
            background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%);
            padding: 40px 30px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid #333;
            transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
        }

        .import-card:hover {
            transform: translateY(-10px);
            border-color: #FFD700;
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.15);
        }

        .import-card i {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: #FFD700;
        }

        .import-card h4 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #FFD700;
        }

        .import-card p {
            opacity: 0.95;
            line-height: 1.7;
        }

        .countries {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 50px;
            flex-wrap: wrap;
        }

        .country-badge {
            background: linear-gradient(135deg, #222222 0%, #1a1a1a 100%);
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            border: 1px solid #444;
            color: #FFD700;
            transition: border-color 0.3s, box-shadow 0.3s;
        }

        .country-badge:hover {
            border-color: #FFD700;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.2);
        }

        /* Services Section */
        .services {
            padding: 80px 0;
            background: linear-gradient(180deg, #0a0a0a 0%, #111111 100%);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .service-card {
            background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%);
            padding: 35px 25px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid #333;
            transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: #FFD700;
            box-shadow: 0 10px 25px rgba(255, 215, 0, 0.1);
        }

        .service-card i {
            font-size: 3rem;
            color: #FFD700;
            margin-bottom: 15px;
        }

        .service-card h4 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #FFD700;
        }

        .service-card p {
            color: #cccccc;
        }

        /* Contact Section */
        .contact {
            padding: 80px 0;
            background: linear-gradient(135deg, #0a0a0a 0%, #111111 100%);
            color: white;
            border-top: 3px solid #FFD700;
        }

        .contact .section-title {
            color: #FFD700;
        }

        .contact .section-title::after {
            background: linear-gradient(90deg, #FFD700, #D4AF37);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info {
            background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid #333;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 30px;
            gap: 15px;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: #FFD700;
            min-width: 30px;
        }

        .contact-item h4 {
            font-size: 1.2rem;
            margin-bottom: 5px;
            color: #FFD700;
        }

        .contact-item p {
            color: #cccccc;
            line-height: 1.6;
        }

        .contact-item a {
            color: #cccccc;
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-item a:hover {
            color: #FFD700;
        }

        .map-container {
            background: #1a1a1a;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #333;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .map-container iframe {
            width: 100%;
            height: 350px;
            border: none;
            border-radius: 10px;
            filter: grayscale(50%) brightness(0.8);
        }

        .hours-badge {
            display: inline-block;
            background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%);
            color: #0a0a0a;
            padding: 10px 20px;
            border-radius: 25px;
            margin-top: 10px;
            font-weight: bold;
        }

        /* Footer */
        footer {
            background: #000000;
            color: #cccccc;
            text-align: center;
            padding: 30px 0;
            border-top: 2px solid #FFD700;
        }

        footer p {
            opacity: 0.8;
        }

        .social-links {
            margin: 20px 0;
        }

        .social-links a {
            color: #FFD700;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s, transform 0.3s;
            display: inline-block;
        }

        .social-links a:hover {
            color: #D4AF37;
            transform: scale(1.2);
        }

        /* Animations */
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

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .import-grid,
            .services-grid {
                grid-template-columns: 1fr;
            }

            .logo-text h1 {
                font-size: 1.3rem;
            }

            .countries {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">
                <img src="https://images.unsplash.com/photo-1560179707-f14e90ef3623?w=200&h=200&fit=crop" alt="Ria Auto House Logo">
                <div class="logo-text">
                    <h1>Ria Auto House</h1>
                    <p>Quality Cars in Windhoek</p>
                </div>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#import">Imports</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Your Trusted Car Dealer in Namibia</h2>
            <p>Quality vehicles imported directly from Asia at competitive prices</p>
            <div class="cta-buttons">
                <a href="tel:+264817131637" class="cta-button"><i class="fas fa-phone"></i> Call: +264 81 713 1637</a>
                <a href="https://wa.me/264817131637" class="cta-button secondary"><i class="fab fa-whatsapp"></i> WhatsApp Us</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Ria Auto House</h2>
            <div class="about-content">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1449965408869-eaa3f722e40d?w=600&h=400&fit=crop" alt="Ria Auto House Showroom">
                </div>
                <div class="about-text">
                    <h3>Bringing Quality Cars from Asia to Namibia</h3>
                    <p>Ria Auto House is your premier destination for quality used and new vehicles in Windhoek, Namibia. We specialize in importing cars directly from trusted suppliers in Asia, ensuring you get the best value for your money.</p>
                    <p>With years of experience in the automotive industry, we understand what Namibian drivers need. Our commitment is to provide reliable, well-maintained vehicles at competitive prices, backed by excellent customer service.</p>
                    <p>Whether you're looking for a family sedan, a rugged bakkie, or a reliable taxi, we source the best options from Japan, Korea, China, and other Asian markets to meet your needs and budget.</p>
                    <p><strong>Why Choose Us?</strong></p>
                    <ul style="margin-left: 20px; margin-top: 10px;">
                        <li>Direct imports from Asia - No middlemen</li>
                        <li>Competitive pricing</li>
                        <li>Verified vehicle history</li>
                        <li>Complete documentation support</li>
                        <li>After-sales support</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Import Section -->
    <section class="import-section" id="import">
        <div class="container">
            <h2 class="section-title">Direct Imports from Asia</h2>
            <p style="text-align: center; font-size: 1.2rem; max-width: 800px; margin: 0 auto 40px;">
                We source our vehicles directly from trusted suppliers across Asia, ensuring quality, competitive pricing, and the latest models for the Namibian market.
            </p>
            
            <div class="import-grid">
                <div class="import-card">
                    <i class="fas fa-ship"></i>
                    <h4>Direct Shipping</h4>
                    <p>Vehicles shipped directly from Asian ports to Walvis Bay, eliminating middlemen and reducing costs. Full container and RORO shipping options available.</p>
                </div>
                <div class="import-card">
                    <i class="fas fa-check-circle"></i>
                    <h4>Quality Verified</h4>
                    <p>Every vehicle undergoes rigorous inspection before purchase. We work with certified auction houses and dealers in Japan, Korea, and China.</p>
                </div>
                <div class="import-card">
                    <i class="fas fa-file-contract"></i>
                    <h4>Complete Documentation</h4>
                    <p>We handle all import paperwork, customs clearance, and registration. NATIS documents, roadworthiness certificates, and full legal compliance guaranteed.</p>
                </div>
            </div>

            <div class="countries">
                <div class="country-badge">
                    <i class="fas fa-flag"></i> Japan
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> South Korea
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> China
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> Thailand
                </div>
                <div class="country-badge">
                    <i class="fas fa-flag"></i> UAE
                </div>
            </div>

            <div style="margin-top: 50px; background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%); padding: 40px; border-radius: 15px; text-align: center; border: 1px solid #333;">
                <h3 style="margin-bottom: 20px; font-size: 1.8rem; color: #FFD700;"><i class="fas fa-sync-alt" style="color: #FFD700;"></i> How Our Import Process Works</h3>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 30px; margin-top: 30px;">
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">1</div>
                        <h4 style="color: #FFD700;">Tell Us What You Need</h4>
                        <p>Contact us with your preferred make, model & budget</p>
                    </div>
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">2</div>
                        <h4 style="color: #FFD700;">We Source It</h4>
                        <p>We purchase and inspect from our Asian partners</p>
                    </div>
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">3</div>
                        <h4 style="color: #FFD700;">Shipping</h4>
                        <p>Vehicle shipped to Walvis Bay (4-6 weeks)</p>
                    </div>
                    <div>
                        <div style="background: linear-gradient(135deg, #FFD700 0%, #D4AF37 100%); color: #0a0a0a; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; font-size: 1.3rem;">4</div>
                        <h4 style="color: #FFD700;">Clear & Deliver</h4>
                        <p>Customs clearance and delivery to Windhoek</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <i class="fas fa-car"></i>
                    <h4>Car Sales</h4>
                    <p>Quality used and new vehicles at competitive prices</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-ship"></i>
                    <h4>Import Services</h4>
                    <p>Custom car import from Asia with full documentation</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-file-alt"></i>
                    <h4>Documentation</h4>
                    <p>Complete NATIS, registration, and customs clearance</p>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 50px; background: linear-gradient(135deg, #1a1a1a 0%, #222222 100%); padding: 40px; border-radius: 15px; color: white; border: 1px solid #333;">
                <h3 style="margin-bottom: 20px; color: #FFD700;"><i class="fas fa-search" style="color: #FFD700;"></i> Looking for a Specific Car?</h3>
                <p style="font-size: 1.1rem; margin-bottom: 25px; max-width: 700px; margin-left: auto; margin-right: auto; color: #cccccc;">
                    Don't see what you need? We can source any vehicle from our Asian partners. 
                    Just tell us your requirements and we'll find the perfect car for you!
                </p>
                <a href="https://wa.me/264817131637?text=I'm looking for a specific car" class="cta-button"><i class="fab fa-whatsapp"></i> Request a Car via WhatsApp</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Visit Our Showroom</h4>
                            <p>Windhoek, Namibia<br>(Exact location provided upon appointment)</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div>
                            <h4>Phone / WhatsApp</h4>
                            <p><a href="tel:+264817131637" style="color: #cccccc; text-decoration: none;">+264 81 713 1637</a></p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <h4>Email</h4>
                            <p><a href="mailto:gwaantewainvestment23@gmail.com" style="color: #cccccc; text-decoration: none;">gwaantewainvestment23@gmail.com</a></p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <h4>Business Hours</h4>
                            <p>Monday - Sunday<br>08:00 AM - 5:00 PM</p>
                            <span class="hours-badge"><i class="fas fa-check-circle"></i> Open Daily 8AM - 5PM</span>
                        </div>
                    </div>
                    <div style="margin-top: 30px; padding: 20px; background: rgba(255, 215, 0, 0.1); border-radius: 10px; border: 1px solid #333;">
                        <h4 style="margin-bottom: 10px; color: #FFD700;"><i class="fab fa-whatsapp" style="color: #FFD700;"></i> Quick Contact via WhatsApp</h4>
                        <p style="color: #cccccc;">For fastest response, message us on WhatsApp. We usually reply within 1 hour during business hours.</p>
                        <a href="https://wa.me/264817131637" class="cta-button" style="margin-top: 15px; display: inline-block;"><i class="fab fa-whatsapp"></i> Chat on WhatsApp</a>
                    </div>
                </div>

                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d114684.12345678901!2d17.0697!3d-22.5597!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjLCsDMzJzM0LjkiUyAxN8KwMDQnMTAuOSJF!5e0!3m2!1sen!2sna!4v1234567890123!5m2!1sen!2sna"
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade">
                    </iframe>
                    <p style="margin-top: 15px; text-align: center; color: #999; font-size: 0.9rem;">
                        <i class="fas fa-info-circle" style="color: #FFD700;"></i> Windhoek, Namibia<br>
                        <a href="https://www.google.com/maps/place/Windhoek" target="_blank" style="color: #FFD700; text-decoration: none;">
                            Get Directions
                        </a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-whatsapp"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2026 Ria Auto House. All Rights Reserved.</p>
            <p style="margin-top: 10px; font-size: 0.9rem;">
                <i class="fas fa-map-marker-alt" style="color: #FFD700;"></i> Windhoek, Namibia | 
                <i class="fas fa-phone" style="color: #FFD700;"></i> +264 81 713 1637 | 
                <i class="fas fa-envelope" style="color: #FFD700;"></i> gwaantewainvestment23@gmail.com
            </p>
            <p style="margin-top: 15px; font-size: 0.85rem; opacity: 0.7;">
                Quality vehicles imported from Japan, Korea, China & UAE | Open Daily 8AM - 5PM
            </p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
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

        // Add scroll effect to header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 2px 20px rgba(255, 215, 0, 0.2)';
            } else {
                header.style.boxShadow = '0 2px 15px rgba(255, 215, 0, 0.15)';
            }
        });
    </script>

</body>
</html>
