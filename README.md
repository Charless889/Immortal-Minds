    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="author" content="Tafadzwa Charles Kachana" />
    <meta name="description" content="Immortal Minds Foundation - Transforming orphaned children's lives through education in Engineering, Technology, and Psychology." />
    <meta name="keywords" content="orphan education, STEM education, psychology support, child development, engineering for kids, technology education" />

    <title>Immortal Minds Foundation</title>

    <link rel="icon" href="https://cdn-icons-png.flaticon.com/512/2913/2913465.png" type="image/png" />

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #0a0a0a;
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Video background styling */
        #bg-video {
            position: fixed;
            right: 0;
            bottom: 0;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: -1;
            object-fit: cover;
            filter: brightness(0.4);
        }

        /* Fallback background if video fails */
        .video-fallback {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            z-index: -2;
        }

        /* Navigation Tabs */
        .tab {
            display: flex;
            justify-content: center;
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(10px);
            padding: 20px;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

            .tab button {
                background: transparent;
                border: 2px solid rgba(255, 255, 255, 0.3);
                color: white;
                padding: 12px 30px;
                margin: 0 10px;
                cursor: pointer;
                font-size: 16px;
                font-weight: 600;
                text-transform: uppercase;
                letter-spacing: 1px;
                transition: all 0.3s ease;
                border-radius: 30px;
                position: relative;
                overflow: hidden;
            }

                .tab button::before {
                    content: '';
                    position: absolute;
                    top: 0;
                    left: -100%;
                    width: 100%;
                    height: 100%;
                    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
                    transition: left 0.5s;
                }

                .tab button:hover::before {
                    left: 100%;
                }

                .tab button:hover {
                    background: rgba(255, 255, 255, 0.1);
                    border-color: #00d4ff;
                    transform: translateY(-2px);
                    box-shadow: 0 5px 20px rgba(0, 212, 255, 0.3);
                }

                .tab button.active {
                    background: linear-gradient(135deg, #00d4ff 0%, #0099cc 100%);
                    border-color: #00d4ff;
                    color: #000;
                    box-shadow: 0 5px 20px rgba(0, 212, 255, 0.4);
                }

        /* Tab Content */
        .tabcontent {
            display: none;
            animation: fadeIn 0.5s ease-in;
            padding: 40px 20px;
            max-width: 1200px;
            margin: 0 auto;
            min-height: calc(100vh - 80px);
        }

            .tabcontent.active {
                display: block;
            }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Home Section */
        #Home {
            text-align: center;
            padding-top: 100px;
        }

            #Home h1 {
                font-size: 4rem;
                margin-bottom: 10px;
                background: linear-gradient(135deg, #00d4ff 0%, #ffffff 100%);
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
                background-clip: text;
                text-shadow: 0 0 30px rgba(0, 212, 255, 0.3);
            }

            #Home h2 {
                font-size: 1.8rem;
                color: #00d4ff;
                margin-bottom: 40px;
                font-weight: 300;
                letter-spacing: 3px;
            }

        .hero-image {
            width: 100%;
            max-width: 600px;
            height: auto;
            border-radius: 20px;
            margin: 30px auto;
            display: block;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
            border: 2px solid rgba(0, 212, 255, 0.3);
        }

        .mission-text {
            color: #e0f7ff;
            font-size: 1.2rem;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto;
            text-align: left;
            background: rgba(0, 0, 0, 0.5);
            padding: 40px;
            border-radius: 15px;
            border-left: 4px solid #00d4ff;
        }

        .quote {
            display: block;
            margin: 30px 0;
            padding: 20px;
            background: rgba(0, 212, 255, 0.1);
            border-left: 4px solid #00d4ff;
            font-style: italic;
            color: #ffffff;
            border-radius: 0 10px 10px 0;
        }

        .tagline {
            display: block;
            margin-top: 30px;
            font-size: 1.3rem;
            color: #00d4ff;
            text-align: center;
            font-weight: 600;
        }

        /* Programs Section */
        #Programmes h1 {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 40px;
            color: #00d4ff;
        }

        .program-stage {
            background: rgba(255, 255, 255, 0.05);
            margin: 30px 0;
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(0, 212, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

            .program-stage:hover {
                transform: translateY(-5px);
                box-shadow: 0 10px 40px rgba(0, 212, 255, 0.2);
            }

            .program-stage h2 {
                color: #00d4ff;
                margin-bottom: 15px;
                font-size: 1.8rem;
            }

            .program-stage ul {
                list-style: none;
                padding-left: 0;
            }

            .program-stage li {
                padding: 8px 0;
                padding-left: 25px;
                position: relative;
            }

                .program-stage li::before {
                    content: '▹';
                    position: absolute;
                    left: 0;
                    color: #00d4ff;
                }

        .impact-box {
            background: rgba(0, 212, 255, 0.1);
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
            border-left: 3px solid #00d4ff;
        }

        .section-image {
            width: 100%;
            max-width: 500px;
            height: auto;
            border-radius: 10px;
            margin: 20px auto;
            display: block;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        /* Contact Section */
        #Contact {
            text-align: center;
        }

            #Contact h1 {
                font-size: 3rem;
                color: #00d4ff;
                margin-bottom: 40px;
            }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(0, 212, 255, 0.2);
            transition: all 0.3s ease;
        }

            .contact-card:hover {
                background: rgba(0, 212, 255, 0.1);
                transform: translateY(-5px);
            }

            .contact-card h3 {
                color: #00d4ff;
                margin-bottom: 15px;
                font-size: 1.5rem;
            }

        .contact-form {
            max-width: 600px;
            margin: 40px auto;
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 15px;
        }

        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }

            .form-group label {
                display: block;
                margin-bottom: 8px;
                color: #00d4ff;
                font-weight: 600;
            }

            .form-group input,
            .form-group textarea {
                width: 100%;
                padding: 12px;
                background: rgba(0, 0, 0, 0.3);
                border: 1px solid rgba(0, 212, 255, 0.3);
                color: white;
                border-radius: 8px;
                font-size: 16px;
                transition: border-color 0.3s;
            }

                .form-group input:focus,
                .form-group textarea:focus {
                    outline: none;
                    border-color: #00d4ff;
                    box-shadow: 0 0 10px rgba(0, 212, 255, 0.3);
                }

        .submit-btn {
            background: linear-gradient(135deg, #00d4ff 0%, #0099cc 100%);
            color: #000;
            border: none;
            padding: 15px 40px;
            font-size: 18px;
            font-weight: 600;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

            .submit-btn:hover {
                transform: translateY(-2px);
                box-shadow: 0 10px 30px rgba(0, 212, 255, 0.4);
            }

        /* Responsive */
        @media (max-width: 768px) {
            .tab {
                flex-wrap: wrap;
                padding: 10px;
            }

                .tab button {
                    margin: 5px;
                    padding: 10px 20px;
                    font-size: 14px;
                }

            #Home h1 {
                font-size: 2.5rem;
            }

            #Home h2 {
                font-size: 1.2rem;
            }

            .mission-text {
                padding: 20px;
                font-size: 1rem;
            }
        }

        /* Loading animation */
        .loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0a0a0a;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.5s;
        }

            .loader.hidden {
                opacity: 0;
                pointer-events: none;
            }

        .loader-circle {
            width: 50px;
            height: 50px;
            border: 3px solid rgba(0, 212, 255, 0.3);
            border-top-color: #00d4ff;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to {
                transform: rotate(360deg);
            }
        }
    </style>
</head>
<body>

    <!-- Loading Screen -->
    <div class="loader" id="loader">
        <div class="loader-circle"></div>
    </div>

    <!-- Video Background -->
    <div class="video-fallback"></div>
    <video autoplay muted loop id="bg-video" playsinline>
        <source src="https://assets.mixkit.co/videos/preview/mixkit-digital-animation-of-a-blue-brain-9887-large.mp4" type="video/mp4">
        <!-- Fallback if video fails -->
        Your browser does not support the video tag.
    </video>

    <!-- Navigation -->
    <div class="tab">
        <button class="tablinks active" onclick="openTab(Event, 'Home')" aria-label="Home">Home</button>
        <button class="tablinks" onclick="openTab(Event, 'Programmes')" aria-label="About Our Programmes">Programmes</button>
        <button class="tablinks" onclick="openTab(Event, 'Contact')" aria-label="Contact Us">Contact</button>
    </div>

    <!-- HOME TAB -->
    <div id="Home" class="tabcontent active">
        <h1>Welcome to Immortal Minds</h1>
        <h2>Where Your Potential is Maximized</h2>

        <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?w=800&auto=format&fit=crop"
             alt="Children learning with technology"
             class="hero-image" />

        <div class="mission-text">
            <p>
                Immortal Minds is a foundation dedicated to transforming the lives of orphaned children through the power of education. We believe that every child, regardless of their background, deserves access to opportunities that unlock their full potential.
            </p>
            <br>
            <p>
                Our focus is centered on three key pillars: <strong>Engineering, Technology, and Psychology</strong>. By combining technical skills with personal development and emotional support, we prepare young minds not only to succeed academically but to thrive in life.
            </p>
            <br>
            <p>
                At Immortal Minds, we are building more than students — we are shaping innovators, problem-solvers, and future leaders who will create lasting change in their communities and beyond.
            </p>
            <br>
            <p>
                Through mentorship, scholarships, hands-on learning, and psychological support, we provide a safe and empowering environment where orphaned children can dream boldly and achieve greatly.
            </p>

            <span class="quote">
                "Education is not the learning of facts, but the training of the mind to think."
                <br>— Albert Einstein
            </span>

            <span class="tagline">
                Education shapes the mind. Support strengthens the heart. Opportunity transforms the future.
                <br><br>
                Join us in building immortal minds.
            </span>
        </div>
    </div>

    <!-- PROGRAMMES TAB -->
    <div id="Programmes" class="tabcontent">
        <h1>Step Into A New World</h1>

        <section id="programs">
            <h1 style="text-align: center; margin-bottom: 40px;">Core Focus Areas</h1>

            <img src="https://kimi-web-img.moonshot.cn/img/letstalkscience.ca/a50443d7166227eb7817538b466813bd4701f0c3.png"
                 alt="Technology and innovation"
                 class="section-image" />

            <p style="text-align: center; max-width: 800px; margin: 0 auto 40px; font-size: 1.2rem;">
                At <strong>Immortal Minds</strong>, we guide orphaned children through a structured
                educational journey from early childhood to young adulthood. Our programs are
                designed to grow with the child, strengthening intellectual, emotional, and
                leadership development at every stage.
            </p>

            <div class="program-stage">
                <h2>Foundation Stage (Ages 6 – 9)</h2>
                <p><strong>Focus:</strong> Curiosity, creativity, and emotional security.</p>
                <img src="https://as2.ftcdn.net/v2/jpg/06/37/50/95/1000_F_637509508_gUcShfWjpGm4HCc7blYyuJIBgNMF2jWv.jpg"
                     alt="Technology and innovation"
                     class="section-image" />
                <ul>
                    <li>Basic Robotics (simple building kits)</li>
                    <li>Introduction to Computers</li>
                    <li>Digital Literacy Basics</li>
                    <li>Emotional Intelligence Skills</li>
                    <li>Confidence Building Activities</li>
                </ul>
                <div class="impact-box">
                    <strong>Development Impact:</strong> Builds confidence, problem-solving skills,
                    teamwork, and emotional awareness during critical early brain development years.
                </div>
            </div>

            <div class="program-stage">
                <h2>Exploration Stage (Ages 10 – 13)</h2>
                <p><strong>Focus:</strong> Skill discovery and structured learning.</p>
                <img src="https://as2.ftcdn.net/v2/jpg/05/62/38/23/1000_F_562382387_5rfYSOZYSj4qXStT8TrRVeLrJJr9l1yd.jpg"
                     alt="Technology and innovation"
                     class="section-image" />
                <ul>
                    <li>Robotics Projects</li>
                    <li>Civil & Mechanical Basics</li>
                    <li>Introduction to Coding & Programming</li>
                    <li>Web Development Basics</li>
                    <li>Mental Health Awareness</li>
                    <li>Leadership Foundations</li>
                </ul>
                <div class="impact-box">
                    <strong>Development Impact:</strong> Strengthens logical thinking, creativity,
                    teamwork, and emotional regulation during early adolescence.
                </div>
            </div>

            <div class="program-stage">
                <h2>Innovation Stage (Ages 14 – 17)</h2>
                <p><strong>Focus:</strong> Advanced skills and career preparation.</p>

                <img src="https://as1.ftcdn.net/v2/jpg/07/33/56/82/1000_F_733568257_37mt7rcArcSSoa0Hr2spj7aYNkNN486M.jpg"
                     alt="Advanced robotics and engineering"
                     class="section-image" />

                <ul>
                    <li>Advanced Robotics & Engineering Projects</li>
                    <li>Civil & Mechanical Engineering Concepts</li>
                    <li>Full Coding & Programming Courses</li>
                    <li>Artificial Intelligence Basics</li>
                    <li>Web Development Projects</li>
                    <li>Leadership Development</li>
                    <li>Counseling & Psychological Support</li>
                </ul>
                <div class="impact-box">
                    <strong>Development Impact:</strong> Prepares learners for university,
                    technical careers, entrepreneurship, and strong emotional resilience.
                </div>
            </div>

            <div class="program-stage">
                <h2>Young Adult Transition (Ages 18 – 21)</h2>
                <p><strong>Focus:</strong> Professional readiness and independence.</p>
                <img src="https://as2.ftcdn.net/v2/jpg/05/10/61/73/1000_F_510617376_IJYuFcp3WOwf1UrVcaaI5LVtscAQHd19.jpg"
                     alt="Advanced robotics and engineering"
                     class="section-image" />
                <ul>
                    <li>Internships & Mentorship Programs</li>
                    <li>Specialized Engineering Training</li>
                    <li>Advanced Technology & AI Applications</li>
                    <li>Career Guidance & Counseling</li>
                    <li>Entrepreneurship Skills</li>
                </ul>

                <div class="impact-box">
                    <strong>Development Impact:</strong> Supports transition into higher education,
                    employment, or entrepreneurship while maintaining strong mental and emotional health.
                </div>
            </div>
        </section>
    </div>

    <!-- CONTACT TAB -->
    <div id="Contact" class="tabcontent">
        <h1>Get In Touch</h1>

        <div class="contact-container">
            <div class="contact-card">
                <h3> Email Us</h3>
                <p>info@immortalminds.org</p>
                <p>support@immortalminds.org</p>
            </div>

            <div class="contact-card">
                <h3> Call Us</h3>
                <p>+263 77 123 4567</p>
                <p>Mon-Fri, 8am-5pm CAT</p>
            </div>

            <div class="contact-card">
                <h3> Visit Us</h3>
                <p>123 Innovation Drive</p>
                <p>Harare, Zimbabwe</p>
            </div>
        </div>

        <div class="contact-form">
            <h2 style="color: #00d4ff; margin-bottom: 30px;">Send us a Message</h2>
            <form onsubmit="handleSubmit(Event)">
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" name="name" required placeholder="Enter your name">
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" required placeholder="Enter your email">
                </div>

                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject" required placeholder="How can we help?">
                </div>

                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" rows="5" required placeholder="Tell us more about your inquiry..."></textarea>
                </div>

                <button type="submit" class="submit-btn">Send Message</button>
            </form>
        </div>
    </div>

    <script>
        // Tab functionality
        function openTab(evt, tabName) {
            // Declare all variables
            var i, tabcontent, tablinks;

            // Get all elements with class="tabcontent" and hide them
            tabcontent = document.getElementsByClassName("tabcontent");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].classList.remove("active");
            }

            // Get all elements with class="tablinks" and remove the class "active"
            tablinks = document.getElementsByClassName("tablinks");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].classList.remove("active");
            }

            // Show the current tab, and add an "active" class to the button that opened the tab
            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");

            // Smooth scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Form submission handler
        function handleSubmit(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            e.target.reset();
        }

        // Remove loader when page loads
        window.addEventListener('load', function () {
            setTimeout(function () {
                document.getElementById('loader').classList.add('hidden');
            }, 500);
        });

        // Video error handling
        document.getElementById('bg-video').addEventListener('error', function () {
            this.style.display = 'none';
            console.log('Video failed to load, using fallback background');
        });
    </script>
</body>
</html>
