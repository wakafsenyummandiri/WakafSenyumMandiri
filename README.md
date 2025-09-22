[landing-page.html](https://github.com/user-attachments/files/22459984/landing-page.html)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WAKAF SENYUM MANDIRI</title>
    <style>
        /* Reset dan Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Sans-serif', Poppins;


            line-height: 1;
            color: #46f054;
            background-color: #f8f9fa;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }


        header {
            background: linear-gradient(135deg, #09b840, #09b840);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo img {
            width: 50px;
            height: 50px;
        }

        .logo h1 {
            font-size: 1.8rem;
            font-weight: bold;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: opacity 0.3s ease;
        }

        nav a:hover {
            opacity: 0.8;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://placeholder-image-service.onrender.com/image/1200x600?prompt=People%20volunteering%20and%20helping%20community%20with%20smiles&id=hero-bg') center/cover no-repeat;
            color: white;
            text-align: center;
            padding: 150px 20px 100px;
            margin-top: 80px;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-weight: bold;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-button {
            display: inline-block;
            background: #ff6b35;
            color: white;
            padding: 15px 40px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: background 0.3s ease, transform 0.2s ease;
            box-shadow: 0 4px 15px rgba(192, 114, 12, 0.3);
        }

        .cta-button:hover {
            background: #e55a2b;
            transform: translateY(-2px);
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background: white;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2.5rem;
            color: #2c7744;
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        /* Programs Section */
        .programs {
            padding: 80px 0;
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: #09b840;
            margin-bottom: 50px;
        }

        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .program-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .program-card:hover {
            transform: translateY(-5px);
        }

        .program-card h3 {
            color: #09b840;
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        /* Articles Section */
        .articles {
            padding: 80px 0;
            background: white;
        }

        .articles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .article-card {
            background: #f8f9fa;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .article-image img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .article-content {
            padding: 20px;
        }

        .article-content h3 {
            color: #2c7744;
            margin-bottom: 10px;
        }

        .read-more {
            color: #ff6b35;
            text-decoration: none;
            font-weight: 500;
        }

        /* Waqaf Section */
        .waqaf {
            padding: 80px 0;
            background: linear-gradient(135deg, #09b840, #09b840);
            color: white;
            text-align: center;
        }

        .waqaf-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .waqaf-content h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .waqaf-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }

        .step {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        .step-number {
            background: #ff6b35;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 1.5rem;
            font-weight: bold;
        }

        /* Contact Section */
        .contact {
            padding: 80px 0;
            background: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info h3 {
            color: #09b840;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        .contact-details {
            margin-bottom: 30px;
        }

        .contact-detail {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .contact-detail i {
            width: 30px;
            color: #ff6b35;
            font-size: 1.2rem;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact-form textarea {
            height: 120px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: #09b840;
            color: white;
            padding: 50px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-section h3 {
            margin-bottom: 20px;
            color: hsl(0, 0%, 91%);
        }

        .footer-section p {
            margin-bottom: 15px;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: #ff6b35;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 20px;
            }

            nav ul {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero {
                padding: 120px 20px 80px;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .contact-container {
                grid-template-columns: 1fr;
            }

            .waqaf-steps {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .logo h1 {
                font-size: 1.5rem;
            }

            .hero h2 {
                font-size: 1.8rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .programs-grid,
            .articles-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="https://placeholder-image-service.onrender.com/image/100x100?prompt=Wakaf%20Senyum%20Mandiri%20logo%20with%20smiling%20sun%20and%20hands&id=logo-wsm" alt="Logo WAKAF SENYUM MANDIRI dengan gambar matahari tersenyum dan tangan saling membantu">
                <h1>WAKAF SENYUM MANDIRI</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Beranda</a></li>
                    <li><a href="#about">Tentang Kami</a></li>
                    <li><a href="#programs">Program</a></li>
                    <li><a href="#articles">Artikel</a></li>
                    <li><a href="#waqaf">Wakaf</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h2>WAKAF SENYUM MANDIRI</h2>
            <p style="font-size: 30px ; text-align: center;" >Menebar Sejuta Manfaat</p>
            <br>
            <br>
            <a href="#waqaf" class="cta-button">Wakaf Sekarang</a>
        </div>
    </section

    <-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>Tentang Kami </h2>
                    <style>
    p {
      text-align: justify;
    }
  </style>
</head>
<body>
                    <p style="text-align: justify;">Wakaf Senyum Mandiri adalah wadah berwakaf yang berlandaskan pada empat pilar utama yaitu Amanah, Mudah, Bermanfaat, </p>
                    <p style="text-align: justify;">Dengan prinsip amanah, setiap titipan dikelola sesuai syariat secara transparan. Melalui kemudahan layanan, siapa pun dapat berwakaf uang maupun aset dengan praktis dan sederhana. </p>
                    <p style="text-align: justify;">Hasilnya diwujudkan dalam program produktif di bidang pendidikan, sosial, dan pemberdayaan ekonomi, sehingga wakaf benar-benar menghadirkan senyum, kemandirian, dan keberkahan bagi umat.</p>
                </div>
                <div class="about-image">
                    <img src="https://placeholder-image-service.onrender.com/image/600x400?prompt=Community%20helping%20each%20other%20with%20smiles%20and%20compassion&id=about-image" alt="Komunitas WAKAF SENYUM MANDIRI sedang membantu sesama dengan penuh senyum dan kasih sayang">
                </div>
            </div>
        </div>
    </section>

    <!-- Programs Section -->
    <section id="programs" class="programs">
        <div class="container">
            <h2 class="section-title">Program Kami</h2>
            <div class="programs-grid">
                <div class="program-card">
                    <h3>Wakaf Al-Quran</h3>
                    <p>deskripsi</p>
                </div>
                <div class="program-card">
                    <h3>Wakaf Karpet</h3>
                     <p>deskripsi</p>
                </div>
                <div class="program-card">
                    <h3>Wakaf Pembangunan Kelas Tahfidz</h3>
                     <p>deskripsi</p>
                </div>
                <div class="program-card">
                    <h3>Wakaf Pembebasan Lahan Asrama</h3>
                                         <p>deskripsi</p>

                </div>
            </div>
        </div>
    </section>

    <!-- Articles Section -->
    <section id="articles" class="articles">
        <div class="container">
            <h2 class="section-title">Artikel Terbaru</h2>
            <div class="articles-grid">
                <div class="article-card">
                    <div class="article-image">
                        <img src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Students%20studying%20with%20new%20books%20and%20uniforms&id=article-1" alt="Siswa-siswa belajar dengan seragam dan buku baru dari program wakaf pendidikan">
                    </div>
                    <div class="article-content">
                        <h3>Dampak Positif Wakaf Pendidikan bagi Masa Depan Anak</h3>
                        <p>Bagaimana wakaf pendidikan telah mengubah hidup ratusan anak dan memberikan mereka harapan baru...</p>
                        <a href="#" class="read-more">Baca Selengkapnya →</a>
                    </div>
                </div>
                <div class="article-card">
                    <div class="article-image">
                        <img src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Medical%20workers%20helping%20patients%20in%20community%20clinic&id=article-2" alt="Tenaga medis membantu pasien di klinik komunitas wakaf kesehatan">
                    </div>
                    <div class="article-content">
                        <h3>Peran Wakaf Kesehatan dalam Meningkatkan Kualitas Hidup</h3>
                        <p>Kisah inspiratif tentang bagaimana layanan kesehatan wakaf menyelamatkan nyawa dan memberikan...</p>
                        <a href="#" class="read-more">Baca Selengkapnya →</a>
                    </div>
                </div>
                <div class="article-card">
                    <div class="article-image">
                        <img src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Small%20business%20owners%20smiling%20with%20their%20products&id=article-3" alt="Pemilik usaha kecil tersenyum dengan produk mereka yang didukung program wakaf ekonomi">
                    </div>
                    <div class="article-content">
                        <h3>Suksesnya Program Wakaf Ekonomi untuk UMKM</h3>
                        <p>Cerita sukses para penerima manfaat wakaf ekonomi yang kini telah mandiri secara finansial...</p>
                        <a href="#" class="read-more">Baca Selengkapnya →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Waqaf Section -->
    <section id="waqaf" class="waqaf">
        <div class="container">
            <div class="waqaf-content">
                <h2> Yuk Wakaf Sekarang</h2>
                <p style="text-align: center;">Dengan satu kali klik, Wakafers dapat memberikan manfaat keberlanjutan bagi yang membutuhkan</p>
                
                <div class="waqaf-steps" style="text-align: center;";">
                    <div class="step">
                        <div class="step-number">1</div>
                        <h3>Pilih Program</h3>
                        <p>Pilih program wakaf yang Wakafers inginkan</p>
                    </div>
                    <div class="step">
                        <div class="step-number">2</div>
                        <h3>Tentukan Nominal</h3>
                        <p>Tentukan jumlah wakaf yang ingin Wakafers berikan</p>
                    </div style="text-align: center">
                    <div class="step" style="text-align: center;">
                        <div class="step-number">3</div style="text-align :center">
                        <h3>Wakaf Sekarang</h3>
                        <p>Lakukan pembayaran dengan mudah melalui berbagai metode pembayaran yang tersedia</p>
                    </div>
                </div>

                <a href="#" class="cta-button">Wakaf Sekarang</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Hubungi Kami</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Informasi Kontak</h3>
                    <div class="contact-details">
                        <div class="contact-detail">
                            <span> Alamat : Jalan Veteran ruko Oesman, Jl. Usman Singawinata Blk. A No.1 ruko, RW.8, Nagri Kaler, Kec. Purwakarta, Kabupaten Purwakarta, Jawa Barat 41115</span>
                        </div>
                        <div class="contact-detail">
                            <span> WhatsApp+62-878-4978-2492</span>
                        </div>
                        <div class="contact-detail">
                            <span>@wakafsenyummandiri</span>
                        </div>
                        <div class="contact-detail">
                            <span> Jam Kerja : Senin - Sabtu: 08:00 - 16:00 WIB</span>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Kirim Pesan</h3>
                    <form>
                        <input type="text" placeholder="Nama Lengkap" required>
                        <input type="email" placeholder="Email" required>
                        <input type="tel" placeholder="Nomor Telepon">
                        <textarea placeholder="Pesan Anda" required></textarea>
                        <button type="submit" class="cta-button">Kirim Pesan</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>WAKAF SENYUM MANDIRI</h3>
                    <p>Menebar Sejuta Manfaat</p>
                </div>
                <div class="footer-section">
                    <h3>Link Cepat</h3>
                    <p><a href="#home">Beranda</a></p>
                    <p><a href="#about">Tentang Kami</a></p>
                    <p><a href="#programs">Program</a></p>
                    <p><a href="#waqaf">Wakaf</a></p>
                </div>
                <div class="footer-section">
                    <h3>Kontak</h3>
                    <p>Email: @wakafsenyummandiri.org</p>
                    <p>Telepon: +62 21 1234 5678</p>
                    <p>Alamat: Jalan Veteran ruko Oesman, Jl. Usman Singawinata Blk. A No.1 ruko, RW.8, Nagri Kaler, Kec. Purwakarta, Kabupaten Purwakarta, Jawa Barat 41115</span>
</p>
                </div>
                <div class="footer-section">
                    <h3>Ikuti Kami</h3>
                    <div class="social-links">
                        <a href="#">Instagram</a> 
                        <br>
                        <a href="#">Facebook</a>
                        <a href="#">Tiktok</a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p style="text-align: center;">&copy; 2025 WAKAF SENYUM MANDIRI</p>
            </div>
        </div>
    </footer>
</body>
</html>
