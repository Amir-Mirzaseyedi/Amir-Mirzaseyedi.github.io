<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Amir Mirzaseyedi · Home</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700;900&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="style.css" />
</head>
<body>

    <nav class="navbar" role="navigation" aria-label="Main navigation">
        <div class="nav-inner">
            <div class="nav-brand">
                <a href="index.html">AMIR MIRZASEYED</a>
            </div>
            <button class="nav-toggle" aria-label="Toggle navigation" id="navToggle">
                <span></span><span></span><span></span>
            </button>
            <ul class="nav-links" id="navLinks">
                <li><a href="index.html" class="active">Home</a></li>
                <li class="dropdown">
                    <a href="about.html" class="dropbtn">About</a>
                    <ul class="dropdown-content">
                        <li><a href="about.html#biography">Biography</a></li>
                        <li><a href="about.html#education">Education</a></li>
                        <li><a href="about.html#skills">Skills</a></li>
                        <li><a href="about.html#honors">Honors &amp; Awards</a></li>
                    </ul>
                </li>
                <li class="dropdown">
                    <a href="research.html" class="dropbtn">Research</a>
                    <ul class="dropdown-content">
                        <li><a href="research.html#interests">Research Interests</a></li>
                        <li><a href="research.html#projects">Current Projects</a></li>
                        <li><a href="research.html#publications">Publications &amp; Submissions</a></li>
                    </ul>
                </li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </div>
    </nav>

    <main>
        <section class="hero">
            <div class="container hero-grid">
                <div class="hero-text animate animate-delay-1">
                    <p class="hero-subtitle">Industrial Management · Quality &amp; Productivity · AI Adoption</p>
                    <h1 class="hero-title">Amir Mirzaseyedi</h1>
                    <p class="hero-bio">
                        I am an industrial management researcher focused on the intersection of AI adoption,
                        quality management, and operational excellence. My work applies multi-criteria
                        decision-making (BWM, TOPSIS) to evaluate emerging technologies in banking and
                        service sectors. I hold an M.Sc. from the University of Tehran and am pursuing
                        research that bridges technical rigor with practical organizational impact.
                    </p>
                    <div class="hero-actions">
                        <a href="about.html" class="btn btn-primary">About Me</a>
                        <a href="research.html" class="btn btn-outline">Research</a>
                    </div>
                </div>
                <div class="hero-avatar animate animate-delay-2">
                    <div class="avatar-placeholder">AM</div>
                </div>
            </div>
        </section>

        <section class="updates">
            <div class="container">
                <h2 class="section-title animate">Recent Updates</h2>
                <div class="updates-list">
                    <article class="update-item animate animate-delay-1">
                        <span class="update-date">Jul 2026</span>
                        <p>
                            <strong>Two papers submitted</strong> to the 12<sup>th</sup> International Conference
                            on Industrial and Systems Engineering (ICISE 2026), Ferdowsi University of Mashhad:
                            <em>&ldquo;A Sustainable Framework for Evaluating the Attractiveness of AI in Banking&rdquo;</em>
                            and <em>&ldquo;A Strategic Roadmap for Banking Digitalization.&rdquo;</em>
                        </p>
                    </article>
                    <article class="update-item animate animate-delay-2">
                        <span class="update-date">Sep 2026</span>
                        <p>
                            <strong>Journal submission</strong> &mdash; <em>&ldquo;Capability–Attractiveness Analysis
                            of AI Technology Applications in Banking Service Quality&rdquo;</em> submitted to the
                            <em>Journal of Decisions and Operations Research</em>.
                        </p>
                    </article>
                    <article class="update-item animate animate-delay-3">
                        <span class="update-date">2024</span>
                        <p>
                            <strong>Honorary direct admission</strong> to the M.Sc. program in Industrial Management
                            at the University of Tehran, ranked 4<sup>th</sup> in cumulative GPA among all
                            undergraduate students.
                        </p>
                    </article>
                </div>
            </div>
        </section>

        <section class="highlights">
            <div class="container highlights-grid">
                <div class="highlight-card animate animate-delay-1">
                    <h3>Education</h3>
                    <p><strong>M.Sc.</strong> Industrial Management (Quality &amp; Productivity)<br />University of Tehran · GPA 19.42/20</p>
                    <p><strong>B.Sc.</strong> Industrial Management<br />University of Tehran · GPA 18.62/20</p>
                    <a href="about.html#education" class="highlight-link">Full education →</a>
                </div>
                <div class="highlight-card animate animate-delay-2">
                    <h3>Research Focus</h3>
                    <ul>
                        <li>AI Adoption &amp; Governance</li>
                        <li>Generative AI &amp; Human–AI Collaboration</li>
                        <li>MCDM · BWM · TOPSIS</li>
                        <li>Digital Transformation Strategy</li>
                    </ul>
                    <a href="research.html#interests" class="highlight-link">All interests →</a>
                </div>
                <div class="highlight-card animate animate-delay-3">
                    <h3>Skills</h3>
                    <p><strong>Methods:</strong> Lean Six Sigma, TQM, SPC, OR &amp; Optimization</p>
                    <p><strong>Tools:</strong> Python, R, Minitab, Tableau, Lingo, QM</p>
                    <a href="about.html#skills" class="highlight-link">Full skills →</a>
                </div>
            </div>
        </section>
    </main>

    <footer class="footer">
        <div class="container footer-inner">
            <p>&copy; 2026 Amir Mirzaseyedi · All rights reserved.</p>
            <p class="footer-small">References and academic records available upon request.</p>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>
