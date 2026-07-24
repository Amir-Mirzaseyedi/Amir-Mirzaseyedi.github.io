<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Amir Mirzaseyed · Academic Portfolio</title>

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Merriweather:wght@400;700&display=swap" rel="stylesheet" />

    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />

    <style>
        /* ===== RESET & BASE ===== */
        *,
        *::before,
        *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --navy: #0f1a2f;
            --navy-light: #1a2d4a;
            --navy-mid: #2c3e6b;
            --blue-accent: #4a7ab5;
            --blue-soft: #6a9bd5;
            --gray-bg: #f6f8fc;
            --gray-border: #e2e8f0;
            --gray-text: #4a5568;
            --gray-light: #a0aec0;
            --text-dark: #1a202c;
            --white: #ffffff;
            --shadow-sm: 0 2px 8px rgba(15, 26, 47, 0.06);
            --shadow-md: 0 4px 20px rgba(15, 26, 47, 0.08);
            --radius: 12px;
            --radius-sm: 8px;
            --transition: 0.25s ease;
            --font-body: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            --font-heading: 'Merriweather', 'Inter', serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-body);
            background: var(--gray-bg);
            color: var(--text-dark);
            line-height: 1.6;
            padding-top: 0;
        }

        a {
            color: var(--blue-accent);
            text-decoration: none;
            transition: color var(--transition);
        }
        a:hover {
            color: var(--navy-mid);
            text-decoration: underline;
        }

        /* ===== UTILITY ===== */
        .container {
            max-width: 1120px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .section-title {
            font-family: var(--font-heading);
            font-weight: 700;
            font-size: 1.75rem;
            letter-spacing: -0.01em;
            color: var(--navy);
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.6rem;
        }
        .section-title i {
            color: var(--blue-accent);
            font-size: 1.4rem;
            width: 2rem;
        }
        .section-title::after {
            content: '';
            flex: 1;
            height: 2px;
            background: linear-gradient(90deg, var(--blue-accent) 0%, transparent 100%);
            margin-left: 0.75rem;
        }

        .card {
            background: var(--white);
            border-radius: var(--radius);
            box-shadow: var(--shadow-sm);
            padding: 1.5rem 1.75rem;
            transition: box-shadow var(--transition), transform var(--transition);
            border: 1px solid var(--gray-border);
        }
        .card:hover {
            box-shadow: var(--shadow-md);
        }

        .tag {
            display: inline-block;
            background: var(--gray-bg);
            color: var(--navy-mid);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            letter-spacing: 0.02em;
            border: 1px solid var(--gray-border);
        }

        /* ============================================================
                   UNIFIED STICKY HEADER (no stats badges)
                   ============================================================ */
        .header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: var(--navy);
            border-bottom: 3px solid var(--blue-accent);
            box-shadow: 0 4px 20px rgba(15, 26, 47, 0.15);
            padding: 0.5rem 0;
        }

        .header-inner {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 0.5rem 1rem;
        }

        /* Left: Brand (name + title, no stats) */
        .header-brand {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            flex-shrink: 0;
        }
        .header-brand .initials {
            width: 44px;
            height: 44px;
            border-radius: 50%;
            background: var(--blue-accent);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.1rem;
            flex-shrink: 0;
            letter-spacing: 0.04em;
            box-shadow: 0 2px 8px rgba(74, 122, 181, 0.3);
        }
        .header-brand .name-title {
            display: flex;
            flex-direction: column;
            line-height: 1.3;
        }
        .header-brand .name-title .name {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--white);
            letter-spacing: 0.01em;
        }
        .header-brand .name-title .title {
            font-weight: 400;
            font-size: 0.75rem;
            color: rgba(255, 255, 255, 0.6);
            letter-spacing: 0.03em;
        }

        /* Center: Contact + mini interests */
        .header-meta {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
            gap: 0.4rem 1rem;
            flex: 1 1 auto;
            justify-content: center;
            padding: 0 0.5rem;
        }
        .header-meta .contact-item {
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.8rem;
            transition: color var(--transition);
            white-space: nowrap;
        }
        .header-meta .contact-item i {
            font-size: 0.8rem;
            color: var(--blue-soft);
            width: 1rem;
            text-align: center;
        }
        .header-meta .contact-item:hover {
            color: var(--white);
            text-decoration: none;
        }
        .header-meta .divider {
            color: rgba(255, 255, 255, 0.15);
            font-weight: 300;
        }
        .header-meta .interests-tags {
            display: inline-flex;
            flex-wrap: wrap;
            gap: 0.3rem 0.5rem;
        }
        .header-meta .interests-tags .mini-tag {
            font-size: 0.6rem;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.5);
            background: rgba(255, 255, 255, 0.06);
            padding: 0.1rem 0.6rem;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            letter-spacing: 0.02em;
            white-space: nowrap;
            transition: background var(--transition), color var(--transition);
        }
        .header-meta .interests-tags .mini-tag:hover {
            background: rgba(255, 255, 255, 0.12);
            color: var(--white);
        }

        /* Right: Navigation */
        .header-nav {
            display: flex;
            align-items: center;
            gap: 0.2rem;
            flex-shrink: 0;
        }
        .header-nav a {
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.8rem;
            font-weight: 500;
            padding: 0.3rem 0.8rem;
            border-radius: 4px;
            transition: background var(--transition), color var(--transition);
            position: relative;
            letter-spacing: 0.02em;
        }
        .header-nav a:hover,
        .header-nav a.active {
            color: var(--white);
            background: rgba(255, 255, 255, 0.08);
            text-decoration: none;
        }
        .header-nav a.active {
            background: rgba(74, 122, 181, 0.25);
            color: var(--white);
        }

        .nav-toggle {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.3rem;
            cursor: pointer;
            padding: 0.2rem 0.6rem;
            margin-left: 0.2rem;
        }

        /* Desktop nav links (hidden on mobile via media query) */
        .nav-links-desktop {
            display: flex;
            gap: 0.2rem;
            align-items: center;
        }

        /* ===== SECTIONS ===== */
        section {
            padding: 3rem 0;
        }
        section:nth-child(even) {
            background: var(--white);
        }
        section:nth-child(odd) {
            background: var(--gray-bg);
        }

        /* ===== RESEARCH INTERESTS ===== */
        .interests-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem 1.2rem;
        }
        .interests-grid .interest-item {
            background: var(--white);
            border: 1px solid var(--gray-border);
            border-radius: 40px;
            padding: 0.45rem 1.2rem;
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--navy-mid);
            box-shadow: var(--shadow-sm);
            transition: background var(--transition), color var(--transition), border-color var(--transition);
        }
        .interests-grid .interest-item:hover {
            background: var(--navy);
            color: var(--white);
            border-color: var(--navy);
        }

        /* ===== EDUCATION ===== */
        .edu-item {
            display: flex;
            flex-direction: column;
            gap: 0.3rem;
        }
        .edu-item+.edu-item {
            margin-top: 1.75rem;
            padding-top: 1.75rem;
            border-top: 1px solid var(--gray-border);
        }
        .edu-item .edu-head {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.5rem 1rem;
        }
        .edu-item .edu-head .degree {
            font-weight: 700;
            font-size: 1.1rem;
            color: var(--navy);
        }
        .edu-item .edu-head .institution {
            font-weight: 500;
            color: var(--gray-text);
        }
        .edu-item .edu-meta {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem 1.5rem;
            font-size: 0.9rem;
            color: var(--gray-text);
        }
        .edu-item .edu-meta .gpa {
            font-weight: 600;
            color: var(--navy-mid);
        }
        .edu-item .edu-thesis {
            margin-top: 0.3rem;
            font-size: 0.95rem;
            color: var(--gray-text);
            background: var(--gray-bg);
            padding: 0.6rem 1rem;
            border-radius: var(--radius-sm);
            border-left: 3px solid var(--blue-accent);
        }
        .edu-item .edu-thesis strong {
            color: var(--text-dark);
        }

        /* ===== EXPERIENCE ===== */
        .exp-item {
            display: flex;
            flex-direction: column;
            gap: 0.2rem;
        }
        .exp-item+.exp-item {
            margin-top: 1.5rem;
            padding-top: 1.5rem;
            border-top: 1px solid var(--gray-border);
        }
        .exp-item .exp-head {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.3rem 1rem;
        }
        .exp-item .exp-head .role {
            font-weight: 700;
            color: var(--navy);
        }
        .exp-item .exp-head .company {
            font-weight: 500;
            color: var(--gray-text);
        }
        .exp-item .exp-desc {
            font-size: 0.95rem;
            color: var(--gray-text);
            margin-top: 0.2rem;
            padding-left: 0.2rem;
        }
        .exp-item .exp-desc ul {
            list-style: none;
            padding: 0;
            margin: 0.2rem 0 0;
        }
        .exp-item .exp-desc ul li {
            position: relative;
            padding-left: 1.2rem;
            margin-bottom: 0.15rem;
        }
        .exp-item .exp-desc ul li::before {
            content: '›';
            position: absolute;
            left: 0;
            color: var(--blue-accent);
            font-weight: 700;
        }

        /* ===== RESEARCH PROJECTS ===== */
        .research-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }
        .research-card {
            display: flex;
            flex-direction: column;
            gap: 0.4rem;
        }
        .research-card .rc-title {
            font-weight: 700;
            font-size: 1rem;
            color: var(--navy);
            line-height: 1.4;
        }
        .research-card .rc-title a {
            color: inherit;
            text-decoration: none;
        }
        .research-card .rc-title a:hover {
            color: var(--blue-accent);
            text-decoration: underline;
        }
        .research-card .rc-meta {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem 0.8rem;
            font-size: 0.8rem;
            color: var(--gray-text);
        }
        .research-card .rc-meta .rc-role {
            font-weight: 500;
            color: var(--navy-mid);
        }
        .research-card .rc-tools {
            font-size: 0.85rem;
            color: var(--gray-text);
        }
        .research-card .rc-tools strong {
            color: var(--text-dark);
            font-weight: 600;
        }
        .research-card .rc-outcome {
            font-size: 0.9rem;
            color: var(--gray-text);
            margin-top: 0.1rem;
            padding: 0.4rem 0.8rem;
            background: var(--gray-bg);
            border-radius: var(--radius-sm);
            border-left: 3px solid var(--blue-accent);
        }

        /* ===== SKILLS ===== */
        .skills-wrapper {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem 2rem;
        }
        .skills-group h4 {
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--navy-mid);
            text-transform: uppercase;
            letter-spacing: 0.04em;
            margin-bottom: 0.5rem;
            border-bottom: 1px solid var(--gray-border);
            padding-bottom: 0.3rem;
        }
        .skills-group .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem 0.7rem;
        }
        .skills-group .skill-tags span {
            background: var(--white);
            border: 1px solid var(--gray-border);
            border-radius: 20px;
            padding: 0.2rem 0.9rem;
            font-size: 0.85rem;
            color: var(--text-dark);
            font-weight: 500;
            transition: background var(--transition), color var(--transition), border-color var(--transition);
        }
        .skills-group .skill-tags span:hover {
            background: var(--navy);
            color: var(--white);
            border-color: var(--navy);
        }

        /* ===== LANGUAGES ===== */
        .lang-list {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem 2.5rem;
        }
        .lang-list .lang-item {
            display: flex;
            align-items: baseline;
            gap: 0.5rem;
            font-size: 1rem;
        }
        .lang-list .lang-item .lang-name {
            font-weight: 600;
            color: var(--navy);
        }
        .lang-list .lang-item .lang-level {
            color: var(--gray-text);
            font-size: 0.9rem;
        }

        /* ===== HONORS ===== */
        .honors-list {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
        .honor-item {
            display: flex;
            gap: 1rem;
            align-items: flex-start;
            padding: 0.75rem 1rem;
            background: var(--white);
            border-radius: var(--radius-sm);
            border: 1px solid var(--gray-border);
            transition: border-color var(--transition);
        }
        .honor-item:hover {
            border-color: var(--blue-accent);
        }
        .honor-item .honor-year {
            font-weight: 700;
            color: var(--blue-accent);
            font-size: 1rem;
            min-width: 3.2rem;
            flex-shrink: 0;
        }
        .honor-item .honor-desc {
            font-size: 0.95rem;
            color: var(--text-dark);
        }

        /* ===== FOOTER ===== */
        .footer {
            background: var(--navy);
            color: rgba(255, 255, 255, 0.6);
            padding: 2rem 0;
            text-align: center;
            border-top: 2px solid var(--blue-accent);
        }
        .footer .container {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }
        .footer p {
            font-size: 0.9rem;
            margin: 0;
        }
        .footer .footer-ref {
            font-size: 0.85rem;
            opacity: 0.7;
            font-style: italic;
        }
        .footer .footer-social {
            display: flex;
            justify-content: center;
            gap: 1.2rem;
            margin-top: 0.3rem;
        }
        .footer .footer-social a {
            color: rgba(255, 255, 255, 0.5);
            font-size: 1.2rem;
            transition: color var(--transition);
        }
        .footer .footer-social a:hover {
            color: var(--white);
            text-decoration: none;
        }

        /* ============================================================
                   RESPONSIVE
                   ============================================================ */
        @media (max-width: 992px) {
            .research-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 820px) {
            .header {
                padding: 0.4rem 0;
            }
            .header-inner {
                flex-wrap: wrap;
                gap: 0.3rem 0.5rem;
            }

            .header-brand .initials {
                width: 36px;
                height: 36px;
                font-size: 0.9rem;
            }
            .header-brand .name-title .name {
                font-size: 1rem;
            }
            .header-brand .name-title .title {
                font-size: 0.65rem;
            }

            .header-meta {
                order: 3;
                flex: 1 1 100%;
                justify-content: flex-start;
                padding: 0.3rem 0 0 0;
                border-top: 1px solid rgba(255, 255, 255, 0.06);
                margin-top: 0.2rem;
                gap: 0.3rem 0.8rem;
            }
            .header-meta .contact-item {
                font-size: 0.7rem;
            }
            .header-meta .interests-tags .mini-tag {
                font-size: 0.55rem;
                padding: 0.05rem 0.5rem;
            }
            .header-meta .divider {
                display: none;
            }

            .header-nav {
                flex: 0 1 auto;
            }
            .header-nav .nav-links-desktop {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 100%;
                right: 0;
                background: var(--navy);
                padding: 0.5rem 1rem;
                border-radius: 0 0 var(--radius-sm) var(--radius-sm);
                box-shadow: var(--shadow-md);
                min-width: 160px;
                border-top: 2px solid var(--blue-accent);
                gap: 0;
            }
            .header-nav .nav-links-desktop.open {
                display: flex;
            }
            .header-nav .nav-links-desktop a {
                padding: 0.4rem 0.6rem;
                font-size: 0.8rem;
                border-radius: 0;
            }
            .nav-toggle {
                display: block;
            }
        }

        @media (max-width: 480px) {
            .header-brand .initials {
                width: 30px;
                height: 30px;
                font-size: 0.75rem;
            }
            .header-brand .name-title .name {
                font-size: 0.85rem;
            }
            .header-brand .name-title .title {
                font-size: 0.55rem;
            }
            .header-meta .contact-item {
                font-size: 0.65rem;
            }
            .header-meta .interests-tags .mini-tag {
                font-size: 0.5rem;
                padding: 0.05rem 0.4rem;
            }
            .container {
                padding: 0 12px;
            }
            .card {
                padding: 1rem 1rem;
            }
            .section-title {
                font-size: 1.4rem;
            }
        }

        @media (min-width: 821px) {
            .nav-toggle {
                display: none !important;
            }
            .header-nav .nav-links-desktop {
                display: flex !important;
                position: static;
                background: transparent;
                box-shadow: none;
                border: none;
                padding: 0;
                flex-direction: row;
                gap: 0.2rem;
                min-width: auto;
            }
            .header-nav .nav-links-desktop a {
                padding: 0.3rem 0.8rem;
                border-radius: 4px;
            }
        }
    </style>
</head>
<body>

    <!-- ============================================================
    UNIFIED STICKY HEADER (without GPA / Top 0.5% badges)
    ============================================================ -->
    <header class="header" id="header">
        <div class="container">
            <div class="header-inner">

                <!-- Left: Brand (name + title only) -->
                <div class="header-brand">
                    <span class="initials">AM</span>
                    <div class="name-title">
                        <span class="name">Amir Mirzaseyed</span>
                        <span class="title">Industrial Management · Quality &amp; Productivity</span>
                    </div>
                </div>

                <!-- Center: Contact + Mini Interests -->
                <div class="header-meta">
                    <a href="mailto:samirzaseyedi@ut.ac.ir" class="contact-item" aria-label="Email">
                        <i class="fas fa-envelope"></i> Email
                    </a>
                    <span class="divider">|</span>
                    <a href="https://www.linkedin.com/in/amir-mirzaseyedi" target="_blank" rel="noopener" class="contact-item" aria-label="LinkedIn">
                        <i class="fab fa-linkedin-in"></i> LinkedIn
                    </a>
                    <span class="divider">|</span>
                    <div class="interests-tags">
                        <span class="mini-tag">AI Adoption</span>
                        <span class="mini-tag">GenAI</span>
                        <span class="mini-tag">ESG</span>
                        <span class="mini-tag">Digital Transformation</span>
                    </div>
                </div>

                <!-- Right: Navigation -->
                <div class="header-nav">
                    <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
                        <i class="fas fa-bars"></i>
                    </button>
                    <nav class="nav-links-desktop" id="navLinks">
                        <a href="#interests" class="active">Interests</a>
                        <a href="#education">Education</a>
                        <a href="#experience">Experience</a>
                        <a href="#research">Research</a>
                        <a href="#skills">Skills</a>
                        <a href="#honors">Honors</a>
                    </nav>
                </div>

            </div>
        </div>
    </header>

    <!-- ===== RESEARCH INTERESTS ===== -->
    <section id="interests">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-lightbulb"></i> Research Interests</h2>
            <div class="interests-grid">
                <span class="interest-item">AI Adoption &amp; Governance in Organizations</span>
                <span class="interest-item">Generative AI &amp; Human–AI Collaboration in Decision-Making</span>
                <span class="interest-item">Sustainable Operations &amp; ESG Integration</span>
                <span class="interest-item">Digital Transformation &amp; Emerging Technology Strategy</span>
                <span class="interest-item">Explainable AI (XAI) &amp; Trust in Automated Systems</span>
            </div>
        </div>
    </section>

    <!-- ===== EDUCATION ===== -->
    <section id="education">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Education</h2>

            <div class="card">
                <div class="edu-item">
                    <div class="edu-head">
                        <span class="degree">M.Sc. in Industrial Management</span>
                        <span class="institution">University of Tehran</span>
                    </div>
                    <div class="edu-meta">
                        <span><i class="far fa-calendar-alt"></i> 2024 – 2026</span>
                        <span class="gpa"><i class="fas fa-star"></i> GPA: 19.42 / 20</span>
                        <span><span class="tag">Quality &amp; Productivity Management</span></span>
                    </div>
                    <div class="edu-thesis">
                        <strong>Thesis:</strong> “AI Adoption in Quality of Banking Services: A Capability–Attractiveness Assessment” — applied BWM and TOPSIS to evaluate and rank AI applications for banking service quality using expert panel data. <em>(Supervisor: Dr. Rohollah Ghasemi)</em>
                    </div>
                </div>

                <div class="edu-item" style="margin-top:1.75rem; padding-top:1.75rem; border-top:1px solid var(--gray-border);">
                    <div class="edu-head">
                        <span class="degree">B.Sc. in Industrial Management</span>
                        <span class="institution">University of Tehran</span>
                    </div>
                    <div class="edu-meta">
                        <span><i class="far fa-calendar-alt"></i> 2020 – 2024</span>
                        <span class="gpa"><i class="fas fa-star"></i> GPA: 18.62 / 20</span>
                    </div>
                    <div class="edu-thesis">
                        <strong>Thesis:</strong> “Satellite Internet Systems and Emerging Applications: A Comprehensive Overview” <em>(Supervisor: Dr. Rohollah Ghasemi)</em>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== WORK EXPERIENCE ===== -->
    <section id="experience">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-briefcase"></i> Work Experience</h2>

            <div class="card">
                <div class="exp-item">
                    <div class="exp-head">
                        <span class="role">Teaching Assistant — Total Quality Management</span>
                        <span class="company">University of Tehran</span>
                    </div>
                    <div class="exp-meta" style="font-size:0.85rem; color:var(--gray-text); margin-bottom:0.2rem;">
                        <span><i class="far fa-calendar-alt"></i> Oct 2023 – Jan 2024</span>
                    </div>
                    <div class="exp-desc">
                        Supported course delivery and student evaluation for TQM, reinforcing the quality-management specialization carried into graduate research.
                    </div>
                </div>

                <div class="exp-item">
                    <div class="exp-head">
                        <span class="role">Finance Department Intern</span>
                        <span class="company">Karan Polymer Part, Tehran, Iran</span>
                    </div>
                    <div class="exp-meta" style="font-size:0.85rem; color:var(--gray-text); margin-bottom:0.2rem;">
                        <span><i class="far fa-calendar-alt"></i> Jul 2023 – Sep 2023</span>
                    </div>
                    <div class="exp-desc">
                        <ul>
                            <li>Worked with: ERP invoice entry, bookkeeping records, purchasing / vendor documentation.</li>
                            <li>Learned: practical financial data workflows and how finance–procurement coordination functions in a manufacturing company.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== RESEARCH PROJECTS ===== -->
    <section id="research">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-flask"></i> Research</h2>

            <div class="research-grid">

                <!-- 1 -->
                <div class="card research-card">
                    <div class="rc-title">A Sustainable Framework for Evaluating the Attractiveness of AI in Banking: Insights from the Best-Worst Method</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Apr 2026 – Jul 2026</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Lead Researcher &amp; First Author</span>
                        <span class="tag">Submitted to ICISE 2026</span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> PRISMA-ScR scoping review, Best-Worst Method (6-expert panel), Triple Bottom Line framework</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> built and validated a TBL-based weighting model — deepened command of hierarchical MCDM design and expert-panel consistency validation (CR, Kendall's W).</div>
                </div>

                <!-- 2 -->
                <div class="card research-card">
                    <div class="rc-title">A Strategic Roadmap for Banking Digitalization: Extracting Tech Trends and Prioritizing Investment Portfolios</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Apr 2026 – Jul 2026</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Lead Researcher &amp; First Author</span>
                        <span class="tag">Submitted to ICISE 2026</span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> PRISMA-ScR scoping review, hybrid BWM–Weighted Sum Model (10-expert panel)</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> produced a ranked technology-investment roadmap — strengthened skills in combining two-stage MCDM methods for practical decision support.</div>
                </div>

                <!-- 3 -->
                <div class="card research-card">
                    <div class="rc-title">Capability-Attractiveness Analysis of AI Technology Applications in Banking Service Quality</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Mar 2026 – Sep 2026</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Lead Researcher &amp; First Author</span>
                        <span class="tag">Submitted to <em>Journal of Decisions and Operations Research</em></span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> BWM, TOPSIS, expert panel data collection</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> led a full research cycle end-to-end and gained hands-on command of MCDM modeling for real-world technology prioritization.</div>
                </div>

                <!-- 4 -->
                <div class="card research-card">
                    <div class="rc-title">Service Quality in Smart Banking: A Meta-Synthesis of Industry 4.0 Technologies and Applications</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Jan 2026 – Apr 2026</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Graduate Researcher, Second Author</span>
                        <span class="tag">Submitted to <em>Industrial Management Journal</em></span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> Sandelowski &amp; Barroso 7-step meta-synthesis method</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> built rigor in qualitative research design and systematic literature synthesis.</div>
                </div>

                <!-- 5 -->
                <div class="card research-card">
                    <div class="rc-title">Strategic Renewal in Organizations: A Systematic Review, Conceptual Integration, and a Practical Framework</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Sep 2025 – Jan 2026</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Student Researcher</span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> Systematic review methodology, concept-centric synthesis of 25 studies</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> strengthened ability to distill scattered literature into a coherent conceptual framework.</div>
                </div>

                <!-- 6 -->
                <div class="card research-card">
                    <div class="rc-title">Analysis and Implementation Framework of ISO 27001 for Information Security Management</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Apr 2025 – Jun 2025</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Student Researcher</span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> ISO 27001 standard analysis (controls, ISMS structure)</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> gained working knowledge of information security management standards and certification processes.</div>
                </div>

                <!-- 7 -->
                <div class="card research-card">
                    <div class="rc-title">EFQM Excellence Model Implementation for Sales Department</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Feb 2025 – Jun 2025</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Research Team Member</span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> EFQM Excellence Model</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> learned to apply a quality-management framework in a real organizational setting through team-based fieldwork.</div>
                </div>

                <!-- 8 -->
                <div class="card research-card">
                    <div class="rc-title">Analysis of Wearable User Interfaces: Applications, Challenges, and Strategic Implications</div>
                    <div class="rc-meta">
                        <span><i class="far fa-calendar-alt"></i> Sep 2024 – Jan 2025</span>
                        <span class="rc-role"><i class="fas fa-user"></i> Student Researcher</span>
                    </div>
                    <div class="rc-tools"><strong>Tools:</strong> Cross-industry technology impact analysis</div>
                    <div class="rc-outcome"><strong>Outcome:</strong> developed early skill in evaluating emerging technologies and their strategic implications.</div>
                </div>

            </div><!-- /research-grid -->
        </div>
    </section>

    <!-- ===== SKILLS ===== -->
    <section id="skills">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-cogs"></i> Skills</h2>

            <div class="card">
                <div class="skills-wrapper">
                    <div class="skills-group">
                        <h4>Software &amp; Tools</h4>
                        <div class="skill-tags">
                            <span>Python</span>
                            <span>R</span>
                            <span>Minitab</span>
                            <span>Tableau</span>
                            <span>Lingo</span>
                            <span>QM</span>
                        </div>
                    </div>
                    <div class="skills-group">
                        <h4>Methods &amp; Techniques</h4>
                        <div class="skill-tags">
                            <span>Lean Six Sigma</span>
                            <span>Total Quality Management</span>
                            <span>Statistical Process Control</span>
                            <span>Operational Research &amp; Optimization Modeling</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== LANGUAGES ===== -->
    <section id="languages" style="background:var(--white);">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-language"></i> Language Proficiency</h2>
            <div class="card">
                <div class="lang-list">
                    <div class="lang-item"><span class="lang-name">Persian</span> <span class="lang-level">· Native</span></div>
                    <div class="lang-item"><span class="lang-name">English</span> <span class="lang-level">· Professional</span></div>
                    <div class="lang-item"><span class="lang-name">French</span> <span class="lang-level">· Basic</span></div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== HONORS & AWARDS ===== -->
    <section id="honors">
        <div class="container">
            <h2 class="section-title"><i class="fas fa-trophy"></i> Honors &amp; Awards</h2>

            <div class="honors-list">
                <div class="honor-item">
                    <span class="honor-year">2024</span>
                    <span class="honor-desc">Received honorary direct admission to the graduate school (M.Sc.) of the Industrial Management Department, University of Tehran, without taking the national entrance exam for graduate schools, in recognition of high academic records and achievements.</span>
                </div>
                <div class="honor-item">
                    <span class="honor-year">2024</span>
                    <span class="honor-desc">Ranked 4th in Cumulative GPA among all undergraduate students in Industrial Management; recognized as Outstanding Student by the university.</span>
                </div>
                <div class="honor-item">
                    <span class="honor-year">2020</span>
                    <span class="honor-desc">Ranked in the top 0.5% in the Nation-wide University Entry Exam among 595,000 Iranian students; recognized as Outstanding Student.</span>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2026 Amir Mirzaseyed · Industrial Management, University of Tehran</p>
            <p class="footer-ref">References and academic records available upon request.</p>
            <div class="footer-social">
                <a href="mailto:samirzaseyedi@ut.ac.ir" aria-label="Email"><i class="fas fa-envelope"></i></a>
                <a href="https://www.linkedin.com/in/amir-mirzaseyedi" target="_blank" rel="noopener" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" aria-label="Google Scholar" style="opacity:0.5; cursor:default;"><i class="fas fa-graduation-cap"></i></a>
            </div>
        </div>
    </footer>

    <!-- ============================================================
    SCRIPT: mobile nav toggle + active link highlight
    ============================================================ -->
    <script>
        (function() {
            'use strict';

            const toggle = document.getElementById('navToggle');
            const nav = document.getElementById('navLinks');

            if (toggle && nav) {
                toggle.addEventListener('click', function(e) {
                    e.stopPropagation();
                    nav.classList.toggle('open');
                    const icon = toggle.querySelector('i');
                    if (nav.classList.contains('open')) {
                        icon.className = 'fas fa-times';
                    } else {
                        icon.className = 'fas fa-bars';
                    }
                });

                nav.querySelectorAll('a').forEach(function(link) {
                    link.addEventListener('click', function() {
                        nav.classList.remove('open');
                        const icon = toggle.querySelector('i');
                        if (icon) icon.className = 'fas fa-bars';
                    });
                });

                document.addEventListener('click', function(e) {
                    if (!e.target.closest('.header') && nav.classList.contains('open')) {
                        nav.classList.remove('open');
                        const icon = toggle.querySelector('i');
                        if (icon) icon.className = 'fas fa-bars';
                    }
                });
            }

            // Active link highlight on scroll
            const sections = document.querySelectorAll('section[id]');
            const navLinks = document.querySelectorAll('.nav-links-desktop a');

            function updateActiveLink() {
                let current = '';
                const scrollPos = window.scrollY + 120;

                sections.forEach(function(section) {
                    const top = section.offsetTop;
                    const height = section.offsetHeight;
                    if (scrollPos >= top && scrollPos < top + height) {
                        current = section.getAttribute('id');
                    }
                });

                navLinks.forEach(function(link) {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === '#' + current) {
                        link.classList.add('active');
                    }
                });
            }

            window.addEventListener('scroll', updateActiveLink);
            window.addEventListener('load', updateActiveLink);

            // Smooth scroll
            navLinks.forEach(function(link) {
                link.addEventListener('click', function(e) {
                    const targetId = link.getAttribute('href');
                    if (targetId && targetId.startsWith('#')) {
                        const target = document.querySelector(targetId);
                        if (target) {
                            e.preventDefault();
                            const offset = 80;
                            const top = target.offsetTop - offset;
                            window.scrollTo({ top: top, behavior: 'smooth' });
                            history.pushState(null, null, targetId);
                        }
                    }
                });
            });

        })();
    </script>

</body>
</html>
