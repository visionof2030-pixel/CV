
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>الملف المهني | فهد الخالدي</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <style>
    :root {
      --primary: #1a365d;
      --secondary: #0f172a;
      --accent: #2563eb;
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
      padding-right: 78px;
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
      position: relative;
    }

    h1 { font-size: 2.1rem; }

    /* ✅ زر اللغة */
    .lang-btn {
      position: absolute;
      left: 20px;
      top: 20px;
      background: white;
      color: var(--accent);
      border: none;
      padding: 8px 14px;
      border-radius: 10px;
      font-weight: bold;
      cursor: pointer;
    }

    nav {
      position: fixed;
      top: 0;
      right: 0;
      height: 100vh;
      width: 78px;
      background: #ffffff;
      border-left: 1px solid #e5e7eb;
      z-index: 999;
    }

    .nav-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-top: 90px;
      gap: 18px;
    }

    .nav-link {
      width: 64px;
      height: 62px;
      font-size: 13px;
      font-weight: bold;
      background: transparent;
      color: #2563eb;
      text-align: center;
      border-radius: 16px;
      text-decoration: none;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
    }

    .nav-link i {
      font-size: 16px;
      margin-bottom: 4px;
    }

    .nav-link.active,
    .nav-link:hover {
      background: #2563eb;
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
      font-size: 1.9rem;
    }

    .card {
      background: white;
      padding: 2.2rem;
      border-radius: 18px;
      margin-bottom: 2rem;
      box-shadow: 0 8px 18px rgba(0,0,0,.08);
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

    ul { padding-right: 20px; }

    /* ✅ شكل لصق الجروح لدرجة 95 */
    .trophy-wrap {
      display: flex;
      justify-content: center;
      margin: 20px 0;
    }

    .trophy {
      background: linear-gradient(135deg, #10b981, #34d399);
      color: white;
      padding: 10px 40px;
      border-radius: 999px;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-size: 15px;
      font-weight: bold;
    }

    /* ✅ الخط الزمني */
    .timeline {
      position: relative;
      padding-right: 40px;
    }

    .timeline::before {
      content: '';
      position: absolute;
      right: 10px;
      top: 0;
      width: 4px;
      height: 100%;
      background: #2563eb;
      border-radius: 10px;
    }

    .timeline-item {
      position: relative;
      background: white;
      border-radius: 20px;
      padding: 20px;
      margin-bottom: 30px;
      margin-right: 30px;
      box-shadow: 0 5px 15px rgba(0,0,0,.1);
    }

    .timeline-item::before {
      content: '';
      position: absolute;
      right: -35px;
      top: 35px;
      width: 22px;
      height: 22px;
      background: #2563eb;
      border-radius: 50%;
    }

    .timeline-date {
      color: #2563eb;
      font-size: 18px;
      font-weight: bold;
      margin-bottom: 8px;
    }

    footer {
      background: var(--primary);
      color: white;
      text-align: center;
      padding: 2rem 0;
    }
  </style>
</head>

<body>

<header>
  <button class="lang-btn" onclick="toggleLang()">EN</button>
  <h1 id="title">الملف المهني للمعلم فهد الخالدي</h1>
</header>

<!-- ✅ الشريط الجانبي -->
<nav>
  <div class="nav-container">
    <a class="nav-link active" data-section="about"><i class="fa-solid fa-user"></i><span class="t-about">نبذة عني</span></a>
    <a class="nav-link" data-section="experience"><i class="fa-solid fa-briefcase"></i><span class="t-exp">خبراتي</span></a>
    <a class="nav-link" data-section="skills"><i class="fa-solid fa-star"></i><span class="t-skill">المهارات</span></a>
    <a class="nav-link" data-section="training"><i class="fa-solid fa-graduation-cap"></i><span class="t-train">الدورات</span></a>
    <a class="nav-link" data-section="contact"><i class="fa-solid fa-envelope"></i><span class="t-contact">تواصل</span></a>
  </div>
</nav>

<main class="container">

<section id="about" class="active">
  <h2 class="section-title t-about">نبذة عني</h2>

  <div class="card" style="text-align:center">

    <div class="profile-img">
      <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
    </div>

    <h3>فهد نغيمش حميد الخالدي</h3>
    <p><b>معلم متقدم – تخصص اللغة الإنجليزية</b></p>

    <p class="t-bio">
      معلّم لغة إنجليزية بخبرة تربوية تمتد لأكثر من أربعة عشر عامًا في التعليم العام،
      أسعى باستمرار إلى تطوير أدائي المهني، وبناء بيئة صفية محفزة تنمّي التفكير النقدي
      والإبداعي لدى الطلاب، وتسهم في تحقيق مستهدفات رؤية المملكة 2030.
    </p>

    <div class="trophy-wrap">
      <div class="trophy">
        ⭐ حققت درجة 95 في التخصص
      </div>
    </div>

  </div>
</section>

<section id="experience">
  <h2 class="section-title">خبراتي</h2>

  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-date">2012 - 2011</div>
      مترجم - وزارة الحج والعمرة<br>
      مكة المكرمة
    </div>

    <div class="timeline-item">
      <div class="timeline-date">2014 - 2012</div>
      معلم لغة إنجليزية - سعيد بن زيد<br>
      عفيف
    </div>

    <div class="timeline-item">
      <div class="timeline-date">2016 - 2015</div>
      معلم لغة إنجليزية – ثانوية الأمير سعود بن عبدالمحسن<br>
      الليث – تعليم الليث
    </div>

    <div class="timeline-item">
      <div class="timeline-date">الآن - 2017</div>
      معلم لغة إنجليزية - سعيد بن العاص<br>
      مكة المكرمة – تعليم مكة
    </div>

  </div>
</section>

<section id="skills">
  <h2 class="section-title">المهارات</h2>
  <div class="card">
    <ul>
      <li>إتقان اللغة الإنجليزية تحدثًا وكتابة</li>
      <li>إدارة الصفوف بفاعلية وتشجيع التعلم الذاتي</li>
      <li>استخدام أدوات القياس والتقويم الإلكترونية بدقة</li>
      <li>دمج مهارات التفكير النقدي والإبداعي في التعليم</li>
      <li>القدرة على التعليم في بيئات متعددة الثقافات</li>
    </ul>
  </div>
</section>

<section id="training">
  <h2 class="section-title">الدورات</h2>
  <div class="card">
    <ul>
      <li>التفكير الناقد والإبداعي</li>
      <li>القياس والتقويم التربوي</li>
      <li>الاستراتيجيات الحديثة في تدريس اللغة الإنجليزية</li>
      <li>تحليل أداء الطلاب والتغذية الراجعة</li>
      <li>أساسيات الترجمة</li>
    </ul>
  </div>
</section>

<section id="contact">
  <h2 class="section-title">تواصل</h2>
  <div class="card" style="text-align:center">
    <p>📧 iFahadenglish@gmail.com</p>
  </div>
</section>

</main>

<footer>
  © جميع الحقوق محفوظة - فهد الخالدي
</footer>

<script>
/* ✅ التنقل */
document.querySelectorAll('.nav-link').forEach(link => {
  link.onclick = () => {
    document.querySelectorAll('.nav-link').forEach(l=>l.classList.remove('active'));
    document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
    link.classList.add('active');
    document.getElementById(link.dataset.section).classList.add('active');
    window.scrollTo({top:0});
  }
});

/* ✅ زر عربي | English */
let isArabic = true;
function toggleLang() {
  isArabic = !isArabic;

  document.getElementById("title").innerText = isArabic
    ? "الملف المهني للمعلم فهد الخالدي"
    : "Professional Portfolio - Fahad Al Khaldi";

  document.querySelector(".lang-btn").innerText = isArabic ? "EN" : "AR";
}
</script>

</body>
</html>
