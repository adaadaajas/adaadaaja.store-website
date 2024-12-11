<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adaadaaja.Store</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #000;
            color: #FFD700;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
            background-color: #111;
        }
        header img {
            height: 50px;
            border-radius: 50%;
        }
        nav ul {
            list-style: none;
            display: flex;
            gap: 15px;
        }
        nav ul li {
            display: inline;
        }
        nav ul li a {
            text-decoration: none;
            color: #FFD700;
            font-weight: bold;
        }
        .hero {
            text-align: center;
            padding: 100px 20px;
            background-image: url('placeholder-image.jpg');
            background-size: cover;
            background-position: center;
            color: white;
        }
        .hero h1 {
            font-size: 48px;
            margin-bottom: 10px;
        }
        .hero p {
            font-size: 24px;
        }
        section {
            padding: 20px;
        }
        .about, .services, .portfolio, .contact {
            margin-bottom: 40px;
        }
        .about h2, .services h2, .portfolio h2, .contact h2 {
            border-bottom: 2px solid #FFD700;
            display: inline-block;
            margin-bottom: 10px;
        }
        .carousel {
            display: flex;
            overflow: hidden;
            position: relative;
            margin-top: 20px;
        }
        .carousel img {
            width: 100%;
            flex-shrink: 0;
            transition: transform 0.5s ease;
        }
        .carousel-controls {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }
        .carousel-controls button {
            background-color: #111;
            border: none;
            color: #FFD700;
            font-size: 24px;
            cursor: pointer;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #111;
            color: #FFD700;
        }
    </style>
</head>
<body>
    <header>
        <img src="logo-circular.png" alt="Logo Adaadaaja.Store">
        <nav>
            <ul>
                <li><a href="#">Beranda</a></li>
                <li><a href="#about">Tentang Kami</a></li>
                <li><a href="#services">Layanan</a></li>
                <li><a href="#portfolio">Portofolio</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
        </nav>
    </header>
    <div class="hero">
        <h1>Selamat Datang di Adaadaaja.Store</h1>
        <p>(BAPALOK) Bangga Pake Lokal</p>
    </div>
    <section id="about" class="about">
        <h2>Tentang Kami</h2>
        <p>Adaadaaja.Store adalah usaha sablon yang bangga mendukung produk lokal dan menawarkan layanan sablon kreatif untuk anak muda perkotaan.</p>
    </section>
    <section id="services" class="services">
        <h2>Layanan</h2>
        <ul>
            <li>Sablon kaos custom</li>
            <li>Desain grafis</li>
            <li>Layanan ekspres untuk kebutuhan mendesak</li>
        </ul>
    </section>
    <section id="portfolio" class="portfolio">
        <h2>Portofolio</h2>
        <p>Berikut adalah beberapa hasil karya kami:</p>
        <div class="carousel">
            <img src="placeholder1.jpg" alt="Portofolio 1">
            <img src="placeholder2.jpg" alt="Portofolio 2">
            <img src="placeholder3.jpg" alt="Portofolio 3">
        </div>
        <div class="carousel-controls">
            <button onclick="prevSlide()">&#10094;</button>
            <button onclick="nextSlide()">&#10095;</button>
        </div>
    </section>
    <section id="contact" class="contact">
        <h2>Kontak</h2>
        <p>Hubungi kami untuk informasi lebih lanjut:</p>
        <ul>
            <li>WhatsApp: <a href="https://wa.me/085737751017" style="color: #FFD700;">085737751017</a></li>
            <li>Email: <a href="mailto:storeadaadaaja@gmail.com" style="color: #FFD700;">storeadaadaaja@gmail.com</a></li>
        </ul>
    </section>
    <footer>
        <p>&copy; 2024 Adaadaaja.Store. Semua Hak Dilindungi.</p>
    </footer>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.carousel img');

        function showSlide(index) {
            slides.forEach((slide, i) => {
                slide.style.transform = `translateX(${(i - index) * 100}%)`;
            });
        }

        function prevSlide() {
            currentSlide = (currentSlide - 1 + slides.length) % slides.length;
            showSlide(currentSlide);
        }

        function nextSlide() {
            currentSlide = (currentSlide + 1) % slides.length;
            showSlide(currentSlide);
        }

        showSlide(currentSlide);
    </script>
</body>
</html>
