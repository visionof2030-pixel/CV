<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>الملف المهني | فهد الخالدي</title>
<!-- إضافة خطوط عربية جميلة -->
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --primary:#1a365d;
  --accent:#2563eb;
  --bg:#f5f7fa;
  --text:#1e293b;
  --light-text:#64748b;
}
*{box-sizing:border-box;font-family:'Tajawal', Tahoma, Arial, sans-serif}

body{
  margin:0;
  background:var(--bg);
  color:var(--text);
  padding-right:90px;
  transition: padding 0.3s ease;
  line-height: 1.7;
}

header{
  background:linear-gradient(135deg,var(--primary),#020617);
  color:#fff;
  text-align:center;
  padding:14px;
  position: relative;
  z-index: 1000;
}
#pageTitle{
  font-size:1.4rem;
  background:rgba(255,255,255,.15);
  padding:8px 20px;
  border-radius:999px;
  display:inline-block;
  font-weight:700;
}

.lang-btn{
  position:fixed;
  top:10px;
  left:10px;
  background:#fff;
  color:var(--accent);
  border:none;
  padding:8px 16px;
  border-radius:8px;
  font-weight:bold;
  cursor:pointer;
  z-index:3000;
  transition: all 0.2s ease;
  font-family: 'Tajawal', sans-serif;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.lang-btn:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.2);
}

/* ===== Sidebar ===== */
nav{
  position:fixed;
  right:0;
  top:0;
  width:80px;
  height:100vh;
  background:#fff;
  border-left:1px solid #ddd;
  z-index:2000;
  transition: all 0.3s ease;
  overflow-y: auto;
  overflow-x: hidden;
}
.nav-container{
  display:flex;
  flex-direction:column;
  align-items:center;
  padding-top:90px;
  padding-bottom: 30px;
  gap:14px;
}
.nav-link{
  width:62px;
  height:62px;
  text-align:center;
  text-decoration:none;
  color:var(--accent);
  border-radius:14px;
  font-size:11px;
  font-weight:bold;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  cursor:pointer;
  transition: all 0.2s ease;
  position: relative;
}
.nav-link svg{width:20px;height:20px;fill:currentColor}
.nav-link.active,
.nav-link:hover{
  background:var(--accent);
  color:white;
  transform: translateX(-2px);
}

.nav-link::after {
  content: "";
  position: absolute;
  left: -8px;
  top: 50%;
  transform: translateY(-50%);
  width: 4px;
  height: 0;
  background: var(--accent);
  border-radius: 2px;
  transition: height 0.3s ease;
}

.nav-link.active::after {
  height: 30px;
}

main{max-width:90000px;margin:auto;padding:-10px}
section{display:none; animation: fadeIn 0.5s ease;}
section.active{display:block}
.section-title{
  text-align:center;
  color:var(--primary); 
  margin-bottom: 25px;
  font-size: 1.8rem;
  font-weight: 800;
  position: relative;
  padding-bottom: 10px;
}

.section-title::after {
  content: "";
  position: absolute;
  bottom: 0;
  right: 50%;
  transform: translateX(50%);
  width: 80px;
  height: 4px;
  background: var(--accent);
  border-radius: 2px;
}

.card{
  background:#fff;
  border-radius:16px;
  padding:25px;
  margin-bottom:25px;
  box-shadow:0 6px 18px rgba(0,0,0,.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border-right: 4px solid transparent;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0,0,0,.1);
  border-right-color: var(--accent);
}

.profile-img{
  width:150px;
  height:150px;
  margin:15px auto;
  border-radius:50%;
  overflow:hidden;
  border:4px solid var(--accent);
  box-shadow: 0 8px 20px rgba(37, 99, 235, 0.2);
}
.profile-img img{
  width:100%;
  height:100%;
  object-fit:cover;
}

.bio{
  text-align:justify;
  font-size:0.80rem;
  line-height: 1.8;
  color: var(--text);
  margin: 15px 0;
}

.badge{
  margin:15px auto;
  text-align:center;
  background:linear-gradient(135deg, #16a34a, #059669);
  color:white;
  padding:8px 20px;
  border-radius:999px;
  font-size:14px;
  display:inline-flex;
  gap:8px;
  align-items:center;
  font-weight: 700;
  box-shadow: 0 4px 10px rgba(22, 163, 74, 0.3);
}

.stats{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
  gap:15px;
  margin-top:20px;
}
.stat{
  background:#f8fafc;
  padding:15px;
  border-radius:12px;
  text-align:center;
  transition: all 0.3s ease;
  border: 1px solid #e2e8f0;
}
.stat:hover {
  background: #f1f5f9;
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(0,0,0,.08);
}
.stat .num{
  color:var(--accent);
  font-weight:800;
  font-size: 1.5rem;
  margin-bottom: 5px;
}
.stat span {
  font-weight: 600;
  color: var(--light-text);
  font-size: 0.9rem;
}

/* Timeline */
.timeline{
  display:flex;
  flex-direction:column-reverse;
  position:relative;
  padding-right:30px;
  gap:18px;
}
.timeline::before{
  content:"";
  position:absolute;
  right:15px;
  top:0;
  bottom:0;
  width:4px;
  background:var(--accent);
  border-radius: 4px;
}
.timeline-item{
  background:white;
  border-radius:14px;
  padding:18px;
  margin-right:35px;
  box-shadow:0 4px 12px rgba(0,0,0,.08);
  position:relative;
  transition: all 0.3s ease;
  border-right: 3px solid var(--accent);
}
.timeline-item:hover {
  transform: translateX(-5px);
  box-shadow: 0 6px 15px rgba(0,0,0,.12);
}
.timeline-item::after{
  content:"";
  position:absolute;
  right:-32px;
  top:22px;
  width:18px;
  height:18px;
  background:var(--accent);
  border-radius:50%;
  box-shadow: 0 0 0 4px rgba(37, 99, 235, 0.2);
}
.timeline-date{
  color:var(--accent);
  font-weight:700;
  font-size: 0.80rem;
  margin-bottom: 8px;
}
.timeline-item div {
  font-weight: 600;
  margin-bottom: 5px;
  color: var(--text);
  font-size: 0.80rem;
}
.timeline-item div:last-child {
  color: var(--light-text);
  font-weight: 500;
  font-size: 0.80rem;
}

/* Achievements */
.achievement-card {
  background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
  border-right: 4px solid var(--accent);
  padding: 25px;
  border-radius: 16px;
  margin-bottom: 20px;
  position: relative;
  overflow: hidden;
}

.achievement-card::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.3)"/></svg>');
  background-size: cover;
}

.achievement-year {
  background: var(--accent);
  color: white;
  padding: 8px 16px;
  border-radius: 20px;
  font-weight: 700;
  display: inline-block;
  margin-bottom: 15px;
  font-size: 0.80rem;
}

.achievement-content {
  position: relative;
  z-index: 1;
}

.achievement-content p {
  line-height: 1.8;
  text-align: justify;
  font-size: 0.80rem;
  color: var(--text);
  margin: 0;
}

/* Skills & Training Lists - Updated colors */
.skills-card, .training-card {
  background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
  border-right: 4px solid var(--accent);
  padding: 25px;
  border-radius: 16px;
  margin-bottom: 20px;
}

.tech-card {
  background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
  border-right: 4px solid var(--accent);
  padding: 25px;
  border-radius: 16px;
  margin-bottom: 20px;
}

.contact-card {
  background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
  border-right: 4px solid var(--accent);
  padding: 25px;
  border-radius: 16px;
  margin-bottom: 20px;
  text-align: center;
}

ul {
  padding-right: 20px;
  margin: 0;
}

li {
  margin-bottom: 12px;
  line-height: 1.7;
  position: relative;
  padding-right: 15px;
  font-size: 0.80rem;
}

li::before {
  content: "•";
  color: var(--accent);
  font-weight: bold;
  position: absolute;
  right: 0;
}

footer{
  background:var(--primary);
  color:white;
  text-align:center;
  padding:20px;
  margin-top:40px;
  border-radius: 12px;
  font-weight: 500;
  font-size: 0.80rem;
}

/* Animation */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Responsive */
@media (max-width: 768px) {
  body {
    padding-right: 0;
  }
  
  nav {
    width: 60px;
  }
  
  .nav-link {
    width: 50px;
    height: 50px;
    font-size: 10px;
  }
  
  .lang-btn {
    top: 5px;
    left: 5px;
    padding: 6px 12px;
    font-size: 0.8rem;
  }
  
  .section-title {
    font-size: 1.5rem;
  }
  
  .card {
    padding: 20px;
  }
  
  .profile-img {
    width: 120px;
    height: 120px;
  }
  
  .nav-link::after {
    left: -6px;
    width: 3px;
  }
  
  .nav-link.active::after {
    height: 25px;
  }
}

/* Scrollbar styling for nav */
nav::-webkit-scrollbar {
  width: 4px;
}

nav::-webkit-scrollbar-track {
  background: #f1f1f1;
}

nav::-webkit-scrollbar-thumb {
  background: var(--accent);
  border-radius: 4px;
}

nav::-webkit-scrollbar-thumb:hover {
  background: #1d4ed8;
}
</style>
</head>

<body>

<button class="lang-btn" id="langBtn">EN</button>

<header>
  <span id="pageTitle">الملف المهني للمعلم فهد الخالدي</span>
</header>

<nav>
  <div class="nav-container">
    <div class="nav-link active" data-section="about">
      <svg viewBox="0 0 24 24"><path d="M12 12a5 5 0 1 0-5-5 5 5 0 0 0 5 5Zm0 2c-4.4 0-8 2.2-8 5v1h16v-1c0-2.8-3.6-5-8-5Z"/></svg>
      <span id="navAbout">نبذة عني</span>
    </div>
    <div class="nav-link" data-section="experience">
      <svg viewBox="0 0 24 24"><path d="M20 6h-4V4a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v2H4a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8a2 2 0 0 0-2-2Z"/></svg>
      <span id="navExp">الخبرات</span>
    </div>
    <div class="nav-link" data-section="achievements">
      <!-- Updated achievement icon -->
      <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 1 0 10 10A10 10 0 0 0 12 2Zm0 18a8 8 0 1 1 8-8 8 8 0 0 1-8 8Z"/><path d="m14.8 10.4-2.2 2.2-1.4-1.4-1.4 1.4 2.8 2.8 3.6-3.6Z"/></svg>
      <span id="navAchievements">الإنجازات</span>
    </div>
    <div class="nav-link" data-section="skills">
      <svg viewBox="0 0 24 24"><path d="M12 17.27 18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21Z"/></svg>
      <span id="navSkills">المهارات</span>
    </div>
    <div class="nav-link" data-section="training">
      <svg viewBox="0 0 24 24"><path d="M12 3 1 9l11 6 9-4.91V17h2V9Zm-7 10.18V17c0 .8 3 2 7 2s7-1.2 7-2v-3.82L12 16Z"/></svg>
      <span id="navTrain">الدورات</span>
    </div>
    <div class="nav-link" data-section="tech">
      <svg viewBox="0 0 24 24"><path d="M4 6h16v10H4Zm-4 12h24v-2H0Z"/></svg>
      <span id="navTech">التقنية</span>
    </div>
    <div class="nav-link" data-section="contact">
      <svg viewBox="0 0 24 24"><path d="M20 4H4v16h16ZM4 6l8 5 8-5"/></svg>
      <span id="navContact">تواصل</span>
    </div>
  </div>
</nav>

<main>

<section id="about" class="active">
<h2 class="section-title" id="aboutTitle">نبذة عني</h2>
<div class="card" style="text-align:center">
  <div class="profile-img">
    <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg" alt="صورة فهد الخالدي">
  </div>

  <h3 id="name" style="font-size: 1rem; margin-bottom: 8px; color: var(--primary);">فهد نغيمش حميد الخالدي</h3>
  <p style="font-size: 0.80rem; margin-bottom: 15px;"><b id="jobTitle">معلم متقدم – تخصص اللغة الإنجليزية</b></p>

  <p class="bio" id="bioText">
أؤمن أن التعليم ليس مجرد نقل معرفة، بل رسالة سامية لصناعة الأثر وبناء الإنسان. أطمح إلى أن أكون جزءًا فاعلًا في تطوير التعليم بالمملكة من خلال توظيف التقنيات الحديثة، وصناعة بيئات تعلم محفزة، تعزز التفكير النقدي والإبداعي، وتبني الثقة لدى الطالب. نظرتي المستقبلية تقوم على التعلم المستمر، وتطوير المهارات المهنية، ومواكبة التحولات الرقمية بما يخدم مخرجات التعليم وجودته في إطار رؤية المملكة 2030.
  </p>

  <div class="badge" id="badge">🏆 حاصل على درجة 95 في التخصص</div>

  <div class="stats">
    <div class="stat"><div class="num">14+</div><span id="stat1">سنوات خبرة</span></div>
    <div class="stat"><div class="num">130+</div><span id="stat2">ساعات تدريبية</span></div>
    <div class="stat"><div class="num">3</div><span id="stat3">مدن تعليمية</span></div>
  </div>
</div>
</section>

<section id="experience">
<h2 class="section-title" id="experienceTitle">الخبرات</h2>
<div class="card">
  <div class="timeline" id="timeline">
    <!-- سيتم ملؤها ديناميكياً -->
  </div>
</div>
</section>

<section id="achievements">
<h2 class="section-title" id="achievementsTitle">الإنجازات</h2>
<div class="card">
  <div class="achievement-card">
    <div class="achievement-year">2022</div>
    <div class="achievement-content">
      <p id="achievementText">
        في عام 2022 حصلتُ على ترقية إلى رتبة معلم متقدم بعد مسيرة مهنية امتدت لسنوات كمعلم ممارس، قدمت خلالها أداءً متميزًا أسهم في تطوير العملية التعليمية داخل المدرسة. جاءت هذه الترقية تقديرًا لجهودي في توظيف استراتيجيات تدريس حديثة تعزز مهارات التفكير النقدي والإبداعي لدى الطلاب، إضافة إلى قدرتي على تحليل نواتج التعلم وبناء خطط علاجية فردية أثمرت عن تحسين واضح في مستويات الطلاب.<br><br>

        وقد عكست هذه الترقية ثقة الجهة التعليمية بمهاراتي المهنية، خصوصًا في مجال تصميم أنشطة مبتكرة تُدمج مهارات الفهم العميق، والعمل التعاوني، والتعليم الذاتي داخل البيئة الصفية. كما كانت اعترافًا بدوري في تطوير البرامج التربوية والأنشطة التعليمية قبل عام 2022، ومساهمتي في بناء بيئة صفية محفزة يشعر فيها الطلاب بالأمان والرغبة في المشاركة والتعلم.<br><br>

        تعد هذه الترقية محطة مهمة في مسيرتي، لأنها لم تكن مجرد انتقال إلى مستوى وظيفي أعلى، بل كانت نتيجة تراكم خبرات وممارسات مهنية أثبتت أثرها على الطلاب وعلى منظومة التعليم داخل المدرسة. واليوم أواصل عملي كمعلم متقدم ملتزم بالتحسين المستمر، وتطبيق أفضل الممارسات التربوية، والمساهمة في رفع جودة التعليم وتحقيق نواتج تعلم أعلى.
      </p>
    </div>
  </div>
</div>
</section>

<section id="skills">
<h2 class="section-title" id="skillsTitle">المهارات</h2>
<div class="skills-card">
  <ul id="skillsList">
    <!-- سيتم ملؤها ديناميكياً -->
  </ul>
</div>
</section>

<section id="training">
<h2 class="section-title" id="trainingTitle">الدورات التدريبية</h2>
<div class="training-card">
  <ul id="trainingList">
    <!-- سيتم ملؤها ديناميكياً -->
  </ul>
</div>
</section>

<section id="tech">
<h2 class="section-title" id="techTitle">التقنية</h2>
<div class="tech-card">
  <p id="techText" style="line-height: 1.8; text-align: justify; margin: 0; font-size: 0.80rem;">
    أتمتع بشغف كبير تجاه التقنية والتعليم الرقمي، وأواكب أحدث التطورات في مجال الذكاء الاصطناعي وتطبيقاته التعليمية. أمتلك خبرة عملية في تصميم وتطوير أنشطة تفاعلية واختبارات إلكترونية باستخدام HTML وCSS وJavaScript، مما يثري تجربة التعلم ويجعلها أكثر تفاعلية وجاذبية للطلاب. أستخدم أدوات الذكاء الاصطناعي في تحليل أداء الطلاب وتصميم خطط تعليمية مخصصة، كما أصمم محتوى رقميًا مبتكرًا يتناسب مع احتياجات التعلم الحديثة. أسعى دائمًا لدمج التقنية في العملية التعليمية بطرق إبداعية تواكب متطلبات العصر الرقمي وتخدم أهداف رؤية المملكة 2030.
  </p>
</div>
</section>

<section id="contact">
<h2 class="section-title" id="contactTitle">تواصل</h2>
<div class="contact-card">
  <p id="contactText" style="font-size: 0.80rem; line-height: 1.8; margin: 0;">📧 iFahadenglish@gmail.com<br>📱 +9665554449824</p>
</div>
</section>

</main>

<footer id="footerText">© جميع الحقوق محفوظة - فهد الخالدي</footer>

<script>
// بيانات الترجمة
const translations = {
  ar: {
    pageTitle: "الملف المهني للمعلم فهد الخالدي",
    navAbout: "نبذة عني",
    navExp: "الخبرات",
    navAchievements: "الإنجازات",
    navSkills: "المهارات",
    navTrain: "الدورات",
    navTech: "التقنية",
    navContact: "تواصل",
    aboutTitle: "نبذة عني",
    experienceTitle: "الخبرات",
    achievementsTitle: "الإنجازات",
    skillsTitle: "المهارات",
    trainingTitle: "الدورات التدريبية",
    techTitle: "التقنية",
    contactTitle: "تواصل",
    name: "فهد نغيمش حميد الخالدي",
    jobTitle: "معلم متقدم – تخصص اللغة الإنجليزية",
    bioText: "أؤمن أن التعليم ليس مجرد نقل معرفة، بل رسالة سامية لصناعة الأثر وبناء الإنسان. أطمح إلى أن أكون جزءًا فاعلًا في تطوير التعليم بالمملكة من خلال توظيف التقنيات الحديثة، وصناعة بيئات تعلم محفزة، تعزز التفكير النقدي والإبداعي، وتبني الثقة لدى الطالب. نظرتي المستقبلية تقوم على التعلم المستمر، وتطوير المهارات المهنية، ومواكبة التحولات الرقمية بما يخدم مخرجات التعليم وجودته في إطار رؤية المملكة 2030.",
    badge: "🏆 حاصل على درجة 95 في التخصص",
    stat1: "سنوات خبرة",
    stat2: "ساعات تدريبية",
    stat3: "مدن تعليمية",
    achievementText: "في عام 2022 حصلتُ على ترقية إلى رتبة معلم متقدم بعد مسيرة مهنية امتدت لسنوات كمعلم ممارس، قدمت خلالها أداءً متميزًا أسهم في تطوير العملية التعليمية داخل المدرسة. جاءت هذه الترقية تقديرًا لجهودي في توظيف استراتيجيات تدريس حديثة تعزز مهارات التفكير النقدي والإبداعي لدى الطلاب، إضافة إلى قدرتي على تحليل نواتج التعلم وبناء خطط علاجية فردية أثمرت عن تحسين واضح في مستويات الطلاب.<br><br>وقد عكست هذه الترقية ثقة الجهة التعليمية بمهاراتي المهنية، خصوصًا في مجال تصميم أنشطة مبتكرة تُدمج مهارات الفهم العميق، والعمل التعاوني، والتعليم الذاتي داخل البيئة الصفية. كما كانت اعترافًا بدوري في تطوير البرامج التربوية والأنشطة التعليمية قبل عام 2022، ومساهمتي في بناء بيئة صفية محفزة يشعر فيها الطلاب بالأمان والرغبة في المشاركة والتعلم.<br><br>تعد هذه الترقية محطة مهمة في مسيرتي، لأنها لم تكن مجرد انتقال إلى مستوى وظيفي أعلى، بل كانت نتيجة تراكم خبرات وممارسات مهنية أثبتت أثرها على الطلاب وعلى منظومة التعليم داخل المدرسة. واليوم أواصل عملي كمعلم متقدم ملتزم بالتحسين المستمر، وتطبيق أفضل الممارسات التربوية، والمساهمة في رفع جودة التعليم وتحقيق نواتج تعلم أعلى.",
    experiences: [
      {date: "2011 - 2012", title: "مترجم – وزارة الحج والعمرة", location: "مكة المكرمة"},
      {date: "2012 - 2014", title: "معلم لغة إنجليزية – سعيد بن زيد", location: "عفيف"},
      {date: "2015 - 2016", title: "معلم لغة إنجليزية – ثانوية الأمير سعود بن عبدالمحسن", location: "الليث"},
      {date: "2017 - الآن", title: "معلم لغة إنجليزية – سعيد بن العاص", location: "مكة المكرمة"}
    ],
    skills: [
      "إتقان اللغة الإنجليزية تحدثا وكتابة",
      "تطوير وتنفيذ خطط تدريس محفزة ومبتكرة",
      "إدارة الصفوف بفاعلية وتشجيع التعلم الذاتي",
      "استخدام أدوات القياس والتقويم الإلكترونية بدقة",
      "دمج مهارات التفكير النقدي والإبداعي في التعليم",
      "شغف مستمر بتعلم اللغات واكتساب مهارات جديدة",
      "القدرة على التعليم في بيئات متعددة الثقافات مع استعداد لتعلم لغات إضافية مثل الصينية"
    ],
    trainings: [
      "التفكير الناقد والإبداعي ودمجه في المواد الدراسية",
      "القياس والتقويم التربوي",
      "الاستراتيجية الحديثة في تدريس أساسيات اللغة الإنجليزية",
      "البيئة الصفية الجاذبة",
      "تحليل أداء الطلاب وتقديم التغذية الراجعة",
      "أساسيات الترجمة",
      "مهارات التعامل مع أدوات القياس والتقويم الإلكترونية",
      "التنمية المهنية لمعلمي اللغة الإنجليزية - المستوى الثالث",
      "العبقرية في العملية التعليمية",
      "بناء الاختيار الجيد",
      "توظيف استراتيجيات التعليم في البيئة التدريبية الجاذبة",
      "تدريس مهارتي التحدث والاستماع",
      "التوعية بقواعد السلوك والمواظبة المحدثة",
      "اللقاءات التخصصية لمادة اللغة الإنجليزية"
    ],
    techText: "أتمتع بشغف كبير تجاه التقنية والتعليم الرقمي، وأواكب أحدث التطورات في مجال الذكاء الاصطناعي وتطبيقاته التعليمية. أمتلك خبرة عملية في تصميم وتطوير أنشطة تفاعلية واختبارات إلكترونية باستخدام HTML وCSS وJavaScript، مما يثري تجربة التعلم ويجعلها أكثر تفاعلية وجاذبية للطلاب. أستخدم أدوات الذكاء الاصطناعي في تحليل أداء الطلاب وتصميم خطط تعليمية مخصصة، كما أصمم محتوى رقميًا مبتكرًا يتناسب مع احتياجات التعلم الحديثة. أسعى دائمًا لدمج التقنية في العملية التعليمية بطرق إبداعية تواكب متطلبات العصر الرقمي وتخدم أهداف رؤية المملكة 2030.",
    contactText: "📧 iFahadenglish@gmail.com<br>📱 +9665554449824",
    footerText: "© جميع الحقوق محفوظة - فهد الخالدي"
  },
  en: {
    pageTitle: "Professional Portfolio - Fahad AlKhaldi",
    navAbout: "About Me",
    navExp: "Experience",
    navAchievements: "Achievements",
    navSkills: "Skills",
    navTrain: "Training",
    navTech: "Technology",
    navContact: "Contact",
    aboutTitle: "About Me",
    experienceTitle: "Professional Experience",
    achievementsTitle: "Achievements",
    skillsTitle: "Skills",
    trainingTitle: "Training Courses",
    techTitle: "Technology",
    contactTitle: "Contact",
    name: "Fahad Nughaimesh Humaid AlKhaldi",
    jobTitle: "Advanced English Teacher",
    bioText: "I believe that education is not merely about transferring knowledge, but a noble mission to make an impact and build individuals. I aspire to be an active part in developing education in the Kingdom by employing modern technologies, creating stimulating learning environments that enhance critical and creative thinking, and building student confidence. My future vision is based on continuous learning, developing professional skills, and keeping pace with digital transformations that serve educational outcomes and quality within the framework of Saudi Vision 2030.",
    badge: "🏆 Achieved a score of 95 in specialization",
    stat1: "Years of Experience",
    stat2: "Training Hours",
    stat3: "Education Cities",
    achievementText: "In 2022, I was promoted to the rank of Advanced Teacher after a professional career spanning years as a practicing teacher, during which I provided outstanding performance that contributed to the development of the educational process within the school. This promotion came in recognition of my efforts in employing modern teaching strategies that enhance students' critical and creative thinking skills, in addition to my ability to analyze learning outcomes and build individual remedial plans that resulted in a clear improvement in student levels.<br><br>This promotion reflected the educational authority's confidence in my professional skills, especially in designing innovative activities that integrate deep understanding skills, collaborative work, and self-learning within the classroom environment. It was also an acknowledgment of my role in developing educational programs and activities before 2022, and my contribution to building a stimulating classroom environment where students feel safe and eager to participate and learn.<br><br>This promotion is an important milestone in my career, as it was not just a transition to a higher functional level, but rather the result of accumulated experiences and professional practices that proved their impact on students and the educational system within the school. Today, I continue my work as a senior teacher committed to continuous improvement, applying the best educational practices, and contributing to raising the quality of education and achieving higher learning outcomes.",
    experiences: [
      {date: "2011 - 2012", title: "Translator - Ministry of Hajj and Umrah", location: "Makkah"},
      {date: "2012 - 2014", title: "English Teacher - Saeed Bin Zaid", location: "Afif"},
      {date: "2015 - 2016", title: "English Teacher - Prince Saud Bin Abdulmohsen Secondary School", location: "Al-Laith"},
      {date: "2017 - Present", title: "English Teacher - Saeed Bin Al-Aas", location: "Makkah"}
    ],
    skills: [
      "Fluent in English speaking and writing",
      "Developing and implementing stimulating and innovative teaching plans",
      "Effective classroom management and encouraging self-learning",
      "Accurate use of electronic measurement and evaluation tools",
      "Integrating critical and creative thinking skills into education",
      "Continuous passion for learning languages and acquiring new skills",
      "Ability to teach in multicultural environments with readiness to learn additional languages such as Chinese"
    ],
    trainings: [
      "Critical and Creative Thinking and its integration into subjects",
      "Educational Measurement and Evaluation",
      "Modern Strategy in Teaching English Fundamentals",
      "Attractive Classroom Environment",
      "Student Performance Analysis and Providing Feedback",
      "Basics of Translation",
      "Skills for Dealing with Electronic Measurement and Evaluation Tools",
      "Professional Development for English Teachers - Level 3",
      "Genius in the Educational Process",
      "Building Good Multiple Choice Questions",
      "Employing Teaching Strategies in Attractive Training Environments",
      "Teaching Speaking and Listening Skills",
      "Awareness of Updated Behavior and Attendance Rules",
      "Specialized English Subject Meetings"
    ],
    techText: "I have a great passion for technology and digital education, and I keep up with the latest developments in the field of artificial intelligence and its educational applications. I have practical experience in designing and developing interactive activities and electronic tests using HTML, CSS, and JavaScript, which enriches the learning experience and makes it more interactive and attractive for students. I use AI tools to analyze student performance and design customized educational plans, and I also design innovative digital content that suits modern learning needs. I always strive to integrate technology into the educational process in creative ways that keep pace with the requirements of the digital age and serve the goals of Saudi Vision 2030.",
    contactText: "📧 iFahadenglish@gmail.com<br>📱 +9665554449824",
    footerText: "© All Rights Reserved - Fahad AlKhaldi"
  }
};

let currentLang = 'ar';

// عناصر DOM
const langBtn = document.getElementById('langBtn');
const pageTitle = document.getElementById('pageTitle');
const navAbout = document.getElementById('navAbout');
const navExp = document.getElementById('navExp');
const navAchievements = document.getElementById('navAchievements');
const navSkills = document.getElementById('navSkills');
const navTrain = document.getElementById('navTrain');
const navTech = document.getElementById('navTech');
const navContact = document.getElementById('navContact');
const aboutTitle = document.getElementById('aboutTitle');
const experienceTitle = document.getElementById('experienceTitle');
const achievementsTitle = document.getElementById('achievementsTitle');
const skillsTitle = document.getElementById('skillsTitle');
const trainingTitle = document.getElementById('trainingTitle');
const techTitle = document.getElementById('techTitle');
const contactTitle = document.getElementById('contactTitle');
const nameEl = document.getElementById('name');
const jobTitle = document.getElementById('jobTitle');
const bioText = document.getElementById('bioText');
const badge = document.getElementById('badge');
const stat1 = document.getElementById('stat1');
const stat2 = document.getElementById('stat2');
const stat3 = document.getElementById('stat3');
const achievementText = document.getElementById('achievementText');
const timeline = document.getElementById('timeline');
const skillsList = document.getElementById('skillsList');
const trainingList = document.getElementById('trainingList');
const techText = document.getElementById('techText');
const contactText = document.getElementById('contactText');
const footerText = document.getElementById('footerText');

// وظيفة لتحميل اللغة
function loadLanguage(lang) {
  const t = translations[lang];
  
  // تحديث النصوص الأساسية
  pageTitle.textContent = t.pageTitle;
  navAbout.textContent = t.navAbout;
  navExp.textContent = t.navExp;
  navAchievements.textContent = t.navAchievements;
  navSkills.textContent = t.navSkills;
  navTrain.textContent = t.navTrain;
  navTech.textContent = t.navTech;
  navContact.textContent = t.navContact;
  aboutTitle.textContent = t.aboutTitle;
  experienceTitle.textContent = t.experienceTitle;
  achievementsTitle.textContent = t.achievementsTitle;
  skillsTitle.textContent = t.skillsTitle;
  trainingTitle.textContent = t.trainingTitle;
  techTitle.textContent = t.techTitle;
  contactTitle.textContent = t.contactTitle;
  nameEl.textContent = t.name;
  jobTitle.textContent = t.jobTitle;
  bioText.textContent = t.bioText;
  badge.textContent = t.badge;
  stat1.textContent = t.stat1;
  stat2.textContent = t.stat2;
  stat3.textContent = t.stat3;
  achievementText.innerHTML = t.achievementText;
  techText.textContent = t.techText;
  contactText.innerHTML = t.contactText;
  footerText.textContent = t.footerText;
  
  // تحديث الخط الزمني
  timeline.innerHTML = '';
  t.experiences.forEach(exp => {
    const item = document.createElement('div');
    item.className = 'timeline-item';
    item.innerHTML = `
      <div class="timeline-date">${exp.date}</div>
      <div>${exp.title}</div>
      <div>${exp.location}</div>
    `;
    timeline.appendChild(item);
  });
  
  // تحديث المهارات
  skillsList.innerHTML = '';
  t.skills.forEach(skill => {
    const li = document.createElement('li');
    li.textContent = skill;
    skillsList.appendChild(li);
  });
  
  // تحديث الدورات
  trainingList.innerHTML = '';
  t.trainings.forEach(training => {
    const li = document.createElement('li');
    li.textContent = training;
    trainingList.appendChild(li);
  });
  
  // تحديث اتجاه النص
  document.documentElement.dir = lang === 'ar' ? 'rtl' : 'ltr';
  document.documentElement.lang = lang;
  
  // تحديث موضع الشريط الجانبي
  const nav = document.querySelector('nav');
  if (lang === 'ar') {
    nav.style.right = '0';
    nav.style.left = 'auto';
    document.body.style.paddingRight = '90px';
    document.body.style.paddingLeft = '0';
  } else {
    nav.style.left = '0';
    nav.style.right = 'auto';
    document.body.style.paddingLeft = '90px';
    document.body.style.paddingRight = '0';
  }
}

// حدث تبديل اللغة
langBtn.addEventListener('click', () => {
  currentLang = currentLang === 'ar' ? 'en' : 'ar';
  loadLanguage(currentLang);
  langBtn.textContent = currentLang === 'ar' ? 'EN' : 'AR';
  langBtn.setAttribute('aria-label', currentLang === 'ar' ? 'Switch to English' : 'التبديل إلى العربية');
});

// التنقل بين الأقسام
document.querySelectorAll(".nav-link").forEach(link => {
  link.addEventListener('click', (e) => {
    e.preventDefault();
    
    // إزالة النشط من جميع الروابط
    document.querySelectorAll(".nav-link").forEach(n => n.classList.remove("active"));
    
    // إضافة النشط للرابط المحدد
    link.classList.add("active");
    
    // إخفاء جميع الأقسام
    document.querySelectorAll("section").forEach(s => s.classList.remove("active"));
    
    // إظهار القسم المحدد
    const targetSection = link.getAttribute('data-section');
    document.getElementById(targetSection).classList.add("active");
    
    // إضافة تأثير التمرير السلس
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });
});

// تحسين إمكانية الوصول للتنقل
document.querySelectorAll(".nav-link").forEach((el) => {
  el.tabIndex = 0;
  el.addEventListener('keydown', (e) => {
    if (e.key === 'Enter' || e.key === ' ') {
      e.preventDefault();
      el.click();
    }
  });
});

// التحميل الأولي
loadLanguage(currentLang);
</script>

</body>
</html>
