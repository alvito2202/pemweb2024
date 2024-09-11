!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            background-image: url('wp.jpg');
            font-family: Verdana, sans-serif;
            margin: 0;
            padding: 0;
        }
        
        h1, h2 {
            color: rgb(246, 250, 246);
            font-family: serif;
        }

        p, li {
            color: rgb(247, 248, 247);
            font-size: 20px;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }

        .content {
            background-image: url('xx.jpg');
            padding: 25px;
            border-radius: 10px;
        }

        /* CSS untuk menu container */
        .menu-container {
            display: flex;
            justify-content: flex-end;
            align-items: center;
            position: relative; /* Untuk posisi absolute pada dropdown */
            margin-bottom: 20px;
        }

        .menu-icon {
            cursor: pointer;
            font-size: 36px; /* Ukuran lebih besar */
            color: rgb(236, 240, 236);
        }

        .dropdown-menu {
            display: none;
            position: absolute;
            right: 0;
            top: 100%; /* Jarak dari ikon garis tiga */
            background-color: rgb(26, 27, 26);
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
            text-align: left;
            z-index: 1000;
        }

        .dropdown-menu a {
            display: block;
            padding: 10px;
            color: rgb(239, 240, 248);
            text-decoration: none;
            border-bottom: 1px solid rgba(0,0,0,0.1);
        }

        .dropdown-menu a:hover {
            background-color: rgb(230, 230, 230);
        }

        /* Tombol Navigasi */
        nav {
            display: none; /* Disembunyikan karena kita menggunakan dropdown menu */
        }

        .section {
            display: none;
        }

        .active {
            display: block;
        }

        .bio-photo {
            display: block;
            margin: 20px auto;
            width: 150px;
            height: 150px;
            border-radius: 50%;
        }

        .social-icons {
            text-align: center;
            margin-top: 20px;
        }

        .social-icons a {
            margin: 0 10px;
            font-size: 24px;
            color: rgb(246, 248, 246);
            text-decoration: none;
        }

        .social-icons a:hover {
            color: rgb(237, 243, 237);
        }
    </style>
    <title>Dynamic Content Website</title>
</head>
<body>

<div class="container">
    <!-- Menu Container -->
    <div class="menu-container">
        <div class="menu-icon" onclick="toggleDropdown()">&#9776;</div> <!-- Ikon Garis Tiga -->
        <div class="dropdown-menu" id="dropdown-menu">
            <a href="#" onclick="showSection('home')">Home</a>
            <a href="#" onclick="showSection('about')">About</a>
            <a href="#" onclick="showSection('contact')">Contact</a>
        </div>
    </div>
    
    <div class="content">
        <!-- Home Section -->
        <div id="home" class="section active">
            <h1>Selamat datang di website saya</h1>
            
            <!-- Tambahan Foto Biodata -->
            <img src="bio.jpeg" alt="Foto Profil" class="bio-photo">
            <p><strong>Nama:</strong> Alvito Dikatama</p>
            <p><strong>Tanggal Lahir:</strong> 11 Oktober 2004</p>
            <p><strong>Alamat:</strong> Jl. Raya Sukoharjo III, Sukoharjo II, Kec. Sukoharjo, Kabupaten Pringsewu, Lampung 35373</p>
            <p><strong>NPM:</strong> 2313025006</p>
            <p><strong>Kelas:</strong> PTI-23B</p>

            <p>Di sini saya hanya sebagai pemula yang tidak bisa apa apa namun di sini saya mencoba untuk bisa namun saat ini saya belum bisa apa apa.</p>
        </div>

        <!-- About Section -->
        <div id="about" class="section">
            <h2>Bahasa Pemrograman Website</h2>
            <ul>
                <p>Saya membuat website ini dngan menggunakan beberpa bahasa di antaranya adalah: </p>
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
                <p>pengalaman saya</p>
                  <li>saya sudah mempelajari beberapa bahasa pemrograman di antaranya seperti yang sudah saya gunakan pada program ini</li>
            </ul>
        </div>

        <!-- Contact Section -->
        <div id="contact" class="section">
            <h2>Kontak:</h2>
            <p>Gmail: alvitodika2202@gmail.com</p>
            <p>WA: 087718516491</p>

            <!-- Tambahan Media Sosial -->
            <div class="social-icons">
                <a href="https://www.instagram.com/tama6415/profilecard/?igsh=MTRtOGV5YmhhN2loMg==" target="_blank">Instagram</a>
                <a href="https://www.facebook.com/profile.php?id=100016070436215" target="_blank">Facebook</a>
            </div>
        </div>
    </div>
</div>

<script>
    function showSection(sectionId) {
        var sections = document.querySelectorAll('.section');
        sections.forEach(function(section) {
            section.classList.remove('active');
        });

        var activeSection = document.getElementById(sectionId);
        activeSection.classList.add('active');
    }

    function toggleDropdown() {
        var dropdownMenu = document.getElementById('dropdown-menu');
        if (dropdownMenu.style.display === 'block') {
            dropdownMenu.style.display = 'none';
        } else {
            dropdownMenu.style.display = 'block';
        }
    }
</script>

</body>
</html>




