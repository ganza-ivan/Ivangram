# Ivangram

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudyHub - Learn Better</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation bar -->
    <header>
        <nav class="navbar">
            <h1 class="logo">Study<span>Hub</span></h1>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#courses">Courses</a></li>
                <li><a href="#about">About</a></li>
            </ul>

            <button class="login-btn" onclick="login()">Login</button>
        </nav>
    </header>

    <!-- Home section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h2>Learn Something <span>New</span> Every Day</h2>

            <p>
                Welcome to StudyHub! Discover courses, improve your skills,
                and achieve your academic goals.
            </p>

            <a href="#courses" class="start-btn">Start Learning</a>
        </div>
    </section>

    <!-- Search section -->
    <section class="search-section">
        <h2>Find Your Course</h2>

        <input type="text" id="searchInput"
               placeholder="Search for a course...">

        <button onclick="searchCourse()">Search</button>
    </section>

    <!-- Courses section -->
    <section class="courses" id="courses">
        <h2>Popular Courses</h2>

        <div class="course-container">

            <div class="course-card">
                <div class="course-icon">💻</div>
                <h3>Web Development</h3>
                <p>Learn HTML, CSS and JavaScript to build websites.</p>
                <button onclick="openCourse('Web Development')">
                    Learn More
                </button>
            </div>

            <div class="course-card">
                <div class="course-icon">📊</div>
                <h3>Mathematics</h3>
                <p>Improve your mathematical and problem-solving skills.</p>
                <button onclick="openCourse('Mathematics')">
                    Learn More
                </button>
            </div>

            <div class="course-card">
                <div class="course-icon">🌍</div>
                <h3>English</h3>
                <p>Improve your grammar, writing and communication.</p>
                <button onclick="openCourse('English')">
                    Learn More
                </button>
            </div>

            <div class="course-card">
                <div class="course-icon">🔬</div>
                <h3>Science</h3>
                <p>Explore science and understand how the world works.</p>
                <button onclick="openCourse('Science')">
                    Learn More
                </button>
            </div>

        </div>
    </section>

    <!-- About section -->
    <section class="about" id="about">
        <h2>About StudyHub</h2>

        <p>
            StudyHub is an educational website designed to help students
            learn easily, access educational resources, and develop new skills.
        </p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 StudyHub. All rights reserved.</p>
        <p>Learn Today, Succeed Tomorrow.</p>
    </footer>

    <script src="script.js"></script>

</body>
</html>

/* General styling */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f7fb;
    color: #333;
}

/* Navigation bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 8%;
    background-color: white;
}

.logo {
    color: #2563eb;
    font-size: 28px;
}

.logo span {
    color: #333;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 30px;
}

.nav-links a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
}

.nav-links a:hover {
    color: #2563eb;
}

.login-btn {
    background-color: #2563eb;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

/* Hero section */
.hero {
    background: linear-gradient(120deg, #2563eb, #60a5fa);
    color: white;
    padding: 100px 8%;
    text-align: center;
}

.hero-content h2 {
    font-size: 45px;
    margin-bottom: 20px;
}

.hero-content h2 span {
    color: #ffdd57;
}

.hero-content p {
    font-size: 18px;
    margin-bottom: 30px;
}

.start-btn {
    display: inline-block;
    text-decoration: none;
    background-color: white;
    color: #2563eb;
    padding: 14px 25px;
    border-radius: 8px;
    font-weight: bold;
}

.start-btn:hover {
    background-color: #e5e7eb;
}

/* Search section */
.search-section {
    text-align: center;
    padding: 50px 20px;
}

.search-section h2 {
    margin-bottom: 20px;
}

.search-section input {
    width: 300px;
    max-width: 90%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.search-section button {
    padding: 12px 20px;
    background-color: #2563eb;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

/* Courses section */
.courses {
    padding: 50px 8%;
    text-align: center;
}

.courses h2 {
    margin-bottom: 30px;
    font-size: 30px;
}

.course-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 25px;
}

.course-card {
    background-color: white;
    width: 250px;
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s;
}

.course-card:hover {
    transform: translateY(-5px);
}

.course-icon {
    font-size: 45px;
    margin-bottom: 15px;
}

.course-card h3 {
    margin-bottom: 15px;
}

.course-card p {
    line-height: 1.6;
    margin-bottom: 20px;
}

.course-card button {
    background-color: #2563eb;
    color: white;
    border: none;
    padding: 10px 18px;
    border-radius: 5px;
    cursor: pointer;
}

.course-card button:hover {
    background-color: #1d4ed8;
}

/* About section */
.about {
    background-color: white;
    text-align: center;
    padding: 60px 8%;
}

.about h2 {
    margin-bottom: 20px;
}

.about p {
    max-width: 700px;
    margin: auto;
    line-height: 1.8;
}

/* Footer */
footer {
    background-color: #1e293b;
    color: white;
    text-align: center;
    padding: 25px;
}

footer p {
    margin: 8px;
}

/* Responsive design */
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        gap: 20px;
    }

    .nav-links {
        gap: 15px;
    }

    .hero-content h2 {
        font-size: 32px;
    }

    .course-container {
        flex-direction: column;
        align-items: center;
    }

    .course-card {
        width: 100%;
        max-width: 350px;
    }
}
