<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shuhaib R - Portfolio</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }
        
        /* Container */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            padding: 100px 0 50px;
            text-align: center;
        }
        
        .header-content h1 {
            font-size: 48px;
            margin-bottom: 10px;
        }
        
        .header-content h2 {
            font-size: 24px;
            font-weight: 300;
            margin-bottom: 30px;
        }
        
        /* Navigation */
        nav {
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li a {
            display: block;
            padding: 20px;
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        nav ul li a:hover {
            color: #3498db;
        }
        
        /* Sections */
        section {
            padding: 80px 0;
        }
        
        section h2 {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
            position: relative;
        }
        
        section h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #3498db;
            margin: 15px auto;
        }
        
        /* About */
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            text-align: center;
        }
        
        .profile-img {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #fff;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Education */
        .education-item {
            background: white;
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .education-item:hover {
            transform: translateY(-5px);
        }
        
        .education-item h3 {
            color: #3498db;
            margin-bottom: 10px;
        }
        
        /* Skills */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }
        
        .skill-item {
            background: white;
            border-radius: 8px;
            padding: 20px;
            min-width: 200px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            background: #3498db;
            color: white;
        }
        
        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            color: #3498db;
            margin-bottom: 10px;
        }
        
        /* Contact */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .form-group input, 
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        .form-group textarea {
            min-height: 150px;
        }
        
        .btn {
            display: inline-block;
            background: #3498db;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background: #2980b9;
        }
        
        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        .social-links {
            margin: 20px 0;
        }
        
        .social-links a {
            display: inline-block;
            margin: 0 10px;
            color: white;
            font-size: 20px;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            color: #3498db;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .about-content {
                flex-direction: column;
                text-align: center;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li a {
                padding: 15px;
            }
            
            .header-content h1 {
                font-size: 36px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <h1>Shuhaib R</h1>
            <h2>Computer Science Student & Developer</h2>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>As a driven and detail-oriented computer science student, I've developed a strong foundation in programming languages, data structures, algorithms, and software engineering principles. With a passion for building innovative solutions, I've applied my skills to a range of projects, from web development and mobile app design to artificial intelligence and machine learning.</p>
                    <p>I'm excited to showcase my projects and share my passion for computer science with you.</p>
                </div>
                <div class="about-image">
                    <img src="/api/placeholder/400/400" alt="Shuhaib R" class="profile-img">
                </div>
            </div>
        </div>
    </section>
    
    <!-- Education Section -->
    <section id="education" style="background-color: #f0f4f8;">
        <div class="container">
            <h2>Education</h2>
            <div class="education-item">
                <h3>BSc Computer Science</h3>
                <p><strong>Institution:</strong> Government Arts and Science College, Gudalur</p>
                <p>Pursuing a bachelor's degree in Computer Science, focusing on software development, algorithms, data structures, and system design.</p>
            </div>
        </div>
    </section>
    
    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2>Skills</h2>
            <div class="skills-container">
                <div class="skill-item">
                    <h3>C</h3>
                </div>
                <div class="skill-item">
                    <h3>C++</h3>
                </div>
                <div class="skill-item">
                    <h3>Linux</h3>
                </div>
                <div class="skill-item">
                    <h3>Java</h3>
                </div>
                <div class="skill-item">
                    <h3>HTML/CSS</h3>
                </div>
                <div class="skill-item">
                    <h3>Web Development</h3>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Projects Section -->
    <section id="projects" style="background-color: #f0f4f8;">
        <div class="container">
            <h2>Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-content">
                        <h3>E-Cart Website</h3>
                        <p>An e-commerce platform with product browsing, shopping cart functionality, user authentication, and payment processing.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3>Cloud Security IBM</h3>
                        <p>Implementation of cloud security solutions using IBM technologies to protect data and applications in cloud environments.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3>IBM Chatbot</h3>
                        <p>Development of an intelligent chatbot using IBM Watson to provide automated responses and assistance to users.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3>College Portal</h3>
                        <p>A comprehensive portal for college management, featuring student information, course registration, grade tracking, and administrative tools.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2>Contact Me</h2>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" required></textarea>
                    </div>
                    
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#">LinkedIn</a>
                <a href="#">GitHub</a>
                <a href="#">Email</a>
            </div>
            <p>&copy; 2025 Shuhaib R. All Rights Reserved.</p>
        </div>
    </footer>
</body>
</html>