<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dandora Girls Secondary School - Knowledge is Power</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        header {
            background: linear-gradient(135deg, #00bcd4 0%, #0288d1 100%);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo {
            width: 70px;
            height: 70px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #0288d1;
            font-size: 22px;
            border: 4px solid #00bcd4;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .school-name h1 {
            font-size: 1.6rem;
            margin-bottom: 5px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.2);
        }

        .school-name p {
            font-size: 0.95rem;
            opacity: 0.95;
            font-style: italic;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 8px 15px;
            border-radius: 5px;
            transition: background 0.3s;
            font-weight: 500;
        }

        nav a:hover {
            background: rgba(255,255,255,0.25);
        }

        .hero {
            background: linear-gradient(rgba(0, 188, 212, 0.9), rgba(2, 136, 209, 0.9)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%230288d1" width="1200" height="600"/><circle fill="%2300bcd4" opacity="0.3" cx="200" cy="100" r="150"/><circle fill="%2300bcd4" opacity="0.3" cx="1000" cy="400" r="200"/><circle fill="%2300bcd4" opacity="0.2" cx="600" cy="300" r="250"/></svg>');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 110px 20px;
            text-align: center;
        }

        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 35px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.2);
        }

        .motto {
            font-size: 1.5rem;
            font-weight: bold;
            font-style: italic;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .cta-button {
            display: inline-block;
            background: white;
            color: #0288d1;
            padding: 16px 45px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 20px rgba(255,255,255,0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(255,255,255,0.5);
        }

        .section {
            padding: 70px 20px;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 50px;
            color: #0288d1;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 35px;
            margin-top: 40px;
        }

        .feature-card {
            background: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,188,212,0.15);
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            border-top: 5px solid #00bcd4;
        }

        .feature-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 30px rgba(0,188,212,0.25);
            border-top-color: #0288d1;
        }

        .feature-icon {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }

        .feature-card h3 {
            color: #0288d1;
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        .about-section {
            background: linear-gradient(135deg, #e0f7fa 0%, #b2ebf2 100%);
        }

        .about-content {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 35px;
            margin-top: 50px;
        }

        .stat-card {
            background: white;
            padding: 35px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .stat-card:hover {
            transform: scale(1.05);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: #00bcd4;
            margin-bottom: 15px;
        }

        .programs-section {
            background: linear-gradient(135deg, #0288d1 0%, #00bcd4 100%);
            color: white;
        }

        .programs-section .section-title {
            color: white;
        }

        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .program-card {
            background: rgba(255,255,255,0.15);
            padding: 30px;
            border-radius: 12px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            transition: background 0.3s;
        }

        .program-card:hover {
            background: rgba(255,255,255,0.25);
        }

        .program-card h3 {
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        .contact-section {
            background: #1a2332;
            color: white;
        }

        .contact-section .section-title {
            color: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }

        .contact-info {
            background: rgba(0,188,212,0.15);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid rgba(0,188,212,0.3);
        }

        .contact-info h3 {
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 12px;
            color: #00bcd4;
            font-size: 1.3rem;
        }

        .contact-info p {
            line-height: 2;
            font-size: 1.05rem;
        }

        .contact-info a {
            color: #00bcd4;
            text-decoration: none;
            font-weight: 500;
        }

        footer {
            background: #0a0a14;
            color: white;
            text-align: center;
            padding: 35px 20px;
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                flex-direction: column;
                width: 100%;
                text-align: center;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .motto {
                font-size: 1.2rem;
            }

            .school-name h1 {
                font-size: 1.3rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo-section">
                    <div class="logo">DGSS</div>
                    <div class="school-name">
                        <h1>Dandora Girls Secondary School</h1>
                        <p>Knowledge is Power</p>
                    </div>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#programs">Programs</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <h2>Welcome to Dandora Girls Secondary School</h2>
            <p class="motto">"Knowledge is Power"</p>
            <p>Empowering young women through quality education and character development. Building confident, capable future leaders.</p>
            <a href="#contact" class="cta-button">Enroll Your Daughter Today</a>
        </div>
    </section>

    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">About Our School</h2>
            <div class="about-content">
                <p style="font-size: 1.15rem; margin-bottom: 35px;">
                    Dandora Girls Secondary School is dedicated to providing excellent education for young women in Nairobi. 
                    We create a supportive environment where girls can excel academically, develop strong character, and prepare for successful futures.
                </p>
                <div class="stats">
                    <div class="stat-card">
                        <div class="stat-number">600+</div>
                        <p>Students Enrolled</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">25+</div>
                        <p>Qualified Teachers</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">18+</div>
                        <p>Years of Excellence</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <h2 class="section-title">Why Choose Dandora Girls?</h2>
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">📚</div>
                    <h3>Academic Excellence</h3>
                    <p>Comprehensive curriculum with experienced teachers dedicated to student success and strong KCSE performance.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">👩‍🎓</div>
                    <h3>Girl-Focused Education</h3>
                    <p>Safe, supportive environment specifically designed to help young women thrive and reach their full potential.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌟</div>
                    <h3>Character Development</h3>
                    <p>Focus on leadership, confidence, and life skills alongside academic achievement.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🔬</div>
                    <h3>Science & Technology</h3>
                    <p>Modern laboratories and ICT facilities supporting STEM education for girls.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🏆</div>
                    <h3>Co-Curricular Activities</h3>
                    <p>Sports, clubs, drama, and music programs that develop well-rounded students.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💪</div>
                    <h3>Empowerment Programs</h3>
                    <p>Mentorship, guidance and counseling to build confident, capable young women.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section programs-section" id="programs">
        <div class="container">
            <h2 class="section-title">Our Programs</h2>
            <div class="programs-grid">
                <div class="program-card">
                    <h3>Form 1-4 Education</h3>
                    <p>Complete secondary education following the Kenyan national curriculum with focus on KCSE excellence and university preparation.</p>
                </div>
                <div class="program-card">
                    <h3>Sciences & Mathematics</h3>
                    <p>Strong emphasis on sciences and mathematics with modern laboratories, qualified teachers, and hands-on learning.</p>
                </div>
                <div class="program-card">
                    <h3>Languages & Arts</h3>
                    <p>Comprehensive programs in English, Kiswahili, humanities, and creative arts.</p>
                </div>
                <div class="program-card">
                    <h3>Leadership & Life Skills</h3>
                    <p>Mentorship programs, guidance and counseling, and leadership training to prepare girls for life beyond school.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section about-section">
        <div class="container">
            <h2 class="section-title">Our Mission</h2>
            <div class="about-content">
                <p style="font-size: 1.15rem; line-height: 1.8;">
                    To provide quality education that empowers young women with knowledge, skills, and confidence to become responsible citizens and leaders in society. 
                    We believe that educating a girl is educating a nation, and we are committed to nurturing the full potential of every student.
                </p>
            </div>
        </div>
    </section>

    <section class="section contact-section" id="contact">
        <div class="container">
            <h2 class="section-title">Get in Touch</h2>
            <p style="text-align: center; font-size: 1.15rem; margin-bottom: 50px;">
                Ready to give your daughter a quality education? Contact us today to learn more about enrollment and visit our school.
            </p>
            <div class="contact-grid">
                <div class="contact-info">
                    <h3>📍 Location</h3>
                    <p>Dandora, Nairobi<br>
                    Kenya</p>
                </div>
                <div class="contact-info">
                    <h3>📞 Phone</h3>
                    <p><a href="tel:+254735252747">0735 252747</a></p>
                    <p>Monday - Friday: 8:00 AM - 5:00 PM</p>
                </div>
                <div class="contact-info">
                    <h3>⏰ School Hours</h3>
                    <p>Monday - Friday<br>
                    7:30 AM - 4:00 PM</p>
                </div>
            </div>
            <div style="text-align: center; margin-top: 50px;">
                <a href="tel:+254735252747" class="cta-button">Call Now to Enroll</a>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Dandora Girls Secondary School. All rights reserved.</p>
            <p style="margin-top: 12px; font-size: 0.95rem;">Empowering Young Women Through Education</p>
        </div>
    </footer>
</body>
</html>
