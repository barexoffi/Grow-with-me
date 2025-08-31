<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Build Your Life — Class Study Hub | Barex</title>
    <meta name="description" content="Study tips, projects, and short lessons from Barex for classmates. Learn smart methods, join weekly challenges, and grow together.">
    <meta property="og:title" content="Build Your Life — Class Study Hub">
    <meta property="og:description" content="Study tips, projects, and short lessons from Barex for classmates.">
    <meta property="og:type" content="website">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Poppins:wght@600;700&display=swap" rel="stylesheet">
    <style>
        /* CSS Variables */
        :root {
            --primary: #0B5FFF;
            --accent: #F6C84C;
            --muted: #F4F6F8;
            --text: #0B1A2B;
            --danger: #E63946;
            --white: #ffffff;
            --gray-light: #F8F9FA;
            --gray: #6C757D;
            --shadow: 0 6px 16px rgba(10,10,10,0.06);
        }

        /* Reset & Base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            font-size: 16px;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--white);
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 16px;
        }

        @media (min-width: 769px) {
            .container {
                padding: 0 32px;
            }
        }

        /* Typography */
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        h1 {
            font-size: 28px;
            line-height: 1.1;
        }

        h2 {
            font-size: 22px;
        }

        h3 {
            font-size: 20px;
        }

        p {
            margin-bottom: 1rem;
        }

        small {
            font-size: 14px;
        }

        /* Links */
        a {
            color: var(--primary);
            text-decoration: none;
            transition: color 0.2s ease;
        }

        a:hover, a:focus {
            color: var(--accent);
            outline: 2px solid var(--primary);
            outline-offset: 2px;
        }

        /* Buttons */
        .btn {
            display: inline-block;
            padding: 12px 24px;
            background: var(--primary);
            color: var(--white);
            border: none;
            border-radius: 8px;
            font-weight: 500;
            text-align: center;
            cursor: pointer;
            transition: all 0.2s ease;
            text-decoration: none;
        }

        .btn:hover, .btn:focus {
            background: var(--accent);
            color: var(--text);
            transform: translateY(-2px);
            box-shadow: var(--shadow);
        }

        .btn-secondary {
            background: var(--white);
            color: var(--primary);
            border: 2px solid var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: var(--white);
        }

        /* Header */
        .site-header {
            background: var(--white);
            padding: 1rem 0;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            font-size: 20px;
            color: var(--primary);
        }

        .menu-toggle {
            display: block;
            background: none;
            border: none;
            font-size: 18px;
            cursor: pointer;
            padding: 8px;
        }

        .nav {
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        .nav.hide {
            display: none;
        }

        @media (max-width: 768px) {
            .nav {
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--white);
                flex-direction: column;
                padding: 1rem;
                box-shadow: var(--shadow);
            }
        }

        @media (min-width: 769px) {
            .menu-toggle {
                display: none;
            }
            
            .nav.hide {
                display: flex;
            }
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: var(--white);
            padding: 4rem 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 32px;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero-actions {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .amharic-text {
            margin-top: 1rem;
            font-size: 14px;
            opacity: 0.8;
        }

        @media (min-width: 481px) {
            .hero h1 {
                font-size: 42px;
            }
        }

        /* Cards */
        .card {
            background: var(--white);
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: var(--shadow);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(10,10,10,0.12);
        }

        .cards-grid {
            display: grid;
            gap: 1.5rem;
            margin: 3rem 0;
        }

        @media (min-width: 481px) {
            .cards-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (min-width: 769px) {
            .cards-grid {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        /* Sections */
        .section {
            padding: 3rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        /* Featured Content */
        .featured {
            background: var(--muted);
            padding: 3rem 0;
        }

        .featured-grid {
            display: grid;
            gap: 2rem;
        }

        @media (min-width: 769px) {
            .featured-grid {
                grid-template-columns: 1fr 1fr;
                align-items: center;
            }
        }

        .featured-image {
            width: 100%;
            height: 200px;
            background: var(--gray-light);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gray);
        }

        /* Footer */
        .site-footer {
            background: var(--text);
            color: var(--white);
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        @media (min-width: 481px) {
            .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (min-width: 769px) {
            .footer-content {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 14px;
            opacity: 0.8;
        }

        /* Forms */
        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: 2px solid #E9ECEF;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.2s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--primary);
        }

        .form-group textarea {
            height: 120px;
            resize: vertical;
        }

        .checkbox-group {
            display: flex;
            align-items: flex-start;
            gap: 0.5rem;
        }

        .checkbox-group input[type="checkbox"] {
            width: auto;
            margin: 0;
        }

        /* Study Tips Page Styles */
        .tip-card {
            border-left: 4px solid var(--primary);
        }

        .tip-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .tip-time {
            background: var(--accent);
            color: var(--text);
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 500;
        }

        /* Projects Page Styles */
        .project-card {
            position: relative;
        }

        .project-image {
            width: 100%;
            height: 150px;
            background: var(--gray-light);
            border-radius: 8px;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gray);
        }

        .project-status {
            position: absolute;
            top: 1rem;
            right: 1rem;
            padding: 4px 12px;
            border-radius: 16px;
            font-size: 12px;
            font-weight: 500;
        }

        .status-ongoing {
            background: var(--accent);
            color: var(--text);
        }

        .status-done {
            background: #28A745;
            color: var(--white);
        }

        .contributors {
            font-size: 14px;
            color: var(--gray);
            margin-top: 0.5rem;
        }

        /* Blog Styles */
        .blog-card {
            border-bottom: 1px solid #E9ECEF;
            padding-bottom: 1.5rem;
            margin-bottom: 2rem;
        }

        .blog-meta {
            font-size: 14px;
            color: var(--gray);
            margin-bottom: 1rem;
        }

        .blog-excerpt {
            color: var(--gray);
            margin-bottom: 1rem;
        }

        /* Utilities */
        .text-center {
            text-align: center;
        }

        .mb-0 { margin-bottom: 0; }
        .mb-1 { margin-bottom: 0.5rem; }
        .mb-2 { margin-bottom: 1rem; }
        .mb-3 { margin-bottom: 1.5rem; }

        .hide {
            display: none !important;
        }

        @media (min-width: 769px) {
            .hide-desktop {
                display: none !important;
            }
        }

        @media (max-width: 768px) {
            .hide-mobile {
                display: none !important;
            }
        }
    </style>
</head>
<body>
    <header class="site-header">
        <div class="container">
            <div class="header-content">
                <a href="/" class="logo">Build Your Life</a>
                <button id="menuToggle" class="menu-toggle" aria-expanded="false" aria-controls="mainNav">☰</button>
                <nav id="mainNav" class="nav hide">
                    <a href="/#study">Study Tips</a>
                    <a href="#projects">Projects</a>
                    <a href="#blog">Blog</a>
                    <a href="#contact">Contact</a>
                </nav>
            </div>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <h1>Build Your Life — For Our Class</h1>
                <p>Study tips, projects, and short lessons from Barex — for our classmates.</p>
                <div class="hero-actions">
                    <a href="#study" class="btn">Start Learning</a>
                    <a href="https://t.me/your_class_group" class="btn btn-secondary">Join Telegram</a>
                </div>
                <div class="amharic-text">
                    ለክላስ መማር እና ማዕከላዊ እርዳታ
                </div>
            </div>
        </section>

        <section class="section" id="benefits">
            <div class="container">
                <div class="cards-grid">
                    <div class="card">
                        <h3>📚 Smart Study Methods</h3>
                        <p>Learn proven techniques like Pomodoro, active recall, and spaced repetition to study more effectively and retain information better.</p>
                    </div>
                    <div class="card">
                        <h3>🎯 Weekly Challenges</h3>
                        <p>Join fun project challenges and activities designed to build skills, confidence, and teamwork with your classmates.</p>
                    </div>
                    <div class="card">
                        <h3>📢 Class Updates</h3>
                        <p>Stay informed with important announcements, study notes, and helpful resources shared by Barex and class leaders.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="featured" id="study">
            <div class="container">
                <h2 class="section-title">Featured Study Tip</h2>
                <div class="featured-grid">
                    <div>
                        <h3>🍅 The Pomodoro Technique</h3>
                        <p>One of the most effective study methods is the Pomodoro Technique. Set a timer for 25 minutes and focus completely on one task. When the timer rings, take a 5-minute break. After completing 4 rounds, take a longer 20-30 minute break. This helps maintain focus and prevents mental fatigue, making your study sessions more productive.</p>
                        <a href="#study-tips" class="btn">See All Study Tips</a>
                    </div>
                    <div class="featured-image">
                        🍅 Study Timer
                    </div>
                </div>
            </div>
        </section>

        <section class="section" id="study-tips">
            <div class="container">
                <h2 class="section-title">Study Tips</h2>
                <div class="cards-grid">
                    <div class="card tip-card">
                        <div class="tip-header">
                            <h3>🍅 Pomodoro Method</h3>
                            <span class="tip-time">30 min</span>
                        </div>
                        <p>Focus for 25 minutes, then take a 5-minute break. After 4 rounds, take a 20-30 minute break. This technique helps maintain concentration and prevents burnout.</p>
                    </div>
                    <div class="card tip-card">
                        <div class="tip-header">
                            <h3>🧠 Active Recall</h3>
                            <span class="tip-time">15 min</span>
                        </div>
                        <p>After studying a topic, close your notes and write down what you remember. This forces your brain to retrieve information, strengthening memory pathways.</p>
                    </div>
                    <div class="card tip-card">
                        <div class="tip-header">
                            <h3>📅 Weekly Review</h3>
                            <span class="tip-time">30 min</span>
                        </div>
                        <p>Every Sunday, spend 30 minutes summarizing what you learned during the week and planning your study goals for the next week.</p>
                    </div>
                    <div class="card tip-card">
                        <div class="tip-header">
                            <h3>🎯 Spaced Repetition</h3>
                            <span class="tip-time">10 min daily</span>
                        </div>
                        <p>Review new information after 1 day, then 3 days, then 1 week, then 2 weeks. This spacing helps move information into long-term memory.</p>
                    </div>
                    <div class="card tip-card">
                        <div class="tip-header">
                            <h3>✍️ Note Taking</h3>
                            <span class="tip-time">During class</span>
                        </div>
                        <p>Use the Cornell Note-Taking method: divide your page into notes, cues, and summary sections. Review and summarize within 24 hours.</p>
                    </div>
                    <div class="card tip-card">
                        <div class="tip-header">
                            <h3>🌅 Morning Study</h3>
                            <span class="tip-time">1-2 hours</span>
                        </div>
                        <p>Your brain is freshest in the morning. Tackle your most challenging subjects when you first wake up for better understanding and retention.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section" id="projects">
            <div class="container">
                <h2 class="section-title">Class Projects</h2>
                <div class="cards-grid">
                    <div class="card project-card">
                        <div class="project-status status-ongoing">Ongoing</div>
                        <div class="project-image">📋 Project Image</div>
                        <h3>Week 1: Summary Notes Challenge</h3>
                        <p>Create a one-page summary of any chapter and present it in class. Winner gets special recognition and their notes shared with everyone.</p>
                        <div class="contributors">Contributors: Barex, Amanuel, Sara, David</div>
                        <a href="#" class="btn" style="margin-top: 1rem;">Join Project</a>
                    </div>
                    <div class="card project-card">
                        <div class="project-status status-done">Completed</div>
                        <div class="project-image">🎤 Presentation</div>
                        <h3>Public Speaking Workshop</h3>
                        <p>A week-long workshop where students practiced presentation skills and overcame stage fright through peer support and practice sessions.</p>
                        <div class="contributors">Contributors: Class of 2024, Barex</div>
                        <a href="#" class="btn" style="margin-top: 1rem;">View Results</a>
                    </div>
                    <div class="card project-card">
                        <div class="project-status status-ongoing">Planning</div>
                        <div class="project-image">📖 Study Group</div>
                        <h3>Peer Teaching Circle</h3>
                        <p>Students take turns teaching difficult topics to classmates. Teaching others is one of the best ways to solidify your own understanding.</p>
                        <div class="contributors">Contributors: Looking for volunteers!</div>
                        <a href="#" class="btn" style="margin-top: 1rem;">Sign Up</a>
                    </div>
                </div>
            </div>
        </section>

        <section class="section" id="blog">
            <div class="container">
                <h2 class="section-title">Latest Lessons</h2>
                <div class="blog-posts">
                    <article class="blog-card">
                        <h3><a href="#">How to Study for Exams (3 Essential Steps)</a></h3>
                        <div class="blog-meta">By Barex • January 15, 2024</div>
                        <p class="blog-excerpt">Exam preparation doesn't have to be stressful. Follow these three proven steps to organize your study time, understand difficult concepts, and perform your best on test day.</p>
                        <a href="#" class="btn">Read More</a>
                    </article>
                    
                    <article class="blog-card">
                        <h3><a href="#">Public Speaking Tips for Class Presentations</a></h3>
                        <div class="blog-meta">By Barex • January 10, 2024</div>
                        <p class="blog-excerpt">Overcome presentation anxiety and deliver confident presentations. Learn practical techniques for organizing your thoughts, engaging your audience, and managing nerves.</p>
                        <a href="#" class="btn">Read More</a>
                    </article>
                    
                    <article class="blog-card">
                        <h3><a href="#">Building Daily Habits That Stick</a></h3>
                        <div class="blog-meta">By Barex • January 5, 2024</div>
                        <p class="blog-excerpt">Small daily habits compound into big results. Discover how to start tiny habits that grow naturally and create lasting positive changes in your academic and personal life.</p>
                        <a href="#" class="btn">Read More</a>
                    </article>
                </div>
            </div>
        </section>

        <section class="section" id="about">
            <div class="container">
                <h2 class="section-title">About Build Your Life</h2>
                <div class="featured-grid">
                    <div>
                        <h3>Who I Am</h3>
                        <p>My name is Barek Yusuf, also known as Barex. I am a 16-year-old student from Ethiopia who is passionate about learning, leadership, and self-improvement.</p>
                        
                        <h3>What Defines Me</h3>
                        <p>I believe education is not only about grades but about building character and discipline. In Grade 9, I graduated at the top of my class, and now in Grade 10, I continue to focus on personal growth, knowledge, and helping others.</p>
                        
                        <h3>My Mission</h3>
                        <p>I want to inspire my fellow students to believe in themselves, develop confidence, and take responsibility for their own growth. This website is part of that mission — a place to share ideas, resources, and encouragement.</p>
                        
                        <p><strong>Thank you for visiting. This is my journey as a student, and I invite you to grow with me.</strong></p>
                        <p>— Barex</p>
                    </div>
                    <div class="featured-image">
                        👨‍🎓 Barex Profile
                    </div>
                </div>
            </div>
        </section>

        <section class="section" id="contact" style="background: var(--muted);">
            <div class="container">
                <h2 class="section-title">Get In Touch</h2>
                <div class="featured-grid">
                    <div>
                        <h3>Contact Information</h3>
                        <p><strong>Telegram Group:</strong> <a href="https://t.me/your_class_group">Join our class group</a></p>
                        <p><strong>Email:</strong> barex.buildyourlife@gmail.com</p>
                        <p><strong>Response Time:</strong> Usually within 24 hours</p>
                        
                        <h3>Best Ways to Reach Me</h3>
                        <ul>
                            <li>Telegram for quick questions</li>
                            <li>Email for detailed discussions</li>
                            <li>Contact form for suggestions</li>
                        </ul>
                    </div>
                    <div>
                        <form name="contact" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
                            <input type="hidden" name="form-name" value="contact">
                            <input type="hidden" name="bot-field">
                            
                            <div class="form-group">
                                <label for="name">Name *</label>
                                <input type="text" id="name" name="name" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="email">Email *</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="subject">Subject</label>
                                <input type="text" id="subject" name="subject">
                            </div>
                            
                            <div class="form-group">
                                <label for="message">Message *</label>
                                <textarea id="message" name="message" required placeholder="Share your thoughts, ask questions, or suggest new topics..."></textarea>
                            </div>
                            
                            <div class="form-group checkbox-group">
                                <input type="checkbox" id="consent" name="consent" required>
                                <label for="consent">I agree to be contacted about class news and updates</label>
                            </div>
                            
                            <button type="submit" class="btn">Send Message</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="site-footer">
        <div class="container">
            <div class="footer-content">
                <div>
                    <h3>Build Your Life</h3>
                    <p>Empowering students through education, discipline, and community. Made with ❤️ for our class.</p>
                </div>
                <div>
                    <h4>Quick Links</h4>
                    <p><a href="#study">Study Tips</a></p>
                    <p><a href="#projects">Projects</a></p>
                    <p><a href="#blog">Blog</a></p>
                    <p><a href="#contact">Contact</a></p>
                </div>
                <div>
                    <h4>Connect</h4>
                    <p><a href="https://t.me/your_class_group">Telegram Group</a></p>
                    <p><a href="mailto:barex.buildyourlife@gmail.com">Email</a></p>
                    <p>Response within 24 hours</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Build Your Life by Barex. Made for our class with dedication and care.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById('menuToggle').addEventListener('click', function () {
            const nav = document.getElementById('mainNav');
            const expanded = this.getAttribute('aria-expanded') === 'true';
            this.setAttribute('aria-expanded', !expanded);
            nav.classList.toggle('hide');
            
            // Change hamburger icon
            this.textContent = expanded ? '☰' : '✕';
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav a').forEach(link => {
            link.addEventListener('click', () => {
                const nav = document.getElementById('mainNav');
                const toggle = document.getElementById('menuToggle');
                nav.classList.add('hide');
                toggle.setAttribute('aria-expanded', 'false');
                toggle.textContent = '☰';
            });
        });

        // Smooth scrolling for anchor links
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

        // Form handling
        const contactForm = document.querySelector('form[name="contact"]');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                const submitBtn = this.querySelector('button[type="submit"]');
                submitBtn.textContent = 'Sending...';
                submitBtn.disabled = true;
                
                // Re-enable after 3 seconds (Netlify will handle the actual submission)
                setTimeout(() => {
                    submitBtn.textContent = 'Send Message';
                    submitBtn.disabled = false;
                }, 3000);
            });
        }

        // Add loading states to buttons
        document.querySelectorAll('.btn').forEach(btn => {
            if (btn.href && btn.href.startsWith('http')) {
                btn.addEventListener('click', function() {
                    if (!this.dataset.loading) {
                        this.dataset.loading = 'true';
                        const originalText = this.textContent;
                        this.textContent = 'Loading...';
                        
                        setTimeout(() => {
                            this.textContent = originalText;
                            delete this.dataset.loading;
                        }, 1000);
                    }
                });
            }
        });

        // Simple analytics (page view tracking)
        if (typeof gtag !== 'undefined') {
            gtag('config', 'GA_TRACKING_ID', {
                page_title: document.title,
                page_location: window.location.href
            });
        }

        // Add fade-in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all cards and sections
        document.querySelectorAll('.card, .section').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });

        // Initialize any lazy loading for images
        if ('loading' in HTMLImageElement.prototype) {
            const images = document.querySelectorAll('img[data-src]');
            images.forEach(img => {
                img.src = img.dataset.src;
                img.removeAttribute('data-src');
            });
        }
    </script>
</body>
</html>
