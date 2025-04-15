<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with CSS Grid</title>
  <style>
    /* Basic reset */
    body, html {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    /* Navigation Bar */
    nav {
      background-color: #333;
      color: white;
      padding: 1rem;
      text-align: center;
    }

    nav a {
      color: white;
      padding: 10px;
      text-decoration: none;
      margin: 0 15px;
    }

    nav a:hover {
      background-color: #575757;
    }

    /* Grid layout */
    .container {
      display: grid;
      grid-template-columns: 1fr 3fr;
      gap: 20px;
      padding: 20px;
    }

    .container .sidebar {
      background-color: #f4f4f4;
      padding: 20px;
    }

    .container .main-content {
      background-color: #fafafa;
      padding: 20px;
    }

    /* Media Queries for Responsiveness */
    @media (max-width: 768px) {
      .container {
        grid-template-columns: 1fr; /* Stack columns vertically */
      }
    }

    @media (max-width: 480px) {
      nav {
        font-size: 14px;
      }

      .container {
        padding: 10px;
      }

      .container .sidebar, .container .main-content {
        padding: 10px;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Services</a>
    <a href="#">Contact</a>
  </nav>

  <!-- Main Content Area -->
  <div class="container">
    <div class="sidebar">
      <h2>Sidebar</h2>
      <p>This is a sidebar with additional content.</p>
    </div>
    <div class="main-content">
      <h1>Main Content</h1>
      <p>This is the main content area.</p>
      <p>Responsive design ensures it looks good on all screen sizes.</p>
    </div>
  </div>

</body>
</html>
