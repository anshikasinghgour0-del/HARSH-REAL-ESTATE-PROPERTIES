# HARSH-REAL-ESTATE-PROPERTIES
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harsh Properties | Building Trust in Rajasthan</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --primary-blue: #0f4c81; /* Classic Blue for Trust */
            --dark-blue: #083055;
            --accent-earth: #c5a065; /* Earthy Gold/Sand for Rajasthan */
            --light-grey: #f8f9fa;
            --medium-grey: #6c757d;
            --text-dark: #212529;
            --white: #ffffff;
            --shadow: 0 4px 15px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            line-height: 1.6;
            background-color: var(--white);
        }

        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }
        img { max-width: 100%; display: block; }

        /* --- HEADER & NAVIGATION --- */
        header {
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-blue);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span { color: var(--accent-earth); }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            font-weight: 500;
            color: var(--text-dark);
            transition: var(--transition);
        }

        .nav-links a:hover { color: var(--primary-blue); }

        .btn-primary {
            background-color: var(--primary-blue);
            color: var(--white);
            padding: 0.7rem 1.5rem;
            border-radius: 5px;
            font-weight: 500;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }

        .btn-primary:hover {
            background-color: var(--dark-blue);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: var(--accent-earth);
            color: var(--white);
            padding: 0.7rem 1.5rem;
            border-radius: 5px;
            font-weight: 500;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }

        .btn-secondary:hover { background-color: #b08d55; }

        .hamburger { display: none; font-size: 1.5rem; cursor: pointer; }

        /* --- HERO SECTION --- */
        .hero {
            height: 90vh;
            background: linear-gradient(rgba(15, 76, 129, 0.7), rgba(8, 48, 85, 0.7)), 
                        url('https://images.unsplash.com/photo-1560518883-ce09059eeffa?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
            margin-top: 60px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* --- SEARCH BAR --- */
        .search-container {
            background: var(--white);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: var(--shadow);
            margin-top: -3rem;
            position: relative;
            z-index: 10;
            max-width: 1000px;
            margin-left: auto;
            margin-right: auto;
        }

        .search-form {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            align-items: end;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--medium-grey);
        }

        .form-group select, .form-group input {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
        }

        /* --- SECTIONS GENERAL --- */
        .section-padding { padding: 5rem 5%; }
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-blue);
            margin-bottom: 0.5rem;
        }
        .section-title p { color: var(--medium-grey); }

        /* --- FEATURED PROPERTIES --- */
        .property-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .property-card {
            background: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .property-card:hover { transform: translateY(-5px); }

        .card-image {
            height: 220px;
            position: relative;
        }

        .card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--accent-earth);
            color: var(--white);
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .card-details { padding: 1.5rem; }

        .price {
            color: var(--primary-blue);
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .location {
            color: var(--medium-grey);
            font-size: 0.9rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .features {
            display: flex;
            justify-content: space-between;
            border-top: 1px solid #eee;
            padding-top: 1rem;
            margin-top: 1rem;
            color: var(--medium-grey);
            font-size: 0.9rem;
        }

        .features span { display: flex; align-items: center; gap: 5px; }

        /* --- ABOUT US --- */
        .about-section {
            background-color: var(--light-grey);
        }

        .about-container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            gap: 3rem;
        }

        .about-image { flex: 1; min-width: 300px; }
        .about-image img { border-radius: 10px; box-shadow: var(--shadow); }
        
        .about-text { flex: 1; min-width: 300px; }
        .about-text h3 { color: var(--accent-earth); margin-bottom: 1rem; }
        .about-text h2 { font-size: 2rem; margin-bottom: 1.5rem; color: var(--primary-blue); }
        .about-text p { margin-bottom: 1rem; color: var(--medium-grey); }

        .stats {
            display: flex;
            gap: 2rem;
            margin-top: 2rem;
        }
        .stat-item h4 { font-size: 2rem; color: var(--primary-blue); }
        .stat-item p { font-size: 0.9rem; }

        /* --- TESTIMONIALS --- */
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .testimonial-card {
            background: var(--light-grey);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }

        .testimonial-card i {
            color: var(--accent-earth);
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .client-name {
            font-weight: 700;
            margin-top: 1rem;
            color: var(--primary-blue);
        }

        /* --- CONTACT --- */
        .contact-section { background-color: var(--primary-blue); color: var(--white); }
        .contact-section .section-title h2 { color: var(--white); }
        .contact-section .section-title p { color: #ccc; }

        .contact-container {
            display: flex;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
            gap: 3rem;
        }

        .contact-info { flex: 1; min-width: 300px; }
        .contact-form-wrapper { flex: 1; min-width: 300px; background: var(--white); padding: 2rem; border-radius: 10px; color: var(--text-dark); }

        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 1.5rem;
        }

        .info-item i {
            font-size: 1.2rem;
            color: var(--accent-earth);
            margin-top: 5px;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
        }

        /* --- FOOTER --- */
        footer {
            background: var(--dark-blue);
            color: var(--white);
            padding: 3rem 5% 1rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto 2rem;
        }

        .footer-col h4 { margin-bottom: 1.5rem; color: var(--accent-earth); }
        .footer-col ul li { margin-bottom: 0.8rem; }
        .footer-col ul li a { color: #ccc; transition: var(--transition); }
        .footer-col ul li a:hover { color: var(--white); padding-left: 5px; }

        .social-icons a {
            display: inline-flex;
            justify-content: center;
            align-items: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            margin-right: 10px;
            transition: var(--transition);
        }

        .social-icons a:hover { background: var(--accent-earth); }

        .copyright {
            text-align: center;
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 1.5rem;
            font-size: 0.9rem;
            color: #ccc;
        }

        /* --- STICKY WHATSAPP --- */
        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 30px;
            right: 30px;
            background-color: #25d366;
