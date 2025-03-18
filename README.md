Project Name
 Responsive Event Management web page

📌 Description
An Event Management Web Page is an online platform designed to streamline the planning, organization, and execution of events. 
It allows users to browse upcoming events, view essential details such as date, time, and venue, and register or book tickets seamlessly. 
The webpage often includes a well-structured event schedule, showcasing sessions, speakers, and activities. For event organizers, it provides an efficient dashboard to manage attendees, send notifications, and track registrations. 
Integrated payment options make ticket purchasing smooth, while real-time updates ensure participants stay informed. 
With a responsive design, the platform works efficiently across mobile and desktop devices, making event planning and participation easier and more convenient.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event Management System</title>
    <link rel="stylesheet" href="styles.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: #f4f4f4;
            color: #333;
        }
        header {
            background: #000000;
            padding: 5px;
            text-align: center;
            color: white;
            font-size: 20px;
            font-weight: 500;
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 5px 30px;
            background: #222;
            color: white;
            height: 50px;
        }
        .nav-links {
            list-style: none;
            display: flex;
            gap: 15px;
            
        }
        .nav-links a {
            font: size 15px;;
            padding:5px 10px;
            color: #f4f4f4;
            text-decoration: none;
            transition: transform 0.3s ease;
            display: inline-block;
        }
        .nav-links a:hover {
            color: #ff6b6b;
            transform: scale(1.2);
        
        }
        .hero {
    text-align: center;
    padding: 100px 20px;
    background-image: url("Site images/frontend images/WhatsApp Image 2025-03-10 at 11.31.31 AM.jpeg");
    background-size: cover; /* Adjusts the image to cover the entire section */
    background-position: center; /* Centers the image */
    color: white;
}

        .hero h1 {
            font-size: 36px;
            margin-bottom: 10px;
            color: cyan;
        }
        .cta-button {
            display: inline-block;
            margin-top: 20px;
            padding: 12px 24px;
            background: white;
            color: #ff6b6b;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            transition: 0.3s;
        }
        .cta-button:hover {
            background: #ff9770;
            color: white;
        }
        .events {
    text-align: center;
    padding: 50px 0;
}

.event-slider {
    display: flex;
    flex-direction: column; /* Keeps cards stacked vertically */
    align-items: center; /* Centers cards horizontally */
    justify-content: center; /* Centers cards vertically */
    height: 100vh; /* Full viewport height to center vertically */
}
body, html {
    height: 100%; /* Full height for parent containers */
    margin: 0;
}

/* Event Card Styling */
.event-card {
    background: white;
    width: 400px !important; /* Adjust width to be horizontally shorter */
    height: 200px !important; /* Force the height */
    padding: 0px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    position: center;
    margin: 10px 0;
}


/* Hover Effect - Pop Up */
.event-card:hover {
    transform: scale(1.1);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
}

/* Prevent shifting on hover */
.event-slider {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    overflow: hidden; /* Prevent scrolling */
}

.event-card {
    overflow: hidden; /* Remove overflow from the cards as well */
}
.event-slider .event-card {
    margin: 0 12px; /* Adds space between event cards */
}


@media (max-width: 768px) {
    .event-card {
        margin: auto;
    }
}






        .event-btn {
            display: inline-block;
            margin-top: 10px;
            padding: 8px 16px;
            background: #ff6b6b;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: 0.3s;
        }
        .event-btn:hover {
            background: #ff9770;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #222;
            color: white;
        }

        /* ======== LOGIN MODAL STYLES ======== */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background: white;
            padding: 20px;
            width: 350px;
            border-radius: 8px;
            text-align: center;
            position: relative;
        }
        .modal-content h2 {
            margin-bottom: 20px;
        }
        .modal-content input {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .modal-content .login-btn {
            background: #ff6b6b;
            color: white;
            border: none;
            padding: 10px;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        .modal-content .login-btn:hover {
            background: #ff9770;
        }
        .close {
            position: absolute;
            right: 15px;
            top: 15px;
            font-size: 24px;
            font-weight: bold;
            cursor: pointer;
            color: #333;
        }
        .close:hover {
            color: #ff6b6b;
        }
        html, body {
    height: 100%;
    margin: 0;
    display: flex;
    flex-direction: column;
}

.content {
    flex: 1;
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html, body {
    width: 100%;
    overflow-x: hidden; /* Prevents horizontal scrolling */
}

.container {
    max-width: 100%;
    overflow-x: hidden; /* Ensures no element overflows */
}


footer {
    text-align: center;
    padding: 20px;
    background: #222;
    color: white;
    position: relative;
    bottom: 0;
    width: 100%;
}

    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">Eventify</div>
            <ul class="nav-links">
                <li><a href="#events">Events</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#" class="btn">Login</a></li>
            </ul>
        </nav>
    </header>
    
    <section class="hero">
        <div class="hero-content">
            <h1>Discover & Book Amazing Events</h1>
            <p>Join thousands of attendees at the best events happening near you.</p>
            <a href="#events" class="cta-button">Explore Events</a>
        </div>
    </section>
    <!-- LOGIN POPUP MODAL -->
<div id="loginModal" class="modal">
    <div class="modal-content">
        <span class="close">&times;</span> <!-- Close Button -->
        <h2>Login</h2>
        <input type="text" placeholder="Username" id="username">
        <input type="password" placeholder="Password" id="password">
        <button class="login-btn">Login</button>
        <p>Don't have an account? <a href="#" id="signupLink">Sign up</a></p>
    </div>
</div>

<head>
    <!-- Include Slick CSS & jQuery -->
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick.min.css"/>
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick-theme.min.css"/>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick.min.js"></script>
    
    
</head>
<body>

<section id="events" class="events">
    <h2>Upcoming Events</h2>
    <div class="event-slider">
        <div class="event-card">
            <h3>Tech Conference 2025</h3>
            <p>Join the biggest tech innovators .</p>
            <a href="#" class="event-btn">Register Now</a>
        </div>
        <div class="event-card">
            <h3>Music Fest</h3>
            <p>Experience music with top artists.</p>
            <a href="#" class="event-btn">Book Tickets</a>
        </div>
        <div class="event-card">
            <h3>Startup Summit</h3>
            <p>Meet successful entrepreneurs and investors.</p>
            <a href="#" class="event-btn">Join Now</a>
        </div>
        <div class="event-card">
            <h3>Art Exhibition</h3>
            <p>Explore stunning artworks from top artists.</p>
            <a href="#" class="event-btn">View More</a>
        </div>
    </div>

  
</section>

<script>
$(document).ready(function(){
    $('.event-slider').slick({
        slidesToShow: 3, // Number of slides visible at once
        slidesToScroll: 1, // Move one slide at a time
        autoplay: true,
        autoplaySpeed: 2000, // Time before sliding to next event (2 sec)
        speed: 700, // Speed of transition (adjust as needed)
        infinite: true, // Keeps looping
        cssEase: 'ease', // Smooth sliding effect
        dots: false, // Hide dots
        arrows: false, // Hide navigation arrows
        centerMode: true, // Ensures slides are centered
    });
});



</script>

</body>

    <!-- Remove this duplicate modal code -->
<!-- LOGIN POPUP MODAL -->
<div id="loginModal" class="modal">
    <div class="modal-content">
        <span class="close">&times;</span> <!-- Close Button -->
        <h2>Login</h2>
        <input type="text" placeholder="Username" id="username">
        <input type="password" placeholder="Password" id="password">
        <button class="login-btn">Login</button>
    </div>
</div>

<div id="signupModal" class="modal">
    <div class="modal-content">
        <span class="close">&times;</span>
        <h2>Sign Up</h2>
        <input type="text" placeholder="Username" id="signupUsername">
        <input type="email" placeholder="Email" id="signupEmail">
        <input type="password" placeholder="Password" id="signupPassword">
        <button class="signup-btn">Sign Up</button>
        <p>Already have an account? <a href="#" id="loginLink">Login</a></p>
    </div>
</div>

    

    <script>
       document.addEventListener("DOMContentLoaded", () => {
    const loginBtn = document.querySelector(".btn");
    const signupLink = document.getElementById("signupLink");
    const loginLink = document.getElementById("loginLink");
    const closeBtns = document.querySelectorAll(".close");

    const loginModal = document.getElementById("loginModal");
    const signupModal = document.getElementById("signupModal");

    loginBtn.addEventListener("click", (e) => {
        e.preventDefault();
        loginModal.style.display = "flex";
    });

    signupLink.addEventListener("click", (e) => {
        e.preventDefault();
        loginModal.style.display = "none";
        signupModal.style.display = "flex";
    });

    loginLink.addEventListener("click", (e) => {
        e.preventDefault();
        signupModal.style.display = "none";
        loginModal.style.display = "flex";
    });

    closeBtns.forEach(btn => {
        btn.addEventListener("click", () => {
            loginModal.style.display = "none";
            signupModal.style.display = "none";
        });
    });

    window.addEventListener("click", (e) => {
        if (e.target === loginModal) {
            loginModal.style.display = "none";
        }
        if (e.target === signupModal) {
            signupModal.style.display = "none";
        }
    });
});
    </script>
    <footer>
        <p>&copy; 2025 Eventify. All Rights Reserved.</p>
        <p><a href="#">About Us</a> | <a href="#">Contact</a> | <a href="#">Privacy Policy</a></p>
    </footer>
</body>
</html>
