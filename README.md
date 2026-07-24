<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Amir Mirzaseyed · Academic Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet" />
    <style>
        /* ---------- RESET & BASE ---------- */
        *,
        *::before,
        *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --navy: #0f1a2e;
            --navy-light: #1a2d4a;
            --navy-mid: #2c3e7a;
            --gray-light: #f5f7fa;
            --gray-mid: #e6e9f0;
            --gray-text: #4a5568;
            --gray-border: #d1d7e3;
            --white: #ffffff;
            --shadow: 0 4px 20px rgba(15, 26, 46, 0.08);
            --radius: 12px;
            --transition: 0.25s ease;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: var(--gray-light);
            color: #1a202c;
            line-height: 1.6;
            font-size: 16px;
            -webkit-font-smoothing: antialiased;
        }

        a {
            color: var(--navy-mid);
            text-decoration: none;
            transition: color var(--transition);
        }
        a:hover {
            color: var(--navy);
            text-decoration: underline;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* ---------- NAVIGATION ---------- */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: rgba(15, 26, 46, 0.92);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            transition: background var(--transition);
        }

        .navbar .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 64px;
        }

        .navbar-brand {
            font-weight: 600;
            font-size: 1.1rem;
            color: #fff;
            letter-spacing: 0.3px;
        }
        .navbar-brand span {
            color: #8aa4d8;
        }

        .nav-links {
            display: flex;
            gap: 28px;
            list-style: none;
            font-size: 0.875rem;
            font-weight: 500;
        }
        .nav-links a {
            color: rgba(255, 255, 255, 0.7);
            transition: color var(--transition);
            position: relative;
        }
        .nav-links a::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -4px;
            width: 0;
            height: 2px;
            background: #8aa4d8;
            transition: width var(--transition);
        }
        .nav-links a:hover {
            color: #fff;
            text-decoration: none;
        }
        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            background: none;
            border: none;
            cursor: pointer;
            padding: 4px;
        }
        .nav-toggle span {
            display: block;
            width: 26px;
            height: 2.5px;
            background: #fff;
            border-radius: 2px;
            transition: var(--transition);
            transform-origin: center;
        }

        /* ---------- HERO ---------- */
        .hero {
            padding: 120px 0 64px;
            background: var(--navy);
            color: #fff;
            position: relative;
            overflow: hidden;
        }
        .hero::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 60px;
            background: var(--gray-light);
            border-radius: 50% 50% 0 0 / 100% 100% 0 0;
            transform: scaleX(1.05);
        }

        .hero .container {
            position: relative;
            z-index: 2;
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            align-items: flex-start;
        }

        .hero-avatar {
            flex: 0 0 140px;
        }
        .hero-avatar img {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
            background: var(--gray-mid);
        }
        .hero-avatar .initials-fallback {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            background: var(--navy-mid);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.2rem;
            font-weight: 600;
            color: #fff;
            border: 3px solid rgba(255, 255, 255, 0.15);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.25);
        }

        .hero-content {
            flex: 1;
            min-width: 240px;
        }
        .hero-content h1 {
            font-size: 2.4rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            margin-bottom: 6px;
            line-height: 1.2;
        }
        .hero-content .subhead {
            font-size: 1.1rem;
            font-weight: 400;
            color: rgba(255, 255, 255, 0.75);
            margin-bottom: 16px;
        }
        .hero-contact {
            display: flex;
            flex-wrap: wrap;
            gap: 12px 24px;
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 18px;
        }
        .hero-contact a {
            color: rgba(255, 255, 255, 0.85);
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }
        .hero-contact a:hover {
            color: #fff;
            text-decoration: none;
        }
        .hero-contact .icon {
            display: inline-block;
            width: 18px;
            text-align: center;
            font-size: 1rem;
        }

        .hero-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px 10px;
            margin-top: 6px;
        }
        .hero-tags .tag {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.12);
            padding: 4px 14px;
            border-radius: 40px;
            font-size: 0.78rem;
            font-weight: 400;
            color: rgba(255, 255, 255, 0.85);
            letter-spacing: 0.2px;
        }

        /* ---------- SECTION COMMON ---------- */
        section {
            padding: 56px 0 48px;
        }
        section:nth-child(even) {
            background: var(--white);
        }

        .section-title {
            font-size: 1.6rem;
            font-weight: 600;
            color: var(--navy);
            letter-spacing: -0.3px;
            margin-bottom: 28px;
            padding-bottom: 10px;
            border-bottom: 3px solid var(--gray-mid);
            position: relative;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 60px;
            height: 3px;
            background: var(--navy-mid);
            border-radius: 2px;
        }

        .card {
            background: var(--white);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            padding: 24px 28px;
            margin-bottom: 20px;
            border: 1px solid var(--gray-border);
            transition: box-shadow var(--transition);
        }
        .card:hover {
            box-shadow: 0 8px 30px rgba(15, 26, 46, 0.12);
        }

        .card-title {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--navy);
            margin-bottom: 2px;
        }
        .card-sub {
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--navy-mid);
            margin-bottom: 2px;
        }
        .card-meta {
            font-size: 0.8rem;
            color: var(--gray-text);
            margin-bottom: 8px;
        }
        .card-body {
            font-size: 0.92rem;
            color: #2d3748;
        }
        .card-body ul {
            list-style: none;
            padding-left: 0;
        }
        .card-body ul li {
            padding-left: 18px;
            position: relative;
            margin-bottom: 4px;
        }
        .card-body ul li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--navy-mid);
            font-weight: 600;
        }
        .card-body .highlight {
            font-weight: 500;
            color: var(--navy);
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        /* ---------- RESEARCH INTERESTS ---------- */
        .interests-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 10px 14px;
        }
        .interests-grid .pill {
            background: var(--gray-light);
            border: 1px solid var(--gray-border);
            padding: 6px 20px;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            color: var(--navy);
            transition: all var(--transition);
        }
        .interests-grid .pill:hover {
            background: var(--navy);
            color: #fff;
            border-color: var(--navy);
            transform: translateY(-2px);
        }

        /* ---------- SKILLS ---------- */
        .skills-wrap {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
        }
        .skills-wrap .skill-group h4 {
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--navy);
            margin-bottom: 8px;
            letter-spacing: 0.3px;
        }
        .skills-wrap .skill-group .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 6px 10px;
        }
        .skills-wrap .skill-group .tags span {
            background: var(--gray-light);
            border: 1px solid var(--gray-border);
            padding: 2px 14px;
            border-radius: 30px;
            font-size: 0.78rem;
            color: var(--gray-text);
        }

        /* ---------- LANGUAGES ---------- */
        .lang-list {
            display: flex;
            flex-wrap: wrap;
            gap: 16px 40px;
        }
        .lang-list .lang-item {
            font-size: 0.95rem;
            font-weight: 500;
            color: var(--navy);
        }
        .lang-list .lang-item .level {
            font-weight: 400;
            color: var(--gray-text);
            font-size: 0.85rem;
            margin-left: 6px;
        }

        /* ---------- HONORS ---------- */
        .honor-item {
            display: flex;
            gap: 16px;
            padding: 14px 0;
            border-bottom: 1px solid var(--gray-mid);
        }
        .honor-item:last-child {
            border-bottom: none;
        }
        .honor-year {
            flex: 0 0 56px;
            font-weight: 700;
            font-size: 1rem;
            color: var(--navy-mid);
        }
        .honor-desc {
            flex: 1;
            font-size: 0.92rem;
            color: #2d3748;
        }

        /* ---------- FOOTER ---------- */
        .footer {
            background: var(--navy);
            color: rgba(255, 255, 255, 0.6);
            padding: 32px 0 28px;
            text-align: center;
            font-size: 0.85rem;
            border-top: 1px solid rgba(255, 255, 255, 0.06);
        }
        .footer a {
            color: rgba(255, 255, 255, 0.7);
        }
        .footer a:hover {
            color: #fff;
            text-decoration: none;
        }
        .footer .sep {
            margin: 0 8px;
            opacity: 0.3;
        }

        /* ---------- RESPONSIVE ---------- */
        @media (max-width: 820px) {
            .hero .container {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }
            .hero-avatar {
                flex: 0 0 auto;
            }
            .hero-content h1 {
                font-size: 1.9rem;
            }
            .hero-contact {
                justify-content: center;
            }
            .hero-tags {
                justify-content: center;
            }

            .grid-2 {
                grid-template-columns: 1fr;
            }

            .skills-wrap {
                grid-template-columns: 1fr;
                gap: 16px;
            }

            .section-title {
                font-size: 1.3rem;
            }
            .section-title::after {
                width: 40px;
            }

            .card {
                padding: 18px 20px;
            }

            .nav-links {
                position: absolute;
                top: 64px;
                left: 0;
                right: 0;
                background: rgba(15, 26, 46, 0.97);
                backdrop-filter: blur(12px);
                flex-direction: column;
                align-items: center;
                padding: 20px 0 28px;
                gap: 16px;
                border-bottom: 1px solid rgba(255, 255, 255, 0.06);
                transform: translateY(-120%);
                transition: transform 0.3s ease;
                opacity: 0;
                pointer-events: none;
            }
            .nav-links.open {
                transform: translateY(0);
                opacity: 1;
                pointer-events: auto;
            }

            .nav-toggle {
                display: flex;
            }

            .hero-avatar img,
            .hero-avatar .initials-fallback {
                width: 110px;
                height: 110px;
                font-size: 2.6rem;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 16px;
            }
            .hero {
                padding: 100px 0 48px;
            }
            .hero-content h1 {
                font-size: 1.6rem;
            }
            .hero-content .subhead {
                font-size: 0.95rem;
            }
            .hero-contact {
                font-size: 0.8rem;
                gap: 8px 16px;
            }
            .card {
                padding: 16px;
            }
            .honor-item {
                flex-direction: column;
                gap: 4px;
            }
            .honor-year {
                flex: 0 0 auto;
            }
            section {
                padding: 40px 0 32px;
            }
        }

        /* ---------- UTILITY ---------- */
        .mt-1 {
            margin-top: 6px;
        }
        .mb-1 {
            margin-bottom: 6px;
        }
        .text-muted {
            color: var(--gray-text);
            font-size: 0.85rem;
        }
        .text-small {
            font-size: 0.82rem;
        }
        .gap-2 {
            gap: 8px;
        }
    </style>
</head>
<body>

    <!-- ========== NAVIGATION ========== -->
    <nav class="navbar" role="navigation" aria-label="Main navigation">
        <div class="container">
            <div class="navbar-brand">AM<span>.</span></div>
            <button class="nav-toggle" aria-label="Toggle navigation menu" id="navToggle">
                <span></span><span></span><span></span>
            </button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#education">Education</a></li>
                <li><a href="#interests">Research</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#honors">Honors</a></li>
                <li><a href="#skills">Skills</a></li>
            </ul>
        </div>
    </nav>

    <!-- ========== HERO ========== -->
    <header class="hero" id="home">
        <div class="container">
            <div class="hero-avatar">
                <div class="initials-fallback" aria-label="Amir Mirzaseyed initials">AM</div>
            </div>
            <div class="hero-content">
                <h1>Amir Mirzaseyed</h1>
                <p class="subhead">Industrial Management &bull; Quality &amp; Productivity &bull; AI Adoption</p>
                <div class="hero-contact">
                    <a href="mailto:samirzaseyedi@ut.ac.ir">
                        <span class="icon">✉</span> samirzaseyedi@ut.ac.ir
                    </a>
                    <a href="https://www.linkedin.com/in/amir-mirzaseyedi" target="_blank" rel="noopener noreferrer">
                        <span class="icon">🔗</span> linkedin.com/in/amir-mirzaseyedi
                    </a>
                </div>
                <div class="hero-tags">
                    <span class="tag">AI Adoption &amp; Governance</span>
                    <span class="tag">Generative AI &amp; Human-AI Collaboration</span>
                    <span class="tag">Sustainable Operations &amp; ESG</span>
                    <span class="tag">Digital Transformation</span>
                    <span class="tag">Explainable AI (XAI)</span>
                </div>
            </div>
        </div>
    </header>

    <!-- ========== EDUCATION ========== -->
    <section id="education">
        <div class="container">
            <h2 class="section-title">Education</h2>

            <div class="card">
                <div class="card-title">M.Sc. in Industrial Management</div>
                <div class="card-sub">Quality &amp; Productivity Management</div>
                <div class="card-meta">2024 – 2026 &bull; University of Tehran &bull; GPA: 19.42/20</div>
                <div class="card-body">
                    <p><strong>Thesis:</strong> “AI Adoption in Quality of Banking Services: A Capability–Attractiveness Assessment” — applied BWM and TOPSIS to evaluate and rank AI applications for banking service quality using expert panel data.</p>
                    <p class="text-muted text-small mt-1">Supervisor: Dr. Rohollah Ghasemi</p>
                </div>
            </div>

            <div class="card">
                <div class="card-title">B.Sc. in Industrial Management</div>
                <div class="card-meta">2020 – 2024 &bull; University of Tehran &bull; GPA: 18.62/20</div>
                <div class="card-body">
                    <p><strong>Thesis:</strong> “Satellite Internet Systems and Emerging Applications: A Comprehensive Overview”</p>
                    <p class="text-muted text-small mt-1">Supervisor: Dr. Rohollah Ghasemi</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ========== RESEARCH INTERESTS ========== -->
    <section id="interests" style="background:var(--white);">
        <div class="container">
            <h2 class="section-title">Research Interests</h2>
            <div class="interests-grid">
                <span class="pill">AI Adoption &amp; Governance in Organizations</span>
                <span class="pill">Generative AI &amp; Human-AI Collaboration in Decision-Making</span>
                <span class="pill">Sustainable Operations &amp; ESG Integration</span>
                <span class="pill">Digital Transformation &amp; Emerging Technology Strategy</span>
                <span class="pill">Explainable AI (XAI) and Trust in Automated Systems</span>
            </div>
        </div>
    </section>

    <!-- ========== WORK EXPERIENCE ========== -->
    <section id="experience">
        <div class="container">
            <h2 class="section-title">Work Experience</h2>

            <div class="card">
                <div class="card-title">Teaching Assistant — Total Quality Management</div>
                <div class="card-meta">Oct 2023 – Jan 2024 &bull; University of Tehran, Tehran, Iran</div>
                <div class="card-body">
                    <p>Supported course delivery and student evaluation for TQM, reinforcing the quality-management specialization carried into graduate research.</p>
                </div>
            </div>

            <div class="card">
                <div class="card-title">Finance Department Intern</div>
                <div class="card-meta">Jul 2023 – Sep 2023 &bull; Karan Polymer Part, Tehran, Iran</div>
                <div class="card-body">
                    <ul>
                        <li>ERP invoice entry, bookkeeping records, purchasing / vendor documentation.</li>
                        <li>Gained practical insight into financial data workflows and finance–procurement coordination in a manufacturing environment.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- ========== RESEARCH PROJECTS ========== -->
    <section id="projects" style="background:var(--white);">
        <div class="container">
            <h2 class="section-title">Research Projects</h2>

            <!-- project 1 -->
            <div class="card">
                <div class="card-title">A Sustainable Framework for Evaluating the Attractiveness of AI in Banking</div>
                <div class="card-sub">Insights from the Best-Worst Method</div>
                <div class="card-meta">Apr 2026 – Jul 2026 &bull; Lead Researcher &amp; First Author (with Dr. Rohollah Ghasemi)</div>
                <div class="card-body">
                    <p><span class="highlight">Submitted to:</span> 12th International Conference on Industrial and Systems Engineering (ICISE 2026), Ferdowsi University of Mashhad</p>
                    <ul>
                        <li><strong>Tools:</strong> PRISMA-ScR scoping review, Best-Worst Method with a 6-expert panel, Triple Bottom Line framework.</li>
                        <li><strong>Outcome:</strong> Built and validated a TBL-based weighting model — deepened command of hierarchical MCDM design and expert-panel consistency validation (CR, Kendall's W).</li>
                    </ul>
                </div>
            </div>

            <!-- project 2 -->
            <div class="card">
                <div class="card-title">A Strategic Roadmap for Banking Digitalization</div>
                <div class="card-sub">Extracting Tech Trends and Prioritizing Investment Portfolios</div>
                <div class="card-meta">Apr 2026 – Jul 2026 &bull; Lead Researcher &amp; First Author (with Prof. Ali Mohaghar)</div>
                <div class="card-body">
                    <p><span class="highlight">Submitted to:</span> 12th International Conference on Industrial and Systems Engineering (ICISE 2026), Ferdowsi University of Mashhad</p>
                    <ul>
                        <li><strong>Tools:</strong> PRISMA-ScR scoping review, hybrid BWM–Weighted Sum Model with a 10-expert panel.</li>
                        <li><strong>Outcome:</strong> Produced a ranked technology-investment roadmap — strengthened skills in combining two-stage MCDM methods for practical decision support.</li>
                    </ul>
                </div>
            </div>

            <!-- project 3 -->
            <div class="card">
                <div class="card-title">Capability-Attractiveness Analysis of AI Technology Applications in Banking Service Quality</div>
                <div class="card-meta">Mar 2026 – Sep 2026 &bull; Lead Researcher &amp; First Author (with Dr. Rohollah Ghasemi &amp; Prof. Ali Mohaghar)</div>
                <div class="card-body">
                    <p><span class="highlight">Submitted to:</span> Journal of Decisions and Operations Research</p>
                    <ul>
                        <li><strong>Tools:</strong> BWM, TOPSIS, expert panel data collection.</li>
                        <li><strong>Outcome:</strong> Led a full research cycle end-to-end and gained hands-on command of MCDM modeling for real-world technology prioritization.</li>
                    </ul>
                </div>
            </div>

            <!-- project 4 -->
            <div class="card">
                <div class="card-title">Service Quality in Smart Banking: A Meta-Synthesis of Industry 4.0 Technologies and Applications</div>
                <div class="card-meta">Jan 2026 – Apr 2026 &bull; Graduate Researcher, Second Author</div>
                <div class="card-body">
                    <p><span class="highlight">Submitted to:</span> Industrial Management Journal</p>
                    <ul>
                        <li><strong>Tools:</strong> Sandelowski &amp; Barroso 7-step meta-synthesis method.</li>
                        <li><strong>Outcome:</strong> Built rigor in qualitative research design and systematic literature synthesis.</li>
                    </ul>
                </div>
            </div>

            <!-- project 5 -->
            <div class="card">
                <div class="card-title">Strategic Renewal in Organizations: A Systematic Review, Conceptual Integration, and a Practical Framework</div>
                <div class="card-meta">Sep 2025 – Jan 2026 &bull; Student Researcher</div>
                <div class="card-body">
                    <ul>
                        <li><strong>Tools:</strong> Systematic review methodology, concept-centric synthesis of 25 studies.</li>
                        <li><strong>Outcome:</strong> Strengthened ability to distill scattered literature into a coherent conceptual framework.</li>
                    </ul>
                </div>
            </div>

            <!-- project 6 -->
            <div class="card">
                <div class="card-title">Analysis and Implementation Framework of ISO 27001 for Information Security Management</div>
                <div class="card-meta">Apr 2025 – Jun 2025 &bull; Student Researcher</div>
                <div class="card-body">
                    <ul>
                        <li><strong>Tools:</strong> ISO 27001 standard analysis (controls, ISMS structure).</li>
                        <li><strong>Outcome:</strong> Gained working knowledge of information security management standards and certification processes.</li>
                    </ul>
                </div>
            </div>

            <!-- project 7 -->
            <div class="card">
                <div class="card-title">EFQM Excellence Model Implementation for Sales Department</div>
                <div class="card-meta">Feb 2025 – Jun 2025 &bull; Research Team Member</div>
                <div class="card-body">
                    <ul>
                        <li><strong>Tools:</strong> EFQM Excellence Model.</li>
                        <li><strong>Outcome:</strong> Learned to apply a quality-management framework in a real organizational setting through team-based fieldwork.</li>
                    </ul>
                </div>
            </div>

            <!-- project 8 -->
            <div class="card">
                <div class="card-title">Analysis of Wearable User Interfaces: Applications, Challenges, and Strategic Implications</div>
                <div class="card-meta">Sep 2024 – Jan 2025 &bull; Student Researcher</div>
                <div class="card-body">
                    <ul>
                        <li><strong>Tools:</strong> Cross-industry technology impact analysis.</li>
                        <li><strong>Outcome:</strong> Developed early skill in evaluating emerging technologies and their strategic implications.</li>
                    </ul>
                </div>
            </div>

        </div>
    </section>

    <!-- ========== HONORS & AWARDS ========== -->
    <section id="honors">
        <div class="container">
            <h2 class="section-title">Honors &amp; Awards</h2>
            <div class="card">
                <div class="honor-item">
                    <div class="honor-year">2024</div>
                    <div class="honor-desc">Received honorary direct admission to the graduate school (M.Sc.) of the Industrial Management Department, University of Tehran, without taking the national entrance exam, in recognition of high academic records and achievements.</div>
                </div>
                <div class="honor-item">
                    <div class="honor-year">2024</div>
                    <div class="honor-desc">Ranked 4th in Cumulative GPA among all undergraduate students in Industrial Management; recognized as Outstanding Student by the university.</div>
                </div>
                <div class="honor-item">
                    <div class="honor-year">2020</div>
                    <div class="honor-desc">Ranked in the top 0.5% in the Nation-wide University Entry Exam among 595,000 Iranian students; recognized as Outstanding Student.</div>
                </div>
            </div>
            <p class="text-muted text-small" style="margin-top:8px;">References and academic records available upon request.</p>
        </div>
    </section>

    <!-- ========== SKILLS & LANGUAGES ========== -->
    <section id="skills" style="background:var(--white);">
        <div class="container">
            <h2 class="section-title">Skills &amp; Languages</h2>

            <div class="skills-wrap">
                <div class="skill-group">
                    <h4>Software &amp; Tools</h4>
                    <div class="tags">
                        <span>Python</span>
                        <span>R</span>
                        <span>Minitab</span>
                        <span>Tableau</span>
                        <span>Lingo</span>
                        <span>QM</span>
                    </div>
                </div>
                <div class="skill-group">
                    <h4>Methods &amp; Techniques</h4>
                    <div class="tags">
                        <span>Lean Six Sigma</span>
                        <span>Total Quality Management</span>
                        <span>Statistical Process Control</span>
                        <span>Operational Research &amp; Optimization Modeling</span>
                    </div>
                </div>
            </div>

            <div style="margin-top:28px;">
                <h4 style="font-size:0.9rem;font-weight:600;color:var(--navy);margin-bottom:10px;letter-spacing:0.3px;">Language Proficiency</h4>
                <div class="lang-list">
                    <span class="lang-item">Persian <span class="level">(Native)</span></span>
                    <span class="lang-item">English <span class="level">(Professional)</span></span>
                    <span class="lang-item">French <span class="level">(Intermediate)</span></span>
                </div>
            </div>
        </div>
    </section>

    <!-- ========== FOOTER ========== -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2026 Amir Mirzaseyed &bull; Built with <span style="color:#8aa4d8;">&#9829;</span> for academic excellence</p>
            <p style="font-size:0.78rem;margin-top:4px;opacity:0.6;">
                <a href="mailto:samirzaseyedi@ut.ac.ir">samirzaseyedi@ut.ac.ir</a>
                <span class="sep">&bull;</span>
                <a href="https://www.linkedin.com/in/amir-mirzaseyedi" target="_blank" rel="noopener noreferrer">LinkedIn</a>
            </p>
        </div>
    </footer>

    <!-- ========== JAVASCRIPT ========== -->
    <script>
        (function() {
            'use strict';

            // Mobile nav toggle
            const toggle = document.getElementById('navToggle');
            const links = document.getElementById('navLinks');

            if (toggle && links) {
                toggle.addEventListener('click', function() {
                    links.classList.toggle('open');
                });

                // Close nav on link click (mobile)
                links.querySelectorAll('a').forEach(function(link) {
                    link.addEventListener('click', function() {
                        links.classList.remove('open');
                    });
                });
            }

            // Smooth scroll for anchor links (with offset for fixed nav)
            document.querySelectorAll('a[href^="#"]').forEach(function(anchor) {
                anchor.addEventListener('click', function(e) {
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    const target = document.querySelector(targetId);
                    if (target) {
                        e.preventDefault();
                        const navHeight = 64;
                        const top = target.getBoundingClientRect().top + window.pageYOffset - navHeight;
                        window.scrollTo({ top: top, behavior: 'smooth' });
                    }
                });
            });

        })();
    </script>

</body>
</html>
