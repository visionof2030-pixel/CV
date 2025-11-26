<!DOCTYPE html>
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
    }

    h1 { font-size: 2.3rem; }

    /* ✅ الشريط الجانبي */
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

    footer {
      background: var(--primary);
      color: white;
      text-align: center;
      padding: 2rem 0;
      margin-top: 3rem;
    }

    ul { padding-right: 20px; }

    /* ✅ العداد */
    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .stat-box {
      background: #f8fafc;
      padding: 18px;
      border-radius: 14px;
      text-align: center;
      border: 1px solid #e5e7eb;
    }

    .stat-number {
      font-size: 26px;
      color: var(--accent);
      font-weight: bold;
    }

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
      font-size: 16px;
      font-weight: bold;
      box-shadow: 0 6px 15px rgba(16,185,129,.35);
      position: relative;
    }

    .trophy::before,
    .trophy::after {
      content: "";
      position: absolute;
      top: 50%;
      width: 14px;
      height: 14px;
      background: rgba(255,255,255,.6);
      border-radius: 50%;
      transform: translateY(-50%);
    }

    .trophy::before { right: 10px; }
    .trophy::after { left: 10px; }

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

  </style>
</head>

<body>

<header>
  <h1>الملف المهني للمعلم فهد الخالدي</h1>
</header>

<!-- ✅ الشريط الجانبي -->
<nav>
  <div class="nav-container">
    <a class="nav-link active" data-section="about"><i class="fa-solid fa-user"></i>نبذة عني</a>
    <a class="nav-link" data-section="experience"><i class="fa-solid fa-briefcase"></i>خبراتي</a>
    <a class="nav-link" data-section="skills"><i class="fa-solid fa-star"></i>المهارات</a>
    <a class="nav-link" data-section="training"><i class="fa-solid fa-graduation-cap"></i>الدورات</a>
    <a class="nav-link" data-section="contact"><i class="fa-solid fa-envelope"></i>تواصل</a>
  </div>
</nav>

<main class="container">

<!-- ✅ نبذة عني -->
<section id="about" class="active">
  <h2 class="section-title">نبذة عني</h2>

  <div class="card" style="text-align:center">

    <div class="profile-img">
      <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
    </div>

    <h3>فهد نغيمش حميد الخالدي</h3>
    <p><b>معلم متقدم – تخصص اللغة الإنجليزية</b></p>

    <p>
      معلّم لغة إنجليزية بخبرة تربوية ممتدة لأكثر من أربعة عشر عامًا في التعليم العام،
      أؤمن بأن التعليم رسالة سامية وصناعة وعي، وأسعى باستمرار إلى تطوير أسلوبي التدريسي
      ورفع جودة مخرجات التعلم بما يواكب تطلعات رؤية المملكة 2030. أمتلك شغفًا كبيرًا
      بتعلم اللغات وصقل مهارات الترجمة، وأسعى لبناء بيئة تعليمية محفزة تُنمّي التفكير
      النقدي والإبداعي لدى المتعلمين.
    </p>

    <!-- ✅ درجة 95 -->
    <div class="trophy-wrap">
      <div class="trophy">
        <i class="fa-solid fa-award"></i>
        حققت درجة 95 في التخصص
      </div>
    </div>

    <div class="stats">
      <div class="stat-box">
        <div class="stat-number">14+</div>
        <div>سنة خبرة</div>
      </div>
      <div class="stat-box">
        <div class="stat-number">+130</div>
        <div>ساعات تدريبية</div>
      </div>
      <div class="stat-box">
        <div class="stat-number">3</div>
        <div>مدارس</div>
      </div>
    </div>

  </div>
</section>

<!-- ✅ الخبرات -->
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

<!-- ✅ المهارات -->
<section id="skills">
  <h2 class="section-title">المهارات</h2>
  <div class="card">
    <ul>
      <li>إتقان اللغة الإنجليزية تحدثًا وكتابة</li>
      <li>تطوير وتنفيذ خطط تدريس محفزة ومبتكرة</li>
      <li>إدارة الصفوف بفاعلية وتشجيع التعلم الذاتي</li>
      <li>استخدام أدوات القياس والتقويم الإلكترونية بدقة</li>
      <li>دمج مهارات التفكير النقدي والإبداعي في التعليم</li>
      <li>شغف مستمر بتعلم اللغات واكتساب مهارات جديدة</li>
      <li>القدرة على التعليم في بيئات متعددة الثقافات مع استعداد لتعلم لغات إضافية مثل الصينية</li>
    </ul>
  </div>
</section>

<!-- ✅ الدورات -->
<section id="training">
  <h2 class="section-title">الدورات</h2>
  <div class="card">
    <ul>
      <li>التفكير الناقد والإبداعي ودمجه في المواد الدراسية</li>
      <li>القياس والتقويم التربوي</li>
      <li>الاستراتيجية الحديثة في تدريس أساسيات اللغة الإنجليزية</li>
      <li>البيئة الصفية الجاذبة</li>
      <li>تحليل أداء الطلاب وتقديم التغذية الراجعة</li>
      <li>أساسيات الترجمة</li>
      <li>مهارات التعامل مع أدوات القياس والتقويم الإلكترونية</li>
      <li>التنمية المهنية لمعلمي اللغة الإنجليزية - المستوى الثالث</li>
      <li>العبقرية في العملية التعليمية</li>
      <li>بناء الاختيار الجيد</li>
      <li>توظيف استراتيجيات التعليم في البيئة التدريبية الجاذبة</li>
      <li>تدريس مهارتي التحدث والاستماع</li>
      <li>التوعية بقواعد السلوك والمواظبة المحدثة</li>
      <li>اللقاءات التخصصية لمادة اللغة الإنجليزية</li>
    </ul>
  </div>
</section>

<!-- ✅ التواصل -->
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
/* ✅ التنقل بين الأقسام */
document.querySelectorAll('.nav-link').forEach(link => {
  link.onclick = () => {
    document.querySelectorAll('.nav-link').forEach(l=>l.classList.remove('active'));
    document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
    link.classList.add('active');
    document.getElementById(link.dataset.section).classList.add('active');
    window.scrollTo({top:0});
  }
});
</script>

</body>
</html>
