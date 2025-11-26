
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>ملفي المهني - فهد الخالدي</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    :root {
      --primary: #1a365d;
      --secondary: #1e293b;
      --accent: #2563eb;
      --dark: #0f172a;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Tahoma, Arial;
    }

    body {
      background: #f5f7fa;
      color: var(--dark);
      line-height: 1.8;
      padding-right: 78px; /* ✅ نفس عرض الشريط */
    }

    .container {
      width: 95%;
      max-width: 1200px;
      margin: auto;
    }

    header {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      color: white;
      padding: 2.5rem 0;
      text-align: center;
    }

    h1 {
      font-size: 2.3rem;
    }

    /* ✅✅✅ شريط جانبي ثابت بدون اهتزاز */
    nav {
      position: fixed;
      top: 0;
      right: 0;
      height: 100vh;
      width: 78px;
      background: #0f172a;
      z-index: 999;
    }

    .nav-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-top: 90px;
      gap: 14px;
    }

    .nav-link {
      width: 60px;
      height: 60px;
      font-size: 11px;
      background: transparent;
      color: #cbd5f5;
      text-align: center;
      border-radius: 14px;
      text-decoration: none;

      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      transition: background 0.2s ease;
    }

    .nav-link.active,
    .nav-link:hover {
      background: #1e40af;
      color: white;
    }

    section {
      display: none;
      padding: 4rem 0;
    }

    section.active {
      display: block;
    }

    .section-title {
      text-align: center;
      margin-bottom: 2rem;
      color: var(--primary);
    }

    .card {
      background: white;
      padding: 2rem;
      border-radius: 12px;
      margin-bottom: 2rem;
      box-shadow: 0 5px 15px rgba(0,0,0,.08);
    }

    .profile-img {
      width: 180px;
      height: 180px;
      margin: auto;
      border-radius: 50%;
      overflow: hidden;
    }

    .profile-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    footer {
      background: var(--primary);
      color: white;
      text-align: center;
      padding: 2rem 0;
      margin-top: 3rem;
    }

    @media (max-width: 768px) {
      body {
        padding-right: 78px;
      }

      h1 {
        font-size: 1.8rem;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="container">
    <h1>ملفي المهني</h1>
    <p>سيرة ذاتية تفاعلية</p>
  </div>
</header>

<!-- ✅✅✅ شريط تنقل جانبي ثابت -->
<nav>
  <div class="nav-container">
    <a class="nav-link active" data-section="about">نبذة</a>
    <a class="nav-link" data-section="experience">الخبرات</a>
    <a class="nav-link" data-section="skills">المهارات</a>
    <a class="nav-link" data-section="training">الدورات</a>
    <a class="nav-link" data-section="portfolio">الملف</a>
    <a class="nav-link" data-section="contact">تواصل</a>
  </div>
</nav>

<main class="container">

  <section id="about" class="active">
    <h2 class="section-title">نبذة عني</h2>
    <div class="card" style="text-align:center">
      <div class="profile-img">
        <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
      </div>
      <h3>فهد نغيمش الخالدي</h3>
      <p>معلم لغة إنجليزية بخبرة أكثر من 14 عامًا في التعليم.</p>
    </div>
  </section>

  <section id="experience">
    <h2 class="section-title">خبراتي</h2>
    <div class="card">معلم لغة إنجليزية – تعليم مكة</div>
  </section>

  <section id="skills">
    <h2 class="section-title">مهاراتي</h2>
    <div class="card">القيادة – التعليم الرقمي – التواصل</div>
  </section>

  <section id="training">
    <h2 class="section-title">الدورات</h2>
    <div class="card">أكثر من 150 ساعة تدريبية</div>
  </section>

  <section id="portfolio">
    <h2 class="section-title">ملفي المهني</h2>
    <div class="card">نماذج من الإنتاج المهني</div>
  </section>

  <section id="contact">
    <h2 class="section-title">التواصل</h2>
    <div class="card">📧 iFahadenglish@gmail.com</div>
  </section>

</main>

<footer>
  <p>© جميع الحقوق محفوظة - فهد الخالدي</p>
</footer>

<script>
  document.querySelectorAll('.nav-link').forEach(link => {
    link.onclick = function () {
      document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
      document.querySelectorAll('section').forEach(s => s.classList.remove('active'));

      this.classList.add('active');
      document.getElementById(this.dataset.section).classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  });
</script>

</body>
</html>
