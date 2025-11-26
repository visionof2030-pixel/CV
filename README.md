            position: sticky;
            top: 0;
            z-index: 100;
     <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ملفي المهني - فهد نغيمش الخالدي</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #2d3748;
            --accent: #3182ce;
            --light: #f7fafc;
            --dark: #2d3748;
            --success: #38a169;
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
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,186.7C384,213,480,235,576,213.3C672,192,768,128,864,128C960,128,1056,192,1152,192C1248,192,1344,128,1392,96L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            background-position: center;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
        }
        
        .title {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 1rem;
            position: relative;
            z-index: 1;
        }
        
        .tagline {
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }
        
        /* Navigation */
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-container {
            display: flex;
            justify-content: center;
            padding: 0;
        }
        
        .nav-link {
            padding: 1rem 1.5rem;
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }
        
        .nav-link:hover, .nav-link.active {
            color: var(--accent);
            border-bottom: 3px solid var(--accent);
        }
        
        /* Section Styles */
        section {
            padding: 4rem 0;
            display: none;
        }
        
        section.active {
            display: block;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 2.5rem;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--accent);
            margin: 0.5rem auto;
            border-radius: 2px;
        }
        
        .card {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 2rem;
            margin-bottom: 2rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #e2e8f0;
        }
        
        /* About Section */
        .about-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            align-items: center;
        }
        
        .profile-side {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .profile-img {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 1.5rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
        }
        
        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
        }
        
        .profile-name {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .profile-title {
            font-size: 1.2rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        .about-content {
            flex: 2;
            min-width: 300px;
        }
        
        .intro-text {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 2rem;
            text-align: justify;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .stat-item {
            text-align: center;
            padding: 1.5rem;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--accent);
            display: block;
        }
        
        .stat-label {
            color: var(--secondary);
            font-weight: 500;
        }
        
        /* Experience Section */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            right: 50%;
            transform: translateX(50%);
            width: 4px;
            height: 100%;
            background: var(--accent);
        }
        
        .timeline-item {
            margin-bottom: 3rem;
            position: relative;
            width: 100%;
        }
        
        .timeline-item:nth-child(odd) .timeline-content {
            margin-right: calc(50% + 2rem);
            margin-left: 0;
        }
        
        .timeline-item:nth-child(even) .timeline-content {
            margin-left: calc(50% + 2rem);
            margin-right: 0;
        }
        
        .timeline-content {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
        }
        
        .timeline-content::before {
            content: '';
            position: absolute;
            top: 1.5rem;
            width: 20px;
            height: 20px;
            background: var(--accent);
            border-radius: 50%;
        }
        
        .timeline-item:nth-child(odd) .timeline-content::before {
            left: -3rem;
        }
        
        .timeline-item:nth-child(even) .timeline-content::before {
            right: -3rem;
        }
        
        .timeline-date {
            color: var(--accent);
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .skill-category h3 {
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .skill-item {
            margin-bottom: 1.5rem;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }
        
        .skill-bar {
            height: 10px;
            background: #e2e8f0;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .skill-level {
            height: 100%;
            background: var(--accent);
            border-radius: 5px;
        }
        
        /* Training Courses Section */
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .course-card {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border-left: 4px solid var(--accent);
        }
        
        .course-card h4 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .course-card p {
            color: var(--secondary);
            font-size: 0.9rem;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #e2e8f0;
            border-radius: 5px;
            font-size: 1rem;
            transition: border 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent);
        }
        
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        
        .btn:hover {
            background: var(--primary);
        }
        
        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: background 0.3s ease;
        }
        
        .social-link:hover {
            background: var(--accent);
        }
        
        /* Portfolio Items */
        .goals-list .goal-item,
        .success-steps .step {
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #e2e8f0;
        }
        
        .goals-list .goal-item:last-child,
        .success-steps .step:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .timeline::before {
                right: 2rem;
            }
            
            .timeline-item:nth-child(odd) .timeline-content,
            .timeline-item:nth-child(even) .timeline-content {
                margin-right: 4rem;
                margin-left: 0;
            }
            
            .timeline-content::before {
                right: -3rem;
                left: auto;
            }
            
            .nav-container {
                flex-wrap: wrap;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .profile-img {
                width: 200px;
                height: 200px;
            }
            
            .profile-name {
                font-size: 1.5rem;
            }
        }
        
        /* تحسينات خاصة للعرض الأفقي على الجوال */
        @media (max-width: 768px) and (orientation: landscape) {
            .profile-img {
                width: 150px;
                height: 150px;
            }
            
            .about-container {
                flex-direction: row;
                align-items: flex-start;
            }
            
            .profile-side {
                flex: 0 0 auto;
                margin-left: 1rem;
            }
            
            .profile-name {
                font-size: 1.3rem;
            }
            
            .profile-title {
                font-size: 1rem;
            }
        }
        
        /* تحسينات للشاشات الصغيرة جداً */
        @media (max-width: 480px) {
            .profile-img {
                width: 180px;
                height: 180px;
            }
            
            .profile-name {
                font-size: 1.4rem;
            }
            
            .nav-link {
                padding: 0.8rem 1rem;
                font-size: 0.9rem;
            }
            
            .card {
                padding: 1.5rem;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
        
        /* تحسينات للعرض الأفقي على الجوال في الشاشات الصغيرة */
        @media (max-width: 480px) and (orientation: landscape) {
            .profile-img {
                width: 120px;
                height: 120px;
            }
            
            .profile-name {
                font-size: 1.2rem;
            }
            
            .about-container {
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container header-content">
            <h1>ملفي المهني</h1>
            <div class="title">سيرة ذاتية تفاعلية</div>
            <div class="tagline">عرض شامل لخبراتي وإنجازاتي في مجال التعليم</div>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <div class="container nav-container">
            <a href="#about" class="nav-link active" data-section="about">نبذة عني</a>
            <a href="#experience" class="nav-link" data-section="experience">خبراتي</a>
            <a href="#skills" class="nav-link" data-section="skills">مهاراتي</a>
            <a href="#training" class="nav-link" data-section="training">الدورات التدريبية</a>
            <a href="#portfolio" class="nav-link" data-section="portfolio">ملفي المهني</a>
            <a href="#contact" class="nav-link" data-section="contact">اتصل بي</a>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="container">
        <!-- About Section -->
        <section id="about" class="active">
            <h2 class="section-title">نبذة عني</h2>
            <div class="card">
                <div class="about-container">
                    <div class="profile-side">
                        <div class="profile-img">
                            <!-- تم إضافة صورتك الشخصية هنا -->
                            <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg" alt="فهد نغيمش الخالدي">
                        </div>
                        <div class="profile-name">فهد نغيمش حميد الخالدي</div>
                        <div class="profile-title">معلم متقدم - تخصص اللغة الإنجليزية</div>
                    </div>
                    <div class="about-content">
                        <div class="intro-text">
                            <p>أنا معلم لغة إنجليزية متمرس بخبرة تمتد لأكثر من 14 عامًا في التعليم العام، تمت ترقيتي إلى معلم متقدم عام 2022 تقديرًا لتميزي في الأداء وتطوير الممارسات التعليمية. أومن بأن التعليم عملية متجددة، وأسعى باستمرار إلى التطور المهني واكتساب مهارات جديدة تعزز جودة مخرجات التعلم.</p>
                            <p>أمتلك شغفًا كبيرًا بتعلم اللغات والترجمة، وأسعى لتوسيع خبرتي الأكاديمية من خلال دراسة اللغة الصينية ضمن برنامج الانبعاث الخاص بوزارة التعليم لشاغلي الوظائف التعليمية، بما يدعم قدرتي على التعليم في بيئات متعددة الثقافات.</p>
                            <p>أتطلع دائمًا إلى أن أكون معلمًا متميزًا يغرس في طلابه القيم الجميلة والأخلاق الفاضلة، إلى جانب تقديم المعرفة المفيدة التي تتماشى مع رؤية المملكة العربية السعودية 2030.</p>
                        </div>
                        
                        <div class="stats">
                            <div class="stat-item">
                                <span class="stat-number">14+</span>
                                <span class="stat-label">سنوات خبرة</span>
                            </div>
                            <div class="stat-item">
                                <span class="stat-number">150+</span>
                                <span class="stat-label">ساعة تدريبية</span>
                            </div>
                            <div class="stat-item">
                                <span class="stat-number">100+</span>
                                <span class="stat-label">ساعة تطوعية</span>
                            </div>
                            <div class="stat-item">
                                <span class="stat-number">3</span>
                                <span class="stat-label">مدن عمل</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience Section -->
        <section id="experience">
            <h2 class="section-title">خبراتي المهنية</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2017 - الآن</div>
                        <h3>معلم لغة إنجليزية - سعيد بن العاص المتوسطة</h3>
                        <p>مكة المكرمة - إدارة تعليم مكة</p>
                        <ul>
                            <li>تطبيق استراتيجيات تدريس حديثة لدمج التفكير النقدي والإبداعي</li>
                            <li>تحليل أداء الطلاب وتقديم تغذية راجعة بناءة لتحسين نواحي التعلم</li>
                            <li>بناء بيئة صفية محفزة تشجع على التعلم الذاتي والتفاعلي</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2014 - 2016</div>
                        <h3>معلم لغة إنجليزية - الأمير سعود بن عبدالمحسن</h3>
                        <p>الليث - إدارة تعليم الليث</p>
                        <ul>
                            <li>تدريس مهارات اللغة الإنجليزية بطرائق مبتكرة</li>
                            <li>الإسهام في تطوير البرامج التربوية والأنشطة التعليمية</li>
                            <li>تعزيز الدافعية الذاتية لدى الطلاب وتفعيل التعليم التعاوني</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2012 - 2014</div>
                        <h3>معلم لغة إنجليزية - سعيد بن زيد</h3>
                        <p>عفيف - إدارة تعليم عفيف</p>
                        <ul>
                            <li>تدريس اللغة الإنجليزية للمراحل التعليمية المختلفة</li>
                            <li>المشاركة في الأنشطة المدرسية والبرامج التطويرية</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2011 - 2012</div>
                        <h3>مترجم - وزارة الحج والعمرة</h3>
                        <p>مكة المكرمة</p>
                        <ul>
                            <li>تقديم خدمات الترجمة للحجاج والمعتمرين</li>
                            <li>التواصل مع الجاليات المختلفة بلغات متعددة</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- باقي الأقسام تبقى كما هي -->
        <!-- ... -->
        
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>فهد نغيمش حميد الخالدي - معلم متقدم لغة إنجليزية</p>
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                <a href="mailto:iFahadenglish@gmail.com" class="social-link"><i class="fas fa-envelope"></i></a>
            </div>
            <p>جميع الحقوق محفوظة &copy; 2023</p>
        </div>
    </footer>

    <script>
        // Navigation functionality
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Remove active class from all links and sections
                document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
                
                // Add active class to clicked link and corresponding section
                this.classList.add('active');
                const sectionId = this.getAttribute('data-section');
                document.getElementById(sectionId).classList.add('active');
                
                // Scroll to top of section
                document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
            });
        });
        
        // Simple animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        // Observe cards for animation
        document.querySelectorAll('.card, .timeline-content, .stat-item, .course-card').forEach(el => {
            el.style.opacity = 0;
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>   }
        
        .nav-container {
            display: flex;
            justify-content: center;
            padding: 0;
        }
        
        .nav-link {
            padding: 1rem 1.5rem;
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }
        
        .nav-link:hover, .nav-link.active {
            color: var(--accent);
            border-bottom: 3px solid var(--accent);
        }
        
        /* Section Styles */
        section {
            padding: 4rem 0;
            display: none;
        }
        
        section.active {
            display: block;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 2.5rem;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--accent);
            margin: 0.5rem auto;
            border-radius: 2px;
        }
        
        .card {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 2rem;
            margin-bottom: 2rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #e2e8f0;
        }
        
        /* About Section */
        .intro-text {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 2rem;
            text-align: justify;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .stat-item {
            text-align: center;
            padding: 1.5rem;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--accent);
            display: block;
        }
        
        .stat-label {
            color: var(--secondary);
            font-weight: 500;
        }
        
        /* Experience Section */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            right: 50%;
            transform: translateX(50%);
            width: 4px;
            height: 100%;
            background: var(--accent);
        }
        
        .timeline-item {
            margin-bottom: 3rem;
            position: relative;
            width: 100%;
        }
        
        .timeline-item:nth-child(odd) .timeline-content {
            margin-right: calc(50% + 2rem);
            margin-left: 0;
        }
        
        .timeline-item:nth-child(even) .timeline-content {
            margin-left: calc(50% + 2rem);
            margin-right: 0;
        }
        
        .timeline-content {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
        }
        
        .timeline-content::before {
            content: '';
            position: absolute;
            top: 1.5rem;
            width: 20px;
            height: 20px;
            background: var(--accent);
            border-radius: 50%;
        }
        
        .timeline-item:nth-child(odd) .timeline-content::before {
            left: -3rem;
        }
        
        .timeline-item:nth-child(even) .timeline-content::before {
            right: -3rem;
        }
        
        .timeline-date {
            color: var(--accent);
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .skill-category h3 {
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .skill-item {
            margin-bottom: 1.5rem;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }
        
        .skill-bar {
            height: 10px;
            background: #e2e8f0;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .skill-level {
            height: 100%;
            background: var(--accent);
            border-radius: 5px;
        }
        
        /* Training Courses Section */
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .course-card {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border-left: 4px solid var(--accent);
        }
        
        .course-card h4 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .course-card p {
            color: var(--secondary);
            font-size: 0.9rem;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #e2e8f0;
            border-radius: 5px;
            font-size: 1rem;
            transition: border 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent);
        }
        
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        
        .btn:hover {
            background: var(--primary);
        }
        
        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: background 0.3s ease;
        }
        
        .social-link:hover {
            background: var(--accent);
        }
        
        /* Portfolio Items */
        .goals-list .goal-item,
        .success-steps .step {
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #e2e8f0;
        }
        
        .goals-list .goal-item:last-child,
        .success-steps .step:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .timeline::before {
                right: 2rem;
            }
            
            .timeline-item:nth-child(odd) .timeline-content,
            .timeline-item:nth-child(even) .timeline-content {
                margin-right: 4rem;
                margin-left: 0;
            }
            
            .timeline-content::before {
                right: -3rem;
                left: auto;
            }
            
            .nav-container {
                flex-wrap: wrap;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .profile-img {
                width: 150px;
                height: 150px;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container profile-container">
            <div class="profile-img">
                <!-- تم إضافة صورتك الشخصية هنا -->
                <img src="https://i.ibb.co/k66psVmZ/20220817-151032.jpg" alt="فهد نغيمش الخالدي">
            </div>
            <h1>فهد نغيمش حميد الخالدي</h1>
            <div class="title">معلم متقدم - تخصص اللغة الإنجليزية</div>
            <div class="tagline">معلم متمرس بخبرة 14 سنة في التعليم، ملتزم بتطوير الممارسات التعليمية وغرس القيم الجميلة في الطلاب</div>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <div class="container nav-container">
            <a href="#about" class="nav-link active" data-section="about">نبذة عني</a>
            <a href="#experience" class="nav-link" data-section="experience">خبراتي</a>
            <a href="#skills" class="nav-link" data-section="skills">مهاراتي</a>
            <a href="#training" class="nav-link" data-section="training">الدورات التدريبية</a>
            <a href="#portfolio" class="nav-link" data-section="portfolio">ملفي المهني</a>
            <a href="#contact" class="nav-link" data-section="contact">اتصل بي</a>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="container">
        <!-- About Section -->
        <section id="about" class="active">
            <h2 class="section-title">نبذة عني</h2>
            <div class="card">
                <div class="intro-text">
                    <p>أنا معلم لغة إنجليزية متمرس بخبرة تمتد لأكثر من 14 عامًا في التعليم العام، تمت ترقيتي إلى معلم متقدم عام 2022 تقديرًا لتميزي في الأداء وتطوير الممارسات التعليمية. أومن بأن التعليم عملية متجددة، وأسعى باستمرار إلى التطور المهني واكتساب مهارات جديدة تعزز جودة مخرجات التعلم.</p>
                    <p>أمتلك شغفًا كبيرًا بتعلم اللغات والترجمة، وأسعى لتوسيع خبرتي الأكاديمية من خلال دراسة اللغة الصينية ضمن برنامج الانبعاث الخاص بوزارة التعليم لشاغلي الوظائف التعليمية، بما يدعم قدرتي على التعليم في بيئات متعددة الثقافات.</p>
                    <p>أتطلع دائمًا إلى أن أكون معلمًا متميزًا يغرس في طلابه القيم الجميلة والأخلاق الفاضلة، إلى جانب تقديم المعرفة المفيدة التي تتماشى مع رؤية المملكة العربية السعودية 2030.</p>
                </div>
                
                <div class="stats">
                    <div class="stat-item">
                        <span class="stat-number">14+</span>
                        <span class="stat-label">سنوات خبرة</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">150+</span>
                        <span class="stat-label">ساعة تدريبية</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">100+</span>
                        <span class="stat-label">ساعة تطوعية</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">3</span>
                        <span class="stat-label">مدن عمل</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience Section -->
        <section id="experience">
            <h2 class="section-title">خبراتي المهنية</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2017 - الآن</div>
                        <h3>معلم لغة إنجليزية - سعيد بن العاص المتوسطة</h3>
                        <p>مكة المكرمة - إدارة تعليم مكة</p>
                        <ul>
                            <li>تطبيق استراتيجيات تدريس حديثة لدمج التفكير النقدي والإبداعي</li>
                            <li>تحليل أداء الطلاب وتقديم تغذية راجعة بناءة لتحسين نواحي التعلم</li>
                            <li>بناء بيئة صفية محفزة تشجع على التعلم الذاتي والتفاعلي</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2014 - 2016</div>
                        <h3>معلم لغة إنجليزية - الأمير سعود بن عبدالمحسن</h3>
                        <p>الليث - إدارة تعليم الليث</p>
                        <ul>
                            <li>تدريس مهارات اللغة الإنجليزية بطرائق مبتكرة</li>
                            <li>الإسهام في تطوير البرامج التربوية والأنشطة التعليمية</li>
                            <li>تعزيز الدافعية الذاتية لدى الطلاب وتفعيل التعليم التعاوني</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2012 - 2014</div>
                        <h3>معلم لغة إنجليزية - سعيد بن زيد</h3>
                        <p>عفيف - إدارة تعليم عفيف</p>
                        <ul>
                            <li>تدريس اللغة الإنجليزية للمراحل التعليمية المختلفة</li>
                            <li>المشاركة في الأنشطة المدرسية والبرامج التطويرية</li>
                        </ul>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2011 - 2012</div>
                        <h3>مترجم - وزارة الحج والعمرة</h3>
                        <p>مكة المكرمة</p>
                        <ul>
                            <li>تقديم خدمات الترجمة للحجاج والمعتمرين</li>
                            <li>التواصل مع الجاليات المختلفة بلغات متعددة</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills">
            <h2 class="section-title">مهاراتي وقدراتي</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>المهارات التعليمية</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>تطوير وتنفيذ خطط التدريس</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 95%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>دمج التفكير النقدي والإبداعي</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 90%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>إدارة الصفوف بفاعلية</span>
                            <span>92%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 92%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>تشجيع التعلم الذاتي</span>
                            <span>88%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 88%"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>المهارات التقنية والشخصية</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>إتقان اللغة الإنجليزية</span>
                            <span>98%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 98%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>استخدام أدوات التقويم الإلكترونية</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 85%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>القدرة على التعليم في بيئات متعددة الثقافات</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 90%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>القيادة وحل المشكلات</span>
                            <span>87%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 87%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Training Courses Section -->
        <section id="training">
            <h2 class="section-title">الدورات التدريبية</h2>
            <div class="card">
                <h3>ملخص الدورات التدريبية</h3>
                <p>خلال مسيرتي المهنية، حضرت أكثر من <strong>150 ساعة تدريبية</strong> في مجالات متنوعة تهدف إلى تطوير الأداء التعليمي والمهني، ومن أبرز هذه الدورات:</p>
                
                <div class="courses-grid" style="margin-top: 2rem;">
                    <div class="course-card">
                        <h4>التفكير الناقد والإبداعي ودمجه في المواد الدراسية</h4>
                        <p>تطوير مهارات التفكير النقدي والإبداعي وتطبيقها في التدريس</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>القياس والتقويم التربوي</h4>
                        <p>أساليب القياس والتقويم الحديثة في العملية التعليمية</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>الاستراتيجية الحديثة في تدريس أساسيات اللغة الإنجليزية</h4>
                        <p>استراتيجيات تدريس اللغة الإنجليزية بطرق مبتكرة</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>البيئة الصفية الجاذبة</h4>
                        <p>تصميم بيئة صفية محفزة للتعلم والتعليم</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>تحليل أداء الطلاب وتقديم التغذية الراجعة</h4>
                        <p>تحليل أداء الطلاب وتقديم تغذية راجعة بناءة</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>أساسيات الترجمة</h4>
                        <p>مبادئ وأسس الترجمة بين اللغات المختلفة</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>مهارات التعامل مع أدوات القياس والتقويم الإلكترونية</h4>
                        <p>استخدام الأدوات الإلكترونية في القياس والتقويم</p>
                    </div>
                    
                    <div class="course-card">
                        <h4>التنمية المهنية لمعلمي اللغة الإنجليزية - المستوى الثالث</h4>
                        <p>برنامج متقدم للتنمية المهنية لمعلمي اللغة الإنجليزية</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Portfolio Section -->
        <section id="portfolio">
            <h2 class="section-title">ملفي المهني</h2>
            
            <div class="card">
                <h3>رؤيتي ورسالتي</h3>
                <p>أتطلع إلى أن أكون معلمًا متميزًا يغرس في طلابه القيم الجميلة والأخلاق الفاضلة، إلى جانب تقديم المعرفة المفيدة التي تتماشى مع رؤية المملكة العربية السعودية 2030.</p>
                <p>أؤمن بأن المعرفة هي أعلى هدف له تأثير كبير على المجتمع، لذا فإن السعي لتحقيق الخير المشترك واجب على كل فرد، بغض النظر عن الظروف. التأثير الذي تتركه المعرفة في نفس الفرد وعقله يجعل التضحية من أجلها أمرًا ممتعًا.</p>
            </div>
            
            <div class="card">
                <h3>أخلاقيات مهنة التدريس</h3>
                <p>ألتزم بأخلاقيات مهنة التدريس التي تؤكد على:</p>
                <ul>
                    <li>تقدير المهنة والسعي المستمر لتحسين المهارات والمعرفة</li>
                    <li>المساهمة في المكانة العلمية والاجتماعية للتدريس</li>
                    <li>الالتزام بقيم وأخلاق المهنة</li>
                    <li>التطوير المهني المستمر واكتساب المعارف والمهارات الجديدة</li>
                    <li>بناء علاقة قائمة على الحب والاحترام مع الطلاب</li>
                </ul>
            </div>
            
            <div class="card">
                <h3>أهدافي القادمة</h3>
                <div class="goals-list">
                    <div class="goal-item">
                        <h4>الاهتمام بالتفاصيل والنهج الإبداعي</h4>
                        <p>الاهتمام بالتفاصيل والنهج الإبداعي الذي أتبعه في الفصل الدراسي</p>
                    </div>
                    <div class="goal-item">
                        <h4>تطوير الحملات التعليمية</h4>
                        <p>محاولة جعل الحملات التعليمية على مستوى آخر بأفكار تأتي من الطلاب أنفسهم</p>
                    </div>
                    <div class="goal-item">
                        <h4>التطوير المستمر للاستراتيجيات</h4>
                        <p>البحث دائمًا عن الفهم التقني القوي من أجل تطوير استراتيجيات ناجحة</p>
                    </div>
                    <div class="goal-item">
                        <h4>ابتكار أساليب تعليمية بسيطة</h4>
                        <p>إنشاء محتوى متميز مع الانخراط لاكتشاف طرق بسيطة لنقل المعرفة من ثقافة أخرى</p>
                    </div>
                </div>
            </div>
            
            <div class="card">
                <h3>كيف أحقق النجاح؟</h3>
                <div class="success-steps">
                    <div class="step">
                        <h4>الخطوة 1: تحديد الأهداف</h4>
                        <p>وضع أهداف واضحة وقابلة للقياس</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 2: البحث والتحضير</h4>
                        <p>البحث والتحضير الشامل قبل البدء في التنفيذ</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 3: تطوير الاستراتيجيات</h4>
                        <p>وضع استراتيجيات فعالة لتحقيق الأهداف</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 4: خطط العمل</h4>
                        <p>تحويل الاستراتيجيات إلى خطط عمل تنفيذية</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 5: قياس التقدم</h4>
                        <p>مراقبة وقياس التقدم بشكل منتظم</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 6: التحسين المستمر</h4>
                        <p>التطوير والتحسين المستمر للأداء</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 7: تحليل النتائج</h4>
                        <p>تحليل النتائج وتقييم الأداء</p>
                    </div>
                    <div class="step">
                        <h4>الخطوة 8: التركيز على المستقبل</h4>
                        <p>التخطيط للمستقبل ووضع أهداف جديدة</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h2 class="section-title">اتصل بي</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">✉️</div>
                        <div>
                            <h3>البريد الإلكتروني</h3>
                            <p>iFahadenglish@gmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">📱</div>
                        <div>
                            <h3>رقم الهاتف</h3>
                            <p>+966554449824</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div>
                            <h3>موقع العمل</h3>
                            <p>مدرسة سعيد بن العاص المتوسطة - مكة المكرمة</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">💼</div>
                        <div>
                            <h3>الوظيفة الحالية</h3>
                            <p>معلم متقدم - تخصص اللغة الإنجليزية</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>أرسل لي رسالة</h3>
                    <form id="messageForm">
                        <div class="form-group">
                            <label for="name">الاسم</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">البريد الإلكتروني</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="subject">الموضوع</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">الرسالة</label>
                            <textarea id="message" rows="5" class="form-control" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn">إرسال الرسالة</button>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>فهد نغيمش حميد الخالدي - معلم متقدم لغة إنجليزية</p>
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                <a href="mailto:iFahadenglish@gmail.com" class="social-link"><i class="fas fa-envelope"></i></a>
            </div>
            <p>جميع الحقوق محفوظة &copy; 2023</p>
        </div>
    </footer>

    <script>
        // Navigation functionality
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Remove active class from all links and sections
                document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
                
                // Add active class to clicked link and corresponding section
                this.classList.add('active');
                const sectionId = this.getAttribute('data-section');
                document.getElementById(sectionId).classList.add('active');
                
                // Scroll to top of section
                document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
            });
        });
        
        // Form submission
        document.getElementById('messageForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('شكرًا لك على رسالتك! سأتواصل معك قريبًا.');
            this.reset();
        });
        
        // Simple animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        // Observe cards for animation
        document.querySelectorAll('.card, .timeline-content, .stat-item, .course-card').forEach(el => {
            el.style.opacity = 0;
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
