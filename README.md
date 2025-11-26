
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>ملفي المهني - فهد نغيمش الخالدي</title>

    <style>
        :root {
            --primary: #1a365d;
            --secondary: #2d3748;
            --accent: #e53e3e;
            --light: #f7fafc;
            --dark: #2d3748;
            --success: #38a169;
            --nav-bg: #2c5282;
            --text-light: #f7fafc;
            --text-dark: #2d3748;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: var(--dark);
            line-height: 1.8;
            font-size: 1.4rem; /* ✅ تم حذف padding-top */
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ✅ nav بدون تثبيت */
        nav {
            background: var(--nav-bg);
            color: var(--text-light);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 0.5rem 0;
            margin: 1.5rem 0;
            border-radius: 12px;
        }

        .nav-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }

        .nav-link {
            padding: 0.8rem 1.5rem;
            text-decoration: none;
            color: var(--text-light);
            font-weight: 500;
            transition: all 0.3s ease;
            border-radius: 25px;
            font-size: 1.2rem;
        }

        .nav-link:hover,
        .nav-link.active {
            background-color: var(--accent);
        }

        section {
            padding: 3rem 0;
            display: none;
        }

        section.active {
            display: block;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary);
            font-size: 2.8rem;
        }

        .card {
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 2.5rem;
            margin-bottom: 2.5rem;
        }

        .profile-img {
            width: 260px;
            height: 260px;
            border-radius: 50%;
            margin: auto;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }

        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .profile-name {
            font-size: 2.5rem;
            color: var(--primary);
            margin: 1rem 0 0.3rem;
            font-weight: bold;
            text-align: center;
        }

        .profile-title {
            font-size: 1.6rem;
            color: var(--accent);
            margin-bottom: 1rem;
            text-align: center;
        }
    </style>
</head>

<body>

<main class="container">

<!-- ✅ نبذة عني -->
<section id="about" class="active">
    <h2 class="section-title">نبذة عني</h2>

    <div class="card">

        <div class="profile-img">
            <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
        </div>

        <div class="profile-name">فهد نغيمش الخالدي</div>
        <div class="profile-title">معلم متقدم - تخصص اللغة الإنجليزية</div>

        <!-- ✅✅✅ شريط التنقل تم نقله هنا فقط -->
        <nav>
            <div class="container nav-container">
                <a class="nav-link active" data-section="about">نبذة عني</a>
                <a class="nav-link" data-section="experience">خبراتي</a>
                <a class="nav-link" data-section="skills">مهاراتي</a>
                <a class="nav-link" data-section="training">الدورات</a>
                <a class="nav-link" data-section="portfolio">ملفي المهني</a>
                <a class="nav-link" data-section="contact">اتصل بي</a>
            </div>
        </nav>

        <p>أنا معلم لغة إنجليزية متمرس بخبرة تتجاوز 14 عامًا في التعليم العام...</p>
    </div>
</section>

<!-- ✅ الأقسام كما هي -->
<section id="experience">
    <h2 class="section-title">خبراتي</h2>
    <div class="card">خبراتي المهنية هنا</div>
</section>

<section id="skills">
    <h2 class="section-title">مهاراتي</h2>
    <div class="card">مهاراتي هنا</div>
</section>

<section id="training">
    <h2 class="section-title">الدورات التدريبية</h2>
    <div class="card">دوراتي هنا</div>
</section>

<section id="portfolio">
    <h2 class="section-title">ملفي المهني</h2>
    <div class="card">ملفي هنا</div>
</section>

<section id="contact">
    <h2 class="section-title">اتصل بي</h2>
    <div class="card">نموذج التواصل هنا</div>
</section>

</main>

<script>
document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', function () {
        document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
        document.querySelectorAll('section').forEach(s => s.classList.remove('active'));

        this.classList.add('active');
        document.getElementById(this.dataset.section).classList.add('active');
        window.scrollTo({ top: 0, behavior: 'smooth' });
    });
});
</script>

</body>
</html>
