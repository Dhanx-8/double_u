<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentation Design Studio | Portfolio & Rate Card 2026</title>
    <link href="[fonts.googleapis.com](https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Playfair+Display:wght@600;700&display=swap)" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #0f172a;
            --accent: #f59e0b;
            --light: #f8fafc;
            --gray: #64748b;
            --border: #e2e8f0;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--light);
            color: var(--secondary);
            line-height: 1.6;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--secondary);
        }

        .logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--gray);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            padding-top: 80px;
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .hero-text h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }

        .hero-text h1 span {
            color: var(--primary);
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--gray);
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(37, 99, 235, 0.3);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary);
            color: var(--secondary);
            margin-left: 1rem;
        }

        .btn-outline:hover {
            background: var(--secondary);
            color: white;
        }

        .hero-visual {
            position: relative;
        }

        .hero-card {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            box-shadow: 0 25px 50px rgba(0,0,0,0.1);
            transform: rotate(3deg);
        }

        .hero-card-inner {
            background: linear-gradient(135deg, var(--primary) 0%, #7c3aed 100%);
            border-radius: 12px;
            padding: 2rem;
            color: white;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: 800;
        }

        .stat-label {
            font-size: 0.85rem;
            opacity: 0.9;
        }

        /* Section Styling */
        section {
            padding: 6rem 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-tag {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .section-subtitle {
            color: var(--gray);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Portfolio Section */
        #portfolio {
            background: white;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .portfolio-card {
            background: var(--light);
            border-radius: 16px;
            overflow: hidden;
            transition: all 0.3s;
            cursor: pointer;
        }

        .portfolio-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .portfolio-image {
            height: 250px;
            background-size: cover;
            background-position: center;
            position: relative;
            overflow: hidden;
        }

        .portfolio-image::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(to bottom, transparent 50%, rgba(0,0,0,0.7));
        }

        .portfolio-category {
            position: absolute;
            top: 1rem;
            left: 1rem;
            background: white;
            padding: 0.4rem 1rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .portfolio-info {
            padding: 1.5rem;
        }

        .portfolio-title {
            font-size: 1.25rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .portfolio-desc {
            color: var(--gray);
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }

        .portfolio-tags {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .tag {
            background: var(--border);
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 500;
        }

        /* Rate Card Section */
        #rates {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: white;
        }

        #rates .section-title,
        #rates .section-subtitle {
            color: white;
        }

        #rates .section-subtitle {
            opacity: 0.8;
        }

        .rate-category {
            margin-bottom: 4rem;
        }

        .rate-category-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid rgba(255,255,255,0.1);
        }

        .rate-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .rate-card {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 20px;
            padding: 2rem;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .rate-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            opacity: 0;
            transition: opacity 0.3s;
        }

        .rate-card:hover {
            background: rgba(255,255,255,0.1);
            transform: translateY(-5px);
        }

        .rate-card:hover::before {
            opacity: 1;
        }

        .rate-card.popular {
            border-color: var(--primary);
            background: rgba(37, 99, 235, 0.1);
        }

        .rate-card.popular::before {
            opacity: 1;
        }

        .popular-badge {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: var(--accent);
            color: var(--secondary);
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 700;
        }

        .rate-name {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .rate-price {
            font-size: 2rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .rate-price span {
            font-size: 1rem;
            font-weight: 400;
            opacity: 0.7;
        }

        .rate-suitable {
            font-size: 0.9rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
        }

        .rate-features {
            list-style: none;
        }

        .rate-features li {
            padding: 0.6rem 0;
            border-bottom: 1px solid rgba(255,255,255,0.05);
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 0.95rem;
        }

        .rate-features li::before {
            content: '✓';
            color: #22c55e;
            font-weight: 700;
        }

        /* Add-ons Section */
        .addons-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .addon-item {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 12px;
            padding: 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .addon-name {
            font-weight: 500;
        }

        .addon-price {
            color: var(--accent);
            font-weight: 700;
        }

        /* Process Section */
        #process {
            background: white;
        }

        .process-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }

        .process-step {
            text-align: center;
            padding: 2rem;
            position: relative;
        }

        .process-step::after {
            content: '→';
            position: absolute;
            right: -1rem;
            top: 50%;
            transform: translateY(-50%);
            font-size: 2rem;
            color: var(--border);
        }

        .process-step:last-child::after {
            display: none;
        }

        .process-number {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary), #7c3aed);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 800;
            color: white;
            margin: 0 auto 1.5rem;
        }

        .process-title {
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .process-desc {
            color: var(--gray);
            font-size: 0.95rem;
        }

        /* Testimonials */
        #testimonials {
            background: var(--light);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: white;
            border-radius: 16px;
            padding: 2rem;
            box-shadow: 0 4px 20px rgba(0,0,0,0.05);
        }

        .testimonial-text {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
            color: var(--secondary);
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), #7c3aed);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
        }

        .author-name {
            font-weight: 700;
        }

        .author-role {
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* Contact Section */
        #contact {
            background: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            margin-bottom: 1.5rem;
        }

        .contact-info p {
            color: var(--gray);
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem 0;
            border-bottom: 1px solid var(--border);
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--light);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
        }

        .contact-label {
            font-size: 0.85rem;
            color: var(--gray);
        }

        .contact-value {
            font-weight: 600;
            font-size: 1.1rem;
        }

        .contact-form {
            background: var(--light);
            border-radius: 20px;
            padding: 2.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid var(--border);
            border-radius: 10px;
            font-size: 1rem;
            font-family: inherit;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        /* Footer */
        footer {
            background: var(--secondary);
            color: white;
            padding: 4rem 0 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-brand .logo {
            color: white;
            margin-bottom: 1rem;
        }

        .footer-brand p {
            color: rgba(255,255,255,0.7);
            font-size: 0.95rem;
        }

        .footer-title {
            font-weight: 700;
            margin-bottom: 1.5rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.75rem;
        }

        .footer-links a {
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: white;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.5);
            font-size: 0.9rem;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            padding: 2rem;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: white;
            border-radius: 20px;
            max-width: 900px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
        }

        .modal-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            width: 40px;
            height: 40px;
            border: none;
            background: var(--light);
            border-radius: 50%;
            cursor: pointer;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10;
        }

        .modal-image {
            width: 100%;
            height: 400px;
            background-size: cover;
            background-position: center;
            border-radius: 20px 20px 0 0;
        }

        .modal-body {
            padding: 2rem;
        }

        .modal-title {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .modal-meta {
            display: flex;
            gap: 2rem;
            margin-bottom: 1.5rem;
            color: var(--gray);
        }

        .modal-desc {
            color: var(--gray);
            line-height: 1.8;
        }

        /* Mobile Menu */
        .mobile-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            background: none;
            border: none;
            cursor: pointer;
        }

        .mobile-toggle span {
            width: 25px;
            height: 3px;
            background: var(--secondary);
            border-radius: 2px;
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-visual {
                display: none;
            }

            .process-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .process-step::after {
                display: none;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .footer-content {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-toggle {
                display: flex;
            }

            .hero-text h1 {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .process-grid {
                grid-template-columns: 1fr;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .footer-content {
                grid-template-columns: 1fr;
            }
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

        .animate {
            animation: fadeInUp 0.6s ease forwards;
        }

        /* Scroll Progress */
        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            z-index: 1001;
            width: 0%;
            transition: width 0.1s;
        }
    </style>
</head>
<body>
    <div class="scroll-progress" id="scrollProgress"></div>

    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">Slide<span>Studio</span></div>
            <ul class="nav-links">
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#rates">Rate Card</a></li>
                <li><a href="#process">Proses</a></li>
                <li><a href="#testimonials">Testimonial</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
            <button class="mobile-toggle" id="mobileToggle">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Presentasi yang <span>Memukau</span> & Meyakinkan</h1>
                    <p>Membantu pembuatan presentasi profesional untuk corporate, startup, agency, dan kebutuhan akademik. Dari pitch deck hingga sidang skripsi.</p>
                    <a href="#rates" class="btn btn-primary">Lihat Rate Card</a>
                    <a href="#portfolio" class="btn btn-outline">Portfolio</a>
                </div>
                <div class="hero-visual">
                    <div class="hero-card">
                        <div class="hero-card-inner">
                            <h3 style="font-size: 1.3rem; margin-bottom: 0.5rem;">Trusted by 500+ Clients</h3>
                            <p style="opacity: 0.9; font-size: 0.95rem;">Corporate • Startup • Academic</p>
                            <div class="stats-grid">
                                <div class="stat-item">
                                    <div class="stat-number">500+</div>
                                    <div class="stat-label">Projects</div>
                                </div>
                                <div class="stat-item">
                                    <div class="stat-number">98%</div>
                                    <div class="stat-label">Satisfied</div>
                                </div>
                                <div class="stat-item">
                                    <div class="stat-number">24h</div>
                                    <div class="stat-label">Express</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio">
        <div class="container">
            <div class="section-header">
                <span class="section-tag">Portfolio</span>
                <h2 class="section-title">Project Terbaru</h2>
                <p class="section-subtitle">Beberapa contoh project yang telah kami kerjakan untuk berbagai klien</p>
            </div>

            <div class="portfolio-grid">
                <div class="portfolio-card" onclick="openModal(0)">
                    <div class="portfolio-image" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">
                        <span class="portfolio-category">Investor Pitch</span>
                    </div>
                    <div class="portfolio-info">
                        <h3 class="portfolio-title">TechVenture Series A Pitch Deck</h3>
                        <p class="portfolio-desc">Pitch deck untuk startup fintech yang berhasil mendapatkan funding Series A senilai $5M</p>
                        <div class="portfolio-tags">
                            <span class="tag">25 Slides</span>
                            <span class="tag">Startup</span>
                            <span class="tag">Investor Ready</span>
                        </div>
                    </div>
                </div>

                <div class="portfolio-card" onclick="openModal(1)">
                    <div class="portfolio-image" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);">
                        <span class="portfolio-category">Corporate</span>
                    </div>
                    <div class="portfolio-info">
                        <h3 class="portfolio-title">Annual Report PT Maju Bersama</h3>
                        <p class="portfolio-desc">Laporan tahunan dengan visualisasi data komprehensif untuk RUPS perusahaan manufaktur</p>
                        <div class="portfolio-tags">
                            <span class="tag">40 Slides</span>
                            <span class="tag">Data Viz</span>
                            <span class="tag">Bilingual</span>
                        </div>
                    </div>
                </div>

                <div class="portfolio-card" onclick="openModal(2)">
                    <div class="portfolio-image" style="background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);">
                        <span class="portfolio-category">Sales Proposal</span>
                    </div>
                    <div class="portfolio-info">
                        <h3 class="portfolio-title">Agency Credentials Deck</h3>
                        <p class="portfolio-desc">Company profile dan case study untuk digital marketing agency pitching ke klien enterprise</p>
                        <div class="portfolio-tags">
                            <span class="tag">30 Slides</span>
                            <span class="tag">Agency</span>
                            <span class="tag">Case Study</span>
                        </div>
                    </div>
                </div>

                <div class="portfolio-card" onclick="openModal(3)">
                    <div class="portfolio-image" style="background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);">
                        <span class="portfolio-category">Academic</span>
                    </div>
                    <div class="portfolio-info">
                        <h3 class="portfolio-title">Thesis Defense - UI Economics</h3>
                        <p class="portfolio-desc">Presentasi sidang skripsi tentang economic policy impact analysis dengan visualisasi data ekonomi</p>
                        <div class="portfolio-tags">
                            <span class="tag">15 Slides</span>
                            <span class="tag">Academic</span>
                            <span class="tag">Research</span>
                        </div>
                    </div>
                </div>

                <div class="portfolio-card" onclick="openModal(4)">
                    <div class="portfolio-image" style="background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);">
                        <span class="portfolio-category">Board Meeting</span>
                    </div>
                    <div class="portfolio-info">
                        <h3 class="portfolio-title">Q4 Strategy Review - FMCG Corp</h3>
                        <p class="portfolio-desc">Executive presentation untuk board of directors dengan strategic roadmap dan financial projections</p>
                        <div class="portfolio-tags">
                            <span class="tag">28 Slides</span>
                            <span class="tag">Executive</span>
                            <span class="tag">Strategy</span>
                        </div>
                    </div>
                </div>

                <div class="portfolio-card" onclick="openModal(5)">
                    <div class="portfolio-image" style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);">
                        <span class="portfolio-category">Competition</span>
                    </div>
                    <div class="portfolio-info">
                        <h3 class="portfolio-title">Business Case Competition - Winner</h3>
                        <p class="portfolio-desc">Deck kompetisi bisnis tingkat nasional yang berhasil meraih juara 1</p>
                        <div class="portfolio-tags">
                            <span class="tag">20 Slides</span>
                            <span class="tag">Student</span>
                            <span class="tag">1st Place</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Rate Card Section -->
    <section id="rates">
        <div class="container">
            <div class="section-header">
                <span class="section-tag">Rate Card 2026</span>
                <h2 class="section-title">Transparent Pricing</h2>
                <p class="section-subtitle">Pilih paket yang sesuai dengan kebutuhan presentasi Anda</p>
            </div>

            <!-- Corporate Package -->
            <div class="rate-category">
                <h3 class="rate-category-title">💼 Corporate / Business Package</h3>
                <div class="rate-cards">
                    <div class="rate-card">
                        <div class="rate-name">Starter Deck</div>
                        <div class="rate-price">Rp1.500.000 <span>mulai dari</span></div>
                        <div class="rate-suitable">Internal meeting • Company profile sederhana</div>
                        <ul class="rate-features">
                            <li>Up to 10 slides</li>
                            <li>Clean professional layout</li>
                            <li>Minor redesign</li>
                            <li>1x revisi</li>
                        </ul>
                    </div>

                    <div class="rate-card popular">
                        <span class="popular-badge">POPULAR</span>
                        <div class="rate-name">Business Deck</div>
                        <div class="rate-price">Rp3.500.000 <span>mulai dari</span></div>
                        <div class="rate-suitable">Sales proposal • Client presentation • Marketing</div>
                        <ul class="rate-features">
                            <li>Up to 20 slides</li>
                            <li>Custom layout design</li>
                            <li>Chart / data visualization</li>
                            <li>2x revisi</li>
                        </ul>
                    </div>

                    <div class="rate-card">
                        <div class="rate-name">Executive Deck</div>
                        <div class="rate-price">Rp7.500.000 <span>mulai dari</span></div>
                        <div class="rate-suitable">Board meeting • Investor pitch • RAKER</div>
                        <ul class="rate-features">
                            <li>Up to 30 slides</li>
                            <li>Full redesign</li>
                            <li>Storytelling structure</li>
                            <li>Premium visual style</li>
                            <li>Priority handling</li>
                            <li>3x revisi</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Academic Package -->
            <div class="rate-category">
                <h3 class="rate-category-title">🎓 Academic / Student Package</h3>
                <div class="rate-cards">
                    <div class="rate-card">
                        <div class="rate-name">Basic Academic</div>
                        <div class="rate-price">Rp500.000 <span>mulai dari</span></div>
                        <div class="rate-suitable">Tugas kuliah • Presentasi kelas • Seminar</div>
                        <ul class="rate-features">
                            <li>Up to 10 slides</li>
                            <li>Simple clean design</li>
                            <li>1x revisi</li>
                        </ul>
                    </div>

                    <div class="rate-card popular">
                        <span class="popular-badge">BEST VALUE</span>
                        <div class="rate-name">Thesis / Sidang Deck</div>
                        <div class="rate-price">Rp900.000 <span>mulai dari</span></div>
                        <div class="rate-suitable">Sidang skripsi • Tesis • Business competition</div>
                        <ul class="rate-features">
                            <li>Up to 15 slides</li>
                            <li>Professional structure</li>
                            <li>Visual improvement</li>
                            <li>2x revisi</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Add-ons -->
            <div class="rate-category">
                <h3 class="rate-category-title">⚡ Add-on Services</h3>
                <div class="addons-grid">
                    <div class="addon-item">
                        <span class="addon-name">Extra Slide</span>
                        <span class="addon-price">Rp150.000/slide</span>
                    </div>
                    <div class="addon-item">
                        <span class="addon-name">Additional Presenter</span>
                        <span class="addon-price">+Rp500.000/orang</span>
                    </div>
                    <div class="addon-item">
                        <span class="addon-name">Presenter Notes</span>
                        <span class="addon-price">+Rp500.000</span>
                    </div>
                    <div class="addon-item">
                        <span class="addon-name">Additional Revision</span>
                        <span class="addon-price">+Rp500.000</span>
                    </div>
                    <div class="addon-item">
                        <span class="addon-name">Express 24 Jam</span>
                        <span class="addon-price">+50%</span>
                    </div>
                    <div class="addon-item">
                        <span class="addon-name">Custom Infographic</span>
                        <span class="addon-price">Rp300.000/slide</span>
                    </div>
                </div>
            </div>

            <div style="background: rgba(255,255,255,0.05); border-radius: 16px; padding: 2rem; margin-top: 3rem;">
                <h4 style="margin-bottom: 1rem;">📋 Notes</h4>
                <ul style="list-style: none; color: rgba(255,255,255,0.8);">
                    <li style="padding: 0.5rem 0;">• Harga final menyesuaikan kompleksitas data, deadline, dan brief project</li>
                    <li style="padding: 0.5rem 0;">• Revisi di luar scope awal akan dikenakan biaya tambahan</li>
                    <li style="padding: 0.5rem 0;">• DP 50% sebelum pengerjaan dimulai</li>
                    <li style="padding: 0.5rem 0;">• File final dikirim dalam format PPTX / PDF</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Process Section -->
    <section id="process">
        <div class="container">
            <div class="section-header">
                <span class="section-tag">How It Works</span>
                <h2 class="section-title">Proses Kerja</h2>
                <p class="section-subtitle">4 langkah sederhana untuk mendapatkan presentasi impian Anda</p>
            </div>

            <div class="process-grid">
                <div class="process-step">
                    <div class="process-number">1</div>
                    <h3 class="process-title">Brief & Konsultasi</h3>
                    <p class="process-desc">Diskusi kebutuhan, tujuan presentasi, dan preferensi desain Anda</p>
                </div>
                <div class="process-step">
                    <div class="process-number">2</div>
                    <h3 class="process-title">Proposal & DP</h3>
                    <p class="process-desc">Kami kirimkan proposal harga. Setelah deal, DP 50% untuk mulai pengerjaan</p>
                </div>
                <div class="process-step">
                    <div class="process-number">3</div>
                    <h3 class="process-title">Desain & Revisi</h3>
                    <p class="process-desc">Proses desain dimulai. Review bersama dan revisi sesuai feedback</p>
                </div>
                <div class="process-step">
                    <div class="process-number">4</div>
                    <h3 class="process-title">Final & Delivery</h3>
                    <p class="process-desc">Pelunasan dan file final (PPTX/PDF) dikirimkan ke Anda</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section id="testimonials">
        <div class="container">
            <div class="section-header">
                <span class="section-tag">Testimonials</span>
                <h2 class="section-title">Kata Mereka</h2>
                <p class="section-subtitle">Feedback dari klien yang telah menggunakan jasa kami</p>
            </div>

            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"Pitch deck yang dibuat sangat profesional dan membantu kami closing deal dengan investor. Prosesnya cepat dan komunikasinya sangat baik. Highly recommended!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">AS</div>
                        <div>
                            <div class="author-name">Andi Susanto</div>
                            <div class="author-role">CEO, TechVenture Indonesia</div>
                        </div>
                    </div>
                </div>

                <div class="testimonial-card">
                    <p class="testimonial-text">"Sidang skripsi saya berjalan lancar berkat presentasi yang rapi dan mudah dipahami. Dosen penguji sampai memuji visualisasinya. Worth every rupiah!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">RW</div>
                        <div>
                            <div class="author-name">Rina Wijaya</div>
                            <div class="author-role">Mahasiswa, Universitas Indonesia</div>
                        </div>
                    </div>
                </div>

                <div class="testimonial-card">
                    <p class="testimonial-text">"Sudah 3 kali pakai jasa mereka untuk berbagai kebutuhan presentasi perusahaan. Konsisten kualitasnya dan selalu on-time delivery."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">BP</div>
                        <div>
                            <div class="author-name">Budi Pratama</div>
                            <div class="author-role">Marketing Director, PT Global Sejahtera</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-header">
                <span class="section-tag">Get in Touch</span>
                <h2 class="section-title">Mari Berkolaborasi</h2>
                <p class="section-subtitle">Ready to help your next presentation look sharper, clearer, and more convincing</p>
            </div>

            <div class="contact-grid">
                <div class="contact-info">
                    <h3>Hubungi Kami</h3>
                    <p>Konsultasikan kebutuhan presentasi Anda. Kami siap membantu dari brief hingga delivery.</p>

                    <div class="contact-item">
                        <div class="contact-icon">📱</div>
                        <div>
                            <div class="contact-label">WhatsApp</div>
                            <div class="contact-value">+62 812-3456-7890</div>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">✉️</div>
                        <div>
                            <div class="contact-label">Email</div>
                            <div class="contact-value">hello@slidestudio.id</div>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div>
                            <div class="contact-label">Location</div>
                            <div class="contact-value">Jakarta, Indonesia</div>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">⏰</div>
                        <div>
                            <div class="contact-label">Working Hours</div>
                            <div class="contact-value">Senin - Sabtu, 09:00 - 18:00 WIB</div>
                        </div>
                    </div>

                    <div style="margin-top: 2rem;">
                        <h4 style="margin-bottom: 1rem;">Follow Us</h4>
                        <div style="display: flex; gap: 1rem;">
                            <a href="#" style="width: 45px; height: 45px; background: var(--light); border-radius: 10px; display: flex; align-items: center; justify-content: center; text-decoration: none; font-size: 1.3rem;">📸</a>
                            <a href="#" style="width: 45px; height: 45px; background: var(--light); border-radius: 10px; display: flex; align-items: center; justify-content: center; text-decoration: none; font-size: 1.3rem;">💼</a>
                            <a href="#" style="width: 45px; height: 45px; background: var(--light); border-radius: 10px; display: flex; align-items: center; justify-content: center; text-decoration: none; font-size: 1.3rem;">🐦</a>
                        </div>
                    </div>
                </div>

                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-row">
                            <div class="form-group">
                                <label>Nama Lengkap</label>
                                <input type="text" placeholder="John Doe" required>
                            </div>
                            <div class="form-group">
                                <label>Email</label>
                                <input type="email" placeholder="john@example.com" required>
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label>No. WhatsApp</label>
                                <input type="tel" placeholder="08123456789" required>
                            </div>
                            <div class="form-group">
                                <label>Paket</label>
                                <select required>
                                    <option value="">Pilih Paket</option>
                                    <option value="starter">Starter Deck - Rp1.5jt</option>
                                    <option value="business">Business Deck - Rp3.5jt</option>
                                    <option value="executive">Executive Deck - Rp7.5jt</option>
                                    <option value="academic">Basic Academic - Rp500rb</option>
                                    <option value="thesis">Thesis/Sidang - Rp900rb</option>
                                    <option value="custom">Custom / Konsultasi</option>
                                </select>
                            </div>
                        </div>
                        <div class="form-group">
                            <label>Deadline</label>
                            <input type="date" required>
                        </div>
                        <div class="form-group">
                            <label>Detail Kebutuhan</label>
                            <textarea placeholder="Ceritakan kebutuhan presentasi Anda: tujuan, jumlah slide, konten yang sudah ada, dll..." required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary" style="width: 100%;">Kirim Inquiry</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-brand">
                    <div class="logo">Slide<span>Studio</span></div>
                    <p style="margin-top: 1rem;">Professional presentation design studio untuk corporate, startup, agency, dan akademik. Membuat presentasi Anda lebih tajam, jelas, dan meyakinkan.</p>
                </div>
                <div>
                    <h4 class="footer-title">Services</h4>
                    <ul class="footer-links">
                        <li><a href="#">Pitch Deck</a></li>
                        <li><a href="#">Company Profile</a></li>
                        <li><a href="#">Sales Proposal</a></li>
                        <li><a href="#">Academic Deck</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="footer-title">Quick Links</h4>
                    <ul class="footer-links">
                        <li><a href="#portfolio">Portfolio</a></li>
                        <li><a href="#rates">Rate Card</a></li>
                        <li><a href="#process">Proses</a></li>
                        <li><a href="#contact">Kontak</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="footer-title">Contact</h4>
                    <ul class="footer-links">
                        <li><a href="tel:+6281234567890">+62 812-3456-7890</a></li>
                        <li><a href="mailto:hello@slidestudio.id">hello@slidestudio.id</a></li>
                        <li><a href="#">Jakarta, Indonesia</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>© 2026 SlideStudio. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Portfolio Modal -->
    <div class="modal" id="portfolioModal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal()">×</button>
            <div class="modal-image" id="modalImage"></div>
            <div class="modal-body">
                <h2 class="modal-title" id="modalTitle"></h2>
                <div class="modal-meta" id="modalMeta"></div>
                <p class="modal-desc" id="modalDesc"></p>
            </div>
        </div>
    </div>

    <script>
        // Portfolio Data
        const portfolioData = [
            {
                title: "TechVenture Series A Pitch Deck",
                category: "Investor Pitch",
                client: "TechVenture Indonesia",
                slides: "25 Slides",
                duration: "2 minggu",
                gradient: "linear-gradient(135deg, #667eea 0%, #764ba2 100%)",
                description: "Pitch deck komprehensif untuk startup fintech yang sedang fundraising Series A. Mencakup problem-solution fit, market size analysis, competitive landscape, business model, traction metrics, financial projections, dan team overview. Deck ini berhasil membantu klien mendapatkan funding sebesar $5M dari venture capital ternama."
            },
            {
                title: "Annual Report PT Maju Bersama",
                category: "Corporate",
                client: "PT Maju Bersama",
                slides: "40 Slides",
                duration: "3 minggu",
                gradient: "linear-gradient(135deg, #f093fb 0%, #f5576c 100%)",
                description: "Laporan tahunan untuk RUPS dengan visualisasi data komprehensif meliputi financial highlights, operational performance, sustainability report, dan future outlook. Dikerjakan dalam format bilingual (Indonesia-English) dengan infografis custom dan chart interaktif."
            },
            {
                title: "Agency Credentials Deck",
                category: "Sales Proposal",
                client: "Digital Marketing Agency",
                slides: "30 Slides",
                duration: "10 hari",
                gradient: "linear-gradient(135deg, #4facfe 0%, #00f2fe 100%)",
                description: "Company profile dan credentials deck untuk agency digital marketing yang pitching ke klien enterprise. Menampilkan portfolio showcase, case studies dengan metrics, service offerings, team expertise, dan client testimonials dalam format yang engaging dan premium."
            },
            {
                title: "Thesis Defense - UI Economics",
                category: "Academic",
                client: "Mahasiswa Universitas Indonesia",
                slides: "15 Slides",
                duration: "5 hari",
                gradient: "linear-gradient(135deg, #43e97b 0%, #38f9d7 100%)",
                description: "Presentasi sidang skripsi dengan topik economic policy impact analysis. Menyajikan research background, methodology, data analysis dengan visualisasi statistik yang clear, findings, dan recommendations. Struktur yang memudahkan dosen penguji mengikuti alur penelitian."
            },
            {
                title: "Q4 Strategy Review - FMCG Corp",
                category: "Board Meeting",
                client: "Perusahaan FMCG Multinasional",
                slides: "28 Slides",
                duration: "2 minggu",
                gradient: "linear-gradient(135deg, #fa709a 0%, #fee140 100%)",
                description: "Executive presentation untuk board of directors dengan strategic roadmap dan financial projections. Mencakup Q4 performance review, market analysis, competitive positioning, strategic initiatives, dan 2026 outlook dengan visualisasi data level C-suite."
            },
            {
                title: "Business Case Competition - Winner",
                category: "Competition",
                client: "Tim Mahasiswa",
                slides: "20 Slides",
                duration: "1 minggu",
                gradient: "linear-gradient(135deg, #a8edea 0%, #fed6e3 100%)",
                description: "Deck untuk kompetisi bisnis tingkat nasional yang berhasil meraih juara 1. Menyajikan business problem analysis, proposed solution, implementation plan, financial feasibility, dan impact measurement dengan storytelling yang compelling dan visual yang memorable."
            }
        ];

        // Modal Functions
        function openModal(index) {
            const data = portfolioData[index];
            document.getElementById('modalImage').style.background = data.gradient;
            document.getElementById('modalTitle').textContent = data.title;
            document.getElementById('modalMeta').innerHTML = `
                <span>📁 ${data.category}</span>
                <span>🏢 ${data.client}</span>
                <span>📄 ${data.slides}</span>
                <span>⏱️ ${data.duration}</span>
            `;
            document.getElementById('modalDesc').textContent = data.description;
            document.getElementById('portfolioModal').classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            document.getElementById('portfolioModal').classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        // Close modal on outside click
        document.getElementById('portfolioModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });

        // Close modal on Escape key
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                closeModal();
            }
        });

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
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

        // Scroll Progress Bar
        window.addEventListener('scroll', function() {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.getElementById('scrollProgress').style.width = scrolled + '%';
        });

        // Form Submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Terima kasih! Pesan Anda telah terkirim. Kami akan menghubungi Anda dalam 1x24 jam.');
            this.reset();
        });

        // Navbar Background on Scroll
        window.addEventListener('scroll', function() {
            const nav = document.querySelector('nav');
            if (window.scrollY > 50) {
                nav.style.boxShadow = '0 4px 20px rgba(0,0,0,0.1)';
            } else {
                nav.style.boxShadow = '0 1px 3px rgba(0,0,0,0.1)';
            }
        });

        // Intersection Observer for Animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.portfolio-card, .rate-card, .process-step, .testimonial-card').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
