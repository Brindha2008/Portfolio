# Ex01 Portfolio
## Date:

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

## HTML 
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - BRINDHA A R</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header>
        <div class="logo">BRINDHA A R</div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home / Hero Section with Your Picture -->
    <section id="home" class="hero">
        <div class="hero-content">
            <!-- Fixed image path because profile.jpg is inside the 'images' folder -->
            <img src="images/profile.jpg" alt="BRINDHA A R" class="profile-img">

            <h1>Hello, I'm <span class="highlight">BRINDHA A R</span></h1>
            <h2>COMPUTER SCIENCE DEPT</h2>
            <p>Welcome to my personal portfolio website.</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <h2>About Me</h2>
        <div class="about-container">
            <p>I am BRINDHA A R from the Computer Science Department. I am passionate about technology, coding, web development, and creating functional, attractive web solutions.</p>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>My Projects</h2>
        <div class="project-grid">
            <div class="project-card">
                <h3>Project One</h3>
                <p>A Web Application created using HTML, CSS, and JavaScript layout techniques.</p>
            </div>
            <div class="project-card">
                <h3>Project Two</h3>
                <p>Computer Science research or coding project showcasing responsive designs.</p>
            </div>
            <div class="project-card">
                <h3>Project Three</h3>
                <p>Interactive web design project focusing on user experience and styling.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <h2>Contact Details</h2>
        <p><strong>Name:</strong> BRINDHA A R</p>
        <p><strong>Department:</strong> Computer Science</p>
        <p><strong>Email:</strong> brindha@example.com</p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 BRINDHA A R. All Rights Reserved.</p>
    </footer>

</body>
</html>
```

## CSS
```
/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    scroll-behavior: smooth;
}

body {
    background-color: #0f172a;
    color: #f8fafc;
    line-height: 1.6;
}

/* Header & Navigation Bar */
header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
    background-color: rgba(15, 23, 42, 0.95);
    backdrop-filter: blur(10px);
    z-index: 1000;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: #38bdf8;
    letter-spacing: 1px;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 25px;
}

nav ul li a {
    text-decoration: none;
    color: #f8fafc;
    font-weight: 600;
    transition: color 0.3s ease;
}

nav ul li a:hover {
    color: #38bdf8;
}

/* Hero Section */
.hero {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 80px 20px 0;
}

/* Circular Profile Picture Styling */
.profile-img {
    width: 180px;
    height: 180px;
    object-fit: cover;
    border-radius: 50%;
    border: 4px solid #38bdf8;
    box-shadow: 0 0 25px rgba(56, 189, 248, 0.4);
    margin-bottom: 20px;
    transition: transform 0.3s ease;
}

.profile-img:hover {
    transform: scale(1.05);
}

.hero-content h1 {
    font-size: 2.8rem;
    margin-bottom: 5px;
}

.hero-content h2 {
    font-size: 1.3rem;
    color: #94a3b8;
    font-weight: 500;
    margin-bottom: 15px;
    letter-spacing: 1.5px;
}

.highlight {
    color: #38bdf8;
}

.hero-content p {
    font-size: 1.1rem;
    margin-bottom: 25px;
    color: #cbd5e1;
}

.btn {
    display: inline-block;
    padding: 12px 28px;
    background-color: #38bdf8;
    color: #0f172a;
    text-decoration: none;
    font-weight: bold;
    border-radius: 5px;
    transition: background 0.3s ease, transform 0.2s ease;
}

.btn:hover {
    background-color: #0ea5e9;
    transform: translateY(-2px);
}

/* General Section Layout */
.section {
    padding: 100px 50px 50px;
    max-width: 1100px;
    margin: 0 auto;
}

.section h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    border-bottom: 2px solid #38bdf8;
    display: inline-block;
    padding-bottom: 5px;
}

/* CSS Grid for Layout */
.project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.project-card {
    background-color: #1e293b;
    padding: 25px;
    border-radius: 8px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(56, 189, 248, 0.2);
}

.project-card h3 {
    margin-bottom: 10px;
    color: #38bdf8;
}

/* Footer Styling */
footer {
    text-align: center;
    padding: 20px;
    background-color: #0b0f19;
    color: #64748b;
    margin-top: 50px;
}
```



## OUTPUT

<img width="1905" height="907" alt="image" src="https://github.com/user-attachments/assets/47c4dadf-8359-485d-a3fe-84a228c7846a" />

<img width="1905" height="898" alt="image" src="https://github.com/user-attachments/assets/157420f9-8185-463c-83e2-9c391d9fca71" />

<img width="1883" height="892" alt="image" src="https://github.com/user-attachments/assets/5af231d9-43d6-4334-9709-94f11e70bd3a" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
