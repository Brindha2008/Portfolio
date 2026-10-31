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
    <title>BRINDHA A R - Portfolio</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: #ffffff;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            z-index: 1000;
        }

        .logo {
            font-size: 20px;
            font-weight: bold;
            color: #007bff;
        }

        nav {
            display: flex;
            gap: 20px;
        }

        nav a {
            text-decoration: none;
            color: #555;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #007bff;
        }

        /* Hero / Introduction Section with Profile Image */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://picsum.photos/1920/1080') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 0 20px;
        }

        .profile-img {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #fff;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            margin-bottom: 20px;
        }

        .hero-content h1 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        .hero-content p {
            font-size: 18px;
            margin-bottom: 25px;
        }

        /* General Sections */
        .section {
            padding: 100px 50px 80px;
            text-align: center;
        }

        .alt-bg {
            background-color: #f1f3f5;
        }

        .section h2 {
            font-size: 36px;
            margin-bottom: 20px;
            color: #222;
        }

        /* Projects Cards Layout (Flexbox) */
        .card-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .card {
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            width: 300px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 15px rgba(0,0,0,0.1);
        }

        .card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .card h3 {
            margin: 15px 0 10px;
            color: #333;
        }

        .card p {
            padding: 0 15px 20px;
            color: #666;
            font-size: 14px;
        }

        /* Buttons & Text */
        .btn {
            display: inline-block;
            background: #007bff;
            color: #fff;
            padding: 10px 25px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .btn:hover {
            background: #0056b3;
        }

        .about-text {
            max-width: 700px;
            margin: 0 auto;
            color: #555;
            font-size: 18px;
        }

        .contact-info {
            margin-top: 20px;
            font-size: 18px;
            color: #555;
        }

        /* Footer */
        footer {
            background: #222;
            color: #fff;
            text-align: center;
            padding: 30px 20px;
        }
    </style>
</head>
<body>

    <!-- Header & Navigation Bar -->
    <header>
        <div class="logo">BRINDHA A R</div>
        <nav>
            <a href="#intro">Home</a>
            <a href="#about">About</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <!-- Introduction Section with Profile Image -->
    <section id="intro" class="hero">
        <img src="images/profile.jpg" alt="BRINDHA A R" class="profile-img">
        <div class="hero-content">
            <h1>Hello, I'm BRINDHA A R</h1>
            <p>Welcome to my professional portfolio showcasing my projects and skills as a Web Developer.</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section alt-bg">
        <h2>About Me</h2>
        <p class="about-text">I am a passionate developer focused on building clean, responsive, and user-friendly web applications using modern technologies.</p>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>My Projects</h2>
        <div class="card-container">
            <div class="card">
                <img src="https://picsum.photos/300/180?random=1" alt="Project 1">
                <h3>Project One</h3>
                <p>A responsive web application built with HTML, CSS, and JavaScript.</p>
            </div>
            <div class="card">
                <img src="https://picsum.photos/300/180?random=2" alt="Project 2">
                <h3>Project Two</h3>
                <p>An interactive portfolio design featuring modern layout techniques.</p>
            </div>
            <div class="card">
                <img src="https://picsum.photos/300/180?random=3" alt="Project 3">
                <h3>Project Three</h3>
                <p>A dynamic user interface optimized for performance and experience.</p>
            </div>
        </div>
    </section>

    <!-- Contact Details Section -->
    <section id="contact" class="section alt-bg">
        <h2>Contact Details</h2>
        <p>Feel free to reach out to me for collaborations or inquiries.</p>
        <div class="contact-info">
            <p><strong>Email:</strong> brindha@example.com</p>
            <p><strong>Phone:</strong> +1 (555) 987-6543</p>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 BRINDHA A R. All rights reserved.</p>
    </footer>

</body>
</html>
```




## OUTPUT
<img width="1917" height="907" alt="image" src="https://github.com/user-attachments/assets/e5ac6e87-b560-4328-ba72-3c938e631a34" />
<img width="1917" height="976" alt="image" src="https://github.com/user-attachments/assets/dc3c1f3c-d4bc-4b26-8b9f-b622d567f9c7" />
<img width="1917" height="1040" alt="image" src="https://github.com/user-attachments/assets/e7bd46e0-86a5-44a2-9500-d1394f009b98" />




## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
