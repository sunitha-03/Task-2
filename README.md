<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Blog</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <div class="logo">My Blog</div>
    <nav class="nav">
      <button id="toggleMenu">☰</button>
      <ul id="navLinks">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <div class="container">
    <aside class="sidebar">
      <h2>Categories</h2>
      <ul>
        <li><a href="#">Technology</a></li>
        <li><a href="#">Life</a></li>
        <li><a href="#">Travel</a></li>
      </ul>
    </aside>

    <main class="content">
      <article class="post">
        <h2>Exploring the Mountains</h2>
        <img src="mountains.jpg" alt="Mountains" />
        <p>This is a summary of the blog post about exploring mountains.</p>
      </article>

      <article class="post">
        <h2>City Life Tips</h2>
        <img src="city.jpg" alt="City" />
        <p>Here's a quick read on how to make the most of living in the city.</p>
      </article>
    </main>
  </div>

  <footer>
    <p>&copy; 2025 My Blog. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f8f9fa;
}

header {
  background: #333;
  color: #fff;
  padding: 15px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 24px;
}

.nav ul {
  list-style: none;
  display: flex;
  gap: 15px;
}

.nav a {
  color: #fff;
  text-decoration: none;
}

#toggleMenu {
  display: none;
  background: none;
  color: #fff;
  font-size: 24px;
  border: none;
}

.container {
  display: flex;
  padding: 20px;
  gap: 20px;
}

.sidebar {
  flex: 1;
  background: #fff;
  padding: 20px;
  border-radius: 8px;
}

.content {
  flex: 3;
}

.post {
  background: #fff;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 8px;
}

.post img {
  max-width: 100%;
  height: auto;
  margin-top: 10px;
}

footer {
  background: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

/* Responsive */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }

  .nav ul {
    flex-direction: column;
    display: none;
  }

  .nav ul.show {
    display: block;
  }

  #toggleMenu {
    display: block;
  }
}const toggleMenu = document.getElementById('toggleMenu');
const navLinks = document.getElementById('navLinks');

toggleMenu.addEventListener('click', () => {
  navLinks.classList.toggle('show');
});
