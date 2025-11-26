
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>السيرة الذاتية - رؤية 2030</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #6a11cb;
            --secondary-color: #2575fc;
            --text-color: #333;
            --light-bg: #f5f5f5;
            --white: #ffffff;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            --border-radius: 10px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
            padding-bottom: 80px; /* مساحة للقائمة السفلية */
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* تصميم الهيدر */
        header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: var(--white);
            padding: 25px 0;
            text-align: center;
            box-shadow: var(--shadow);
            margin-bottom: 30px;
            border-radius: 0 0 var(--border-radius) var(--border-radius);
        }
        
        header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        /* تصميم القائمة الجانبية للوضع الأفقي */
        .sidebar {
            background-color: var(--white);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            padding: 25px;
            margin-bottom: 30px;
            width: 280px;
            float: right;
            margin-left: 30px;
            position: sticky;
            top: 20px;
        }
        
        .sidebar h2 {
            color: var(--primary-color);
            margin-bottom: 20px;
            font-size: 1.5rem;
            border-bottom: 2px solid #f0f0f0;
            padding-bottom: 10px;
            text-align: center;
        }
        
        .sidebar ul {
            list-style-type: none;
        }
        
        .sidebar li {
            margin-bottom: 15px;
        }
        
        .sidebar a {
            text-decoration: none;
            color: var(--text-color);
            font-size: 1.2rem;
            display: block;
            padding: 12px 15px;
            border-radius: 8px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
        }
        
        .sidebar a i {
            margin-left: 10px;
            font-size: 1.3rem;
        }
        
        .sidebar a:hover {
            background-color: #f0f0f0;
            color: var(--primary-color);
            transform: translateX(-5px);
        }
        
        .sidebar a.active {
            background-color: rgba(106, 17, 203, 0.1);
            color: var(--primary-color);
            font-weight: bold;
        }
        
        /* المحتوى الرئيسي */
        .main-content {
            background-color: var(--white);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            padding: 30px;
            overflow: hidden;
        }
        
        .section {
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 1px solid #f0f0f0;
        }
        
        .section:last-child {
            border-bottom: none;
        }
        
        .section h2 {
            color: var(--primary-color);
            margin-bottom: 20px;
            font-size: 1.8rem;
            padding-bottom: 10px;
            border-bottom: 2px solid #f0f0f0;
            display: flex;
            align-items: center;
        }
        
        .section h2 i {
            margin-left: 10px;
        }
        
        .section p {
            font-size: 1.2rem;
            margin-bottom: 15px;
            line-height: 1.8;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .skill-item {
            background-color: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .skill-item i {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        .timeline {
            position: relative;
            margin: 30px 0;
            padding-right: 30px;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            right: 0;
            top: 0;
            bottom: 0;
            width: 4px;
            background-color: var(--primary-color);
        }
        
        .timeline-item {
            margin-bottom: 30px;
            position: relative;
            padding-right: 30px;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            right: -38px;
            top: 5px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: var(--primary-color);
            border: 4px solid var(--white);
            box-shadow: 0 0 0 3px var(--primary-color);
        }
        
        .timeline-date {
            font-weight: bold;
            color: var(--primary-color);
            margin-bottom: 5px;
            font-size: 1.2rem;
        }
        
        .timeline-content {
            background-color: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            font-size: 1.2rem;
        }
        
        /* تصميم القائمة السفلية للوضع العمودي */
        .bottom-nav {
            display: none;
            position: fixed;
            bottom: 0;
            right: 0;
            left: 0;
            background-color: var(--white);
            box-shadow: 0 -2px 15px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 15px 0;
            border-radius: var(--border-radius) var(--border-radius) 0 0;
        }
        
        .nav-items {
            display: flex;
            justify-content: space-around;
            list-style-type: none;
        }
        
        .nav-items li {
            flex: 1;
            text-align: center;
        }
        
        .nav-items a {
            text-decoration: none;
            color: var(--text-color);
            font-size: 1.5rem; /* تكبير الخط بنسبة 50% تقريبًا */
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 8px 5px;
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .nav-items a i {
            font-size: 1.8rem;
            margin-bottom: 5px;
        }
        
        .nav-items a span {
            font-size: 0.9rem;
        }
        
        .nav-items a:hover, .nav-items a.active {
            background-color: rgba(106, 17, 203, 0.1);
            color: var(--primary-color);
        }
        
        /* استعلامات الوسائط للوضع العمودي */
        @media (max-width: 992px) {
            .sidebar {
                width: 250px;
            }
        }
        
        @media (max-width: 768px) {
            .sidebar {
                display: none;
            }
            
            .bottom-nav {
                display: block;
            }
            
            .main-content {
                margin-bottom: 30px;
                width: 100%;
                float: none;
            }
            
            /* تكبير الخطوط في المحتوى للوضع العمودي */
            .section h2 {
                font-size: 2.1rem; /* زيادة بنسبة 50% */
            }
            
            .section p, .timeline-content, .timeline-date {
                font-size: 1.5rem; /* زيادة بنسبة 50% */
            }
            
            header h1 {
                font-size: 3rem; /* زيادة بنسبة 50% */
            }
            
            header p {
                font-size: 1.8rem; /* زيادة بنسبة 50% */
            }
            
            .skill-item {
                font-size: 1.4rem;
            }
        }
        
        @media (min-width: 769px) {
            .bottom-nav {
                display: none;
            }
            
            .sidebar {
                display: block;
            }
        }
        
        /* تذييل الصفحة */
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            background-color: #333;
            color: white;
            font-size: 1.2rem;
            border-radius: var(--border-radius) var(--border-radius) 0 0;
        }
        
        /* تأثيرات إضافية */
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            background-color: #f9f9f9;
            padding: 10px 15px;
            border-radius: 8px;
            flex: 1;
            min-width: 200px;
        }
        
        .contact-item i {
            margin-left: 10px;
            color: var(--primary-color);
            font-size: 1.5rem;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>رؤية 2030 - السيرة الذاتية</h1>
            <p>مطور ويب ومصمم واجهات مستخدم</p>
        </div>
    </header>
    
    <div class="container">
        <!-- القائمة الجانبية للوضع الأفقي -->
        <aside class="sidebar">
            <div class="profile-img">
                <i class="fas fa-user"></i>
            </div>
            <h2>القائمة</h2>
            <ul>
                <li><a href="#about" class="active"><i class="fas fa-user"></i> نبذة عني</a></li>
                <li><a href="#experience"><i class="fas fa-briefcase"></i> خبراتي المهنية</a></li>
                <li><a href="#skills"><i class="fas fa-cogs"></i> مهاراتي</a></li>
                <li><a href="#courses"><i class="fas fa-certificate"></i> الدورات التدريبية</a></li>
                <li><a href="#contact"><i class="fas fa-envelope"></i> التواصل</a></li>
            </ul>
        </aside>
        
        <!-- المحتوى الرئيسي -->
        <main class="main-content">
            <section id="about" class="section">
                <h2><i class="fas fa-user"></i> نبذة عني</h2>
                <p>أنا مطور واجهات مستخدم متخصص في إنشاء تطبيقات ويب تفاعلية وجذابة. لدي خبرة تزيد عن 5 سنوات في مجال تطوير الويب، وأعمل حاليًا على مشاريع متنوعة تهدف إلى تحقيق رؤية 2030.</p>
                <p>أتمتع بشغف كبير لتعلم التقنيات الحديثة وتطبيقها في مشاريع حقيقية، وأسعى دائمًا لتطوير مهاراتي وتحسين جودة العمل المقدم.</p>
            </section>
            
            <section id="experience" class="section">
                <h2><i class="fas fa-briefcase"></i> خبراتي المهنية</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-date">2017 - الآن</div>
                        <div class="timeline-content">
                            <h3>مطور ويب مستقل</h3>
                            <p>عملت على تطوير العديد من مواقع الويب والتطبيقات لعملاء من مختلف القطاعات. قمت بتصميم واجهات مستخدم متجاوبة وتجربة مستخدم محسنة.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-date">2015 - 2017</div>
                        <div class="timeline-content">
                            <h3>مصمم جرافيك</h3>
                            <p>عملت في وكالة إعلانية كمصمم جرافيك، حيث كنت مسؤولاً عن تصميم الهويات البصرية والمواد التسويقية للعديد من العلامات التجارية.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <section id="skills" class="section">
                <h2><i class="fas fa-cogs"></i> مهاراتي</h2>
                <div class="skills-grid">
                    <div class="skill-item">
                        <i class="fab fa-html5"></i>
                        <h3>HTML5</h3>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-css3-alt"></i>
                        <h3>CSS3</h3>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-js"></i>
                        <h3>JavaScript</h3>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-react"></i>
                        <h3>React</h3>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-git"></i>
                        <h3>Git</h3>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-mobile-alt"></i>
                        <h3>التصميم المتجاوب</h3>
                    </div>
                </div>
            </section>
            
            <section id="courses" class="section">
                <h2><i class="fas fa-certificate"></i> الدورات التدريبية</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-date">2022</div>
                        <div class="timeline-content">
                            <h3>تطوير تطبيقات الويب باستخدام React</h3>
                            <p>دورة متقدمة في تطوير تطبيقات الويب باستخدام مكتبة React وتقنياتها الحديثة مثل Hooks وContext API.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-date">2021</div>
                        <div class="timeline-content">
                            <h3>أمن المعلومات للويب</h3>
                            <p>دورة متخصصة في تأمين تطبيقات الويب ضد الهجمات الإلكترونية الشائعة مثل XSS وCSRF.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-date">2020</div>
                        <div class="timeline-content">
                            <h3>تحسين محركات البحث SEO</h3>
                            <p>دورة شاملة في تحسين مواقع الويب لمحركات البحث وزيادة الظهور العضوي.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <section id="contact" class="section">
                <h2><i class="fas fa-envelope"></i> التواصل</h2>
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>example@vision2030.com</span>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <span>+966 50 123 4567</span>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-linkedin"></i>
                        <span>linkedin.com/in/example</span>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-github"></i>
                        <span>github.com/vision2030</span>
                    </div>
                </div>
            </section>
        </main>
    </div>
    
    <!-- القائمة السفلية للوضع العمودي -->
    <nav class="bottom-nav">
        <ul class="nav-items">
            <li><a href="#about" class="active"><i class="fas fa-user"></i> <span>نبذة</span></a></li>
            <li><a href="#experience"><i class="fas fa-briefcase"></i> <span>خبرات</span></a></li>
            <li><a href="#skills"><i class="fas fa-cogs"></i> <span>مهارات</span></a></li>
            <li><a href="#courses"><i class="fas fa-certificate"></i> <span>دورات</span></a></li>
            <li><a href="#contact"><i class="fas fa-envelope"></i> <span>التواصل</span></a></li>
        </ul>
    </nav>
    
    <footer>
        <div class="container">
            <p>جميع الحقوق محفوظة &copy; 2023 | رؤية 2030</p>
        </div>
    </footer>
    
    <script>
        // كود JavaScript للتحكم في التنقل النشط
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.sidebar a, .bottom-nav a');
            
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    // إزالة النشط من جميع الروابط
                    navLinks.forEach(l => l.classList.remove('active'));
                    // إضافة النشط للرابط المحدد
                    this.classList.add('active');
                    
                    // إغلاق القائمة الجانبية على الأجهزة المحمولة (إذا كانت مفتوحة)
                    if (window.innerWidth <= 768) {
                        const sidebar = document.querySelector('.sidebar');
                        if (sidebar) sidebar.style.display = 'none';
                    }
                });
            });
            
            // كشف القسم النشط أثناء التمرير
            window.addEventListener('scroll', function() {
                const sections = document.querySelectorAll('.section');
                const navLinks = document.querySelectorAll('.sidebar a, .bottom-nav a');
                
                let current = '';
                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    const sectionHeight = section.clientHeight;
                    if (scrollY >= (sectionTop - 200)) {
                        current = section.getAttribute('id');
                    }
                });
                
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === `#${current}`) {
                        link.classList.add('active');
                    }
                });
            });
        });
    </script>
</body>
</html>
