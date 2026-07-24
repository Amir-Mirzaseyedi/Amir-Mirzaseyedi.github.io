<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Amir Mirzaseyedi · Academic Portfolio</title>

    <!-- Google Fonts: Inter (modern, clean) -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet" />

    <!-- Font Awesome 6 (free icons) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />

    <style>
        /* ---------- RESET & BASE ---------- */
        *,
        *::before,
        *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        :root {
            --navy: #0f1a2f;
            --navy-light: #1a2d4a;
            --navy-lighter: #2a4068;
            --gray-soft: #f6f8fa;
            --gray-border: #e2e7ef;
            --gray-text: #4a5568;
            --gray-light: #8a9bb5;
            --white: #ffffff;
            --accent: #3b6ea5;
            --accent-hover: #2d5a8a;
            --shadow: 0 8px 30px rgba(15, 26, 47, 0.08);
            --radius: 12px;
            --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font);
            background: var(--gray-soft);
            color: #1a2634;
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 1120px;
            margin: 0 auto;
            background: var(--white);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            overflow: hidden;
        }

        /* ---------- UTILITY ---------- */
        .section-title {
            font-size: 1.5rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            color: var(--navy);
            border-bottom: 3px solid var(--navy);
            padding-bottom: 0.4rem;
            margin-bottom: 1.5rem;
            display: inline-block;
        }

        .section-title i {
            color: var(--accent);
            margin-right: 0.5rem;
            font-size: 1.3rem;
        }

        .badge {
            display: inline-block;
            background: var(--navy);
            color: var(--white);
            font-size: 0.7rem;
            font-weight: 600;
            padding: 0.15rem 0.7rem;
            border-radius: 20px;
            letter-spacing: 0.02em;
            text-transform: uppercase;
        }

        .badge-soft {
            background: var(--gray-soft);
            color: var(--navy);
            border: 1px solid var(--gray-border);
        }

        .gap-1 {
            gap: 0.5rem;
        }
        .gap-2 {
            gap: 1rem;
        }

        .flex {
            display: flex;
            flex-wrap: wrap;
        }
        .flex-center {
            align-items: center;
        }
        .flex-between {
            justify-content: space-between;
        }

        /* ---------- HEADER / HERO ---------- */
        .hero {
            background: var(--navy);
            color: var(--white);
            padding: 2.5rem 2.5rem 2rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 2rem;
        }

        .hero-avatar {
            flex-shrink: 0;
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: var(--navy-lighter);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.2rem;
            font-weight: 600;
            color: var(--white);
            border: 3px solid rgba(255, 255, 255, 0.25);
            user-select: none;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }

        .hero-info {
            flex: 1;
            min-width: 220px;
        }

        .hero-info h1 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            margin-bottom: 0.15rem;
            line-height: 1.2;
        }

        .hero-info .subtitle {
            font-size: 1.05rem;
            font-weight: 400;
            color: rgba(255, 255, 255, 0.75);
            margin-bottom: 0.75rem;
        }

        .hero-contact {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem 2rem;
            font-size: 0.9rem;
        }

        .hero-contact a {
            color: rgba(255, 255, 255, 0.85);
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.45rem;
            transition: color 0.2s;
            font-weight: 400;
        }

        .hero-contact a:hover {
            color: var(--white);
        }

        .hero-contact i {
            font-size: 1rem;
            width: 1.1rem;
            text-align: center;
            color: rgba(255, 255, 255, 0.6);
        }

        /* ---------- MAIN CONTENT ---------- */
        .main {
            padding: 2.5rem;
        }

        /* ---------- RESEARCH INTERESTS (grid) ---------- */
        .interests-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem 1rem;
            margin-top: 0.25rem;
        }

        .interests-grid span {
            background: var(--gray-soft);
            padding: 0.3rem 1rem;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--navy);
            border: 1px solid var(--gray-border);
        }

        /* ---------- EDUCATION ---------- */
        .edu-item {
            margin-bottom: 1.75rem;
        }

        .edu-item:last-child {
            margin-bottom: 0;
        }

        .edu-head {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.5rem 1rem;
            margin-bottom: 0.2rem;
        }

        .edu-head h3 {
            font-size: 1.15rem;
            font-weight: 600;
            color: var(--navy);
        }

        .edu-head .date {
            font-size: 0.85rem;
            font-weight: 500;
            color: var(--gray-light);
        }

        .edu-meta {
            font-weight: 500;
            color: var(--navy-lighter);
            font-size: 0.95rem;
            margin-bottom: 0.3rem;
        }

        .edu-meta .gpa {
            font-weight: 600;
            color: var(--accent);
        }

        .edu-thesis {
            font-size: 0.95rem;
            color: var(--gray-text);
            background: var(--gray-soft);
            padding: 0.6rem 1rem;
            border-radius: 8px;
            border-left: 4px solid var(--accent);
            margin-top: 0.4rem;
        }

        .edu-thesis strong {
            color: var(--navy);
        }

        /* ---------- WORK EXPERIENCE ---------- */
        .work-item {
            margin-bottom: 1.75rem;
        }

        .work-item:last-child {
            margin-bottom: 0;
        }

        .work-head {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.5rem 1rem;
            margin-bottom: 0.15rem;
        }

        .work-head h3 {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--navy);
        }

        .work-head .role {
            font-weight: 500;
            color: var(--accent);
            font-size: 0.95rem;
        }

        .work-head .date {
            font-size: 0.85rem;
            font-weight: 500;
            color: var(--gray-light);
        }

        .work-desc {
            font-size: 0.95rem;
            color: var(--gray-text);
            margin-top: 0.2rem;
            padding-left: 0.2rem;
        }

        .work-desc ul {
            list-style: none;
            padding-left: 0;
            margin-top: 0.2rem;
        }

        .work-desc ul li {
            padding-left: 1.2rem;
            position: relative;
            margin-bottom: 0.1rem;
        }

        .work-desc ul li::before {
            content: "•";
            color: var(--accent);
            font-weight: 700;
            position: absolute;
            left: 0;
        }

        /* ---------- RESEARCH PROJECTS ---------- */
        .research-item {
            background: var(--gray-soft);
            border-radius: 10px;
            padding: 1.25rem 1.5rem;
            margin-bottom: 1.25rem;
            border: 1px solid var(--gray-border);
            transition: box-shadow 0.2s;
        }

        .research-item:hover {
            box-shadow: 0 4px 16px rgba(15, 26, 47, 0.06);
        }

        .research-item:last-child {
            margin-bottom: 0;
        }

        .research-head {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.5rem 1rem;
            margin-bottom: 0.25rem;
        }

        .research-head h4 {
            font-size: 1.05rem;
            font-weight: 600;
            color: var(--navy);
        }

        .research-head .status {
            font-size: 0.75rem;
            font-weight: 600;
            color: var(--accent);
            background: rgba(59, 110, 165, 0.1);
            padding: 0.1rem 0.8rem;
            border-radius: 20px;
            border: 1px solid rgba(59, 110, 165, 0.2);
        }

        .research-meta {
            font-size: 0.85rem;
            color: var(--gray-light);
            margin-bottom: 0.3rem;
        }

        .research-meta .authors {
            color: var(--gray-text);
            font-weight: 500;
        }

        .research-tools {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem 0.7rem;
            margin: 0.4rem 0 0.3rem;
        }

        .research-tools span {
            background: var(--white);
            border: 1px solid var(--gray-border);
            padding: 0.1rem 0.7rem;
            border-radius: 16px;
            font-size: 0.75rem;
            font-weight: 500;
            color: var(--navy-lighter);
        }

        .research-outcome {
            font-size: 0.95rem;
            color: var(--gray-text);
            margin-top: 0.3rem;
            padding-top: 0.3rem;
            border-top: 1px dashed var(--gray-border);
        }

        .research-outcome strong {
            color: var(--navy);
        }

        /* ---------- SKILLS & LANGUAGES ---------- */
        .skills-lang {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .skills-group h4,
        .lang-group h4 {
            font-size: 1rem;
            font-weight: 600;
            color: var(--navy);
            margin-bottom: 0.6rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
        }

        .skills-group h4 i,
        .lang-group h4 i {
            color: var(--accent);
            font-size: 1rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem 0.7rem;
        }

        .skill-tags span {
            background: var(--white);
            border: 1px solid var(--gray-border);
            padding: 0.2rem 0.9rem;
            border-radius: 20px;
            font-size: 0.82rem;
            font-weight: 500;
            color: var(--navy);
        }

        .lang-list {
            list-style: none;
            padding: 0;
        }

        .lang-list li {
            display: flex;
            justify-content: space-between;
            padding: 0.25rem 0;
            border-bottom: 1px solid var(--gray-border);
            font-size: 0.92rem;
        }

        .lang-list li:last-child {
            border-bottom: none;
        }

        .lang-list .lang-name {
            font-weight: 500;
            color: var(--navy);
        }

        .lang-list .lang-level {
            color: var(--gray-light);
            font-size: 0.85rem;
        }

        /* ---------- HONORS ---------- */
        .honors-list {
            list-style: none;
            padding: 0;
        }

        .honors-list li {
            display: flex;
            gap: 1rem;
            padding: 0.6rem 0;
            border-bottom: 1px solid var(--gray-border);
            font-size: 0.95rem;
            color: var(--gray-text);
        }

        .honors-list li:last-child {
            border-bottom: none;
        }

        .honors-list .year {
            font-weight: 600;
            color: var(--navy);
            flex-shrink: 0;
            min-width: 3.2rem;
        }

        .honors-list .honor-badge {
            color: var(--accent);
            margin-right: 0.2rem;
        }

        /* ---------- FOOTER ---------- */
        .footer {
            background: var(--navy);
            color: rgba(255, 255, 255, 0.6);
            text-align: center;
            padding: 1.5rem 2rem;
            font-size: 0.85rem;
            border-top: 1px solid rgba(255, 255, 255, 0.06);
        }

        .footer a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
        }

        .footer a:hover {
            color: var(--white);
        }

        /* ---------- RESPONSIVE ---------- */
        @media (max-width: 820px) {
            body {
                padding: 1rem 0.75rem;
            }

            .hero {
                padding: 1.75rem 1.5rem 1.5rem;
                flex-direction: column;
                text-align: center;
                gap: 1.25rem;
            }

            .hero-avatar {
                width: 100px;
                height: 100px;
                font-size: 2.8rem;
            }

            .hero-info h1 {
                font-size: 1.8rem;
            }

            .hero-contact {
                justify-content: center;
                gap: 0.8rem 1.5rem;
                font-size: 0.85rem;
                flex-wrap: wrap;
            }

            .main {
                padding: 1.5rem;
            }

            .section-title {
                font-size: 1.25rem;
            }

            .skills-lang {
                grid-template-columns: 1fr;
                gap: 1.5rem;
            }

            .edu-head,
            .work-head,
            .research-head {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.15rem;
            }

            .research-item {
                padding: 1rem 1.2rem;
            }

            .interests-grid {
                gap: 0.4rem 0.7rem;
            }

            .interests-grid span {
                font-size: 0.8rem;
                padding: 0.2rem 0.8rem;
            }

            .honors-list li {
                flex-wrap: wrap;
                gap: 0.2rem 0.5rem;
            }
        }

        @media (max-width: 480px) {
            .hero-info h1 {
                font-size: 1.5rem;
            }

            .hero {
                padding: 1.25rem 1rem 1.25rem;
            }

            .main {
                padding: 1.25rem;
            }

            .hero-contact {
                font-size: 0.8rem;
                gap: 0.5rem 1rem;
            }

            .research-head h4 {
                font-size: 0.95rem;
            }

            .edu-head h3 {
                font-size: 1rem;
            }
        }

        /* ---------- PRINT HINT (optional) ---------- */
        @media print {
            body {
                background: white;
                padding: 0;
            }
            .container {
                box-shadow: none;
                border-radius: 0;
            }
            .hero {
                -webkit-print-color-adjust: exact;
                print-color-adjust: exact;
            }
            .research-item:hover {
                box-shadow: none;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- ===== HERO ===== -->
        <header class="hero">
            <div class="hero-avatar" aria-hidden="true">AM</div>
            <div class="hero-info">
                <h1>Amir Mirzaseyedi</h1>
                <div class="subtitle">Industrial Management &bull; Quality &amp; Productivity &bull; AI Adoption</div>
                <div class="hero-contact">
                    <a href="mailto:samirzaseyedi@ut.ac.ir" aria-label="Email">
                        <i class="fas fa-envelope"></i> samirzaseyedi@ut.ac.ir
                    </a>
                    <a href="https://www.linkedin.com/in/amir-mirzaseyedi" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
                        <i class="fab fa-linkedin-in"></i> linkedin.com/in/amir-mirzaseyedi
                    </a>
                    <span><i class="fas fa-map-marker-alt"></i> Tehran, Iran</span>
                </div>
            </div>
        </header>

        <!-- ===== MAIN ===== -->
        <div class="main">

            <!-- ===== RESEARCH INTERESTS ===== -->
            <section>
                <h2 class="section-title"><i class="fas fa-bolt"></i> Research Interests</h2>
                <div class="interests-grid">
                    <span>AI Adoption &amp; Governance in Organizations</span>
                    <span>Generative AI &amp; Human–AI Collaboration in Decision-Making</span>
                    <span>Sustainable Operations &amp; ESG Integration</span>
                    <span>Digital Transformation &amp; Emerging Technology Strategy</span>
                    <span>Explainable AI (XAI) &amp; Trust in Automated Systems</span>
                </div>
            </section>

            <!-- ===== EDUCATION ===== -->
            <section style="margin-top: 2.5rem;">
                <h2 class="section-title"><i class="fas fa-graduation-cap"></i> Education</h2>

                <div class="edu-item">
                    <div class="edu-head">
                        <h3>University of Tehran</h3>
                        <span class="date">2024 – 2026</span>
                    </div>
                    <div class="edu-meta">
                        M.Sc., Industrial Management (Quality &amp; Productivity Management)
                        <span class="gpa">— GPA: 19.42/20</span>
                    </div>
                    <div class="edu-thesis">
                        <strong>Thesis:</strong> “AI Adoption in Quality of Banking Services: A Capability–Attractiveness Assessment” — applied BWM and TOPSIS to evaluate and rank AI applications for banking service quality using expert panel data. <span style="font-size:0.85rem;color:var(--gray-light);">(Supervisor: Dr. Rohollah Ghasemi)</span>
                    </div>
                </div>

                <div class="edu-item" style="margin-bottom:0;">
                    <div class="edu-head">
                        <h3>University of Tehran</h3>
                        <span class="date">2020 – 2024</span>
                    </div>
                    <div class="edu-meta">
                        B.Sc., Industrial Management
                        <span class="gpa">— GPA: 18.62/20</span>
                    </div>
                    <div class="edu-thesis">
                        <strong>Thesis:</strong> “Satellite Internet Systems and Emerging Applications: A Comprehensive Overview” <span style="font-size:0.85rem;color:var(--gray-light);">(Supervisor: Dr. Rohollah Ghasemi)</span>
                    </div>
                </div>
            </section>

            <!-- ===== WORK EXPERIENCE ===== -->
            <section style="margin-top: 2.5rem;">
                <h2 class="section-title"><i class="fas fa-briefcase"></i> Work Experience</h2>

                <div class="work-item">
                    <div class="work-head">
                        <h3>University of Tehran</h3>
                        <span class="role">Teaching Assistant — Total Quality Management</span>
                        <span class="date">Oct 2023 – Jan 2024</span>
                    </div>
                    <div class="work-desc">
                        Supported course delivery and student evaluation for TQM, reinforcing the quality‑management specialization carried into graduate research.
                    </div>
                </div>

                <div class="work-item" style="margin-bottom:0;">
                    <div class="work-head">
                        <h3>Karan Polymer Part</h3>
                        <span class="role">Finance Department Intern</span>
                        <span class="date">Jul 2023 – Sep 2023</span>
                    </div>
                    <div class="work-desc">
                        <ul>
                            <li>ERP invoice entry, bookkeeping records, purchasing and vendor documentation.</li>
                            <li>Practical financial data workflows and finance–procurement coordination in a manufacturing company.</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- ===== RESEARCH PROJECTS ===== -->
            <section style="margin-top: 2.5rem;">
                <h2 class="section-title"><i class="fas fa-flask"></i> Research</h2>

                <!-- 1 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>A Sustainable Framework for Evaluating the Attractiveness of AI in Banking: Insights from the Best‑Worst Method</h4>
                        <span class="status">Submitted · ICISE 2026</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Lead Researcher &amp; First Author</span> (with Dr. Rohollah Ghasemi)
                    </div>
                    <div class="research-tools">
                        <span>PRISMA‑ScR scoping review</span>
                        <span>Best‑Worst Method (6‑expert panel)</span>
                        <span>Triple Bottom Line framework</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> built and validated a TBL‑based weighting model — deepened command of hierarchical MCDM design and expert‑panel consistency validation (CR, Kendall's W).
                    </div>
                </div>

                <!-- 2 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>A Strategic Roadmap for Banking Digitalization: Extracting Tech Trends and Prioritizing Investment Portfolios</h4>
                        <span class="status">Submitted · ICISE 2026</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Lead Researcher &amp; First Author</span> (with Prof. Ali Mohaghar)
                    </div>
                    <div class="research-tools">
                        <span>PRISMA‑ScR scoping review</span>
                        <span>hybrid BWM–Weighted Sum Model</span>
                        <span>10‑expert panel</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> produced a ranked technology‑investment roadmap — strengthened skills in combining two‑stage MCDM methods for practical decision support.
                    </div>
                </div>

                <!-- 3 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>Capability‑Attractiveness Analysis of AI Technology Applications in Banking Service Quality</h4>
                        <span class="status">Submitted · Journal of Decisions and Operations Research</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Lead Researcher &amp; First Author</span> (with Dr. Rohollah Ghasemi &amp; Prof. Ali Mohaghar)
                    </div>
                    <div class="research-tools">
                        <span>BWM</span>
                        <span>TOPSIS</span>
                        <span>expert panel data collection</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> led a full research cycle end‑to‑end and gained hands‑on command of MCDM modeling for real‑world technology prioritization.
                    </div>
                </div>

                <!-- 4 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>Service Quality in Smart Banking: A Meta‑Synthesis of Industry 4.0 Technologies and Applications</h4>
                        <span class="status">Submitted · Industrial Management Journal</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Graduate Researcher, Second Author</span>
                    </div>
                    <div class="research-tools">
                        <span>Sandelowski &amp; Barroso 7‑step meta‑synthesis</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> built rigor in qualitative research design and systematic literature synthesis.
                    </div>
                </div>

                <!-- 5 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>Strategic Renewal in Organizations: A Systematic Review, Conceptual Integration, and a Practical Framework</h4>
                        <span class="status">Student Researcher</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Sep 2025 – Jan 2026</span>
                    </div>
                    <div class="research-tools">
                        <span>systematic review methodology</span>
                        <span>concept‑centric synthesis of 25 studies</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> strengthened ability to distill scattered literature into a coherent conceptual framework.
                    </div>
                </div>

                <!-- 6 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>Analysis and Implementation Framework of ISO 27001 for Information Security Management</h4>
                        <span class="status">Student Researcher</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Apr 2025 – Jun 2025</span>
                    </div>
                    <div class="research-tools">
                        <span>ISO 27001 standard analysis (controls, ISMS structure)</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> gained working knowledge of information security management standards and certification processes.
                    </div>
                </div>

                <!-- 7 -->
                <div class="research-item">
                    <div class="research-head">
                        <h4>EFQM Excellence Model Implementation for Sales Department</h4>
                        <span class="status">Research Team Member</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Feb 2025 – Jun 2025</span>
                    </div>
                    <div class="research-tools">
                        <span>EFQM Excellence Model</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> learned to apply a quality‑management framework in a real organizational setting through team‑based fieldwork.
                    </div>
                </div>

                <!-- 8 -->
                <div class="research-item" style="margin-bottom:0;">
                    <div class="research-head">
                        <h4>Analysis of Wearable User Interfaces: Applications, Challenges, and Strategic Implications</h4>
                        <span class="status">Student Researcher</span>
                    </div>
                    <div class="research-meta">
                        <span class="authors">Sep 2024 – Jan 2025</span>
                    </div>
                    <div class="research-tools">
                        <span>cross‑industry technology impact analysis</span>
                    </div>
                    <div class="research-outcome">
                        <strong>Outcome:</strong> developed early skill in evaluating emerging technologies and their strategic implications.
                    </div>
                </div>
            </section>

            <!-- ===== SKILLS & LANGUAGES ===== -->
            <section style="margin-top: 2.5rem;">
                <h2 class="section-title"><i class="fas fa-cogs"></i> Skills &amp; Languages</h2>
                <div class="skills-lang">

                    <div>
                        <div class="skills-group">
                            <h4><i class="fas fa-laptop-code"></i> Software &amp; Tools</h4>
                            <div class="skill-tags">
                                <span>Python</span><span>R</span><span>Minitab</span><span>Tableau</span>
                                <span>Lingo</span><span>QM</span>
                            </div>
                        </div>

                        <div class="skills-group" style="margin-top:1.25rem;">
                            <h4><i class="fas fa-chart-line"></i> Methods &amp; Techniques</h4>
                            <div class="skill-tags">
                                <span>Lean Six Sigma</span><span>Total Quality Management</span>
                                <span>Statistical Process Control</span><span>Operational Research &amp; Optimization Modeling</span>
                            </div>
                        </div>
                    </div>

                    <div>
                        <div class="lang-group">
                            <h4><i class="fas fa-language"></i> Language Proficiency</h4>
                            <ul class="lang-list">
                                <li><span class="lang-name">Persian</span><span class="lang-level">Native</span></li>
                                <li><span class="lang-name">English</span><span class="lang-level">Professional working proficiency</span></li>
                                <li><span class="lang-name">French</span><span class="lang-level">Limited working proficiency</span></li>
                            </ul>
                        </div>
                    </div>

                </div>
            </section>

            <!-- ===== HONORS & AWARDS ===== -->
            <section style="margin-top: 2.5rem;">
                <h2 class="section-title"><i class="fas fa-trophy"></i> Honors &amp; Awards</h2>
                <ul class="honors-list">
                    <li>
                        <span class="year">2024</span>
                        <span><span class="honor-badge">+</span> Received honorary direct admission to the graduate school (M.Sc.) of the Industrial Management Department, University of Tehran, without taking the national entrance exam for graduate schools, in recognition of high academic records and achievements.</span>
                    </li>
                    <li>
                        <span class="year">2024</span>
                        <span><span class="honor-badge">+</span> Ranked 4th in Cumulative GPA among all undergraduate students in Industrial Management; recognized as Outstanding Student by the university.</span>
                    </li>
                    <li>
                        <span class="year">2020</span>
                        <span><span class="honor-badge">+</span> Ranked in the top 0.5% in the Nation‑wide University Entry Exam among 595,000 Iranian students; recognized as Outstanding Student.</span>
                    </li>
                </ul>
                <p style="margin-top:0.75rem;font-size:0.9rem;color:var(--gray-light);font-style:italic;">
                    <i class="fas fa-file-alt" style="margin-right:0.3rem;"></i> References and academic records available upon request.
                </p>
            </section>

        </div>
        <!-- /main -->

        <!-- ===== FOOTER ===== -->
        <footer class="footer">
            &copy; 2026 <a href="mailto:samirzaseyedi@ut.ac.ir">Amir Mirzaseyedi</a>.
        </footer>

    </div>
    <!-- /container -->

</body>
</html>
