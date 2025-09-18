<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <title>VABER NAIYA</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <!-- Custom CSS -->
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
        }

        /* Navbar */
        .navbar {
            background-color: transparent;
            position: absolute;
            width: 100%;
            z-index: 10;
        }

        .navbar-brand {
            font-weight: 700;
            font-size: 30px;
        }

        .navbar-brand span {
            color: #ff0000;

        }

        .navbar-nav .nav-link {
            color: #fff !important;
            margin-left: 20px;
            font-weight: 500;
            transition: 0.3s;
        }

        .navbar-nav .nav-link.active,
        .navbar-nav .nav-link:hover {
            color: #fc0000 !important;
        }

        .hero {
            height: 130vh;
            background: url("https://websitedemos.net/guitarist-02/wp-content/uploads/sites/880/2021/06/about-me-part-2.jpg") no-repeat center center;
            background-size: cover;
        
            background-position: center;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: flex-start;
            color: #fff;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 700px;
            margin-left: 80px;
        }

        .hero-content h5 {
            color: #fc0000;
            font-weight: 700;
            font-size: 25px;
            letter-spacing: 2px;
        }

        .hero-content h1 {
            font-size: 68px;
            font-weight: 700;
            margin: 15px 0;
        }

        .hero-content .btn-custom {
            border: 2px solid #ff0000;
            color: #ffffff;
            font-weight: bold;
            padding: 10px 20px;
            text-transform: uppercase;
            margin-top: 20px;
            transition: 0.3s;
        }

        .hero-content .btn-custom:hover {
            background: #ff0000;
            color: #000;
        }

        .social-icons {
            margin-top: 25px;
        }

        .social-icons .icon {
            display: inline-block;
            width: 45px;
            height: 45px;
            line-height: 45px;
            border: 2px solid #ff0000;
            border-radius: 50%;
            color: #082dfc;
            text-align: center;
            margin-right: 12px;
            font-size: 18px;
            transition: 0.3s;
        }

        .social-icons .icon-2 {
            color: red;
            display: inline-block;
            width: 45px;
            height: 45px;
            line-height: 45px;
            border: 2px solid #ff0000;
            border-radius: 50%;

            text-align: center;
            margin-right: 12px;
            font-size: 18px;
            transition: 0.3s;
        }

        .social-icons .icon-3 {
            color: rgb(21, 255, 0);
            display: inline-block;
            width: 45px;
            height: 45px;
            line-height: 45px;
            border: 2px solid #df0000;
            border-radius: 50%;

            text-align: center;
            margin-right: 12px;
            font-size: 18px;
            transition: 0.3s;
        }

        .social-icons .icon:hover {
            background: #fc0000;
            color: #000;
        }

        .social-icons .icon-2:hover {
            background: #fc0000;
            color: #000;
        }

        .social-icons .icon-3:hover {
            background: #fc0000;
            color: #000;
        }


    /* ==== Hero Animations ==== */
    .hero-content h5 {
        animation: fadeDown 1s ease-out forwards;
        opacity: 0;
    }

    .hero-content h1 {
        animation: fadeUp 1.2s ease-out forwards;
        animation-delay: 0.5s;
        opacity: 0;
    }

    .hero-content .btn-custom {
        animation: scaleIn 1s ease-out forwards;
        animation-delay: 1s;
        opacity: 0;
    }

    .social-icons a {
        opacity: 0;
        transform: translateY(20px);
        animation: fadeInUp 0.8s ease forwards;
    }

    .social-icons a:nth-child(1) {
        animation-delay: 1.4s;
    }

    .social-icons a:nth-child(2) {
        animation-delay: 1.6s;
    }

    .social-icons a:nth-child(3) {
        animation-delay: 1.8s;
    }

    /* ==== Keyframes ==== */
    @keyframes fadeDown {
        0% {
            opacity: 0;
            transform: translateY(-40px);
        }
        100% {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes fadeUp {
        0% {
            opacity: 0;
            transform: translateY(40px);
        }
        100% {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes scaleIn {
        0% {
            opacity: 0;
            transform: scale(0.8);
        }
        100% {
            opacity: 1;
            transform: scale(1);
        }
    }

    @keyframes fadeInUp {
        0% {
            opacity: 0;
            transform: translateY(20px);
        }
        100% {
            opacity: 1;
            transform: translateY(0);
        }
    }



        /* quote-section */
        .quote-section {
            background: #000;
           
            color: #fff;
        }

        .quote-title {
            color: #fc0000;
         
            font-weight: 700;
            font-size: 28px;
            margin-bottom: 25px;
            letter-spacing: 1px;
        }

        .quote-text {
            font-size: 16px;
            color: #ddd;
          
            max-width: 800px;
            margin: 0 auto 30px;
            line-height: 1.7;
        }

        .quote-author {
            font-size: 18px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* about me */
        body {
            background-color: #0d0d0d;
            color: #fff;
            font-family: 'Arial', sans-serif;
        }

        .about-section {
            padding: 60px 0;
        }

        .about-title {
            color: #ff0000;
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .about-text {
            color: #ccc;
            line-height: 1.8;
        }

        .about-img img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.6);
        }

        /* footer */


        .footer {
            background-color: #111;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        .footer-logo {
            font-weight: 700;
            letter-spacing: 1px;
            font-size: 26px;
        }

        .footer-title {
            font-weight: 600;
            margin-bottom: 15px;
            letter-spacing: 1px;
            color: red;
        }

        .footer-text {
            font-size: 14px;
            color: #ccc;
            line-height: 1.7;
        }

        .c1 {
            color: red;
        }

        /* Links */
        .footer-link {
            color: #bbb;
            text-decoration: none;
            display: inline-block;
            padding: 3px 0;
            transition: all 0.3s ease;
        }

        .footer-link:hover {
            color: #ff0707;
            padding-left: 5px;
        }

        /* Social Icons */
        .social-icons a {
            color: #bbb;
            margin: 0 10px;
            font-size: 18px;
            transition: color 0.3s ease, transform 0.3s ease;
        }

        .social-icons a:hover {
            color: #ff0707;
            transform: scale(1.2);
        }

        /* Footer Bottom */
        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 15px;
        }

        /* Responsive Fix */
        @media (max-width: 767px) {
            .footer-logo {
                text-align: center;
            }

            .footer-title,
            .footer-text {
                text-align: center;
            }

            .social-icons {
                margin-top: 10px;
            }
        }
    </style>
</head>

<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg">
        <div class="container">
            <a class="navbar-brand text-white" href="#"><span>VABER</span> NAIYA</a>
            <button class="navbar-toggler bg-white" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Lessons</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Shows</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="https://wa.me/qr/VW4APLZWJPR4I1 ">Contact</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <section class="hero">
        <div class="hero-content">
            <h5>GUITARIST & MUSICIAN</h5>
            <h1>FORHAD AHMED</h1>
            <a href=" https://wa.me/qr/VW4APLZWJPR4I1 " class="btn btn-custom">Contact Us</a>

            <!-- Social Icons -->
            <div class="social-icons mt-4">
                <a href="https://www.facebook.com/share/14Q4e8nGFbK/" class="icon"><i class="fab fa-facebook-f"></i></a>
                <a href="https://www.youtube.com/@vaber-naiya" class="icon-2"><i class="fab fa-youtube"></i></a>
                <a href=" https://wa.me/qr/VW4APLZWJPR4I1 " class="icon-3"><i class="fab fa-whatsapp"></i></a>
            </div>
        </div>
    </section>
    
    <!-- Quote Section -->
    <section class="quote-section text-center py-5">
        <div class="container">
            <h2 class="quote-title">Welcome to the world of vaber naiya.</h2>
            <p class="quote-text">
                "VABER NAIYA" of thoughts flows through the ocean of the heart,
                The call of the waves awakens in a restless dream.
                In light and darkness, he seeks the assurance of the shore,
                Yet the traveler knows—the breath of freedom is in the hands of the Naiya.
            </p>
            <h5 class="quote-author">
                Thank you very much for visiting my website.</h5>
        </div>
    </section>

    <section class="about-section">
        <div class="container">
            <div class="row align-items-center">
                <!-- Image Part -->
                <div class="col-md-6 about-img mb-4 mb-md-0">
                    <img src="/picture/myself.jpg" alt="About Me Image">
                </div>
                <!-- Text Part -->
                <div class="col-md-6">
                    <h2 class="about-title">ABOUT ME</h2>
                    <p class="about-text">
                        "I am Forhad Ahmed", a passionate guitarist and singer. Music has always been the heartbeat
                        of my life, and the guitar is my closest companion. From an early age, my love for melodies
                        led me to the world of guitar playing and singing.

                    </p>
                    <p class="about-text">

                        For me, music is not just entertainment — it is a language of emotions, love, and dreams.
                        Through the strings of my guitar and the depth of my voice, I aspire to tell stories and
                        touch hearts.
                        My goal is to inspire people through music and spread joy and peace with every note I play
                        and every song I sing.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section class="about-section">
        <div class="container">
            <div class="row align-items-center">
                <!-- Text Part -->
                <div class="col-md-6">
                    <h2 class="about-title">MY STUDIO</h2>
                    <p class="about-text">
                        "VABER NAIYA" – A Journey of Music and Emotions.
                        This studio is where melodies meet feelings. I mainly sing, and through this creative space, I
                        bring my songs to life with soulful expression.

                    </p>
                    <p class="about-text">

                        The name Bhaver Naiya means “The Boatman of Emotions” — one who rows the boat of music to take
                        listeners to the shore of feelings. Every tune here carries love, stories, and the
                        depth of the soul.
                    </p>
                </div>
                <!-- Image Part -->
                <div class="col-md-6 about-img mb-4 mb-md-0">
                    <img src="/picture/my studio (2).jpg" alt="About Me Image">
                </div>
            </div>
        </div>
    </section>
    <!-- Footer Section -->
    <footer class="footer bg-dark text-light pt-5 pb-3">
        <div class="container">
            <div class="row">

                <!-- Left Info -->
                <div class="col-md-3 mb-4">
                    <h2 class="footer-logo"><span class="c1">VABER</span> NAIYA</h2>
                    <p class="footer-text">
                        Vaber Naiya sails on melody’s way,
                        Through night or dawn’s first gentle ray.
                        On waves of song the heart does float,
                        Spreading peace with every note.
                    </p>
                </div>

                <!-- Music List -->
                <div class="col-md-3 mb-4">
                    <h5 class="footer-title ">MUSIC</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="footer-link">Folk</a></li>
                        <li><a href="#" class="footer-link">Baul</a></li>
                        <li><a href="#" class="footer-link">Bhatiali</a></li>
                        <li><a href="#" class="footer-link">Bhawaiya</a></li>
                    </ul>
                </div>

                <!-- Band List -->
                <div class="col-md-3 mb-4">
                    <h5 class="footer-title">BAND</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="footer-link">Vaber naiya</a></li>
                        <li><a href="#" class="footer-link">Melody sailor</a></li>
                        <li><a href="#" class="footer-link">Rhithm waves</a></li>
                        <li><a href="#" class="footer-link">Song voyager</a></li>
                    </ul>
                </div>

                <!-- Contact Info -->
                <div class="col-md-3 mb-4">
                    <h5 class="footer-title ">CONTACT</h5>
                    <p class="footer-text">
                        Mithapukur,<br>
                        Rangpur,<br>
                        Bangladesh<br>
                        <strong>Phone:</strong> +8801912119265
                        <br>
                        <strong>E-mail:</strong> mf497137@gmail.com
                    </p>
                </div>

            </div>

            <!-- Footer Bottom -->
            <div class="footer-bottom text-center mt-4">
                <ul class="nav justify-content-center mb-3">
                    <li class="nav-item"><a href="#" class="nav-link px-2 footer-link">Home</a></li>
                    <li class="nav-item"><a href="#" class="nav-link px-2 footer-link">About</a></li>
                    <li class="nav-item"><a href="#" class="nav-link px-2 footer-link">Lessons</a></li>
                    <li class="nav-item"><a href="#" class="nav-link px-2 footer-link">Shows</a></li>
                    <li class="nav-item"><a href="#" class="nav-link px-2 footer-link">Contact</a></li>
                </ul>

                <!-- Social Media Icons -->
                <div class="social-icons">
                    <a href="https://www.facebook.com/share/14Q4e8nGFbK/"><i class="fab fa-facebook fa-lg"></i></a>
                    <a href="https://www.instagram.com/forhad39388?igsh=Z21iYmVxaGx4Zjh4"><i class="fab fa-instagram fa-lg"></i></a>
                    <a href="https://www.youtube.com/@vaber-naiya"><i class="fab fa-youtube fa-lg"></i></a>
                </div>
            </div>

        </div>
    </footer>


    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>

</html> VaberNaiya
