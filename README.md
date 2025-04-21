<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yafet Hailu | Computer Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #4E2A84; /* Northwestern purple */
            --secondary: #0366d6;
            --dark: #212121;
            --light: #f8f9fa;
            --success: #28a745;
            --info: #17a2b8;
            --warning: #ffc107;
            --danger: #dc3545;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--dark);
            background-color: var(--light);
            line-height: 1.6;
        }
        
        a {
            text-decoration: none;
            color: var(--secondary);
            transition: all 0.3s ease;
        }
        
        a:hover {
            color: var(--primary);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--dark);
            font-weight: 500;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        

        /* Hamburger menu for mobile */
        .menu-toggle {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }
        
        /* Hero section */
        .hero {
            padding: 150px 0 100px;
            text-align: center;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        
        .profile-pic {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 4px solid var(--secondary);
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            margin: 0 auto 30px;
            object-fit: cover;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 30px;
        }
        
        .badge {
            background-color: var(--dark);
            color: white;
            padding: 8px 16px;
            border-radius: 50px;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .badge.purple {
            background-color: purple;
        }
        
        .badge.blue {
            background-color: var(--secondary);
        }
        
        .badge.nu {
            background-color: var(--primary);
        }
        
        .quote {
            font-style: italic;
            border-left: 4px solid var(--primary);
            padding-left: 20px;
            max-width: 800px;
            margin: 0 auto;
        }
        
        /* Section styling */
        section {
            padding: 80px 0;
        }
        
        section:nth-child(even) {
            background-color: #f8f9fa;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background-color: var(--secondary);
            margin: 10px auto 0;
        }
        
        /* Projects */
        .projects-grid,
        .hardware-grid,
        .passion-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-desc {
            margin-bottom: 15px;
            color: #666;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .project-tag {
            background-color: #e9ecef;
            color: #495057;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 0.8rem;
        }
        
        .project-links {
            display: flex;
            gap: 15px;
        }
        
        .project-link {
            padding: 8px 15px;
            background-color: var(--secondary);
            color: white;
            border-radius: 4px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .project-link:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Connect Section */
        .connect {
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            font-size: 2rem;
            margin-top: 30px;
        }
        
        .social-links a {
            color: var(--dark);
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--primary);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .nav-links {
                display: none;
                flex-direction: column;
                width: 100%;
                margin-top: 20px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 10px 0;
            }
            
            .menu-toggle {
                display: block;
                position: absolute;
                top: 20px;
                right: 20px;
            }
            
            .hero {
                padding: 120px 0 80px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Yafet Hailu</div>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
                <ul class="nav-links">
                    <li><a href="#about">About</a></li>
                    <li><a href="#software">Software Projects</a></li>
                    <li><a href="#hardware">Hardware Projects</a></li>
                    <li><a href="#passion">Passion Projects</a></li>
                    <li><a href="#connect">Connect</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="about">
        <div class="container">
            <img src="/api/placeholder/200/200" alt="Yafet Hailu" class="profile-pic">
            <h1>Hello World! 👋 I'm Yafet</h1>
            
            <div class="badges">
                <div class="badge purple">
                    <i class="fas fa-microchip"></i> Computer Engineering
                </div>
                <div class="badge blue">
                    <i class="fas fa-brain"></i> ML & Data Science
                </div>
                <div class="badge nu">
                    <i class="fas fa-university"></i> Northwestern '26
                </div>
            </div>
            
            <div class="quote">
                <p>💡 Passionate about building innovative solutions at the intersection of software & hardware</p>
                <p>🎓 Currently exploring System Software and Computer Architecture</p>
                <p>🤖 Working on robotics and embedded systems projects</p>
            </div>
        </div>
    </section>
    
    <!-- Software Projects -->
    <section id="software">
        <div class="container">
            <h2 class="section-title">👨‍💻 Software Development Projects</h2>
            
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Tom & Jerry Cloud Chase Game</h3>
                        <p class="project-desc">Written over 2000 lines of code in ARM assembly to design an interactive tom and jerry chasing game.</p>
                        <div class="project-tags">
                            <span class="project-tag">C</span>
                            <span class="project-tag">ARM Assembly</span>
                            <span class="project-tag">Pseudocode</span>
                        </div>
                        <div class="project-links">
                            <a href="https://docs.google.com/document/d/1BqEZzUOgDm5AOslF-2MKjSonROjrSVq2eyBfkXSExuA/edit?usp=sharing" class="project-link" target="_blank">
                                <i class="fas fa-code"></i> Code
                            </a>
                            <a href="https://youtu.be/KjnQi0JLn8s?si=26kwtI3CYzWU6DZs" class="project-link" target="_blank">
                                <i class="fas fa-play-circle"></i> Demo
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Ethiopian Medical Students Association Website</h3>
                        <p class="project-desc">Developed responsive website for the Ethiopian Medical Students Association.</p>
                        <div class="project-tags">
                            <span class="project-tag">HTML</span>
                            <span class="project-tag">CSS</span>
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">React</span>
                        </div>
                        <div class="project-links">
                            <a href="https://yafethailu.github.io/EMSAsite/" class="project-link" target="_blank">
                                <i class="fas fa-globe"></i> Live Site
                            </a>
                            <a href="https://github.com/yafethailu/EMSAsite.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                            <a href="https://youtu.be/SJZf9dYf8ag" class="project-link" target="_blank">
                                <i class="fas fa-play-circle"></i> Demo
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">University Campus Navigator</h3>
                        <p class="project-desc">A C++ application to parse and visualize campus map data, displaying building locations and nearby bus stops using XML and JSON.</p>
                        <div class="project-tags">
                            <span class="project-tag">C++</span>
                            <span class="project-tag">API Integration</span>
                            <span class="project-tag">JSON</span>
                            <span class="project-tag">XML</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/OpenStreetMaps.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                            <a href="https://github.com/yafethailu/OpenStreetMaps.git" class="project-link" target="_blank">
                                <i class="fas fa-file-alt"></i> ReadMe
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 4 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">nuPython C Parser</h3>
                        <p class="project-desc">Developed a Python-like language parser in C, creating an execution environment using token-based processing.</p>
                        <div class="project-tags">
                            <span class="project-tag">C</span>
                            <span class="project-tag">API Integration</span>
                            <span class="project-tag">JSON</span>
                            <span class="project-tag">XML</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/nuPython.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Hardware Projects -->
    <section id="hardware">
        <div class="container">
            <h2 class="section-title">📺 Hardware Development Projects</h2>
            
            <div class="hardware-grid">
                <!-- Hardware Project 1 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Pipelined RISC-V CPU</h3>
                        <p class="project-desc">Designed a fully functional RISC-V CPU using Verilog with pipelining and a 32-bit execution unit.</p>
                        <div class="project-tags">
                            <span class="project-tag">Verilog</span>
                            <span class="project-tag">RISC-V Assembly</span>
                            <span class="project-tag">C/C++</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/RISC-V-CPU.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Hardware Project 2 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">SRAM Bank</h3>
                        <p class="project-desc">Developed a 4x4 SRAM bank with 6T SRAM cells, a clocked sense amplifier, bitline conditioning, and write circuitry.</p>
                        <div class="project-tags">
                            <span class="project-tag">Cadence Virtuoso</span>
                        </div>
                    </div>
                </div>
                
                <!-- Hardware Project 3 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Lacrosse Robot Goalkeeper</h3>
                        <p class="project-desc">Designing an automated lacrosse goalkeeper for the women's lacrosse team using computer vision for real-time ball tracking.</p>
                        <div class="project-tags">
                            <span class="project-tag">Python</span>
                            <span class="project-tag">NVIDIA Jetson</span>
                            <span class="project-tag">C/C++</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/NUROBOTICS-LAX-24.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Hardware Project 4 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Audio Spectrum Visualizer</h3>
                        <p class="project-desc">Employed an Analog microphone and ESP32 microcontroller to construct an 8x8 LED matrix with audio spectrum visualization.</p>
                        <div class="project-tags">
                            <span class="project-tag">ESP32</span>
                            <span class="project-tag">Arduino</span>
                            <span class="project-tag">Breadboarding</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/audiospectrum.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Hardware Project 5 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Weight Wizard</h3>
                        <p class="project-desc">Prototyped a smart weight scale with wireless display and vibration feedback for patients with lower extremity injuries during physiotherapy.</p>
                        <div class="project-tags">
                            <span class="project-tag">ESP32</span>
                            <span class="project-tag">Wireless Display</span>
                            <span class="project-tag">C/C++</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/WeightWizard.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Passion Projects -->
    <section id="passion">
        <div class="container">
            <h2 class="section-title">😄 Passion Projects</h2>
            
            <div class="passion-grid">
                <!-- Passion Project 1 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Milo's MOSFET Adventure</h3>
                        <p class="project-desc">A children's book on the concept of MOSFETs made for children between ages 6-9 with hand-drawn animations.</p>
                        <div class="project-tags">
                            <span class="project-tag">Canva</span>
                            <span class="project-tag">Children's Book</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/Milo-s-MOSFET-adventures.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Passion Project 2 -->
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Bu and Bo Discover Machine Learning</h3>
                        <p class="project-desc">A children's book on Machine Learning and its applications for children ages 6-9 with hand-drawn animations.</p>
                        <div class="project-tags">
                            <span class="project-tag">Canva</span>
                            <span class="project-tag">Children's Book</span>
                        </div>
                        <div class="project-links">
                            <a href="https://github.com/yafethailu/Book2.git" class="project-link" target="_blank">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Connect Section -->
    <section id="connect" class="connect">
        <div class="container">
            <h2 class="section-title">Connect With Me</h2>
            <p>Feel free to reach out for collaborations or just a friendly chat!</p>
            
            <div class="social-links">
                <a href="https://www.linkedin.com/in/yafet-hailu-a8b854205" target="_blank">
                    <i class="fab fa-linkedin"></i>
                </a>
                <a href="https://www.instagram.com/vaffabraham_16/" target="_blank">
                    <i class="fab fa-instagram"></i>
                </a>
                <a href="https://github.com/yafethailu" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 Yafet Hailu. All rights reserved.</p>
        </div>
    </footer>
    
    <script>
        // Mobile menu functionality
        document.querySelector('.menu-toggle').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector('.nav-links').classList.remove('active');
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Add fixed header background when scrolling
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
            } else {
                header.style.boxShadow = 'none';
            }
        });
    </script>
</body>
</html>
