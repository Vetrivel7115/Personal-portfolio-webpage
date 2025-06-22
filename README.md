# Personal-portfolio-webpage

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Portfolio</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
      background: #f4f4f4;
    }

    header {
      background: #333;
      color: white;
      padding: 20px 0;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
    }

    header nav a:hover {
      text-decoration: underline;
    }

    section {
      padding: 60px 20px;
      max-width: 1000px;
      margin: auto;
    }

    h1, h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    .about, .contact {
      text-align: center;
    }

    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .project-card {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 20px 0;
      margin-top: 40px;
    }

    .photo-upload {
      text-align: center;
      margin-bottom: 20px;
    }

    .photo-upload img {
      width: 150px;
      height: 150px;
      object-fit: cover;
      border-radius: 50%;
      border: 4px solid #007bff;
      margin-bottom: 10px;
    }

    .photo-upload input {
      display: block;
      margin: 10px auto;
    }

    @media (max-width: 600px) {
      header nav a {
        display: block;
        margin: 10px 0;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Vetrivel Rajarathinam</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome to My Portfolio</h2>
    <div class="photo-upload">
      <img id="profilePreview" src="https://via.placeholder.com/150" alt="Profile Photo">
      <input type="file" id="photoInput" accept="image/*" />
      <small>Upload your profile photo</small>
    </div>
    <p style="text-align:center; max-width: 600px; margin: 0 auto;">I’m a passionate web developer and computer science student. I love building interactive websites and real-time applications.</p>
  </section>

  <section id="about">
    <h2>About Me</h2>
    <div class="about">
      <p>Hi! I’m Vetrivel, a dedicated front-end developer with internship experience from CodTech. I enjoy transforming ideas into reality using code.</p>
      <p>Skills: HTML, CSS, JavaScript, React, WebSockets</p>
    </div>
  </section>

  <section id="projects">
    <h2>My Projects</h2>
    <div class="projects">
      <div class="project-card">
        <h3>Quiz App</h3>
        <p>Interactive quiz app with scoring and feedback using HTML, CSS, JavaScript.</p>
      </div>
      <div class="project-card">
        <h3>Chat App</h3>
        <p>Real-time chat using WebSocket and plain HTML/JS. Supports multiple clients.</p>
      </div>
      <div class="project-card">
        <h3>Portfolio Website</h3>
        <p>You're viewing it right now! Fully responsive and single-page with navigation.</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <div class="contact">
      <p>Email: <a href="mailto:youremail@example.com">youremail@example.com</a></p>
      <p>LinkedIn: <a href="https://linkedin.com/in/yourprofile" target="_blank">linkedin.com/in/yourprofile</a></p>
      <p>GitHub: <a href="https://github.com/yourusername" target="_blank">github.com/yourusername</a></p>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 Vetrivel R | All Rights Reserved</p>
  </footer>

  <script>
    const input = document.getElementById('photoInput');
    const preview = document.getElementById('profilePreview');

    input.addEventListener('change', () => {
      const file = input.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = e => {
          preview.src = e.target.result;
        };
        reader.readAsDataURL(file);
      }
    });
  </script>
</body>
</html>
