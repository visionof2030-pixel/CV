<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الملف المهني | فهد الخالدي</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a365d;
            --primary-light: #2d4a80;
            --accent: #2563eb;
            --accent-light: #3b82f6;
            --bg: #f8fafc;
            --bg-gradient: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            --card-bg: #ffffff;
            --text: #1e293b;
            --light-text: #64748b;
            --shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
            --shadow-hover: 0 15px 35px rgba(0, 0, 0, 0.12);
            --border-radius: 20px;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            box-sizing: border-box;
            font-family: 'Tajawal', Tahoma, Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        body {
            background: var(--bg-gradient);
            color: var(--text);
            line-height: 1.7;
            overflow-x: hidden;
            padding-right: 90px;
            transition: padding 0.3s ease;
            font-weight: 700; /* جعل النص عريضًا */
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), #020617);
            color: #fff;
            text-align: center;
            padding: 18px;
            position: relative;
            z-index: 1000;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        #pageTitle {
            font-size: 1.5rem;
            background: rgba(255, 255, 255, 0.15);
            padding: 10px 25px;
            border-radius: 999px;
            display: inline-block;
            font-weight: 800;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Language Button */
        .lang-btn {
            position: fixed;
            top: 15px;
            left: 15px;
            background: rgba(255, 255, 255, 0.9);
            color: var(--accent);
            border: none;
            padding: 10px 18px;
            border-radius: 12px;
            font-weight: bold;
            cursor: pointer;
            z-index: 3000;
            transition: var(--transition);
            font-family: 'Tajawal', sans-serif;
            box-shadow: var(--shadow);
            backdrop-filter: blur(10px);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .lang-btn:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow-hover);
            background: white;
        }

        /* Sidebar Navigation */
        nav {
            position: fixed;
            right: 0;
            top: 0;
            width: 90px;
            height: 100vh;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(15px);
            z-index: 2000;
            transition: var(--transition);
            overflow-y: auto;
            overflow-x: hidden;
            box-shadow: -5px 0 15px rgba(0, 0, 0, 0.05);
            border-left: 1px solid rgba(0, 0, 0, 0.05);
        }

        .nav-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 100px;
            padding-bottom: 30px;
            gap: 16px;
        }

        .nav-link {
            width: 65px;
            height: 65px;
            text-align: center;
            text-decoration: none;
            color: var(--accent);
            border-radius: 18px;
            font-size: 11px;
            font-weight: bold;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: var(--transition);
            position: relative;
            background: rgba(255, 255, 255, 0.7);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
        }

        .nav-link svg {
            width: 22px;
            height: 22px;
            fill: currentColor;
            margin-bottom: 5px;
        }

        .nav-link.active,
        .nav-link:hover {
            background: var(--accent);
            color: white;
            transform: translateX(-3px);
            box-shadow: 0 8px 15px rgba(37, 99, 235, 0.3);
        }

        .nav-link::after {
            content: "";
            position: absolute;
            left: -10px;
            top: 50%;
            transform: translateY(-50%);
            width: 5px;
            height: 0;
            background: var(--accent);
            border-radius: 3px;
            transition: var(--transition);
        }

        .nav-link.active::after {
            height: 35px;
        }

        /* Main Content */
        main {
            max-width: 4000px;
            margin: 25px auto;
            padding: 9px;
        }

        section {
            display: none;
            animation: fadeInUp 0.6s ease forwards;
            opacity: 0;
            transform: translateY(20px);
        }

        section.active {
            display: block;
        }

        .section-title {
            text-align: center;
            color: var(--primary);
            margin-bottom: 35px;
            font-size: 2.2rem;
            font-weight: 800;
            position: relative;
            padding-bottom: 15px;
        }

        .section-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            right: 50%;
            transform: translateX(50%);
            width: 100px;
            height: 5px;
            background: linear-gradient(to right, var(--accent), var(--primary));
            border-radius: 3px;
        }

        /* Cards */
        .card {
            background: var(--card-bg);
            border-radius: var(--border-radius);
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to left, var(--accent), var(--primary));
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: var(--shadow-hover);
        }

        /* Profile Section */
        .profile-img {
            width: 170px;
            height: 170px;
            margin: 20px auto;
            border-radius: 50%;
            overflow: hidden;
            border: 5px solid var(--accent);
            box-shadow: 0 10px 25px rgba(37, 99, 235, 0.25);
            position: relative;
            transition: var(--transition);
        }

        .profile-img:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(37, 99, 235, 0.35);
        }

        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .bio {
            text-align: justify;
            font-size: 0.80rem;
            line-height: 1.9;
            color: var(--text);
            margin: 20px 0;
            padding: 0 10px;
            font-weight: 700; /* جعل النص عريضًا */
        }

        .badge {
            margin: 20px auto;
            text-align: center;
            background: linear-gradient(135deg, #16a34a, #059669);
            color: white;
            padding: 10px 25px;
            border-radius: 999px;
            font-size: 0.80rem;
            display: inline-flex;
            gap: 10px;
            align-items: center;
            font-weight: 700;
            box-shadow: 0 6px 15px rgba(22, 163, 74, 0.35);
            transition: var(--transition);
        }

        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(22, 163, 74, 0.4);
        }

        /* Stats */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 25px;
        }

        .stat {
            background: linear-gradient(135deg, #f8fafc, #f1f5f9);
            padding: 20px;
            border-radius: 16px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid #e2e8f0;
            position: relative;
            overflow: hidden;
        }

        .stat::before {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 4px;
            background: var(--accent);
        }

        .stat:hover {
            background: #f1f5f9;
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .stat .num {
            color: var(--accent);
            font-weight: 800;
            font-size: 1.8rem;
            margin-bottom: 8px;
        }

        .stat span {
            font-weight: 700;
            color: var(--light-text);
            font-size: 0.80rem;
        }

        /* Timeline */
        .timeline {
            display: flex;
            flex-direction: column-reverse;
            position: relative;
            padding-right: 35px;
            gap: 22px;
        }

        .timeline::before {
            content: "";
            position: absolute;
            right: 18px;
            top: 0;
            bottom: 0;
            width: 5px;
            background: linear-gradient(to bottom, var(--accent), var(--primary));
            border-radius: 5px;
        }

        .timeline-item {
            background: white;
            border-radius: 18px;
            padding: 22px;
            margin-right: 40px;
            box-shadow: var(--shadow);
            position: relative;
            transition: var(--transition);
            border-right: 4px solid var(--accent);
        }

        .timeline-item:hover {
            transform: translateX(-5px);
            box-shadow: var(--shadow-hover);
        }

        .timeline-item::after {
            content: "";
            position: absolute;
            right: -38px;
            top: 25px;
            width: 20px;
            height: 20px;
            background: var(--accent);
            border-radius: 50%;
            box-shadow: 0 0 0 5px rgba(37, 99, 235, 0.25);
        }

        .timeline-date {
            color: var(--accent);
            font-weight: 700;
            font-size: 0.80rem;
            margin-bottom: 10px;
        }

        .timeline-item div {
            font-weight: 700;
            margin-bottom: 8px;
            color: var(--text);
            font-size: 0.80rem;
        }

        .timeline-item div:last-child {
            color: var(--light-text);
            font-weight: 700;
            font-size: 0.80rem;
        }

        /* Achievement Cards */
        .achievement-card {
            background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
            border-right: 5px solid var(--accent);
            padding: 30px;
            border-radius: var(--border-radius);
            margin-bottom: 25px;
            position: relative;
            overflow: hidden;
            box-shadow: var(--shadow);
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
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: 700;
            display: inline-block;
            margin-bottom: 18px;
            font-size: 0.80rem;
            box-shadow: 0 4px 10px rgba(37, 99, 235, 0.3);
        }

        .achievement-content {
            position: relative;
            z-index: 1;
        }

        .achievement-content p {
            line-height: 1.9;
            text-align: justify;
            font-size: 0.80rem;
            color: var(--text);
            margin: 0;
            font-weight: 700; /* جعل النص عريضًا */
        }

        /* Skills & Training Lists */
        .skills-card, .training-card, .tech-card, .contact-card {
            background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
            border-right: 5px solid var(--accent);
            padding: 30px;
            border-radius: var(--border-radius);
            margin-bottom: 25px;
            box-shadow: var(--shadow);
        }

        .contact-card {
            text-align: center;
        }

        ul {
            padding-right: 25px;
            margin: 0;
        }

        li {
            margin-bottom: 15px;
            line-height: 1.8;
            position: relative;
            padding-right: 20px;
            font-size: 0.80rem;
            transition: var(--transition);
            font-weight: 700; /* جعل النص عريضًا */
        }

        li:hover {
            transform: translateX(-5px);
        }

        li::before {
            content: "•";
            color: var(--accent);
            font-weight: bold;
            position: absolute;
            right: 0;
            font-size: 1.5rem;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            text-align: center;
            padding: 25px;
            margin-top: 50px;
            border-radius: var(--border-radius);
            font-weight: 700;
            font-size: 0.80rem;
            box-shadow: var(--shadow);
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
            100% {
                transform: scale(1);
            }
        }

        .pulse {
            animation: pulse 2s infinite;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            body {
                padding-right: 0;
            }
            
            nav {
                width: 70px;
            }
            
            .nav-link {
                width: 55px;
                height: 55px;
                font-size: 10px;
            }
            
            .nav-link svg {
                width: 18px;
                height: 18px;
            }
            
            .lang-btn {
                top: 10px;
                left: 10px;
                padding: 8px 15px;
                font-size: 0.85rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .card {
                padding: 25px;
            }
            
            .profile-img {
                width: 140px;
                height: 140px;
            }
            
            .nav-link::after {
                left: -8px;
                width: 4px;
            }
            
            .nav-link.active::after {
                height: 30px;
            }
            
            main {
                padding: 15px;
            }
        }

        /* Scrollbar Styling */
        nav::-webkit-scrollbar {
            width: 5px;
        }

        nav::-webkit-scrollbar-track {
            background: #f1f1f1;
        }

        nav::-webkit-scrollbar-thumb {
            background: var(--accent);
            border-radius: 5px;
        }

        nav::-webkit-scrollbar-thumb:hover {
            background: #1d4ed8;
        }

        /* Particles Background */
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
        }

        /* تعديلات إضافية للنصوص */
        h3#name {
            font-size: 1rem;
            margin-bottom: 10px;
            color: var(--primary);
            font-weight: 700;
        }

        p#jobTitle {
            font-size: 0.80rem;
            margin-bottom: 20px;
            font-weight: 700;
        }

        p#contactText {
            font-size: 0.80rem;
            line-height: 1.9;
            margin: 0;
            font-weight: 700;
        }

        p#techText {
            line-height: 1.9;
            text-align: justify;
            margin: 0;
            font-size: 0.80rem;
            font-weight: 700;
        }
    </style>
</head>

<body>
    <!-- Particles Background -->
    <div id="particles-js"></div>

    <button class="lang-btn" id="langBtn">
        <i class="fas fa-language"></i> EN
    </button>

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

                <h3 id="name">فهد نغيمش حميد الخالدي</h3>
                <p id="jobTitle"><b>معلم متقدم – تخصص اللغة الإنجليزية</b></p>

                <p class="bio" id="bioText">
                    أؤمن أن التعليم ليس مجرد نقل معرفة، بل رسالة سامية لصناعة الأثر وبناء الإنسان. أطمح إلى أن أكون جزءًا فاعلًا في تطوير التعليم بالمملكة من خلال توظيف التقنيات الحديثة، وصناعة بيئات تعلم محفزة، تعزز التفكير النقدي والإبداعي، وتبني الثقة لدى الطالب. نظرتي المستقبلية تقوم على التعلم المستمر، وتطوير المهارات المهنية، ومواكبة التحولات الرقمية بما يخدم مخرجات التعليم وجودته في إطار رؤية المملكة 2030.
                </p>

                <div class="badge pulse" id="badge">🏆 حاصل على درجة 95 في التخصص</div>

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
                <p id="techText">
                    أتمتع بشغف كبير تجاه التقنية والتعليم الرقمي، وأواكب أحدث التطورات في مجال الذكاء الاصطناعي وتطبيقاته التعليمية. أمتلك خبرة عملية في تصميم وتطوير أنشطة تفاعلية واختبارات إلكترونية باستخدام HTML وCSS وJavaScript، مما يثري تجربة التعلم ويجعلها أكثر تفاعلية وجاذبية للطلاب. أستخدم أدوات الذكاء الاصطناعي في تحليل أداء الطلاب وتصميم خطط تعليمية مخصصة، كما أصمم محتوى رقميًا مبتكرًا يتناسب مع احتياجات التعلم الحديثة. أسعى دائمًا لدمج التقنية في العملية التعليمية بطرق إبداعية تواكب متطلبات العصر الرقمي وتخدم أهداف رؤية المملكة 2030.
                </p>
            </div>
        </section>

        <section id="contact">
            <h2 class="section-title" id="contactTitle">تواصل</h2>
            <div class="contact-card">
                <p id="contactText">📧 iFahadenglish@gmail.com<br>📱 +9665554449824</p>
            </div>
        </section>
    </main>

    <footer id="footerText">© جميع الحقوق محفوظة - فهد الخالدي</footer>

    <!-- Particles.js -->
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    
    <script>
        // تهيئة particles.js
        document.addEventListener('DOMContentLoaded', function() {
            particlesJS('particles-js', {
                particles: {
                    number: { value: 80, density: { enable: true, value_area: 800 } },
                    color: { value: "#2563eb" },
                    shape: { type: "circle" },
                    opacity: { value: 0.3, random: true },
                    size: { value: 3, random: true },
                    line_linked: {
                        enable: true,
                        distance: 150,
                        color: "#2563eb",
                        opacity: 0.2,
                        width: 1
                    },
                    move: {
                        enable: true,
                        speed: 2,
                        direction: "none",
                        random: true,
                        out_mode: "out"
                    }
                },
                interactivity: {
                    detect_on: "canvas",
                    events: {
                        onhover: { enable: true, mode: "repulse" },
                        onclick: { enable: true, mode: "push" }
                    }
                }
            });
        });

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
                contactText: "📧 iFahadenglish@gmail.com<br>📱 +966554449824",
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
            langBtn.innerHTML = currentLang === 'ar' ? '<i class="fas fa-language"></i> EN' : '<i class="fas fa-language"></i> AR';
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
