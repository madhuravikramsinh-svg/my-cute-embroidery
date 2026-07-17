<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Threads & Needles | Premium Embroidery Studio</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #fdfbf7;
            color: #333;
            line-height: 1.6;
        }

        /* Navigation Bar */
        header {
            background-color: #ffffff;
            padding: 15px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.03);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-size: 24px;
            font-weight: 700;
            color: #b85c74;
            letter-spacing: 1px;
        }

        nav a {
            text-decoration: none;
            color: #4a4a4a;
            margin-left: 25px;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #b85c74;
        }

        /* Hero Banner */
        .hero {
            background: linear-gradient(rgba(255, 245, 247, 0.8), rgba(255, 245, 247, 0.8)), 
                        url('https://unsplash.com') no-repeat center center/cover;
            height: 65vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }

        .hero h1 {
            font-size: 46px;
            color: #3b2229;
            margin-bottom: 15px;
            font-weight: 700;
        }

        .hero p {
            font-size: 18px;
            color: #615558;
            max-width: 650px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background-color: #b85c74;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(184, 92, 116, 0.3);
        }

        .btn:hover {
            background-color: #94455a;
            transform: translateY(-2px);
        }

        /* Gallery Layout */
        .container {
            max-width: 1200px;
            margin: 60px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-size: 36px;
            color: #3b2229;
            margin-bottom: 45px;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background-color: #b85c74;
            margin: 12px auto 0;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .card {
            background-color: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.04);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card img {
            width: 100%;
            height: 280px;
            object-fit: cover;
        }

        .card-info {
            padding: 25px;
        }

        .card-info h3 {
            font-size: 22px;
            color: #3b2229;
            margin-bottom: 10px;
        }

        .card-info p {
            color: #666;
            font-size: 15px;
            margin-bottom: 15px;
        }

        .price {
            font-size: 18px;
            font-weight: 700;
            color: #b85c74;
        }

        /* Contact Section */
        .contact-section {
            background-color: #fff5f6;
            padding: 60px 0;
        }

        .contact-form {
            max-width: 550px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.03);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #4a4a4a;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #e1e1e1;
            border-radius: 6px;
            outline: none;
            background-color: #fafafa;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: #b85c74;
            background-color: #fff;
        }

        /* Footer */
        footer {
            background-color: #3b2229;
            color: #fdfbf7;
            text-align: center;
            padding: 25px;
            font-size: 14px;
        }

        @media (max-width: 768px) {
            header { flex-direction: column; gap: 15px; }
            nav a { margin: 0 12px; }
            .hero h1 { font-size: 32px; }
        }
    </style>
</head>
<body>

    <!-- Header Navigation -->
    <header>
        <div class="logo">✨ Threads & Needles</div>
        <nav>
            <a href="#home">Home</a>
            <a href="#collection">Collection</a>
            <a href="#contact">Contact Us</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <h1>Exquisite Handcrafted Embroidery</h1>
        <p>Elevate your wardrobe and spaces with premium custom threadwork designs.</p>
        <a href="#collection" class="btn">Explore Collection</a>
    </section>

    <!-- Collection Section with New Best Images -->
    <section class="container" id="collection">
        <h2 class="section-title">Our Featured Designs</h2>
        <div class="gallery">
            
            <!-- Card 1: Beautiful Hoop Art -->
            <div class="card">
                <img src="https://unsplash.com" alt="Floral Hoop Art">
                <div class="card-info">
                    <h3>Floral Hoop Art</h3>
                    <p>Beautiful vibrant botanical layouts crafted tightly on premium linen rings.</p>
                    <div class="price">$45.00</div>
                </div>
            </div>

            <!-- Card 2: Intricate Garment Work -->
            <div class="card">
                <img src="https://unsplash.com" alt="Custom Garment Stitches">
                <div class="card-info">
                    <h3>Premium Apparel Work</h3>
                    <p>Intricate, multi-colored thread patterns suitable for bridal wear and luxury textiles.</p>
                    <div class="price">$85.00</div>
                </div>
            </div>

            <!-- Card 3: Artisan Macro Stitching -->
            <div class="card">
                <img src="https://unsplash.com" alt="Detailed Needle Work">
                <div class="card-info">
                    <h3>Detailed Needle Work</h3>
                    <p>High-precision traditional patterns meticulously woven with professional grade floss.</p>
                    <div class="price">$35.00</div>
                </div>
            </div>

        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact-section" id="contact">
        <h2 class="section-title">Place Your Custom Order</h2>
        <div class="contact-form">
            <form action="#" method="POST" onsubmit="alert('Thank you! Your submission has been noted.'); return false;">
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" required placeholder="Enter your name">
                </div>
                <div class="form-group">
                    <label>Email / Phone Number</label>
                    <input type="text" required placeholder="Where can we contact you?">
                </div>
                <div class="form-group">
                    <label>Design Details</label>
                    <textarea rows="4" required placeholder="Describe your request..."></textarea>
                </div>
                <button type="submit" class="btn" style="border: none; width: 100%; cursor: pointer;">Send Inquiry</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Threads & Needles Studio. All rights reserved.</p>
    </footer>

</body>
</html>

