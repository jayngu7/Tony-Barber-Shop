<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tony's Barbershop</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Tony's Barbershop</h1>
    </header>
    <main>
        <section id="about">
            <h2>About Us</h2>
            <p>Welcome to Tony's Barbershop! We offer a wide range of services for men, women, and children, including haircuts, shaves, beard trims, and more. Our experienced barbers provide personalized attention and ensure you leave with a perfect cut and a great experience.</p>
        </section>
        <section id="tonys-barbershop">
            <div class="shop-box">
                <img src="tony-barber-shop-logo.png" alt="Tony's Barbershop Logo">
                <h2>Tony's Barbershop</h2>
            </div>
        </section>
        <section id="schedule">
            <div class="schedule-box">
                <h2>Open Hours</h2>
                <p>Monday - Saturday: 8am - 7pm</p>
                <p>Sunday: 9am - 6pm</p>
                <p>Closed on Tuesday</p>
            </div>
        </section>
        <section id="gallery">
            <div class="gallery-box">
                <h2>Gallery</h2>
                <div class="carousel-container">
                    <div class="carousel-item active">
                        <img src="image1.jpg" alt="Image 1">
                    </div>
                    <div class="carousel-item">
                        <img src="image2.jpg" alt="Image 2">
                    </div>
                    <div class="carousel-item">
                        <img src="image3.jpg" alt="Image 3">
                    </div>
                </div>
            </div>
        </section>
        <section id="services">
            <h2>Our Services</h2>
            <ul>
                <li>Haircuts</li>
                <li>Shaves</li>
                <li>Beard Trims</li>
                <li>Hair Coloring</li>
                <li>Styling</li>
            </ul>
        </section>
        <section id="contact">
            <h2>Contact Us</h2>
            <p>Address: 13520 100th Ave NE Suite 55 Kirkland, Washington, 98034</p>
            <p>Phone: (425) 821-3767 for booking</p>
            <p>Walk-ins are welcome!</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Tony's Barbershop</p>
    </footer>
    <script src="script.js"></script> </body>
</html>

/* Basic Styling */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #f0f0f0;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
}

h2 {
    color: #333;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    margin-bottom: 10px;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: #fff;
}

/* Tony's Barbershop Styling */
#tonys-barbershop .shop-box {
    background-color: #000; /* Black background */
    color: #fff; /* White text */
    padding: 20px;
    border-radius: 10px; /* Rounded corners */
    text-align: center;
}

#tonys-barbershop h2 {
    color: #fff; /* White heading */
}

/* Schedule Box Styling */
#schedule .schedule-box {
    background-color: #f5f5f5;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
}

/* Gallery Box Styling */
#gallery .gallery-box {
    padding: 20px;
    border-radius: 10px;
}

.carousel-container {
    position: relative;
    width: 100%;
    overflow: hidden;
}

.carousel-item {
    display: none;
    width: 100%;
    transition: opacity 0.5s ease;
}

.carousel-item.active {
    display: block;
    opacity: 1;
}

.carousel-item img {
    width: 100%;
    height: auto;
}

const carouselContainer = document.querySelector('.carousel-container');
const carouselItems = document.querySelectorAll('.carousel-item');
let currentItem = 0;

function showNextItem() {
    carouselItems[currentItem].classList.remove('active');
    currentItem = (currentItem + 1) % carouselItems.length;
    carouselItems[currentItem].classList.add('active');
}

setInterval(showNextItem, 3000); // Change image every 3 seconds
