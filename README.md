<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ملفي المهني - فهد نغيمش الخالدي</title>

<style>
:root {
    --primary: #1a365d;
    --secondary: #2d3748;
    --accent: #e53e3e;
    --nav-bg: #2c5282;
    --dark: #2d3748;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, sans-serif;
}

body {
    background: #f5f7fa;
    color: var(--dark);
    line-height: 1.8;
    font-size: 1.3rem;
    padding-right: 100px;
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 20px;
}

/* ✅ شريط تنقل جانبي عمودي */
nav {
    position: fixed;
    top: 50%;
    right: 10px;
    transform: translateY(-50%);
    background: var(--nav-bg);
    padding: 12px;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    z-index: 999;
}

.nav-container {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.nav-link {
    color: white;
    text-decoration: none;
    padding: 10px 16px;
    border-radius: 50px;
    background: rgba(255,255,255,0.15);
    text-align: center;
    transition: 0.3s;
}

.nav-link:hover,
.nav-link.active {
    background: var(--accent);
}

/* الأقسام */
section {
    display: none;
    padding: 50px 0;
}

section.active {
    display: block;
}

.section-title {
    text-align: center;
    color: var(--primary);
    font-size: 2.5rem;
    margin-bottom: 30px;
}

.card {
    background: white;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
}

/* نبذة */
.profile-img {
    width: 260px;
    height: 260px;
    border-radius: 50%;
    overflow: hidden;
    margin: 20px auto;
}

.profile-img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.profile-name {
    text-align: center;
    font-size: 2.2rem;
    font-weight: bold;
    color: var(--primary);
}

.profile-title {
    text-align: center;
    font-size: 1.6rem;
    color: var(--accent);
}

@media (max-width: 768px) {
    body {
        padding-right: 80px;
        font-size: 1.1rem;
    }
}
</style>
</head>

<body>

<!-- ✅ شريط التنقل الجانبي -->
<nav>
    <div class="nav-container">
        <a class="nav-link active" data-section="about">نبذة</a>
        <a class="nav-link" data-section="experience">خبراتي</a>
        <a class="nav-link" data-section="skills">مهاراتي</a>
        <a class="nav-link" data-section="training">الدورات</a>
        <a class="nav-link" data-section="portfolio">ملفي</a>
        <a class="nav-link" data-section="contact">تواصل</a>
    </div>
</nav>

<main class="container">

<section id="about" class="active">
    <h2 class="section-title">نبذة عني</h2>
    <div class="card">
        <div class="profile-img">
            <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
        </div>
        <div class="profile-name">فهد نغيمش حميد الخالدي</div>
        <div class="profile-title">معلم لغة إنجليزية</div>
        <p style="margin-top:20px">
        معلم لغة إنجليزية بخبرة تتجاوز 14 عامًا في التعليم العام، معلم متقدم منذ عام 2022، وأسعى دائمًا لتطوير الممارسات التعليمية بما يحقق رؤية المملكة 2030.
        </p>
    </div>
</section>

<section id="experience">
    <h2 class="section-title">خبراتي</h2>
    <div class="card">
        <ul>
            <li>معلم لغة إنجليزية – مكة المكرمة</li>
            <li>معلم لغة إنجليزية – الليث</li>
            <li>مترجم – وزارة الحج والعمرة</li>
        </ul>
    </div>
</section>

<section id="skills">
    <h2 class="section-title">مهاراتي</h2>
    <div class="card">
        <ul>
            <li>إتقان اللغة الإنجليزية</li>
            <li>إدارة الصف</li>
            <li>التفكير الإبداعي</li>
            <li>القياس والتقويم</li>
        </ul>
    </div>
</section>

<section id="training">
    <h2 class="section-title">الدورات</h2>
    <div class="card">
        <ul>
            <li>التفكير الناقد</li>
            <li>البيئة الصفية الجاذبة</li>
            <li>القياس والتقويم</li>
        </ul>
    </div>
</section>

<section id="portfolio">
    <h2 class="section-title">ملفي المهني</h2>
    <div class="card">
        <p>رؤيتي، أخلاقياتي، أهدافي التعليمية، وخطط تطويري المستقبلي.</p>
    </div>
</section>

<section id="contact">
    <h2 class="section-title">تواصل</h2>
    <div class="card">
        <p>📧 iFahadenglish@gmail.com</p>
        <p>📱 0554449824</p>
    </div>
</section>

</main>

<script>
document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', function() {
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
