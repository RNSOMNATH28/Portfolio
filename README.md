# Ex01 Portfolio
## Date: 30/10/2026
## NAME: R N SOMNATH
## REGISTER NO : 212224240158

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Somnath R.N. | Portfolio</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: 'Inter', sans-serif;
    background: #08090d;
    color: #ffffff;
    overflow-x: hidden;
}

/* Background grid */

body::before {
    content: "";
    position: fixed;
    inset: 0;
    background-image:
        linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
    background-size: 45px 45px;
    pointer-events: none;
    z-index: -1;
}

/* Navigation */

header {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 20px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(8,9,13,0.88);
    backdrop-filter: blur(15px);
    border-bottom: 1px solid #202127;
    z-index: 1000;
}

.logo {
    font-size: 22px;
    font-weight: 800;
    color: white;
}

.logo span {
    color: #4d8dff;
}

nav {
    display: flex;
    gap: 32px;
}

nav a {
    text-decoration: none;
    color: #aaa;
    font-size: 13px;
    transition: 0.3s;
}

nav a:hover,
nav a.active {
    color: #5b9cff;
}

.menu {
    display: none;
    font-size: 26px;
    cursor: pointer;
}

/* Common sections */

section {
    padding: 110px 10%;
    scroll-margin-top: 65px;
}

.section-label {
    color: #5797ff;
    font-size: 13px;
    letter-spacing: 3px;
    margin-bottom: 15px;
    text-transform: uppercase;
}

.section-title {
    font-size: 38px;
    margin-bottom: 35px;
}

.gradient {
    background: linear-gradient(90deg, #ffffff, #579aff);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
}

/* Home */

#home {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
    padding-top: 140px;
}

.hero-content {
    max-width: 700px;
}

.intro {
    color: #579aff;
    font-size: 14px;
    margin-bottom: 20px;
    letter-spacing: 2px;
}

.hero-content h1 {
    font-size: clamp(45px, 7vw, 78px);
    line-height: 1.12;
    font-weight: 800;
    margin-bottom: 20px;
}

.hero-content h2 {
    font-size: 25px;
    color: #aaa;
    margin-bottom: 25px;
}

.hero-content p {
    color: #999;
    line-height: 1.9;
    font-size: 15px;
    max-width: 590px;
}

.hero-buttons {
    display: flex;
    gap: 15px;
    margin-top: 35px;
    flex-wrap: wrap;
}

.btn {
    padding: 13px 25px;
    border-radius: 7px;
    text-decoration: none;
    font-size: 13px;
    font-weight: 600;
    transition: 0.3s;
}

.primary {
    background: #438aff;
    color: white;
}

.primary:hover {
    background: #246bd8;
    transform: translateY(-3px);
}

.secondary {
    border: 1px solid #444;
    color: white;
}

.secondary:hover {
    border-color: #579aff;
    color: #579aff;
}

.socials {
    display: flex;
    gap: 22px;
    margin-top: 35px;
}

.socials a {
    color: #aaa;
    text-decoration: none;
    font-size: 14px;
}

.socials a:hover {
    color: #579aff;
}

/* Hero card */

.hero-card {
    width: 290px;
    min-width: 250px;
    padding: 35px;
    border: 1px solid #252a36;
    border-radius: 18px;
    background: linear-gradient(145deg, #151a25, #0d0f15);
    text-align: center;
    box-shadow: 0 0 60px rgba(55,120,255,0.08);
}

.avatar {
    width: 115px;
    height: 115px;
    border-radius: 50%;
    margin: auto auto 22px;
    background: linear-gradient(135deg, #2563eb, #101a35);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 42px;
    font-weight: 800;
}

.hero-card h3 {
    margin-bottom: 10px;
}

.hero-card p {
    color: #999;
    font-size: 13px;
    line-height: 1.8;
}

/* About */

.content-box {
    border: 1px solid #252a36;
    background: #101219;
    padding: 30px;
    border-radius: 12px;
}

.content-box p {
    color: #aaa;
    line-height: 2;
    font-size: 14px;
}

/* Skills */

.skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
}

.skill-card {
    padding: 25px;
    border: 1px solid #252a36;
    border-radius: 10px;
    background: #101219;
    transition: 0.3s;
}

.skill-card:hover {
    transform: translateY(-5px);
    border-color: #438aff;
}

.skill-card h3 {
    color: #579aff;
    margin-bottom: 13px;
    font-size: 16px;
}

.skill-card p {
    color: #999;
    font-size: 13px;
    line-height: 1.9;
}

/* Projects */

.projects-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 22px;
}

.project-card {
    background: #101219;
    border: 1px solid #252a36;
    border-radius: 12px;
    padding: 28px;
    transition: 0.3s;
}

.project-card:hover {
    transform: translateY(-5px);
    border-color: #438aff;
}

.project-card .number {
    color: #579aff;
    font-size: 13px;
    margin-bottom: 20px;
}

.project-card h3 {
    font-size: 19px;
    margin-bottom: 15px;
}

.project-card p {
    color: #999;
    font-size: 13px;
    line-height: 1.9;
}

.tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 20px;
}

.tags span {
    background: #1a2539;
    color: #79aaff;
    padding: 7px 11px;
    border-radius: 5px;
    font-size: 11px;
}

/* Experience */

.experience-card {
    padding: 28px;
    border-left: 2px solid #438aff;
    background: #101219;
    border-radius: 0 10px 10px 0;
}

.experience-card h3 {
    margin-bottom: 10px;
}

.experience-card p {
    color: #999;
    font-size: 14px;
    line-height: 1.9;
}

/* Contact */

.contact-box {
    text-align: center;
    padding: 50px 25px;
    border: 1px solid #252a36;
    border-radius: 15px;
    background: #101219;
}

.contact-box h2 {
    font-size: 32px;
    margin-bottom: 18px;
}

.contact-box p {
    color: #999;
    line-height: 1.8;
    margin-bottom: 25px;
}

footer {
    text-align: center;
    padding: 25px;
    color: #777;
    border-top: 1px solid #252a36;
    font-size: 12px;
}

/* Responsive */

@media(max-width: 850px) {
    header {
        padding: 18px 6%;
    }

    .menu {
        display: block;
    }

    nav {
        display: none;
        position: absolute;
        top: 70px;
        left: 0;
        width: 100%;
        background: #101219;
        padding: 25px;
        flex-direction: column;
        align-items: center;
        border-bottom: 1px solid #252a36;
    }

    nav.show {
        display: flex;
    }

    #home {
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
    }

    .hero-card {
        width: 100%;
    }

    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 550px) {
    section {
        padding: 90px 7%;
    }

    .skills-grid,
    .projects-grid {
        grid-template-columns: 1fr;
    }

    .section-title {
        font-size: 30px;
    }

    .hero-content h2 {
        font-size: 20px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">SOMNATH<span>.</span></div>

    <div class="menu" onclick="toggleMenu()">☰</div>

    <nav id="navbar">
        <a href="#home" class="active">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<!-- HOME -->

<section id="home">

    <div class="hero-content">

        <div class="intro">HELLO, WELCOME TO MY PORTFOLIO</div>

        <h1>
            I'm <span class="gradient">Somnath R.N.</span>
        </h1>

        <h2>AI & Machine Learning Student | Developer</h2>

        <p>
            I am an aspiring AI and Machine Learning developer
            passionate about building intelligent applications
            and solving real-world problems through technology.
            I enjoy exploring machine learning, deep learning,
            web development and innovative software solutions.
        </p>

        <div class="hero-buttons">
            <a href="#projects" class="btn primary">Explore Projects →</a>
            <a href="resume.pdf" download class="btn secondary">Download Resume ↓</a>
        </div>

        <div class="socials">
            <a href="https://github.com/RNSOMNATH28" target="_blank">GitHub ↗</a>
            <a href="https://www.linkedin.com/" target="_blank">LinkedIn ↗</a>
        </div>

    </div>

    <div class="hero-card">
        <div class="avatar">SR</div>
        <h3>Somnath R.N.</h3>
        <p>
            AI & ML Student<br>
            Developer & Problem Solver<br>
            Passionate about Innovation
        </p>
    </div>

</section>

<!-- ABOUT -->

<section id="about">

    <div class="section-label">01 / ABOUT ME</div>
    <h2 class="section-title">A Little <span class="gradient">About Me</span></h2>

    <div class="content-box">
        <p>
            I am an Artificial Intelligence and Machine Learning
            student at Saveetha Engineering College, interested
            in developing intelligent systems and modern
            applications.

            My technical interests include Python programming,
            machine learning, deep learning, data science and
            full-stack web development.

            I believe in continuous learning, teamwork and
            practical implementation. I follow Agile development
            practices using Scrum and Kanban frameworks to
            organize tasks, collaborate with teams and deliver
            projects efficiently.

            My goal is to become a skilled AI/ML engineer and
            contribute to meaningful technology solutions.
        </p>
    </div>

</section>

<!-- SKILLS -->

<section id="skills">

    <div class="section-label">02 / TECHNICAL EXPERTISE</div>
    <h2 class="section-title">My <span class="gradient">Skills</span></h2>

    <div class="skills-grid">

        <div class="skill-card">
            <h3>Programming</h3>
            <p>Python, C, JavaScript</p>
        </div>

        <div class="skill-card">
            <h3>AI & Machine Learning</h3>
            <p>Machine Learning, Deep Learning, CNN, Classification, Prediction</p>
        </div>

        <div class="skill-card">
            <h3>Web Development</h3>
            <p>HTML, CSS, JavaScript, React, Django</p>
        </div>

        <div class="skill-card">
            <h3>Data Science</h3>
            <p>NumPy, Pandas, Matplotlib, Data Analysis</p>
        </div>

        <div class="skill-card">
            <h3>Database</h3>
            <p>MySQL, PostgreSQL, SQL</p>
        </div>

        <div class="skill-card">
            <h3>Tools & Methodologies</h3>
            <p>Git, GitHub, VS Code, Agile, Scrum, Kanban</p>
        </div>

    </div>

</section>

<!-- PROJECTS -->

<section id="projects">

    <div class="section-label">03 / MY WORK</div>
    <h2 class="section-title">Featured <span class="gradient">Projects</span></h2>

    <div class="projects-grid">

        <div class="project-card">
            <div class="number">PROJECT 01</div>
            <h3>Brain Tumor Classification</h3>
            <p>
                An AI-based medical image classification
                project that uses deep learning and Vision
                Transformer architectures to classify brain
                tumors from MRI images, with explainability
                techniques such as Grad-CAM and LIME.
            </p>
            <div class="tags">
                <span>Python</span>
                <span>Deep Learning</span>
                <span>ViT</span>
                <span>Grad-CAM</span>
            </div>
        </div>

        <div class="project-card">
            <div class="number">PROJECT 02</div>
            <h3>Chest X-ray Disease Detection</h3>
            <p>
                A deep learning-based medical image analysis
                system designed to classify diseases from
                chest X-ray images and provide interpretable
                predictions using explainable AI techniques.
            </p>
            <div class="tags">
                <span>Python</span>
                <span>CNN</span>
                <span>Deep Learning</span>
                <span>LIME</span>
            </div>
        </div>

        <div class="project-card">
            <div class="number">PROJECT 03</div>
            <h3>MR.BOT Voice Assistant</h3>
            <p>
                A Python-based voice assistant featuring
                voice-activated search, dynamic to-do lists,
                weather forecasting and additional
                productivity functionalities.
            </p>
            <div class="tags">
                <span>Python</span>
                <span>Voice Assistant</span>
                <span>Automation</span>
            </div>
        </div>

        <div class="project-card">
            <div class="number">PROJECT 04</div>
            <h3>Birthday Wishes Website</h3>
            <p>
                An interactive birthday greeting website
                featuring creative animations, elegant
                styling and personalized messages using
                modern web technologies.
            </p>
            <div class="tags">
                <span>HTML</span>
                <span>CSS</span>
                <span>JavaScript</span>
            </div>
            <br>
            <a href="https://github.com/RNSOMNATH28/birthday-wishes"
               target="_blank" class="secondary btn">
                View Project ↗
            </a>
        </div>

    </div>

</section>

<!-- EXPERIENCE -->

<section id="experience">

    <div class="section-label">04 / EXPERIENCE</div>
    <h2 class="section-title">My <span class="gradient">Experience</span></h2>

    <div class="experience-card">
        <h3>Web Development Intern</h3>
        <p style="color:#579aff; margin-bottom:12px;">
            Arjun Vision Tech | July 2025 – August 2025
        </p>
        <p>
            Worked on web development using HTML, CSS and
            JavaScript. Developed practical applications
            including a simple calculator and weather
            detection project while gaining experience in
            frontend development and implementation.
        </p>
    </div>

</section>

<!-- CONTACT -->

<section id="contact">

    <div class="section-label">05 / GET IN TOUCH</div>

    <div class="contact-box">

        <h2>Let's <span class="gradient">Connect</span></h2>

        <p>
            Interested in collaborating, discussing technology
            or exploring opportunities? Feel free to connect
            with me.
        </p>

        <a href="https://github.com/RNSOMNATH28"
           target="_blank" class="btn primary">
            Visit My GitHub ↗
        </a>

        <a href="mailto:YOUR_EMAIL@gmail.com"
           class="btn secondary">
            Email Me
        </a>

    </div>

</section>

<footer>
    © 2026 Somnath R.N. | Designed & Developed by Somnath
</footer>

<script>
function toggleMenu() {
    document.getElementById("navbar").classList.toggle("show");
}

const navLinks = document.querySelectorAll("nav a");

navLinks.forEach(link => {
    link.addEventListener("click", () => {
        document.getElementById("navbar").classList.remove("show");
    });
});

const sections = document.querySelectorAll("section");

window.addEventListener("scroll", () => {
    let current = "";

    sections.forEach(section => {
        const top = section.offsetTop - 150;

        if (window.scrollY >= top) {
            current = section.getAttribute("id");
        }
    });

    navLinks.forEach(link => {
        link.classList.remove("active");

        if (link.getAttribute("href") === "#" + current) {
            link.classList.add("active");
        }
    });
});
</script>

</body>
</html>
```

## OUTPUT

<img width="1917" height="1198" alt="image" src="https://github.com/user-attachments/assets/4ee65fba-3f07-4eae-a013-8232db7cdb70" />
<img width="1917" height="1198" alt="image" src="https://github.com/user-attachments/assets/e3086280-4fe1-4d34-9bdc-0acca2561fc4" />
<img width="1917" height="1198" alt="image" src="https://github.com/user-attachments/assets/bffc25a8-22d9-4a56-8453-2e8265bbad6d" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
