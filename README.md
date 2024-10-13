# Fraell
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pembahasan Teknologi</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Montserrat:wght@600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 20px;
            background: linear-gradient(135deg, #121212, #1e1e1e);
            background-image: url('https://www.transparenttextures.com/patterns/asfalt-dark.png');
            color: #ffffff;
            overflow-x: hidden; /* Menghindari scroll horizontal */
        }
        .marquee {
            position: absolute;
            width: 100%;
            top: 10px; /* Atur posisi atas */
            text-align: center;
            font-size: 1.5em; /* Ukuran font lebih kecil */
            white-space: nowrap;
            overflow: hidden;
            animation: marquee 10s linear infinite;
            background: linear-gradient(90deg, #ff6b6b, #f7aef8); /* Gradien warna */
            border-radius: 10px; /* Sudut membulat */
            padding: 10px 0; /* Jarak atas dan bawah lebih kecil */
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5); /* Bayangan */
            color: #ffffff; /* Warna teks */
            font-weight: bold; /* Ketebalan teks */
            z-index: 1; /* Memastikan di atas elemen lainnya */
        }
        @keyframes marquee {
            0% { transform: translateX(-100%); } /* Mulai dari kiri */
            50% { transform: translateX(0); } /* Di tengah */
            100% { transform: translateX(100%); } /* Masuk ke kanan */
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        header, main, .section {
            opacity: 0;
            animation: fadeIn 0.8s forwards;
        }
        header {
            position: relative; /* Agar marquee bisa diposisikan relatif terhadap header */
            margin-top: 70px; /* Jarak untuk memberikan ruang bagi marquee */
            background: linear-gradient(135deg, #C0392B, #E74C3C);
            color: white;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
            transition: transform 0.3s;
        }
        header:hover {
            transform: scale(1.03);
        }
        header h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5em;
            margin: 0;
        }
        nav {
            padding: 10px;
            margin: 20px 0;
            text-align: center;
        }
        nav a {
            color: #00BFFF;
            text-decoration: none;
            padding: 10px 15px;
            margin: 0 15px;
            border-radius: 5px;
            transition: background 0.3s, transform 0.3s;
            display: inline-block;
            font-size: 1.1em;
        }
        nav a:hover {
            background-color: #292929;
            transform: translateY(-2px);
        }
        main {
            max-width: 900px;
            margin: auto;
            padding: 20px;
            background: #2c2c2c;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            overflow: hidden; /* Menghindari scroll pada main */
        }
        p {
            line-height: 1.6;
            margin: 15px 0;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            background: #292929;
            margin: 10px 0;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(255, 255, 255, 0.1);
            transition: background 0.3s;
        }
        li:hover {
            background: #333;
        }
        footer {
            margin-top: 30px;
            text-align: center;
            font-size: 0.9em;
            color: #bbb;
        }
        .img-container {
            text-align: center;
            margin: 20px 0;
            border: 5px solid #4CAF50;
            border-radius: 10px;
            padding: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }
        .img-container img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            transition: transform 0.3s;
        }
        .img-container img:hover {
            transform: scale(1.05);
        }
        .section {
            background-color: #3c3c3c; /* Warna latar belakang yang lebih terang */
            padding: 15px;
            border-radius: 8px;
            margin: 10px 0;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5); /* Tambahkan bayangan */
        }
        .highlight {
            color: #00BFFF;
            font-weight: bold;
        }
        .social-links a {
            color: #00BFFF;
            margin: 0 10px;
            font-size: 1.1em;
        }
        .social-links a:hover {
            text-decoration: underline;
        }
        .card {
            background: #292929;
            border-radius: 8px;
            padding: 15px;
            margin: 10px 0;
            box-shadow: 0 2px 5px rgba(255, 255, 255, 0.1);
            transition: transform 0.3s;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 10px rgba(255, 255, 255, 0.3);
        }
    </style>
    <script>
        function scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            section.scrollIntoView({ behavior: 'smooth' });
        }
        
        document.addEventListener('DOMContentLoaded', () => {
            const elements = document.querySelectorAll('header, main, .section');
            elements.forEach((element, index) => {
                element.style.animationDelay = ${index * 0.2}s; // Tambahkan delay pada animasi
            });
            // Menampilkan elemen dengan animasi
            elements.forEach(element => {
                element.style.opacity = 1;
            });
        });
    </script>
</head>
<body>
    <div class="marquee">Selamat datang di website Fraell :)</div>
    <header>
        <h1>Pembahasan Teknologi</h1>
    </header>
    <nav>
        <a href="#home" onclick="scrollToSection('home'); return false;">Beranda</a>
        <a href="#isi" onclick="scrollToSection('isi'); return false;">Isi</a>
        <a href="#penutup" onclick="scrollToSection('penutup'); return false;">Penutup</a>
        <a href="#kontak" onclick="scrollToSection('kontak'); return false;">Kontak</a>
    </nav>
    <main>
        <div id="home" class="section">
            <p>Teknologi telah menjadi bagian penting dalam kehidupan kita sehari-hari. Dari komunikasi hingga kesehatan, inovasi teknologi telah mengubah cara kita berinteraksi, belajar, dan bekerja. Di era digital ini, hampir semua aspek kehidupan kita terhubung dengan teknologi, dan pemahaman tentang penerapannya menjadi sangat penting.</p>
        </div>
        
        <div class="img-container">
            <img src="https://www.researchgate.net/profile/Muhammad-Hafidz-16/publication/367147392/figure/fig1/AS:11431281113080142@1673703699900/Gambar-1-Perkembangan-Teknologi-Informasi-dan-Komunikasi-Anwar-2021.jpg" alt="Teknologi">
        </div>
        
        <div id="isi" class="section">
            <p>Perkembangan teknologi yang pesat memberikan banyak kemudahan, tetapi juga menghadirkan tantangan baru yang perlu kita hadapi. Mari kita eksplorasi lebih dalam tentang penerapan teknologi di berbagai bidang. Misalnya, dalam bidang komunikasi, smartphone telah mengubah cara kita berinteraksi. Kini, kita dapat berkomunikasi dengan siapa saja di seluruh dunia hanya dalam hitungan detik.</p>
        </div>
        
        <ul>
            <li class="card"><strong class="highlight">Komunikasi:</strong> Dengan smartphone, kita dapat berkomunikasi dengan siapa saja di seluruh dunia dalam hitungan detik. Aplikasi seperti WhatsApp dan Facebook Messenger memungkinkan kita untuk mengirim pesan teks, gambar, dan video secara real-time.</li>
            <li class="card"><strong class="highlight">Pendidikan:</strong> E-learning dan platform pendidikan online seperti Coursera dan Khan Academy membuat akses belajar menjadi lebih mudah. Siswa dapat belajar dari rumah dengan fleksibilitas waktu, dan institusi pendidikan dapat menjangkau lebih banyak siswa di berbagai lokasi.</li>
            <li class="card"><strong class="highlight">Transportasi:</strong> Teknologi telah mengubah cara kita bepergian, dari aplikasi ride-sharing seperti Gojek dan Grab hingga kendaraan listrik yang lebih ramah lingkungan. Mobilitas menjadi lebih efisien dan terjangkau.</li>
            <li class="card"><strong class="highlight">Kesehatan:</strong> Inovasi dalam teknologi medis telah meningkatkan diagnosis dan perawatan pasien. Alat kesehatan yang canggih dan aplikasi kesehatan dapat membantu kita memantau kondisi kesehatan secara lebih efektif dan memberikan perawatan yang lebih cepat dan tepat.</li>
            <li class="card"><strong class="highlight">Keamanan:</strong> Teknologi juga berperan dalam meningkatkan keamanan, baik dalam dunia maya maupun fisik. Sistem pengawasan yang menggunakan kecerdasan buatan dapat membantu mendeteksi ancaman dan merespons dengan cepat, sementara perangkat lunak keamanan melindungi data pribadi kita dari serangan siber.</li>
        </ul>

        <div id="penutup" class="section">
            <h2 style="text-align: center;">Penutup</h2>
            <p>Teknologi terus berkembang dan membawa perubahan yang signifikan dalam berbagai aspek kehidupan kita. Dari cara kita berkomunikasi hingga cara kita belajar dan berinteraksi, inovasi teknologi tidak hanya mempermudah hidup kita, tetapi juga menghadirkan tantangan yang perlu kita hadapi bersama. Oleh karena itu, penting bagi kita untuk terus belajar dan beradaptasi dengan perkembangan ini, sehingga kita dapat memanfaatkan teknologi dengan bijak. Mari kita sambut masa depan dengan semangat, siap untuk berinovasi dan menjawab tantangan yang ada di depan kita.</p>
        </div>

        <div id="kontak" class="section">
            <h2 style="text-align: center;">Kontak Sosial Media</h2>
            <div class="social-links" style="text-align: center;">
                <a href="https://instagram.com/Fraell" target="_blank">Instagram</a>
                <a href="https://facebook.com/Fraell" target="_blank">Facebook</a>
                <a href="mailto:fraell@example.com">Gmail</a>
            </div>
        </div>
    </main>
    <footer>
        <p>© 2024 Fraell. Semua hak dilindungi.</p>
    </footer>
</body>
</html>
