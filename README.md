<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet" />
</head>
<body>

    <!-- ========== NAVIGATION (DELETE THIS BLOCK TO REMOVE THE TOP BAR) ========== -->
    <!-- NAVBAR START -->
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
    <!-- NAVBAR END -->

    <!-- ========== HERO (DELETE THIS BLOCK TO REMOVE THE BLUE BANNER) ========== -->
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
                    <p><strong>Thesis:</strong> "AI Adoption in Quality of Banking Services: A Capability–Attractiveness Assessment" — applied BWM and TOPSIS to evaluate and rank AI applicatio[...]
                    <p class="text-muted text-small mt-1">Supervisor: Dr. Rohollah Ghasemi</p>
                </div>
            </div>

            <div class="card">
                <div class="card-title">B.Sc. in Industrial Management</div>
                <div class="card-meta">2020 – 2024 &bull; University of Tehran &bull; GPA: 18.62/20</div>
                <div class="card-body">
                    <p><strong>Thesis:</strong> "Satellite Internet Systems and Emerging Applications: A Comprehensive Overview"</p>
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

            <div class="card">
                <div class="card-title">A Sustainable Framework for Evaluating the Attractiveness of AI in Banking</div>
                <div class="card-sub">Insights from the Best-Worst Method</div>
                <div class="card-meta">Apr 2026 – Jul 2026 &bull; Lead Researcher &amp; First Author (with Dr. Rohollah Ghasemi)</div>
                <div class="card-body">
                    <p><span class="highlight">Submitted to:</span> 12th International Conference on Industrial and Systems Engineering (ICISE 2026), Ferdowsi University of Mashhad</p>
                    <ul>
                        <li><strong>Tools:</strong> PRISMA-ScR scoping review, Best-Worst Method with a 6-expert panel, Triple Bottom Line framework.</li>
                        <li><strong>Outcome:</strong> Built and validated a TBL-based weighting model — deepened command of hierarchical MCDM design and expert-panel consistency validation (CR, Kend[...]
                    </ul>
                </div>
            </div>

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
                    <div class="honor-desc">Received honorary direct admission to the graduate school (M.Sc.) of the Industrial Management Department, University of Tehran, without taking the national[...]
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

            const toggle = document.getElementById('navToggle');
            const links = document.getElementById('navLinks');

            if (toggle && links) {
                toggle.addEventListener('click', function() {
                    links.classList.toggle('open');
                });
                links.querySelectorAll('a').forEach(function(link) {
                    link.addEventListener('click', function() {
                        links.classList.remove('open');
                    });
                });
            }

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
