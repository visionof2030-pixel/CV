
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>الملف المهني | فهد نغيمش الخالدي</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    :root {
      --primary: #1a365d;
      --secondary: #0f172a;
      --accent: #2563eb;
      --light: #ffffff;
      --bg: #f5f7fa;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Tahoma, Arial;
    }

    body {
      background: var(--bg);
      color: #1e293b;
      line-height: 1.8;
      padding-right: 62px; /* ✅ عرض الشريط الجديد */
    }

    .container {
      width: 94%;
      max-width: 1200px;
      margin: auto;
    }

    header {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      color: white;
      padding: 2.8rem 0;
      text-align: center;
    }

    h1 { font-size: 2.3rem; }

    /* ✅✅✅ شريط جانبي أنحف ولون خط أبيض */
    nav {
      position: fixed;
      top: 0;
      right: 0;
      height: 100vh;
      width: 62px;
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
      width: 50px;
      height: 52px;
      font-size: 10px;
      background: transparent;
      color: #ffffff;  /* ✅ لون يعاكس الأزرق */
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
      background: var(--accent);
      color: #ffffff;
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
      font-size: 1.8rem;
    }

    .card {
      background: white;
      padding: 2rem;
      border-radius: 14px;
      margin-bottom: 2rem;
      box-shadow: 0 5px 15px rgba(0,0,0,.08);
    }

    .profile-img {
      width: 170px;
      height: 170px;
      margin: auto;
      border-radius: 50%;
      overflow: hidden;
      margin-bottom: 1rem;
      border: 4px solid var(--accent);
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

    ul { padding-right: 20px; }

    @media (max-width: 768px) {
      body { padding-right: 62px; }
      h1 { font-size: 1.7rem; }
    }
  </style>
</head>

<body>

<header>
  <div class="container">
    <h1>الملف المهني</h1>
    <p>سيرة ذاتية تفاعلية احترافية</p>
  </div>
</header>

<!-- ✅ شريط تنقل جانبي مصغر -->
<nav>
  <div class="nav-container">
    <a class="nav-link active" data-section="about">نبذة</a>
    <a class="nav-link" data-section="experience">خبراتي</a>
    <a class="nav-link" data-section="skills">مهاراتي</a>
    <a class="nav-link" data-section="training">الدورات</a>
    <a class="nav-link" data-section="portfolio">الملف</a>
    <a class="nav-link" data-section="contact">تواصل</a>
  </div>
</nav>

<main class="container">

  <!-- نبذة -->
  <section id="about" class="active">
    <h2 class="section-title">نبذة عني</h2>
    <div class="card" style="text-align:center">
      <div class="profile-img">
        <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
      </div>
      <h3>فهد نغيمش حميد الخالدي</h3>
      <p><b>معلم متقدم – تخصص اللغة الإنجليزية</b></p>
      <p>
        معلم لغة إنجليزية بخبرة تزيد عن 14 عامًا في التعليم العام، تمت ترقيتي إلى معلم متقدم عام 2022.
        أسعى باستمرار إلى تطوير أدائي المهني، وتوظيف التقنيات الحديثة في التعليم، وتحقيق مخرجات تعلم عالية الجودة 
        بما يتوافق مع رؤية المملكة 2030.
      </p>
    </div>
  </section>

  <!-- الخبرات -->
  <section id="experience">
    <h2 class="section-title">الخبرات المهنية</h2>
    <div class="card">
      <ul>
        <li>معلم لغة إنجليزية – سعيد بن العاص المتوسطة (2017 – الآن)</li>
        <li>معلم لغة إنجليزية – الأمير سعود بن عبدالمحسن (2014 – 2016)</li>
        <li>معلم لغة إنجليزية – سعيد بن زيد (2012 – 2014)</li>
        <li>مترجم – وزارة الحج والعمرة (2011 – 2012)</li>
      </ul>
    </div>
  </section>

  <!-- المهارات -->
  <section id="skills">
    <h2 class="section-title">المهارات</h2>
    <div class="card">
      <ul>
        <li>التعليم التفاعلي والرقمي</li>
        <li>القيادة الصفية وبناء الدافعية</li>
        <li>التقويم والتغذية الراجعة</li>
        <li>الترجمة والتواصل متعدد الثقافات</li>
      </ul>
    </div>
  </section>

  <!-- الدورات -->
  <section id="training">
    <h2 class="section-title">الدورات التدريبية</h2>
    <div class="card">
      <ul>
        <li>أكثر من 150 ساعة تدريبية معتمدة</li>
        <li>استراتيجيات التدريس الحديثة</li>
        <li>التعليم الإلكتروني</li>
        <li>القيادة المدرسية</li>
      </ul>
    </div>
  </section>

  <!-- الملف المهني -->
  <section id="portfolio">
    <h2 class="section-title">الملف المهني</h2>
    <div class="card">
      <ul>
        <li>إعداد اختبارات تفاعلية</li>
        <li>تصميم ملفات HTML تعليمية</li>
        <li>مبادرات تعليمية تطوعية</li>
        <li>برامج دعم التحصيل الدراسي</li>
      </ul>
    </div>
  </section>

  <!-- التواصل -->
  <section id="contact">
    <h2 class="section-title">التواصل</h2>
    <div class="card" style="text-align:center">
      <p>📧 البريد الإلكتروني:  
        <b>iFahadenglish@gmail.com</b>
      </p>
    </div>
  </section>

</main>

<footer>
  <p>© جميع الحقوق محفوظة - فهد نغيمش الخالدي</p>
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
