# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

/* Base Styles */
:root {
    --primary-color: #3498db;
    --secondary-color: #2c3e50;
    --accent-color: #e74c3c;
    --light-color: #ecf0f1;
    --dark-color: #333;
    --text-color: #333;
    --text-light: #7f8c8d;
    --box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    --transition: all 0.3s ease;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    line-height: 1.6;
    color: var(--text-color);
    background-color: #f9f9f9;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

a {
    text-decoration: none;
    color: inherit;
}

.btn {
    display: inline-block;
    padding: 12px 24px;
    background-color: var(--primary-color);
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: var(--transition);
    font-weight: 600;
}

.btn:hover {
    background-color: #2980b9;
    transform: translateY(-3px);
}

.section-title {
    font-size: 2rem;
    margin-bottom: 2rem;
    position: relative;
    text-align: center;
}

.section-title::after {
    content: '';
    display: block;
    width: 80px;
    height: 4px;
    background: var(--primary-color);
    margin: 10px auto 0;
}

/* Header & Navigation */
.header {
    background-color: white;
    box-shadow: var(--box-shadow);
    position: fixed;
    width: 100%;
    z-index: 1000;
}

.header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;
}

.logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--secondary-color);
}

.nav-list {
    display: flex;
    list-style: none;
    gap: 30px;
}

.nav-list a {
    font-weight: 600;
    transition: var(--transition);
    position: relative;
}

.nav-list a:hover {
    color: var(--primary-color);
}

.nav-list a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--primary-color);
    transition: var(--transition);
}

.nav-list a:hover::after {
    width: 100%;
}

.hamburger {
    display: none;
    cursor: pointer;
}

.bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    background-color: var(--dark-color);
    transition: var(--transition);
}

/* Hero Section */
.hero {
    padding: 120px 0 60px;
    background-color: var(--light-color);
}

.hero .container {
    display: flex;
    align-items: center;
    gap: 40px;
}

.hero-content {
    flex: 1;
}

.hero-content h1 {
    font-size: 2.5rem;
    margin-bottom: 20px;
    line-height: 1.2;
}

.hero-content p {
    font-size: 1.1rem;
    margin-bottom: 30px;
    color: var(--text-light);
}

.hero-image {
    flex: 1;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: var(--box-shadow);
}

.hero-image img {
    width: 100%;
    height: auto;
    display: block;
}

/* Services Section */
.services {
    padding: 80px 0;
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
}

.service-card {
    background-color: white;
    padding: 30px;
    border-radius: 8px;
    box-shadow: var(--box-shadow);
    transition: var(--transition);
    text-align: center;
}

.service-card:hover {
    transform: translateY(-10px);
}

.service-icon {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 20px;
}

.service-card h3 {
    margin-bottom: 15px;
    font-size: 1.3rem;
}

/* About Section */
.about {
    padding: 80px 0;
    background-color: var(--light-color);
}

.about .container {
    display: flex;
    align-items: center;
    gap: 40px;
}

.about-content {
    flex: 1;
}

.about-content p {
    margin-bottom: 15px;
    line-height: 1.7;
}

.about-image {
    flex: 1;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: var(--box-shadow);
}

.about-image img {
    width: 100%;
    height: auto;
    display: block;
}

/* Contact Section */
.contact {
    padding: 80px 0;
}

.contact-container {
    display: flex;
    gap: 40px;
}

.contact-form {
    flex: 1;
    background-color: white;
    padding: 30px;
    border-radius: 8px;
    box-shadow: var(--box-shadow);
}

.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 8px;
    font-weight: 600;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-family: inherit;
}

.form-group textarea {
    min-height: 150px;
    resize: vertical;
}

.contact-info {
    flex: 1;
    padding: 30px;
    background-color: var(--secondary-color);
    color: white;
    border-radius: 8px;
}

.contact-info h3 {
    margin-bottom: 20px;
}

.contact-info p {
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 10px;
}

/* Footer */
.footer {
    background-color: var(--secondary-color);
    color: white;
    padding: 40px 0 20px;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
}

.footer-logo {
    font-size: 1.5rem;
    font-weight: 700;
}

.social-links {
    display: flex;
    gap: 15px;
}

.social-links a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    transition: var(--transition);
}

.social-links a:hover {
    background-color: var(--primary-color);
    transform: translateY(-3px);
}

.copyright {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
}

/* Media Queries for Responsive Design */
@media (max-width: 992px) {
    .hero .container,
    .about .container {
        flex-direction: column;
        text-align: center;
    }

    .hero-image,
    .about-image {
        margin-top: 40px;
        max-width: 600px;
    }

    .contact-container {
        flex-direction: column;
    }

    .contact-info {
        margin-top: 30px;
    }
}

@media (max-width: 768px) {
    .hamburger {
        display: block;
    }

    .hamburger.active .bar:nth-child(2) {
        opacity: 0;
    }

    .hamburger.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }

    .hamburger.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }

    .nav-list {
        position: fixed;
        left: -100%;
        top: 80px;
        gap: 0;
        flex-direction: column;
        background-color: white;
        width: 100%;
        text-align: center;
        transition: var(--transition);
        box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
        padding: 20px 0;
    }

    .nav-list.active {
        left: 0;
    }

    .nav-list li {
        margin: 15px 0;
    }

    .hero-content h1 {
        font-size: 2rem;
    }
}

@media (max-width: 576px) {
    .section-title {
        font-size: 1.8rem;
    }

    .hero {
        padding: 100px 0 40px;
    }

    .services-grid {
        grid-template-columns: 1fr;
    }

    .footer-content {
        flex-direction: column;
        gap: 20px;
    }
}
