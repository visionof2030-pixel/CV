
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>الملف المهني | فهد الخالدي</title>

<style>
:root{
  --primary:#1a365d;
  --accent:#2563eb;
  --bg:#f5f7fa;
}
*{box-sizing:border-box;font-family:Tahoma,Arial}

body{
  margin:0;
  background:var(--bg);
  color:#0f172a;
  padding-right:90px;
  transition: padding 0.3s ease;
}

header{
  background:linear-gradient(135deg,var(--primary),#020617);
  color:#fff;
  text-align:center;
  padding:14px;
}
#pageTitle{
  font-size:.82rem;
  background:rgba(255,255,255,.15);
  padding:4px 14px;
  border-radius:999px;
  display:inline-block;
}

.lang-btn{
  position:fixed;
  top:10px;
  left:10px;
  background:#fff;
  color:var(--accent);
  border:none;
  padding:6px 12px;
  border-radius:8px;
  font-weight:bold;
  cursor:pointer;
  z-index:3000;
  transition: all 0.2s ease;
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
}
.nav-container{
  display:flex;
  flex-direction:column;
  align-items:center;
  padding-top:90px;
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
}
.nav-link svg{width:20px;height:20px;fill:currentColor}
.nav-link.active,
.nav-link:hover{
  background:var(--accent);
  color:white;
  transform: translateX(-2px);
}

main{max-width:1100px;margin:auto;padding:20px}
section{display:none; animation: fadeIn 0.5s ease;}
section.active{display:block}
.section-title{text-align:center;color:var(--primary); margin-bottom: 20px;}

.card{
  background:#fff;
  border-radius:14px;
  padding:18px;
  margin-bottom:18px;
  box-shadow:0 6px 18px rgba(0,0,0,.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0,0,0,.1);
}

.profile-img{
  width:130px;height:130px;
  margin:10px auto;
  border-radius:50%;
  overflow:hidden;
  border:3px solid var(--accent);
}
.profile-img img{width:100%;height:100%;object-fit:cover}

.bio{text-align:justify;font-size:.95rem; line-height: 1.7;}

.badge{
  margin:10px auto;
  text-align:center;
  background:#16a34a;
  color:white;
  padding:6px 18px;
  border-radius:999px;
  font-size:12px;
  display:inline-flex;
  gap:6px;
  align-items:center;
}

.stats{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(120px,1fr));
  gap:10px;
  margin-top:12px;
}
.stat{
  background:#f1f5f9;
  padding:10px;
  border-radius:10px;
  text-align:center;
  transition: all 0.3s ease;
}
.stat:hover {
  background: #e2e8f0;
  transform: translateY(-3px);
}
.stat .num{color:var(--accent);font-weight:bold; font-size: 1.2rem;}

/* Timeline */
.timeline{
  display:flex;
  flex-direction:column-reverse;
  position:relative;
  padding-right:30px;
  gap:14px;
}
.timeline::before{
  content:"";
  position:absolute;
  right:10px;
  top:0;
  bottom:0;
  width:4px;
  background:var(--accent);
}
.timeline-item{
  background:white;
  border-radius:12px;
  padding:12px;
  margin-right:28px;
  box-shadow:0 4px 12px rgba(0,0,0,.08);
  position:relative;
  transition: all 0.3s ease;
}
.timeline-item:hover {
  transform: translateX(-5px);
  box-shadow: 0 6px 15px rgba(0,0,0,.12);
}
.timeline-item::after{
  content:"";
  position:absolute;
  right:-25px;
  top:18px;
  width:14px;
  height:14px;
  background:var(--accent);
  border-radius:50%;
}
.timeline-date{color:var(--accent);font-weight:bold}

footer{
  background:var(--primary);
  color:white;
  text-align:center;
  padding:16px;
  margin-top:30px;
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
    padding: 4px 8px;
    font-size: 0.8rem;
  }
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

  <h3 id="name">فهد نغيمش حميد الخالدي</h3>
  <p><b id="jobTitle">معلم متقدم – تخصص اللغة الإنجليزية</b></p>

  <p class="bio" id="bioText">
أؤمن أن التعليم ليس مجرد نقل معرفة، بل رسالة سامية لصناعة الأثر وبناء الإنسان. أطمح إلى أن أكون جزءًا فاعلًا في تطوير التعليم بالمملكة من خلال توظيف التقنيات الحديثة، وصناعة بيئات تعلم محفزة، تعزز التفكير النقدي والإبداعي، وتبني الثقة لدى الطالب. نظرتي المستقبلية تقوم على التعلم المستمر، وتطوير المهارات المهنية، ومواكبة التحولات الرقمية بما يخدم مخرجات التعليم وجودته في إطار رؤية المملكة 2030.
  </p>

  <div class="badge" id="badge">🏆 حاصل على درجة متميزة في التخصص</div>

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

<section id="skills">
<h2 class="section-title" id="skillsTitle">المهارات</h2>
<div class="card">
  <ul id="skillsList">
    <!-- سيتم ملؤها ديناميكياً -->
  </ul>
</div>
</section>

<section id="training">
<h2 class="section-title" id="trainingTitle">الدورات التدريبية</h2>
<div class="card">
  <ul id="trainingList">
    <!-- سيتم ملؤها ديناميكياً -->
  </ul>
</div>
</section>

<section id="tech">
<h2 class="section-title" id="techTitle">التقنية</h2>
<div class="card">
  <p id="techText">أواكب التقنيات التعليمية الحديثة، وأستخدم أدوات التعليم الرقمي، وتصميم الاختبارات الإلكترونية، وتوظيف الذكاء الاصطناعي في تحسين الأداء التعليمي.</p>
</div>
</section>

<section id="contact">
<h2 class="section-title" id="contactTitle">تواصل</h2>
<div class="card" style="text-align:center">
  <p id="contactText">📧 iFahadenglish@gmail.com<br>📱 +9665554449824</p>
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
    navSkills: "المهارات",
    navTrain: "الدورات",
    navTech: "التقنية",
    navContact: "تواصل",
    aboutTitle: "نبذة عني",
    experienceTitle: "الخبرات",
    skillsTitle: "المهارات",
    trainingTitle: "الدورات التدريبية",
    techTitle: "التقنية",
    contactTitle: "تواصل",
    name: "فهد نغيمش حميد الخالدي",
    jobTitle: "معلم متقدم – تخصص اللغة الإنجليزية",
    bioText: "أؤمن أن التعليم ليس مجرد نقل معرفة، بل رسالة سامية لصناعة الأثر وبناء الإنسان. أطمح إلى أن أكون جزءًا فاعلًا في تطوير التعليم بالمملكة من خلال توظيف التقنيات الحديثة، وصناعة بيئات تعلم محفزة، تعزز التفكير النقدي والإبداعي، وتبني الثقة لدى الطالب. نظرتي المستقبلية تقوم على التعلم المستمر، وتطوير المهارات المهنية، ومواكبة التحولات الرقمية بما يخدم مخرجات التعليم وجودته في إطار رؤية المملكة 2030.",
    badge: "🏆 حاصل على درجة متميزة في التخصص",
    stat1: "سنوات خبرة",
    stat2: "ساعات تدريبية",
    stat3: "مدن تعليمية",
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
    techText: "أواكب التقنيات التعليمية الحديثة، وأستخدم أدوات التعليم الرقمي، وتصميم الاختبارات الإلكترونية، وتوظيف الذكاء الاصطناعي في تحسين الأداء التعليمي.",
    contactText: "📧 iFahadenglish@gmail.com<br>📱 +9665554449824",
    footerText: "© جميع الحقوق محفوظة - فهد الخالدي"
  },
  en: {
    pageTitle: "Professional Portfolio - Fahad AlKhaldi",
    navAbout: "About Me",
    navExp: "Experience",
    navSkills: "Skills",
    navTrain: "Training",
    navTech: "Technology",
    navContact: "Contact",
    aboutTitle: "About Me",
    experienceTitle: "Professional Experience",
    skillsTitle: "Skills",
    trainingTitle: "Training Courses",
    techTitle: "Technology",
    contactTitle: "Contact",
    name: "Fahad Naghimish Hamid AlKhaldi",
    jobTitle: "Senior English Teacher",
    bioText: "I believe that education is not merely about transferring knowledge, but a noble mission to make an impact and build individuals. I aspire to be an active part in developing education in the Kingdom by employing modern technologies, creating stimulating learning environments that enhance critical and creative thinking, and building student confidence. My future vision is based on continuous learning, developing professional skills, and keeping pace with digital transformations that serve educational outcomes and quality within the framework of Saudi Vision 2030.",
    badge: "🏆 Achieved an excellent grade in specialization",
    stat1: "Years of Experience",
    stat2: "Training Hours",
    stat3: "Education Cities",
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
    techText: "I keep up with modern educational technologies, use digital education tools, design electronic tests, and employ artificial intelligence in improving educational performance.",
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
const navSkills = document.getElementById('navSkills');
const navTrain = document.getElementById('navTrain');
const navTech = document.getElementById('navTech');
const navContact = document.getElementById('navContact');
const aboutTitle = document.getElementById('aboutTitle');
const experienceTitle = document.getElementById('experienceTitle');
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
  navSkills.textContent = t.navSkills;
  navTrain.textContent = t.navTrain;
  navTech.textContent = t.navTech;
  navContact.textContent = t.navContact;
  aboutTitle.textContent = t.aboutTitle;
  experienceTitle.textContent = t.experienceTitle;
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
      ${exp.title}<br>${exp.location}
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
});

// التنقل بين الأقسام
document.querySelectorAll(".nav-link").forEach(link => {
  link.addEventListener('click', () => {
    document.querySelectorAll(".nav-link").forEach(n => n.classList.remove("active"));
    document.querySelectorAll("section").forEach(s => s.classList.remove("active"));
    link.classList.add("active");
    document.getElementById(link.dataset.section).classList.add("active");
    
    // إضافة تأثير التمرير السلس
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });
});

// التحميل الأولي
loadLanguage(currentLang);
</script>

</body>
</html>
