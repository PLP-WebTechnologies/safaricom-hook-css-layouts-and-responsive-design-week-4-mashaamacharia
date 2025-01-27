# Assignment: Responsive Web Design

## Objective:
Create a responsive webpage using modern CSS techniques, specifically Flexbox, Grid, and Media Queries. The goal is to ensure the webpage adapts gracefully to various screen sizes.

## Assignment Tasks

### Designing a Responsive Layout
a. Create a webpage with the following sections:

Header (including a logo and navigation links).
Main content area (with two columns: one for text content and the other for an image).
Footer (with links to social media and a copyright notice).
b. Use Flexbox to style the navigation menu in the header.
c. Use CSS Grid to structure the main content area.

### Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically.
Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns.
Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.

### Bonus

Add animations or transitions when resizing the screen.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Web Design Assignment</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">Logo</div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <div class="text-content">
            <h1>Welcome to Our Website</h1>
            <p>Your engaging content goes here.</p>
        </div>
        <div class="image-content">
            <img src="image.jpg" alt="Descriptive Alt Text">
        </div>
    </main>
    <footer>
        <div class="social-media">
            <a href="#">Facebook</a>
            <a href="#">Twitter</a>
            <a href="#">LinkedIn</a>
        </div>
        <div class="copyright">
            &copy; 2025 Your Company. All rights reserved.
        </div>
    </footer>
</body>
</html>


/* Base Styles */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

header, footer {
    background-color: #333;
    color: #fff;
    padding: 1em;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav ul {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
}

nav li {
    margin-left: 1em;
}

nav a {
    color: #fff;
    text-decoration: none;
}

main {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1em;
    padding: 1em;
}

main img {
    width: 100%;
    height: auto;
}

footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

footer a {
    color: #fff;
    text-decoration: none;
    margin-right: 1em;
}

/* Media Queries */
@media (max-width: 1024px) {
    main {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 600px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    nav ul {
        flex-direction: column;
        width: 100%;
    }

    nav li {
        margin: 0.5em 0;
    }

    footer {
        flex-direction: column;
        align-items: flex-start;
    }
}

