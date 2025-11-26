
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>ملفي المهني - فهد الخالدي</title>

<style>
:root {
--primary:#1a365d;
--accent:#e53e3e;
--nav-bg:#2c5282;
}

body{
margin:0;
font-family:Tajawal,Arial;
background:#f4f6f8;
font-size:1.3rem;
}

.container{max-width:1200px;margin:auto;padding:20px;}

section{display:none;padding:3rem 0;}
section.active{display:block;}

.section-title{text-align:center;font-size:2.5rem;color:var(--primary);margin-bottom:2rem;}

.card{
background:#fff;
padding:2.5rem;
border-radius:18px;
margin-bottom:2.5rem;
box-shadow:0 10px 25px rgba(0,0,0,0.08);
}

/* الصورة */
.profile-img{
width:260px;height:260px;
margin:auto;
border-radius:50%;
overflow:hidden;
box-shadow:0 10px 25px rgba(0,0,0,0.25);
}
.profile-img img{width:100%;height:100%;object-fit:cover;}

.profile-name{text-align:center;font-size:2.2rem;font-weight:bold;margin-top:1rem;}
.profile-title{text-align:center;font-size:1.5rem;color:var(--accent);margin-bottom:1rem;}

/* شريط التنقل الجديد */
.profile-nav{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:10px;
margin-bottom:2rem;
}

.profile-nav .nav-link{
background:var(--nav-bg);
color:white;
padding:10px 20px;
border-radius:30px;
cursor:pointer;
text-decoration:none;
transition:.3s;
}

.profile-nav .nav-link:hover,
.profile-nav .nav-link.active{
background:var(--accent);
}

/* تايم لاين */
.timeline{max-width:800px;margin:auto;}
.timeline-item{margin-bottom:2rem;}
.timeline-content{
background:white;
padding:1.8rem;
border-radius:15px;
box-shadow:0 5px 20px rgba(0,0,0,.08);
}

.skill-bar{
height:12px;
background:#ddd;
border-radius:8px;
overflow:hidden;
}

.skill-level{
height:100%;
background:var(--accent);
}

/* الفورم */
.form-control{
width:100%;
padding:10px;
border:2px solid #ccc;
border-radius:8px;
margin-bottom:1rem;
}

.btn{
background:var(--accent);
color:white;
border:none;
padding:12px 30px;
border-radius:8px;
cursor:pointer;
}
</style>
</head>

<body>

<main class="container">

<!-- ABOUT -->
<section id="about" class="active">
<h2 class="section-title">نبذة عني</h2>

<div class="card">

<div class="profile-img">
<img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg">
</div>

<div class="profile-name">فهد نغيمش الخالدي</div>
<div class="profile-title">معلم متقدم - لغة إنجليزية</div>

<!-- ✅ شريط التنقل في منتصف الصفحة -->
<div class="profile-nav">
<a class="nav-link active" data-section="about">نبذة</a>
<a class="nav-link" data-section="experience">خبراتي</a>
<a class="nav-link" data-section="skills">مهاراتي</a>
<a class="nav-link" data-section="training">الدورات</a>
<a class="nav-link" data-section="portfolio">الملف</a>
<a class="nav-link" data-section="contact">تواصل</a>
</div>

<p>أنا معلم لغة إنجليزية بخبرة تتجاوز 14 عامًا...</p>

</div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
<h2 class="section-title">خبراتي</h2>

<div class="timeline">

<div class="timeline-item">
<div class="timeline-content">
<h3>2017 - الآن</h3>
<p>معلم لغة إنجليزية - إدارة تعليم مكة</p>
</div>
</div>

<div class="timeline-item">
<div class="timeline-content">
<h3>2014 - 2016</h3>
<p>معلم لغة إنجليزية - تعليم الليث</p>
</div>
</div>

</div>
</section>

<!-- SKILLS -->
<section id="skills">
<h2 class="section-title">مهاراتي</h2>

<div class="card">
<p>إتقان اللغة الإنجليزية</p>
<div class="skill-bar"><div class="skill-level" style="width:95%"></div></div>
</div>

</section>

<!-- TRAINING -->
<section id="training">
<h2 class="section-title">الدورات</h2>

<div class="card">برنامج التفكير الناقد</div>
<div class="card">القياس والتقويم</div>

</section>

<!-- PORTFOLIO -->
<section id="portfolio">
<h2 class="section-title">ملفي المهني</h2>
<div class="card">رؤيتي – رسالتي – أهدافي</div>
</section>

<!-- CONTACT -->
<section id="contact">
<h2 class="section-title">اتصل بي</h2>

<div class="card">
<input class="form-control" placeholder="اسمك">
<input class="form-control" placeholder="بريدك">
<textarea class="form-control" placeholder="رسالتك"></textarea>
<button class="btn">إرسال</button>
</div>

</section>

</main>

<script>
document.querySelectorAll('.nav-link').forEach(link=>{
link.onclick=()=>{
document.querySelectorAll('.nav-link').forEach(l=>l.classList.remove('active'));
document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
link.classList.add('active');
document.getElementById(link.dataset.section).classList.add('active');
window.scrollTo({top:0,behavior:"smooth"});
};
});
</script>

</body>
</html>
