            box-shadow: var(--shadow);
            padding: 30px;
            overflow: hidden;
        }
        <د
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
            --accent: #e53e3e;
            --light: #f7fafc;
            --dark: #2d3748;
            --success: #38a169;
            --nav-bg: #1a202c;
            --nav-text: #f7fafc;
            --nav-hover: #2d3748;
            --text-light: #f7fafc;
            --text-dark: #2d3748;
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
            line-height: 1.8;
            font-size: 1.4rem;
            padding-bottom: 80px; /* مساحة لشريط التنقل في الأسفل */
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Navigation - تصميم جديد */
        nav {
            background: var(--nav-bg);
            color: var(--nav-text);
            box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.2);
            position: fixed;
            bottom: 0;
            right: 0;
            left: 0;
            z-index: 100;
            padding: 0.5rem 0;
        }
        
        .nav-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            padding: 0;
        }
        
        .nav-link {
            padding: 0.8rem 1.2rem;
            text-decoration: none;
            color: var(--nav-text);
            font-weight: 500;
            transition: all 0.3s ease;
            border-radius: 8px;
            margin: 0.2rem;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            min-width: 80px;
        }
        
        .nav-link i {
            margin-bottom: 0.3rem;
            font-size: 1.2rem;
        }
        
        .nav-link:hover, .nav-link.active {
            background-color: var(--nav-hover);
            color: var(--accent);
        }
        
        /* Section Styles */
        section {
            padding: 3rem 0;
            display: none;
        }
        
        section.active {
            display: block;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary);
            position: relative;
            font-size: 2.8rem;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 120px;
            height: 6px;
            background: var(--accent);
            margin: 1rem auto;
            border-radius: 3px;
        }
        
        .card {
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 2.5rem;
            margin-bottom: 2.5rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .card h3 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            padding-bottom: 0.8rem;
            border-bottom: 3px solid #e2e8f0;
            font-size: 2.2rem;
        }
        
        /* About Section */
        .about-container {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
            align-items: center;
        }
        
        .profile-side {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .profile-img {
            width: 280px;
            height: 280px;
            border-radius: 50%;
            border: 6px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
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
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 0.8rem;
            font-weight: bold;
        }
        
        .profile-title {
            font-size: 1.8rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }
        
        .about-content {
            flex: 2;
            min-width: 300px;
        }
        
        .intro-text {
            font-size: 1.6rem;
            line-height: 1.9;
            margin-bottom: 2.5rem;
            text-align: justify;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 2.5rem;
        }
        
        .stat-item {
            text-align: center;
            padding: 2rem;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .stat-number {
            font-size: 3.5rem;
            font-weight: bold;
            color: var(--accent);
            display: block;
        }
        
        .stat-label {
            color: var(--secondary);
            font-weight: 500;
            font-size: 1.5rem;
        }
        
        /* Experience Section */
        .timeline {
            position: relative;
            max-width: 900px;
            margin: 0 auto;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            right: 50%;
            transform: translateX(50%);
            width: 6px;
            height: 100%;
            background: var(--accent);
        }
        
        .timeline-item {
            margin-bottom: 3.5rem;
            position: relative;
            width: 100%;
        }
        
        .timeline-item:nth-child(odd) .timeline-content {
            margin-right: calc(50% + 2.5rem);
            margin-left: 0;
        }
        
        .timeline-item:nth-child(even) .timeline-content {
            margin-left: calc(50% + 2.5rem);
            margin-right: 0;
        }
        
        .timeline-content {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
            font-size: 1.5rem;
        }
        
        .timeline-content::before {
            content: '';
            position: absolute;
            top: 2rem;
            width: 25px;
            height: 25px;
            background: var(--accent);
            border-radius: 50%;
        }
        
        .timeline-item:nth-child(odd) .timeline-content::before {
            left: -3.5rem;
        }
        
        .timeline-item:nth-child(even) .timeline-content::before {
            right: -3.5rem;
        }
        
        .timeline-date {
            color: var(--accent);
            font-weight: bold;
            margin-bottom: 0.8rem;
            font-size: 1.7rem;
        }
        
        .timeline-content h3 {
            font-size: 1.9rem;
            margin-bottom: 0.8rem;
        }
        
        .timeline-content p {
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }
        
        .timeline-content ul {
            padding-right: 1.5rem;
        }
        
        .timeline-content li {
            margin-bottom: 0.8rem;
            font-size: 1.5rem;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2.5rem;
        }
        
        .skill-category h3 {
            margin-bottom: 2rem;
            color: var(--primary);
            font-size: 2.2rem;
        }
        
        .skill-item {
            margin-bottom: 2rem;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.8rem;
            font-size: 1.6rem;
        }
        
        .skill-bar {
            height: 14px;
            background: #e2e8f0;
            border-radius: 7px;
            overflow: hidden;
        }
        
        .skill-level {
            height: 100%;
            background: var(--accent);
            border-radius: 7px;
        }
        
        /* Training Courses Section */
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .course-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border-left: 6px solid var(--accent);
        }
        
        .course-card h4 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.8rem;
        }
        
        .course-card p {
            color: var(--secondary);
            font-size: 1.5rem;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }
        
        .contact-icon {
            width: 70px;
            height: 70px;
            background: var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.8rem;
        }
        
        .contact-form {
            background: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-form h3 {
            font-size: 2.2rem;
            margin-bottom: 1.5rem;
        }
        
        .form-group {
            margin-bottom: 2rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.8rem;
            font-weight: 500;
            font-size: 1.6rem;
        }
        
        .form-control {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            font-size: 1.5rem;
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
            padding: 1.2rem 2.5rem;
            border: none;
            border-radius: 8px;
            font-size: 1.6rem;
            font-weight: 500;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        
        .btn:hover {
            background: #c53030;
        }
        
        /* Responsive - تحسينات جديدة */
        @media (max-width: 768px) {
            body {
                font-size: 1.2rem;
                padding-bottom: 70px;
            }
            
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
                flex-wrap: nowrap;
                overflow-x: auto;
                justify-content: flex-start;
                padding: 0 10px;
            }
            
            .nav-link {
                padding: 0.6rem 0.8rem;
                font-size: 0.9rem;
                min-width: 70px;
                flex-shrink: 0;
            }
            
            .nav-link span {
                font-size: 0.8rem;
            }
            
            .nav-link i {
                font-size: 1rem;
            }
            
            .profile-img {
                width: 220px;
                height: 220px;
            }
            
            .profile-name {
                font-size: 2rem;
            }
            
            .profile-title {
                font-size: 1.5rem;
            }
            
            .section-title {
                font-size: 2.2rem;
            }
            
            .intro-text {
                font-size: 1.3rem;
            }
        }
        
        /* تحسينات خاصة للعرض الأفقي على الجوال */
        @media (max-width: 768px) and (orientation: landscape) {
            .profile-img {
                width: 180px;
                height: 180px;
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
                font-size: 1.6rem;
            }
            
            .profile-title {
                font-size: 1.3rem;
            }
            
            .nav-container {
                justify-content: center;
            }
        }
        
        /* تحسينات للشاشات الصغيرة جداً */
        @media (max-width: 480px) {
            body {
                font-size: 1.1rem;
                padding-bottom: 60px;
            }
            
            .profile-img {
                width: 200px;
                height: 200px;
            }
            
            .profile-name {
                font-size: 1.8rem;
            }
            
            .nav-link {
                padding: 0.5rem 0.6rem;
                font-size: 0.8rem;
                min-width: 60px;
            }
            
            .nav-link span {
                font-size: 0.7rem;
            }
            
            .nav-link i {
                font-size: 0.9rem;
            }
            
            .card {
                padding: 1.8rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
        }
        
        /* تحسينات للعرض الأفقي على الجوال في الشاشات الصغيرة */
        @media (max-width: 480px) and (orientation: landscape) {
            .profile-img {
                width: 150px;
                height: 150px;
            }
            
            .profile-name {
                font-size: 1.5rem;
            }
            
            .about-container {
                gap: 1rem;
            }
        }
        
        /* شريط التنقل في الشاشات الكبيرة */
        @media (min-width: 1024px) {
            body {
                padding-bottom: 0;
                padding-top: 80px;
            }
            
            nav {
                top: 0;
                bottom: auto;
                box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            }
            
            .nav-container {
                flex-wrap: nowrap;
                justify-content: center;
            }
            
            .nav-link {
                flex-direction: row;
                min-width: auto;
                padding: 1rem 1.5rem;
                font-size: 1.3rem;
            }
            
            .nav-link i {
                margin-bottom: 0;
                margin-left: 0.5rem;
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
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

    <!-- Navigation - تم نقله للأسفل -->
    <nav>
        <div class="container nav-container">
            <a href="#about" class="nav-link active" data-section="about">
                <i class="fas fa-user"></i>
                <span>نبذة عني</span>
            </a>
            <a href="#experience" class="nav-link" data-section="experience">
                <i class="fas fa-briefcase"></i>
                <span>خبراتي</span>
            </a>
            <a href="#skills" class="nav-link" data-section="skills">
                <i class="fas fa-chart-bar"></i>
                <span>مهاراتي</span>
            </a>
            <a href="#training" class="nav-link" data-section="training">
                <i class="fas fa-graduation-cap"></i>
                <span>الدورات</span>
            </a>
            <a href="#portfolio" class="nav-link" data-section="portfolio">
                <i class="fas fa-folder"></i>
                <span>ملفي المهني</span>
            </a>
            <a href="#contact" class="nav-link" data-section="contact">
                <i class="fas fa-envelope"></i>
                <span>اتصل بي</span>
            </a>
        </div>
    </nav>

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
