# naveenkumarkanoji.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Naveen Kumar Kanoji | Business Analytics Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #1a252f;
            --gray: #95a5a6;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 100px 0;
        }
        
        h1, h2, h3, h4 {
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        p {
            margin-bottom: 15px;
        }
        
        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--primary);
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .menu-btn {
            display: none;
            cursor: pointer;
            font-size: 24px;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 600px;
            z-index: 2;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: white;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .hero-btns {
            display: flex;
            gap: 15px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--accent);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .hero-bg {
            position: absolute;
            top: 0;
            right: 0;
            height: 100%;
            width: 50%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: cover;
        }
        
        /* About Section */
        .about {
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-text p {
            margin-bottom: 20px;
        }
        
        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        /* Timeline Section */
        .timeline {
            background-color: #f8f9fa;
            position: relative;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background-color: var(--secondary);
        }
        
        .timeline-item {
            width: 50%;
            padding: 20px 40px;
            position: relative;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            top: 30px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: var(--secondary);
            border: 4px solid white;
            box-shadow: 0 0 0 3px var(--secondary);
        }
        
        .timeline-item:nth-child(odd)::before {
            right: -10px;
        }
        
        .timeline-item:nth-child(even)::before {
            left: -10px;
        }
        
        .timeline-content {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .timeline-content:hover {
            transform: translateY(-5px);
        }
        
        .timeline-date {
            font-weight: 600;
            color: var(--secondary);
            margin-bottom: 10px;
        }
        
        /* Skills Section */
        .skills {
            background-color: white;
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background-color: #f8f9fa;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
        }
        
        .skill-category h3 {
            color: var(--secondary);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }
        
        .skill-category h3 i {
            margin-right: 10px;
        }
        
        .skill-list {
            list-style: none;
        }
        
        .skill-list li {
            margin-bottom: 10px;
            padding: 10px 0;
            border-bottom: 1px solid #e9ecef;
            position: relative;
            overflow: hidden;
        }
        
        .skill-list li::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            transition: width 0.5s ease;
        }
        
        .skill-list li:hover::before {
            width: 100%;
        }
        
        /* Projects Section */
        .projects {
            background-color: #f8f9fa;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .project-img {
            height: 200px;
            background-color: var(--secondary);
            position: relative;
            overflow: hidden;
        }
        
        .project-img::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(52, 152, 219, 0.8), rgba(231, 76, 60, 0.8));
            opacity: 0.8;
        }
        
        .project-content {
            padding: 25px;
        }
        
        .project-tools {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin: 15px 0;
        }
        
        .project-tool {
            background-color: #e9ecef;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            color: var(--primary);
        }
        
        /* Contact Section */
        .contact {
            background-color: white;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--secondary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 20px;
        }
        
        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        
        .form-group label {
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-control {
            padding: 12px 15px;
            border: 1px solid #e9ecef;
            border-radius: 5px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .timeline::before {
                left: 30px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 20px;
                left: 0 !important;
            }
            
            .timeline-item::before {
                left: 20px !important;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: all 0.5s ease;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .menu-btn {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: flex-start;
            }
        }
        
        /* Animation Classes */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }
        
        .fade-in.active {
            opacity: 1;
            transform: translateY(0);
        }
        
        .slide-in-left {
            opacity: 0;
            transform: translateX(-50px);
            transition: all 0.8s ease;
        }
        
        .slide-in-left.active {
            opacity: 1;
            transform: translateX(0);
        }
        
        .slide-in-right {
            opacity: 0;
            transform: translateX(50px);
            transition: all 0.8s ease;
        }
        
        .slide-in-right.active {
            opacity: 1;
            transform: translateX(0);
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Naveen<span>Kumar</span></div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#timeline">Timeline</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="menu-btn">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Naveen Kumar Kanoji</h1>
                <p>Business Analytics Graduate Student | Data-Driven Problem Solver | Strategic Analyst</p>
                <div class="hero-btns">
                    <a href="#projects" class="btn">View My Work</a>
                    <a href="#contact" class="btn btn-outline">Get In Touch</a>
                </div>
            </div>
        </div>
        <div class="hero-bg"></div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text slide-in-left">
                    <p>Analytical and detail-driven Business Analytics graduate student with hands-on experience delivering business value through forecasting, customer analytics, and strategic modeling.</p>
                    <p>Proficient in SQL, Python, Power BI, and Tableau, with a strong track record of using data to optimize risk management, revenue strategy, and customer insights.</p>
                    <p>Collaborative communicator with real-world experience in large-scale data processing and executive-facing dashboards.</p>
                    <div class="contact-info">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Location</h4>
                                <p>New Haven, CT</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>naveenkanoji5@gmail.com</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>+1 (203) 948-5525</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="about-image slide-in-right">
                    <!-- Placeholder for profile image -->
                    <div style="width:100%; height:400px; background:linear-gradient(45deg, var(--secondary), var(--accent)); display:flex; align-items:center; justify-content:center; color:white; font-size:24px;">
                        <i class="fas fa-user" style="font-size: 80px;"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Timeline Section -->
    <section id="timeline" class="timeline">
        <div class="container">
            <h2 class="section-title">Education & Experience</h2>
            <div class="timeline-container">
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-date">2025</div>
                        <h3>Master of Science in Business Analytics</h3>
                        <h4>University of New Haven</h4>
                        <p>New Haven, CT</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-date">2022</div>
                        <h3>Bachelor of Business Administration (BBA)</h3>
                        <h4>Chaitanya Degree College</h4>
                        <p>Warangal, India</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-content">
                        <div class="timeline-date">Aug 2024 - Dec 2024</div>
                        <h3>Client Marketing Project</h3>
                        <h4>Trinity Academy Hartford | University of New Haven</h4>
                        <p>Partnered with a team to create a comprehensive social media and branding strategy for a nonprofit elementary school. Conducted audience analysis, competitor benchmarking, and identified key marketing challenges.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <h2 class="section-title">Skills & Abilities</h2>
            <div class="skills-container">
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-chart-line"></i> Data Analytics</h3>
                    <ul class="skill-list">
                        <li>SQL</li>
                        <li>Excel</li>
                        <li>R</li>
                        <li>Python (Pandas)</li>
                        <li>Power BI</li>
                        <li>Tableau</li>
                    </ul>
                </div>
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-calculator"></i> Modeling & Forecasting</h3>
                    <ul class="skill-list">
                        <li>Logistic Regression</li>
                        <li>ARIMA</li>
                        <li>Customer Lifetime Value (CLV)</li>
                        <li>Survival Analysis</li>
                    </ul>
                </div>
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-database"></i> Database Tools</h3>
                    <ul class="skill-list">
                        <li>SQL Server</li>
                        <li>SSIS</li>
                        <li>MySQL</li>
                    </ul>
                </div>
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-brain"></i> Business & Strategy</h3>
                    <ul class="skill-list">
                        <li>Break-even Analysis</li>
                        <li>Revenue Modeling</li>
                        <li>Risk Assessment</li>
                    </ul>
                </div>
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-chart-bar"></i> Visualization</h3>
                    <ul class="skill-list">
                        <li>Power BI</li>
                        <li>Tableau</li>
                        <li>Excel</li>
                    </ul>
                </div>
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-users"></i> Soft Skills</h3>
                    <ul class="skill-list">
                        <li>Stakeholder Communication</li>
                        <li>Problem Solving</li>
                        <li>Cross-functional Collaboration</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Project Experience</h2>
            <div class="projects-grid">
                <div class="project-card fade-in">
                    <div class="project-img">
                        <!-- Project image placeholder -->
                    </div>
                    <div class="project-content">
                        <h3>Corpay - Credit Risk & Customer Lifecycle Optimization</h3>
                        <p>Processed over 1B records using SSIS pipelines for behavioral risk analysis and customer segmentation. Predicted customer churn and default risk using logistic regression and ARIMA forecasting.</p>
                        <div class="project-tools">
                            <span class="project-tool">SQL Server</span>
                            <span class="project-tool">SSIS</span>
                            <span class="project-tool">Python</span>
                            <span class="project-tool">R</span>
                            <span class="project-tool">Power BI</span>
                            <span class="project-tool">Tableau</span>
                        </div>
                    </div>
                </div>
                <div class="project-card fade-in">
                    <div class="project-img">
                        <!-- Project image placeholder -->
                    </div>
                    <div class="project-content">
                        <h3>Port Authority Bus Terminal Forecasting (Capstone)</h3>
                        <p>Built time-series forecasts of bus departures through 2030; identified congestion thresholds and seasonal anomalies. Integrated external events into model to explain usage spikes with 85% accuracy.</p>
                        <div class="project-tools">
                            <span class="project-tool">Power BI</span>
                            <span class="project-tool">Excel</span>
                        </div>
                    </div>
                </div>
                <div class="project-card fade-in">
                    <div class="project-img">
                        <!-- Project image placeholder -->
                    </div>
                    <div class="project-content">
                        <h3>Apple Console Strategy Simulation</h3>
                        <p>Designed a complete GTM strategy for a conceptual Apple console: projected $3.5B revenue in year one. Modeled investments in R&D, supply chain, and marketing across a 3-year roadmap.</p>
                        <div class="project-tools">
                            <span class="project-tool">Excel</span>
                            <span class="project-tool">Strategic Planning</span>
                            <span class="project-tool">Break-even Analysis</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h4>Location</h4>
                            <p>New Haven, CT</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h4>Email</h4>
                            <p>naveenkanoji5@gmail.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h4>Phone</h4>
                            <p>+1 (203) 948-5525</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fab fa-linkedin"></i>
                        </div>
                        <div>
                            <h4>LinkedIn</h4>
                            <p>linkedin.com/in/naveen-kumar-kanoji-990b8920b</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" class="form-control" placeholder="Enter your name">
                    </div>
                    <div class="form-group">
                        <label for="email">Your Email</label>
                        <input type="email" id="email" class="form-control" placeholder="Enter your email">
                    </div>
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" class="form-control" placeholder="Enter subject">
                    </div>
                    <div class="form-group">
                        <label for="message">Your Message</label>
                        <textarea id="message" class="form-control" placeholder="Enter your message"></textarea>
                    </div>
                    <button class="btn">Send Message</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="mailto:naveenkanoji5@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="https://www.linkedin.com/in/naveen-kumar-kanoji-990b8920b" class="social-link">
                    <i class="fab fa-linkedin"></i>
                </a>
                <a href="tel:+12039485525" class="social-link">
                    <i class="fas fa-phone"></i>
                </a>
            </div>
            <p>&copy; 2023 Naveen Kumar Kanoji. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // GSAP Animations
        gsap.registerPlugin(ScrollTrigger);
        
        // Animate elements on scroll
        gsap.utils.toArray('.fade-in').forEach(element => {
            gsap.fromTo(element, {
                opacity: 0,
                y: 50
            }, {
                opacity: 1,
                y: 0,
                duration: 1,
                scrollTrigger: {
                    trigger: element,
                    start: "top 80%",
                    end: "bottom 20%",
                    toggleActions: "play none none reverse"
                }
            });
        });
        
        gsap.utils.toArray('.slide-in-left').forEach(element => {
            gsap.fromTo(element, {
                opacity: 0,
                x: -50
            }, {
                opacity: 1,
                x: 0,
                duration: 1,
                scrollTrigger: {
                    trigger: element,
                    start: "top 80%",
                    end: "bottom 20%",
                    toggleActions: "play none none reverse"
                }
            });
        });
        
        gsap.utils.toArray('.slide-in-right').forEach(element => {
            gsap.fromTo(element, {
                opacity: 0,
                x: 50
            }, {
                opacity: 1,
                x: 0,
                duration: 1,
                scrollTrigger: {
                    trigger: element,
                    start: "top 80%",
                    end: "bottom 20%",
                    toggleActions: "play none none reverse"
                }
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.padding = '10px 0';
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.padding = '20px 0';
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.95)';
            }
        });
        
        // Mobile menu toggle
        const menuBtn = document.querySelector('.menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        menuBtn.addEventListener('click', function() {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', function() {
                navLinks.classList.remove('active');
            });
        });
    </script>
</body>
</html>
