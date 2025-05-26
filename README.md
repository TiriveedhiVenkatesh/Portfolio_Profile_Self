<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Portfolio Profile</title>
  <style>
    /* Reset some default styles */
    body, h1, h2, h3, p, ul, li, table {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
    }

    /* Top Ribbon */
    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      background: #222;
      color: #fff;
      z-index: 1000;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 60px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .nav-list {
      list-style: none;
      display: flex;
      gap: 2rem;
    }
    .nav-list li {
      display: inline;
    }
    .nav-list a {
      color: #fff;
      text-decoration: none;
      font-size: 1.1rem;
      padding: 8px 16px;
      transition: background 0.2s, color 0.2s;
    }
    .nav-list a:hover {
      background: #444;
      color: #ffd700;
      border-radius: 4px;
    }

    /* Main content below navbar */
    .container {
      margin-top: 80px;
      padding: 2rem;
      max-width: 1000px;
      margin-left: auto;
      margin-right: auto;
    }

    /* Table Section */
    .table-section {
      background: #eaeaea; /* Non-white background */
      padding: 2rem;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }
    table {
      width: 100%;
      border-collapse: collapse;
      background: none;
    }
    th, td {
      padding: 12px;
      border-bottom: 1px solid #ccc;
      text-align: left;
    }
    th {
      background: #d1d1d1;
    }
  </style>
</head>
<body>
  <!-- Top Ribbon / Navigation Bar -->
  <nav class="navbar">
    <ul class="nav-list">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
      <!-- Add more tabs as needed -->
    </ul>
  </nav>

  <div class="container">
    <h1 id="home">Welcome to My Portfolio</h1>
    <p>This is the home section. Scroll down to see the table data section.</p>

    <section class="table-section" id="projects">
      <h2>Project Table</h2>
      <table>
        <thead>
          <tr>
            <th>Project Name</th>
            <th>Description</th>
            <th>Year</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Portfolio Website</td>
            <td>Personal portfolio to showcase my projects and skills.</td>
            <td>2025</td>
          </tr>
          <tr>
            <td>Data Visualizer</td>
            <td>A tool for visualizing datasets interactively.</td>
            <td>2024</td>
          </tr>
          <!-- Add more rows as needed -->
        </tbody>
      </table>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: youremail@example.com</p>
    </section>
  </div>
</body>
</html>
