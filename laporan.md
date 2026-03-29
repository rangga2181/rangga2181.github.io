# LAPORAN PRAKTIKUM PEMBUATAN WEB PROFILE

**Nama:** Rangga Pradarrell Fathi  
**NIM:** 2311102200  
**Kelas:** Reguler  
**Asisten:** [Nama Asisten]  

**PROGRAM STUDI TEKNIK INFORMATIKA**  
**FAKULTAS INFORMATIKA**  
**UNIVERSITAS TELKOM**  
**PURWOKERTO**  
**2026**

---

## DAFTAR ISI

- DAFTAR ISI
- BAB I PENDAHULUAN
  - 1.1 Latar Belakang
  - 1.2 Tujuan Praktikum
- BAB II DESKRIPSI WEBSITE
  - 2.1 Gambaran Umum Website
  - 2.2 Tujuan Pembuatan Website
  - 2.3 Fitur-Fitur Website
- BAB III STRUKTUR DAN DESAIN WEBSITE
  - 3.1 Struktur Halaman HTML
  - 3.2 Desain CSS yang Digunakan
  - 3.3 Implementasi Bootstrap
- BAB IV IMPLEMENTASI PEMROGRAMAN
  - 4.1 Implementasi JavaScript
  - 4.2 Implementasi AJAX
  - 4.3 Web Service / API yang Digunakan
- BAB V PENJELASAN POTONGAN KODE PROGRAM
  - 5.1 Penjelasan Kode HTML
  - 5.2 Penjelasan Kode CSS
  - 5.3 Penjelasan Kode JavaScript
- BAB VI HASIL DAN PEMBAHASAN
  - 6.1 Hasil Tampilan Website
  - 6.2 Analisis Fungsionalitas Website
- BAB VII PENUTUP
  - 7.1 Kesimpulan

---

# BAB I PENDAHULUAN

## 1.1. Latar Belakang

Pada era digital saat ini, keberadaan portofolio online menjadi sangat penting bagi seorang developer untuk menampilkan kemampuan dan proyek yang telah dikerjakan. Website profil pribadi berfungsi sebagai media untuk memperkenalkan diri, menampilkan informasi pendidikan, keterampilan, serta karya yang telah dibuat dalam satu platform yang mudah diakses.

Praktikum ini bertujuan untuk membuat sebuah website web profile pribadi menggunakan HTML, CSS, JavaScript, dan Bootstrap. Website yang dibuat mengimplementasikan konsep single page website, dimana semua informasi ditampilkan dalam satu halaman dengan navigasi smooth scroll. Selain itu, website juga terintegrasi dengan berbagai public API untuk menampilkan data dinamis seperti quote motivasi, informasi cuaca, dan profil GitHub.

## 1.2. Tujuan Praktikum

Tujuan dari praktikum ini adalah:
1. Memahami struktur HTML5 semantik untuk pembangunan website
2. Mampu menerapkan Bootstrap untuk membuat layout yang responsif
3. Menguasai penggunaan CSS untuk desain visual yang menarik
4. Mampu mengimplementasikan JavaScript untuk interaktivitas website
5. Memahami konsep AJAX untuk mengambil data dari public API
6. Membuat website portofolio pribadi yang informatif dan profesional

---

# BAB II DESKRIPSI WEBSITE

## 2.1. Gambaran Umum Website

Website yang dibuat merupakan web profile pribadi dengan konsep single page application. Semua konten utama ditempatkan dalam satu file HTML (`webprofile.html`) dan dibagi menjadi beberapa section yaitu home, about, education, skills, portfolio, API data, dan contact. Navigasi antar section dilakukan melalui navbar yang固定在 bagian atas halaman dengan fitur smooth scrolling.

Website ini menggunakan template Clark yang dimodifikasi sesuai kebutuhan, dengan tambahan custom CSS untuk komponen khusus seperti GitHub profile card, weather card, dan quote section. Integrasi dengan public API membuat website menampilkan data yang selalu diperbarui secara otomatis.

## 2.2. Tujuan Pembuatan Website

Website ini dibuat dengan tujuan:
1. Sebagai media portofolio digital untuk menampilkan identitas dan kemampuan pribadi
2. Menampilkan proyek-proyek yang telah dikerjakan selama perkuliahan
3. Sebagai sarana pembelajaran implementasi teknologi web frontend (HTML, CSS, JavaScript, Bootstrap)
4. Mengimplementasikan integrasi dengan public API untuk konten dinamis
5. Menyediakan sarana kontak bagi pengunjung yang ingin berkolaborasi

## 2.3. Fitur-Fitur Website

Fitur utama pada website ini antara lain:
- **Navbar Responsive** – Menu navigasi dengan smooth scroll ke setiap section
- **Hero Section** – Tampilan awal dengan nama, jabatan, dan foto background
- **About Me** – Informasi pribadi lengkap (nama, NIM, tanggal lahir, alamat, email, telepon)
- **Education** – Riwayat pendidikan formal dengan IPK saat ini
- **Skills** – Tiga kategori kemampuan (Technical Skills, Soft Skills, Languages)
- **Portfolio** – Galeri proyek dengan overlay dan badges kategori
- **API Data Section** – Integrasi live data dari 3 public API (Quote, Weather, GitHub)
- **Contact Form** – Formulir kontak terintegrasi dengan FormSubmit API
- **Contact Information** – Informasi kontak (alamat, telepon, email, website)
- **Footer** – Tautan navigasi dan informasi kontak tambahan
- **Responsive Design** – Tampilan optimal untuk desktop, tablet, dan mobile

---

# BAB III STRUKTUR DAN DESAIN WEBSITE

## 3.1. Struktur Halaman HTML

Struktur website dibangun menggunakan HTML5 dengan elemen-elemen semantik. Berikut adalah struktur utama website:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta tags & CSS links -->
</head>
<body data-spy="scroll" data-target=".site-navbar-target" data-offset="300">

    <!-- Navbar Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark ftco_navbar">...</nav>

    <!-- Home/Hero Section -->
    <section id="home-section">...</section>

    <!-- About Section -->
    <section id="about-section">...</section>

    <!-- Education Section -->
    <section id="education-section">...</section>

    <!-- Skills Section -->
    <section id="skills-section">...</section>

    <!-- Portfolio Section -->
    <section id="portfolio-section">...</section>

    <!-- API Data Section -->
    <section id="api-section">...</section>

    <!-- Contact Section -->
    <section id="contact-section">...</section>

    <!-- Footer -->
    <footer class="ftco-footer ftco-section">...</footer>

    <!-- JavaScript Libraries & Custom Scripts -->
    <script src="..."></script>
    <script>
        // AJAX & API Integration
    </script>
</body>
</html>
```

### Penjelasan Struktur:
- `<!DOCTYPE html>` – Deklarasi tipe dokumen HTML5
- `<html lang="en">` – Elemen root dengan atribut bahasa Inggris
- `<meta charset="utf-8">` – Encoding karakter UTF-8
- `<meta name="viewport">` – Responsive viewport setting
- `data-spy="scroll"` – Mengaktifkan Bootstrap scrollspy untuk highlight menu aktif
- Setiap section menggunakan atribut `id` unik untuk navigasi anchor link
- Struktur menggunakan container Bootstrap untuk layout responsif
- Grid system Bootstrap (`row`, `col-md-*`, `col-lg-*`) untuk layout kolom

## 3.2. Desain CSS yang Digunakan

### CSS Eksternal:
Website menggunakan beberapa stylesheet eksternal dari template Clark:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css">
<link rel="stylesheet" href="css/open-iconic-bootstrap.min.css">
<link rel="stylesheet" href="css/animate.css">
<link rel="stylesheet" href="css/owl.carousel.min.css">
<link rel="stylesheet" href="css/owl.theme.default.min.css">
<link rel="stylesheet" href="css/magnific-popup.css">
<link rel="stylesheet" href="css/aos.css">
<link rel="stylesheet" href="css/ionicons.min.css">
<link rel="stylesheet" href="css/flaticon.css">
<link rel="stylesheet" href="css/icomoon.css">
<link rel="stylesheet" href="css/style.css">
```

### Custom CSS:
Custom CSS ditambahkan di dalam tag `<style>` untuk komponen khusus:

#### a. Quote Section
```css
.quote-section {
    background: linear-gradient(135deg, #667eea 0%, #774ba2 100%);
    color: #fff;
    padding: 40px 20px;
    border-radius: 10px;
    margin: 30px 0;
}
```

#### b. Weather Card
```css
.weather-card {
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    color: #fff;
    padding: 30px;
    border-radius: 15px;
    text-align: center;
    margin: 20px 0;
}
```

#### c. GitHub Profile Card
```css
.github-profile {
    background: linear-gradient(130deg, #0f172a 0%, #1e293b 40%, #0b1120 100%);
    border-radius: 22px;
    padding: 34px;
    margin: 22px 0;
    color: #e2e8f0;
    position: relative;
    overflow: hidden;
    box-shadow: 0 20px 45px rgba(2, 6, 23, 0.45);
}

.github-profile::before,
.github-profile::after {
    content: "";
    position: absolute;
    border-radius: 999px;
    z-index: 0;
    pointer-events: none;
}

.github-profile::before {
    width: 320px;
    height: 320px;
    right: -130px;
    top: -130px;
    background: radial-gradient(circle, rgba(56, 189, 248, 0.32) 0%, rgba(56, 189, 248, 0) 70%);
}
```

#### d. Portfolio Project Overlay
```css
.portfolio-grid .project {
    border-radius: 16px;
    overflow: hidden;
    min-height: 360px;
    height: 100%;
    margin-bottom: 24px;
    box-shadow: 0 14px 32px rgba(0, 0, 0, 0.18);
    background-color: #111;
    background-size: cover;
    background-position: center;
    position: relative;
    isolation: isolate;
}

.portfolio-grid .project .overlay {
    opacity: 1;
    z-index: 0;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0.35) 0%, rgba(0, 0, 0, 0.86) 70%, rgba(0, 0, 0, 0.95) 100%);
}
```

### Teknik CSS yang Digunakan:
| Teknik | Deskripsi |
|--------|-----------|
| **Linear Gradient** | Background berwarna gradasi untuk visual menarik |
| **Radial Gradient** | Efek glow dekoratif pada GitHub profile card |
| **Flexbox** | Layout fleksibel untuk header GitHub dan stats |
| **CSS Grid** | Grid 4 kolom untuk GitHub statistics |
| **Media Queries** | Responsive design untuk layar mobile (< 768px) |
| **Pseudo-elements** | `::before` dan `::after` untuk efek dekoratif |
| **Box Shadow** | Efek kedalaman pada card dan tombol |
| **Backdrop Filter** | Efek blur pada stat-box GitHub profile |

## 3.3. Implementasi Bootstrap

### Versi Bootstrap:
Bootstrap 4.6.2 digunakan melalui CDN:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/js/bootstrap.bundle.min.js"></script>
```

### Komponen Bootstrap yang Digunakan:

#### a. Navbar
```html
<nav class="navbar navbar-expand-lg navbar-dark ftco_navbar ftco-navbar-light site-navbar-target" id="ftco-navbar">
    <div class="container">
        <a class="navbar-brand" href="webprofile.html">Rangga</a>
        <button class="navbar-toggler js-fh5co-nav-toggle fh5co-nav-toggle" type="button" 
                data-toggle="collapse" data-target="#ftco-nav">
            <span class="oi oi-menu"></span> Menu
        </button>
        <div class="collapse navbar-collapse" id="ftco-nav">
            <ul class="navbar-nav nav ml-auto">
                <li class="nav-item"><a href="#home-section" class="nav-link">Home</a></li>
                <li class="nav-item"><a href="#about-section" class="nav-link">About</a></li>
                <li class="nav-item"><a href="#portfolio-section" class="nav-link">Portfolio</a></li>
                <li class="nav-item"><a href="#contact-section" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </div>
</nav>
```

#### b. Grid System
```html
<div class="container">
    <div class="row">
        <div class="col-md-6 col-lg-4">
            <!-- Konten kolom -->
        </div>
    </div>
</div>
```

#### c. Buttons
```html
<a href="#contact-section" class="btn btn-primary py-3 px-4">Contact Me</a>
<a href="images/CV Rangga Pradarrell Fathi_INDO.pdf" download class="btn btn-primary py-3 px-3">Download CV</a>
```

#### d. Forms
```html
<form class="bg-light p-4 contact-form" id="contactForm">
    <div class="form-group">
        <input type="text" name="name" class="form-control" placeholder="Your Name" required>
    </div>
    <div class="form-group">
        <input type="email" name="email" class="form-control" placeholder="Your Email" required>
    </div>
    <div class="form-group">
        <textarea name="message" class="form-control" placeholder="Message" required></textarea>
    </div>
    <input type="submit" value="Send Message" class="btn btn-primary py-3 px-5">
</form>
```

#### e. Alerts
```html
<div class="alert alert-success alert-dismissible fade show" role="alert">
    <strong>Success!</strong> Your message has been sent.
    <button type="button" class="close" data-dismiss="alert">
        <span aria-hidden="true">&times;</span>
    </button>
</div>
```

#### f. Utilities
- `text-center` – Text alignment center
- `mb-4`, `mt-3` – Margin bottom/top spacing
- `p-4`, `py-3`, `px-5` – Padding spacing
- `d-flex` – Display flex
- `justify-content-center` – Flex justification
- `align-items-center` – Flex alignment
- `ftco-animate` – Animation class dari template

---

# BAB IV IMPLEMENTASI PEMROGRAMAN

## 4.1. Implementasi JavaScript

### Library JavaScript yang Digunakan:
- **jQuery 3.6.0** – Untuk manipulasi DOM dan AJAX
- **Bootstrap Bundle 4.6.2** – Untuk komponen interaktif Bootstrap
- **jQuery Migrate 3.0.1** – Kompatibilitas jQuery
- **Popper.js** – Untuk tooltip dan popover
- **jQuery Easing 1.3** – Animasi easing
- **jQuery Waypoints** – Trigger fungsi saat scroll
- **jQuery Stellar** – Parallax scrolling
- **Owl Carousel** – Slider carousel
- **Magnific Popup** – Lightbox popup
- **AOS (Animate On Scroll)** – Animasi scroll
- **jQuery AnimateNumber** – Animasi counter angka
- **Scrollax** – Parallax effect
- **Main.js** – Script utama template

### Fitur JavaScript yang Diimplementasikan:

#### a. Document Ready Handler
```javascript
$(document).ready(function () {
    // Inisialisasi semua fungsi saat DOM siap
    fetchQuote();
    fetchWeather();
    fetchGitHubProfile();
    setInterval(fetchQuote, 30000); // Refresh quote setiap 30 detik
});
```

#### b. Weather Description Helper
```javascript
function getWeatherDescription(code) {
    const descriptions = {
        0: "Clear Sky",
        1: "Mainly Clear",
        2: "Partly Cloudy",
        3: "Overcast",
        45: "Foggy",
        61: "Slight Rain",
        63: "Moderate Rain",
        65: "Heavy Rain",
        80: "Slight Rain Showers",
        95: "Thunderstorm"
    };
    return descriptions[code] || "Unknown";
}
```

## 4.2. Implementasi AJAX

AJAX (Asynchronous JavaScript and XML) diimplementasikan menggunakan jQuery `$.ajax()` untuk mengambil data dari public API tanpa reload halaman.

### a. Fetch Motivational Quote
```javascript
function fetchQuote() {
    $.ajax({
        url: "https://type.fit/api/quotes",
        method: "GET",
        dataType: "json",
        success: function (data) {
            const randomQuote = data[Math.floor(Math.random() * data.length)];
            $("#quote-container").html(`
                <p class="quote-text">"${randomQuote.text}"</p>
                <p class="quote-author">- ${randomQuote.author || "Unknown"}</p>
            `);
        },
        error: function () {
            $("#quote-container").html(`
                <p class="quote-text">"The only way to do great work is to love what you do."</p>
                <p class="quote-author">- Steve Jobs</p>
            `);
        }
    });
}
```

**Cara Kerja:**
1. `$.ajax()` mengirim HTTP GET request ke API quote
2. Response JSON diterima di callback `success`
3. Quote random dipilih menggunakan `Math.floor(Math.random() * data.length)`
4. HTML diupdate dengan `.html()` untuk menampilkan quote
5. Jika error, ditampilkan quote fallback dari Steve Jobs
6. `setInterval(fetchQuote, 30000)` mengulang fetch setiap 30 detik

### b. Fetch Weather Data
```javascript
function fetchWeather() {
    $.ajax({
        url: "https://api.open-meteo.com/v1/forecast?latitude=-6.5944&longitude=110.8380&current_weather=true&timezone=Asia%2FJakarta",
        method: "GET",
        dataType: "json",
        success: function (data) {
            const weather = data.current_weather;
            const temp = weather.temperature;
            const desc = getWeatherDescription(weather.weathercode);
            $("#weather-container").html(`
                <div class="weather-temp">${temp}°C</div>
                <div class="weather-desc">${desc}</div>
                <div class="mt-3">Wind: ${weather.windspeed} km/h</div>
            `);
        },
        error: function () {
            $("#weather-container").html(`
                <div class="weather-temp">28°C</div>
                <div class="weather-desc">Partly Cloudy</div>
                <div class="mt-3">Location: Jepara, Indonesia</div>
            `);
        }
    });
}
```

**Cara Kerja:**
1. API Open-Meteo dipanggil dengan koordinat Jepara (-6.5944, 110.8380)
2. Response berisi data cuaca real-time dalam `current_weather`
3. Weather code dikonversi ke deskripsi menggunakan fungsi helper `getWeatherDescription()`
4. Suhu, deskripsi, dan kecepatan angin ditampilkan
5. Jika error, ditampilkan data fallback

### c. Fetch GitHub Profile
```javascript
function fetchGitHubProfile() {
    $.ajax({
        url: "https://api.github.com/users/rangga2181",
        method: "GET",
        dataType: "json",
        success: function (data) {
            const joinedYear = data.created_at ? new Date(data.created_at).getFullYear() : null;
            const websiteLink = data.blog && data.blog.trim() !== ""
                ? (data.blog.startsWith("http") ? data.blog : "https://" + data.blog)
                : null;

            $("#github-container").html(`
                <div class="github-header">
                    <img src="${data.avatar_url}" alt="GitHub Avatar" class="github-avatar">
                    <div>
                        <div class="github-name">${data.name || data.login}</div>
                        <div class="github-username">@${data.login}</div>
                        <p class="github-bio">${data.bio || "Web Developer..."}</p>
                        <ul class="github-meta">
                            ${data.location ? `<li><i class="icon-map-pin mr-1"></i>${data.location}</li>` : ""}
                            ${data.company ? `<li><i class="icon-briefcase mr-1"></i>${data.company}</li>` : ""}
                            ${joinedYear ? `<li><i class="icon-calendar mr-1"></i>Joined ${joinedYear}</li>` : ""}
                        </ul>
                    </div>
                </div>
                <div class="github-actions">
                    <a href="${data.html_url}" target="_blank" class="btn btn-primary btn-sm">Visit GitHub</a>
                    <a href="${data.html_url}?tab=repositories" target="_blank" class="btn btn-outline-light btn-sm">View Repositories</a>
                    ${websiteLink ? `<a href="${websiteLink}" target="_blank" class="btn btn-outline-light btn-sm">Portfolio</a>` : ""}
                </div>
                <div class="github-stats">
                    <div class="stat-box">
                        <div class="stat-number">${data.public_repos}</div>
                        <div class="stat-label">Repositories</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">${data.followers}</div>
                        <div class="stat-label">Followers</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">${data.following}</div>
                        <div class="stat-label">Following</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">${data.public_gists}</div>
                        <div class="stat-label">Gists</div>
                    </div>
                </div>
            `);
        },
        error: function () {
            $("#github-container").html(`
                <div class="icon" style="font-size: 74px; color: #67e8f9;">
                    <i class="icon-github"></i>
                </div>
                <h3 class="github-name mb-2">@rangga2181</h3>
                <p class="github-bio mb-3">GitHub profile is temporarily unavailable.</p>
                <p><a href="https://github.com/rangga2181" target="_blank" class="btn btn-primary">Open GitHub Profile</a></p>
            `);
        }
    });
}
```

**Cara Kerja:**
1. GitHub User API dipanggil dengan username `rangga2181`
2. Data profil (avatar, nama, bio, stats) diambil dari response
3. Template literal digunakan untuk render HTML dinamis
4. Conditional rendering untuk data opsional (location, company, website)
5. Stats ditampilkan dalam grid 4 kolom (repos, followers, following, gists)
6. Jika error, ditampilkan fallback UI dengan link langsung ke profil

### d. Contact Form Submit dengan AJAX
```javascript
$("#contactForm").on("submit", function (e) {
    e.preventDefault();

    const form = $(this);
    const submitBtn = $("#submitBtn");
    const formMessage = $("#form-message");
    const formData = form.serialize();

    submitBtn.prop("disabled", true).html('<span class="spinner-border spinner-border-sm mr-2"></span>Sending...');
    formMessage.html("");

    $.ajax({
        url: "https://formsubmit.co/ajax/ranggapf04@gmail.com",
        method: "POST",
        data: formData,
        dataType: "json",
        success: function () {
            formMessage.html(`
                <div class="alert alert-success alert-dismissible fade show" role="alert">
                    <strong>Success!</strong> Your message has been sent.
                    <button type="button" class="close" data-dismiss="alert">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
            `);
            form[0].reset();
        },
        error: function () {
            formMessage.html(`
                <div class="alert alert-danger alert-dismissible fade show" role="alert">
                    <strong>Error!</strong> Failed to send message.
                </div>
            `);
        },
        complete: function () {
            submitBtn.prop("disabled", false).html("Send Message");
        }
    });
});
```

**Cara Kerja:**
1. Event submit dicegah dengan `e.preventDefault()` agar tidak reload
2. Data form diserialisasi dengan `.serialize()` menjadi query string
3. Tombol submit dinonaktifkan dan ditampilkan loading spinner
4. AJAX POST dikirim ke FormSubmit API
5. Response sukses menampilkan alert hijau, error menampilkan alert merah
6. Form di-reset setelah pengiriman berhasil
7. Tombol submit diaktifkan kembali di callback `complete`

## 4.3. Web Service / API yang Digunakan

| API | Endpoint | Fungsi | Response Data |
|-----|----------|--------|---------------|
| **Type.fit Quote API** | `https://type.fit/api/quotes` | Mengambil quote motivasi random | Array of `{text, author}` |
| **Open-Meteo Weather API** | `https://api.open-meteo.com/v1/forecast` | Cuaca real-time Jepara | `{current_weather: {temperature, weathercode, windspeed}}` |
| **GitHub User API** | `https://api.github.com/users/rangga2181` | Profil GitHub publik | `{avatar_url, name, bio, public_repos, followers, following, public_gists}` |
| **FormSubmit API** | `https://formsubmit.co/ajax/ranggapf04@gmail.com` | Pengiriman form kontak | `{success: true/false}` |

### Contoh Response API:

#### Quote API Response:
```json
[
    {"text": "The only way to do great work is to love what you do.", "author": "Steve Jobs"},
    {"text": "Innovation distinguishes between a leader and a follower.", "author": "Steve Jobs"},
    {"text": "Stay hungry, stay foolish.", "author": "Steve Jobs"}
]
```

#### Open-Meteo Weather Response:
```json
{
    "current_weather": {
        "temperature": 28.5,
        "windspeed": 12.3,
        "weathercode": 2,
        "time": "2026-03-29T14:00"
    }
}
```

#### GitHub API Response:
```json
{
    "login": "rangga2181",
    "name": "Rangga Fathi",
    "avatar_url": "https://avatars.githubusercontent.com/u/...",
    "bio": "Web Developer focused on modern solutions",
    "location": "Indonesia",
    "company": "Telkom University",
    "blog": "https://rangga2181.github.io/",
    "public_repos": 15,
    "followers": 10,
    "following": 5,
    "public_gists": 3,
    "created_at": "2020-01-15T08:30:00Z",
    "html_url": "https://github.com/rangga2181"
}
```

---

# BAB V PENJELASAN POTONGAN KODE PROGRAM

## 5.1. Penjelasan Kode HTML

HTML digunakan untuk membangun struktur utama website. Berikut adalah penjelasan potongan kode penting:

### a. Navbar Navigation

```html
<nav class="navbar navbar-expand-lg navbar-dark ftco_navbar ftco-navbar-light site-navbar-target" id="ftco-navbar">
    <div class="container">
        <a class="navbar-brand" href="webprofile.html">Rangga</a>
        <button class="navbar-toggler js-fh5co-nav-toggle fh5co-nav-toggle" type="button" 
                data-toggle="collapse" data-target="#ftco-nav" 
                aria-controls="ftco-nav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="oi oi-menu"></span> Menu
        </button>
        <div class="collapse navbar-collapse" id="ftco-nav">
            <ul class="navbar-nav nav ml-auto">
                <li class="nav-item"><a href="#home-section" class="nav-link"><span>Home</span></a></li>
                <li class="nav-item"><a href="#about-section" class="nav-link"><span>About</span></a></li>
                <li class="nav-item"><a href="#education-section" class="nav-link"><span>Education</span></a></li>
                <li class="nav-item"><a href="#skills-section" class="nav-link"><span>Skills</span></a></li>
                <li class="nav-item"><a href="#portfolio-section" class="nav-link"><span>Portfolio</span></a></li>
                <li class="nav-item"><a href="#api-section" class="nav-link"><span>API Data</span></a></li>
                <li class="nav-item"><a href="#contact-section" class="nav-link"><span>Contact</span></a></li>
            </ul>
        </div>
    </div>
</nav>
```

**Penjelasan:**
- `<nav>` – Elemen semantik untuk navigasi utama
- `navbar navbar-expand-lg` – Class Bootstrap untuk navbar responsive
- `navbar-dark` – Navbar dengan teks terang dan background gelap
- `site-navbar-target` – Custom class untuk scrollspy targeting
- `navbar-brand` – Logo/nama website di sebelah kiri
- `navbar-toggler` – Tombol hamburger untuk mobile view
- `data-toggle="collapse"` – Bootstrap data attribute untuk toggle menu
- `ml-auto` – Margin left auto untuk mendorong menu ke kanan
- Setiap `nav-link` memiliki `href` anchor link ke section соответствующий

### b. Hero Section

```html
<section class="hero-wrap js-fullheight" id="home-section" 
         style="background-image: url('images/bg_1.jpg');" data-stellar-background-ratio="0.5">
    <div class="overlay"></div>
    <div class="container">
        <div class="row no-gutters slider-text js-fullheight align-items-center justify-content-center">
            <div class="col-md-12 ftco-animate text-center">
                <h1 class="mb-4">I'm <span>Rangga Pradarrell Fathi</span></h1>
                <h2 class="mb-4">Web Developer</h2>
                <p>A software developer and technology innovator dedicated to building intelligent solutions 
                   across AI and full-stack web and mobile platforms.</p>
                <p><a href="#contact-section" class="btn btn-primary py-3 px-4">Contact Me</a></p>
            </div>
        </div>
    </div>
</section>
```

**Penjelasan:**
- `<section>` – Elemen semantik untuk section halaman
- `hero-wrap js-fullheight` – Class untuk section full height
- `background-image` – Inline CSS untuk background image
- `data-stellar-background-ratio` – Parallax scrolling effect
- `.overlay` – Layer gelap di atas background image
- `ftco-animate` – Class animasi dari template
- `text-center` – Bootstrap utility untuk text alignment center

### c. About Section

```html
<section class="ftco-about img ftco-section ftco-no-pb" id="about-section">
    <div class="container">
        <div class="row d-flex">
            <div class="col-md-6 col-lg-5 d-flex">
                <div class="img-about img d-flex align-items-stretch">
                    <div class="overlay"></div>
                    <div class="img d-flex align-self-stretch align-items-center" 
                         style="background-image:url(images/bg_1.png);">
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-7 pl-lg-5 pb-5">
                <div class="row justify-content-start pb-3">
                    <div class="col-md-12 heading-section ftco-animate">
                        <h1 class="big">About</h1>
                        <h2 class="mb-4">About Me</h2>
                        <p>Hello! I'm Rangga Pradarrell Fathi...</p>
                        <ul class="about-info mt-4 px-md-0 px-2">
                            <li class="d-flex"><span>Name:</span> <span>Rangga Pradarrell Fathi</span></li>
                            <li class="d-flex"><span>NIM:</span> <span>2311102200</span></li>
                            <li class="d-flex"><span>Email:</span> <span>ranggapf04@gmail.com</span></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```

**Penjelasan:**
- Layout 2 kolom: kiri untuk gambar, kanan untuk informasi
- `col-md-6 col-lg-5` – Kolom kiri (gambar)
- `col-md-6 col-lg-7` – Kolom kanan (konten)
- `.about-info` – List informasi pribadi
- `d-flex` – Display flex untuk layout
- `big` – Class untuk teks "About" besar di background

### d. Portfolio Project Card

```html
<div class="col-md-6 col-lg-4">
    <div class="project ftco-animate d-flex align-items-end" 
         style="background-image: url(images/cukurmen.png);">
        <div class="overlay"></div>
        <div class="text">
            <h3><a href="#">Cukurmen</a></h3>
            <span>Fullstack Development</span>
            <p>Platform booking barbershop yang membantu pengguna membuat janji layanan dengan cepat dan efisien.</p>
            <div class="project-tags">
                <span class="badge badge-primary">Fullstack</span>
                <span class="badge badge-info">Booking System</span>
                <span class="badge badge-success">Web Platform</span>
            </div>
        </div>
    </div>
</div>
```

**Penjelasan:**
- Grid 3 kolom untuk portfolio (`col-md-6 col-lg-4`)
- `background-image` – Inline CSS untuk gambar proyek
- `.overlay` – Layer gradasi di atas gambar
- `.text` – Konten teks di bagian bawah card
- `.project-tags` – Container untuk badges kategori
- `badge badge-*` – Class Bootstrap untuk label berwarna

### e. Contact Form

```html
<form action="https://formsubmit.co/ranggapf04@gmail.com" method="POST" 
      class="bg-light p-4 p-md-5 contact-form" id="contactForm">
    <input type="hidden" name="_subject" value="New Message from Web Profile!">
    <input type="hidden" name="_captcha" value="false">
    <input type="hidden" name="_template" value="table">
    <input type="hidden" name="_honey" style="display:none">
    
    <div class="form-group">
        <input type="text" name="name" class="form-control" placeholder="Your Name" required>
    </div>
    <div class="form-group">
        <input type="email" name="email" class="form-control" placeholder="Your Email" required>
    </div>
    <div class="form-group">
        <textarea name="message" id="message" cols="30" rows="7" 
                  class="form-control" placeholder="Message" required></textarea>
    </div>
    <div class="form-group">
        <input type="submit" value="Send Message" class="btn btn-primary py-3 px-5" id="submitBtn">
    </div>
    <div id="form-message" class="mt-3"></div>
</form>
```

**Penjelasan:**
- `action` – Endpoint FormSubmit API untuk pengiriman email
- `method="POST"` – HTTP method untuk mengirim data
- Input hidden untuk konfigurasi FormSubmit (subject, captcha, template)
- `_honey` – Honeypot field untuk mencegah spam
- `form-control` – Class Bootstrap untuk styling input
- `required` – HTML5 validation untuk field wajib
- `form-message` – Container untuk alert response

## 5.2. Penjelasan Kode CSS

### a. Linear Gradient Background

```css
.quote-section {
    background: linear-gradient(135deg, #667eea 0%, #774ba2 100%);
    color: #fff;
    padding: 40px 20px;
    border-radius: 10px;
    margin: 30px 0;
}
```

**Penjelasan:**
- `linear-gradient(135deg, ...)` – Gradasi diagonal 135 derajat
- `#667eea 0%` – Warna ungu di awal (0%)
- `#774ba2 100%` – Warna ungu tua di akhir (100%)
- `color: #fff` – Teks berwarna putih
- `padding: 40px 20px` – Padding vertikal 40px, horizontal 20px
- `border-radius: 10px` – Sudut melengkung 10px
- `margin: 30px 0` – Margin vertikal 30px

### b. GitHub Profile Card dengan Pseudo-elements

```css
.github-profile {
    background: linear-gradient(130deg, #0f172a 0%, #1e293b 40%, #0b1120 100%);
    border-radius: 22px;
    padding: 34px;
    margin: 22px 0;
    color: #e2e8f0;
    position: relative;
    overflow: hidden;
    box-shadow: 0 20px 45px rgba(2, 6, 23, 0.45);
}

.github-profile::before {
    content: "";
    position: absolute;
    width: 320px;
    height: 320px;
    right: -130px;
    top: -130px;
    background: radial-gradient(circle, rgba(56, 189, 248, 0.32) 0%, rgba(56, 189, 248, 0) 70%);
}

.github-profile::after {
    content: "";
    position: absolute;
    width: 300px;
    height: 300px;
    left: -120px;
    bottom: -150px;
    background: radial-gradient(circle, rgba(16, 185, 129, 0.24) 0%, rgba(16, 185, 129, 0) 72%);
}
```

**Penjelasan:**
- `linear-gradient(130deg, ...)` – Gradasi diagonal untuk background utama
- `position: relative` – Parent untuk pseudo-elements absolute
- `overflow: hidden` – Memotong pseudo-elements yang overflow
- `box-shadow` – Bayangan untuk efek kedalaman
- `::before` – Glow effect biru di kanan atas
- `::after` – Glow effect hijau di kiri bawah
- `radial-gradient(circle, ...)` – Gradasi radial untuk glow effect
- `rgba(56, 189, 248, 0.32)` – Warna biru semi-transparan

### c. CSS Grid untuk GitHub Stats

```css
.github-stats {
    display: grid;
    grid-template-columns: repeat(4, minmax(110px, 1fr));
    gap: 12px;
    margin-top: 18px;
}

.stat-box {
    background: rgba(15, 23, 42, 0.7);
    border: 1px solid rgba(56, 189, 248, 0.25);
    border-radius: 14px;
    padding: 16px;
    text-align: center;
    backdrop-filter: blur(2px);
}
```

**Penjelasan:**
- `display: grid` – Mengaktifkan CSS Grid layout
- `grid-template-columns: repeat(4, ...)` – 4 kolom dengan lebar sama
- `minmax(110px, 1fr)` – Lebar minimal 110px, maksimal 1fr
- `gap: 12px` – Jarak antar grid item
- `backdrop-filter: blur(2px)` – Efek blur di belakang stat-box
- `rgba(15, 23, 42, 0.7)` – Background semi-transparan

### d. Media Query untuk Responsive

```css
@media (max-width: 768px) {
    .hero-wrap {
        background-size: contain !important;
        background-position: center center !important;
        min-height: 100vh;
    }

    .slider-text h1 {
        font-size: 32px !important;
    }

    .slider-text h2 {
        font-size: 18px !important;
    }

    .github-profile {
        padding: 26px 18px;
    }

    .github-header {
        flex-direction: column;
        text-align: center;
        gap: 14px;
    }

    .github-stats {
        grid-template-columns: repeat(2, minmax(120px, 1fr));
        gap: 10px;
    }

    .github-meta,
    .github-actions {
        justify-content: center;
    }

    .portfolio-grid .project {
        min-height: 320px;
    }

    .portfolio-grid .project .text {
        padding: 20px;
    }
}
```

**Penjelasan:**
- `@media (max-width: 768px)` – Berlaku untuk layar ≤ 768px (tablet/mobile)
- `background-size: contain` – Background image menyesuaikan lebar layar
- `flex-direction: column` – Stack elemen secara vertikal
- `grid-template-columns: repeat(2, ...)` – Ubah grid dari 4 ke 2 kolom
- `justify-content: center` – Center elemen horizontal
- `!important` – Override style default dengan prioritas tinggi

## 5.3. Penjelasan Kode JavaScript

### a. Document Ready dan Inisialisasi

```javascript
$(document).ready(function () {
    fetchQuote();
    fetchWeather();
    fetchGitHubProfile();
    setInterval(fetchQuote, 30000);
});
```

**Penjelasan:**
- `$(document).ready()` – Event handler saat DOM selesai dimuat
- Memastikan semua elemen HTML siap sebelum manipulasi
- Ketiga fungsi API dipanggil sekali saat halaman dimuat
- `setInterval(fetchQuote, 30000)` – Refresh quote setiap 30000ms (30 detik)
- Fungsi dijalankan secara asynchronous tanpa blocking UI

### b. Template Literal untuk Dynamic HTML

```javascript
$("#quote-container").html(`
    <p class="quote-text">"${randomQuote.text}"</p>
    <p class="quote-author">- ${randomQuote.author || "Unknown"}</p>
`);
```

**Penjelasan:**
- Template literal menggunakan backticks (`` ` ``)
- Interpolasi string dengan `${variable}`
- `|| "Unknown"` – Logical OR untuk fallback jika `author` null/undefined
- `.html()` – jQuery method untuk mengganti innerHTML elemen
- Multi-line string tanpa perlu concatenation

### c. Conditional Rendering

```javascript
const joinedYear = data.created_at ? new Date(data.created_at).getFullYear() : null;
const websiteLink = data.blog && data.blog.trim() !== ""
    ? (data.blog.startsWith("http") ? data.blog : "https://" + data.blog)
    : null;

// Dalam template literal:
${data.location ? `<li><i class="icon-map-pin mr-1"></i>${data.location}</li>` : ""}
${joinedYear ? `<li><i class="icon-calendar mr-1"></i>Joined ${joinedYear}</li>` : ""}
${websiteLink ? `<a href="${websiteLink}" class="btn btn-outline-light btn-sm">Portfolio</a>` : ""}
```

**Penjelasan:**
- Ternary operator `condition ? true : false`
- `data.created_at ? ... : null` – Cek apakah data ada
- `data.blog && data.blog.trim() !== ""` – Cek string tidak kosong
- `startsWith("http")` – Validasi URL memiliki protocol
- Conditional rendering dalam template literal dengan `${condition ? 'HTML' : ""}`

### d. Error Handling

```javascript
error: function () {
    $("#weather-container").html(`
        <div class="weather-temp">28°C</div>
        <div class="weather-desc">Partly Cloudy</div>
        <div class="mt-3">Location: Jepara, Indonesia</div>
    `);
}
```

**Penjelasan:**
- Callback `error` menangani kegagalan HTTP request
- Data fallback ditampilkan agar UI tetap informatif
- Mencegah halaman kosong atau error saat API down
- Hardcoded values sebagai fallback yang masuk akal

### e. Form Serialization

```javascript
const formData = form.serialize();

$.ajax({
    url: "https://formsubmit.co/ajax/ranggapf04@gmail.com",
    method: "POST",
    data: formData,
    dataType: "json",
    // ...
});
```

**Penjelasan:**
- `.serialize()` – Mengubah form data menjadi query string
- Contoh hasil: `name=Rangga&email=rangga%40gmail.com&message=Hello`
- Mempermudah pengiriman data form via AJAX POST
- Semua input dengan atribut `name` akan disertakan

### f. Button State Management

```javascript
submitBtn.prop("disabled", true).html('<span class="spinner-border spinner-border-sm mr-2"></span>Sending...');

// Di callback complete:
submitBtn.prop("disabled", false).html("Send Message");
```

**Penjelasan:**
- `.prop("disabled", true)` – Nonaktifkan tombol saat loading
- `.html(...)` – Ganti teks tombol dengan loading spinner
- `spinner-border` – Class Bootstrap untuk loading spinner
- Callback `complete` dijalankan setelah success/error
- Mencegah multiple submission saat request berjalan

---

# BAB VI HASIL DAN PEMBAHASAN

## 6.1. Hasil Tampilan Website

Website web profile berhasil dibuat dan ditampilkan dalam satu halaman (single page) dengan struktur yang terorganisir. Berikut adalah deskripsi tampilan setiap section:

### 6.1.1 Hero Section (Home)
Hero section menampilkan:
- Background image dengan overlay gelap
- Nama lengkap "Rangga Pradarrell Fathi" dengan font besar
- Subjudul "Web Developer"
- Deskripsi singkat tentang profil
- Tombol "Contact Me" yang scroll ke contact section

### 6.1.2 About Section
About section menampilkan:
- Layout 2 kolom (gambar di kiri, informasi di kanan)
- Foto profil pribadi
- Informasi lengkap: nama, tanggal lahir, NIM, alamat, email, telepon
- Counter jumlah proyek yang telah diselesaikan (6 proyek)
- Tombol "Download CV" untuk mengunduh file PDF

### 6.1.3 Education Section
Education section menampilkan:
- Riwayat pendidikan formal
- Nama universitas: Telkom University Purwokerto
- Program studi: S1 Teknik Informatika
- Tahun studi: 2023 - Present
- IPK saat ini: 3.9 / 4.0

### 6.1.4 Skills Section
Skills section menampilkan 3 kolom:
- **Technical Skills:** HTML & CSS, Bootstrap, JavaScript, AJAX, Fullstack Development, UI/UX Design, Data Analysis, Cybersecurity, Penetration Testing, GitHub
- **Soft Skills:** Project Management, Public Speaking, Strategic Planning, Teamwork, Leadership, Communication, Problem Solving, Critical Thinking
- **Languages:** Bahasa Indonesia (Native), English (Fluent)

### 6.1.5 Portfolio Section
Portfolio section menampilkan:
- Grid 3 kolom untuk project cards
- 3 proyek: Cukurmen, Banyurise, My Educom
- Setiap card memiliki:
  - Gambar background project
  - Overlay gradasi hitam
  - Judul project
  - Kategori development
  - Deskripsi singkat
  - Badges kategori (Fullstack, Booking System, dll)

### 6.1.6 API Data Section
API Data section menampilkan 3 card:

**Quote Card:**
- Background gradasi ungu
- Quote motivasi random yang berubah setiap 30 detik
- Nama penulis quote
- Loading spinner saat fetch data

**Weather Card:**
- Background gradasi pink
- Suhu real-time Jepara
- Deskripsi kondisi cuaca
- Kecepatan angin
- Data diambil dari Open-Meteo API

**GitHub Profile Card:**
- Background gradasi gelap dengan glow effects
- Avatar GitHub
- Nama dan username
- Bio, lokasi, perusahaan
- Stats grid: Repositories, Followers, Following, Gists
- Tombol ke profil GitHub dan repositories

### 6.1.7 Contact Section
Contact section menampilkan:
- 4 kotak informasi kontak (alamat, telepon, email, website)
- Form kontak dengan field: nama, email, subject, message
- Tombol "Send Message" dengan loading state
- Alert success/error setelah pengiriman
- Background image di sebelah kanan form

### 6.1.8 Footer
Footer menampilkan:
- 4 kolom: About, Links, Skills, Have Questions?
- Social media links (Instagram, GitHub)
- Navigasi cepat ke setiap section
- Informasi kontak lengkap

### 6.1.9 Responsive Design
Website tampil responsif di berbagai device:
- **Desktop (> 992px):** Layout penuh dengan grid 3-4 kolom
- **Tablet (768px - 991px):** Grid 2 kolom, navbar collapse
- **Mobile (< 768px):** Single column layout, font size disesuaikan

## 6.2. Analisis Fungsionalitas Website

### 6.2.1 Navigasi
✅ Navbar berfungsi dengan baik
✅ Smooth scroll ke setiap section bekerja
✅ Scrollspy highlight menu aktif berfungsi
✅ Mobile menu toggle (hamburger) responsif

### 6.2.2 API Integration
✅ Quote API berhasil menampilkan quote random
✅ Weather API menampilkan data real-time Jepara
✅ GitHub API menampilkan profil lengkap dengan stats
✅ Auto-refresh quote setiap 30 detik berfungsi
✅ Error handling dengan fallback data bekerja

### 6.2.3 Contact Form
✅ Form validation HTML5 berfungsi
✅ AJAX POST ke FormSubmit berhasil
✅ Loading state pada tombol submit
✅ Alert success/error ditampilkan
✅ Form reset setelah pengiriman berhasil

### 6.2.4 Responsive Design
✅ Layout menyesuaikan ukuran layar
✅ Grid system Bootstrap bekerja optimal
✅ Font size dan padding disesuaikan di mobile
✅ Images scale dengan baik
✅ Navbar collapse di mobile view

### 6.2.5 Animasi dan Interaktivitas
✅ Animasi fade-in saat scroll (AOS)
✅ Counter animations untuk statistics
✅ Hover effects pada buttons dan cards
✅ Loading spinner saat fetch API
✅ Smooth transitions pada semua interaksi

### 6.2.6 Kendala dan Solusi

**Kendala 1: API Quote kadang timeout**
- **Solusi:** Implementasi error handling dengan fallback quote hardcoded

**Kendala 2: GitHub API rate limiting**
- **Solusi:** Error handling dengan tampilan fallback dan link langsung ke profil

**Kendala 3: Weather code interpretation**
- **Solusi:** Membuat helper function `getWeatherDescription()` untuk mapping WMO codes

**Kendala 4: Form spam**
- **Solusi:** Menambahkan honeypot field `_honey` dan disable captcha di FormSubmit

---

# BAB VII PENUTUP

## 7.1. Kesimpulan

Berdasarkan praktikum yang telah dilaksanakan, dapat disimpulkan bahwa:

1. **Website web profile pribadi berhasil dibuat** menggunakan HTML, CSS, JavaScript, dan Bootstrap 4.6.2 dalam satu file (`webprofile.html`) dengan konsep single page website.

2. **Struktur HTML semantik** diterapkan dengan baik menggunakan elemen-elemen seperti `<nav>`, `<section>`, `<header>`, `<footer>` untuk aksesibilitas dan SEO.

3. **Bootstrap framework** dimanfaatkan secara optimal untuk:
   - Grid system (row, col-md-*, col-lg-*)
   - Komponen (navbar, cards, buttons, forms, alerts)
   - Utilities (spacing, flexbox, text alignment)
   - Responsive design

4. **Custom CSS** ditambahkan untuk komponen khusus:
   - Gradient backgrounds (quote, weather, GitHub cards)
   - Pseudo-elements untuk decorative effects
   - CSS Grid untuk GitHub stats layout
   - Media queries untuk responsive mobile

5. **JavaScript dan AJAX** diimplementasikan untuk:
   - Fetch data dari 4 public APIs (Quote, Weather, GitHub, FormSubmit)
   - Dynamic HTML rendering dengan template literals
   - Error handling dengan fallback data
   - Form submission dengan loading states
   - Auto-refresh quote setiap 30 detik

6. **Integrasi Web Service/API** berhasil menampilkan data dinamis:
   - Type.fit Quote API untuk quotes motivasi
   - Open-Meteo Weather API untuk cuaca real-time
   - GitHub User API untuk profil dan statistics
   - FormSubmit API untuk pengiriman email kontak

7. **Responsive design** tercapai dengan baik:
   - Tampilan optimal di desktop, tablet, dan mobile
   - Layout menyesuaikan dengan media queries
   - Navbar collapse di mobile view
   - Grid columns menyesuaikan ukuran layar

8. **Fitur interaktif** berfungsi dengan baik:
   - Smooth scroll navigation
   - Scrollspy menu highlighting
   - Loading spinners
   - Alert notifications
   - Hover animations

### Pembelajaran yang Didapat:

1. Memahami struktur HTML5 semantik untuk website modern
2. Menguasai Bootstrap grid system dan komponen UI
3. Implementasi CSS modern (gradient, flexbox, grid, pseudo-elements)
4. Teknik AJAX dengan jQuery untuk fetch API data
5. Error handling untuk fallback saat API gagal
6. Template literal JavaScript untuk dynamic HTML
7. Form handling dengan AJAX dan validation
8. Responsive design dengan media queries

### Saran Pengembangan:

1. Menambahkan dark/light mode toggle
2. Implementasi typing animation di hero section
3. Menambahkan modal untuk detail proyek
4. Integrasi Google Analytics untuk tracking
5. Optimasi performa dengan lazy loading images
6. Menambahkan PWA (Progressive Web App) features
7. Implementasi email templates yang lebih custom di FormSubmit

---

**Demikian laporan praktikum ini dibuat. Semoga dapat bermanfaat dan menjadi referensi untuk pengembangan lebih lanjut.**

**Purwokerto, 29 Maret 2026**

**Rangga Pradarrell Fathi**  
**NIM 2311102200**
