<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سيرتي الذاتية | أحمد التميمي</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
            --warning: #f39c12;
            --gray: #7f8c8d;
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --radius: 12px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e7f1 100%);
            color: var(--dark);
            line-height: 1.8;
            overflow-x: hidden;
            position: relative;
        }

        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill="none" width="100" height="100"/><path d="M20,20 C40,0 60,0 80,20 C100,40 100,60 80,80 C60,100 40,100 20,80 C0,60 0,40 20,20 Z" fill="rgba(52, 152, 219, 0.03)" stroke="none"/></svg>');
            background-size: 120px;
            opacity: 0.3;
            z-index: -1;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* تصميم الشريط العلوي */
        header {
            background: rgba(255, 255, 255, 0.95);
            box-shadow: var(--shadow);
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
        }

        .logo i {
            color: var(--secondary);
            margin-left: 10px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-size: 1.1rem;
            padding: 8px 15px;
            border-radius: 30px;
            transition: var(--transition);
            position: relative;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        nav ul li a::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 3px;
            background: var(--secondary);
            transition: var(--transition);
            border-radius: 3px;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.8rem;
            color: var(--primary);
            cursor: pointer;
        }

        /* قسم المقدمة */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 100px 0 50px;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .hero-text {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }

        .hero-image {
            flex: 1;
            min-width: 300px;
            display: flex;
            justify-content: center;
            position: relative;
        }

        .profile-image {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            object-fit: cover;
            border: 8px solid white;
            box-shadow: var(--shadow);
            animation: float 6s ease-in-out infinite;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: var(--primary);
            line-height: 1.2;
        }

        .hero-text h1 span {
            color: var(--secondary);
        }

        .hero-text p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: var(--gray);
        }

        .typed-text {
            color: var(--accent);
            font-weight: 700;
        }

        .btn {
            display: inline-block;
            padding: 15px 35px;
            background: var(--secondary);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.1rem;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
        }

        .btn:hover {
            background: var(--primary);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(52, 152, 219, 0.4);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary);
            color: var(--secondary);
            margin-right: 15px;
        }

        .btn-outline:hover {
            background: var(--secondary);
            color: white;
        }

        .social-icons {
            display: flex;
            margin-top: 30px;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: white;
            border-radius: 50%;
            margin-left: 15px;
            color: var(--secondary);
            font-size: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }

        .social-icons a:hover {
            transform: translateY(-5px);
            color: white;
            background: var(--secondary);
        }

        /* الأقسام العامة */
        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 70px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.8rem;
            color: var(--primary);
            display: inline-block;
            padding-bottom: 15px;
            position: relative;
        }

        .section-title h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }

        /* قسم عني */
        .about-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
            gap: 40px;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--primary);
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .stat-box {
            background: white;
            padding: 25px;
            border-radius: var(--radius);
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .stat-box:hover {
            transform: translateY(-10px);
        }

        .stat-box i {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .stat-box .number {
            font-size: 2.2rem;
            font-weight: 800;
            color: var(--primary);
            display: block;
            margin-bottom: 5px;
        }

        .stat-box .text {
            color: var(--gray);
            font-size: 1.1rem;
        }

        /* قسم المهارات */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background: white;
            padding: 30px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        .skill-category h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            color: var(--primary);
            display: flex;
            align-items: center;
        }

        .skill-category h3 i {
            margin-left: 10px;
            color: var(--secondary);
        }

        .skill-item {
            margin-bottom: 25px;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .skill-bar {
            height: 10px;
            background: #e0e0e0;
            border-radius: 5px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: var(--secondary);
            border-radius: 5px;
            position: relative;
            transition: width 1.5s ease-in-out;
        }

        .skill-progress::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 20px;
            height: 100%;
            background: rgba(255, 255, 255, 0.3);
            transform: translateX(-100%);
            animation: progress-shine 1.5s infinite;
        }

        /* قسم الخبرات */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::before {
            content: "";
            position: absolute;
            top: 0;
            bottom: 0;
            width: 4px;
            background: var(--secondary);
            left: 50%;
            transform: translateX(-50%);
        }

        .timeline-item {
            position: relative;
            width: calc(50% - 40px);
            margin-bottom: 60px;
        }

        .timeline-item:nth-child(odd) {
            float: left;
            clear: right;
        }

        .timeline-item:nth-child(even) {
            float: right;
            clear: left;
        }

        .timeline-content {
            background: white;
            padding: 30px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            position: relative;
        }

        .timeline-content::before {
            content: "";
            position: absolute;
            top: 30px;
            width: 20px;
            height: 20px;
            background: white;
            transform: rotate(45deg);
        }

        .timeline-item:nth-child(odd) .timeline-content::before {
            right: -10px;
        }

        .timeline-item:nth-child(even) .timeline-content::before {
            left: -10px;
        }

        .timeline-date {
            background: var(--secondary);
            color: white;
            padding: 8px 15px;
            border-radius: 30px;
            font-weight: 600;
            display: inline-block;
            margin-bottom: 15px;
        }

        .timeline-content h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }

        .timeline-content h4 {
            color: var(--secondary);
            margin-bottom: 10px;
        }

        /* قسم المشاريع */
        .projects-filter {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 40px;
        }

        .filter-btn {
            padding: 10px 25px;
            margin: 5px;
            background: white;
            border: none;
            border-radius: 30px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--secondary);
            color: white;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .project-image {
            height: 250px;
            overflow: hidden;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-image img {
            transform: scale(1.1);
        }

        .project-content {
            padding: 25px;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            margin-bottom: 15px;
        }

        .project-tag {
            background: #e0f7ff;
            color: var(--secondary);
            padding: 5px 15px;
            border-radius: 30px;
            font-size: 0.9rem;
            margin-left: 5px;
            margin-bottom: 5px;
        }

        .project-content h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }

        .project-links {
            display: flex;
            margin-top: 20px;
        }

        .project-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #f5f5f5;
            border-radius: 50%;
            margin-left: 10px;
            color: var(--secondary);
            transition: var(--transition);
        }

        .project-links a:hover {
            background: var(--secondary);
            color: white;
            transform: translateY(-5px);
        }

        /* قسم التواصل */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .contact-info {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            padding: 40px;
            border-radius: var(--radius);
            color: white;
            box-shadow: var(--shadow);
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }

        .contact-info h3::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: white;
            border-radius: 2px;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 30px;
        }

        .contact-item i {
            font-size: 1.5rem;
            margin-left: 15px;
            min-width: 30px;
        }

        .contact-details h4 {
            font-size: 1.2rem;
            margin-bottom: 5px;
        }

        .contact-form {
            background: white;
            padding: 40px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }

        .form-control {
            width: 100%;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: var(--radius);
            font-family: 'Tajawal', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* التذييل */
        footer {
            background: var(--primary);
            color: white;
            padding: 70px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 15px;
        }

        .footer-column h3::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--secondary);
            border-radius: 2px;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 15px;
        }

        .footer-links a {
            color: #bbb;
            text-decoration: none;
            transition: var(--transition);
            display: flex;
            align-items: center;
        }

        .footer-links a:hover {
            color: var(--secondary);
            transform: translateX(5px);
        }

        .footer-links a i {
            margin-left: 10px;
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bbb;
            font-size: 0.9rem;
        }

        /* التأثيرات والرسوم المتحركة */
        @keyframes float {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
            100% {
                transform: translateY(0px);
            }
        }

        @keyframes progress-shine {
            0% {
                transform: translateX(-100%);
            }
            100% {
                transform: translateX(500%);
            }
        }

        /* التصميم المتجاوب */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .social-icons {
                justify-content: center;
            }
            
            .timeline::before {
                left: 30px;
            }
            
            .timeline-item {
                width: 100%;
                padding-right: 70px;
                padding-left: 30px;
            }
            
            .timeline-item:nth-child(odd),
            .timeline-item:nth-child(even) {
                float: none;
            }
            
            .timeline-item:nth-child(odd) .timeline-content::before {
                left: -10px;
                right: auto;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 80px;
                left: 0;
                background: white;
                width: 100%;
                flex-direction: column;
                align-items: center;
                padding: 20px 0;
                box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
                transform: translateY(-150%);
                transition: var(--transition);
            }
            
            nav ul.active {
                transform: translateY(0);
            }
            
            nav ul li {
                margin: 15px 0;
            }
            
            .hero-text h1 {
                font-size: 2.8rem;
            }
            
            .section-title h2 {
                font-size: 2.2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 576px) {
            .hero-text h1 {
                font-size: 2.3rem;
            }
            
            .btn {
                display: block;
                width: 100%;
                margin-bottom: 15px;
                text-align: center;
            }
            
            .btn-outline {
                margin-right: 0;
            }
            
            .profile-image {
                width: 250px;
                height: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- الشريط العلوي -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">
                <i class="fas fa-code"></i>
                أحمد.كوم
            </a>
            
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav>
                <ul>
                    <li><a href="#home">الرئيسية</a></li>
                    <li><a href="#about">عني</a></li>
                    <li><a href="#skills">المهارات</a></li>
                    <li><a href="#experience">الخبرات</a></li>
                    <li><a href="#projects">المشاريع</a></li>
                    <li><a href="#contact">التواصل</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- قسم المقدمة -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <div class="hero-text">
                <h1>مرحبًا، أنا <span>أحمد التميمي</span> <br> مطور ويب و تطبيقات</h1>
                <p>أقوم بتحويل الأفكار إلى تطبيقات رقمية مبتكرة مع تجارب مستخدم متميزة.</p>
                <p>متخصص في: <span class="typed-text">تطوير تطبيقات الويب المتكاملة, تصميم واجهات المستخدم, تطوير تطبيقات الجوال</span></p>
                
                <div class="hero-buttons">
                    <a href="#projects" class="btn btn-outline">تصفح أعمالي</a>
                    <a href="#contact" class="btn">تواصل معي</a>
                </div>
                
                <div class="social-icons">
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-behance"></i></a>
                </div>
            </div>
            
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=774&q=80" alt="أحمد التميمي" class="profile-image">
            </div>
        </div>
    </section>

    <!-- قسم عني -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>عني</h2>
            </div>
            
            <div class="about-content">
                <div class="about-text">
                    <h3>أنا مطور ويب مبتكر مع شغف لخلق حلول رقمية</h3>
                    <p>أعمل كمطور ويب ومصمم واجهات مستخدم محترف لأكثر من 7 سنوات. خلال مسيرتي المهنية، عملت مع شركات ناشئة وشركات كبيرة لإنشاء تطبيقات ويب مبتكرة وسهلة الاستخدام.</p>
                    <p>أؤمن بأن التصميم الجيد لا يتعلق بالمظهر فقط، بل يتعلق بحل المشاكل الحقيقية وتقديم تجربة مستخدم استثنائية. أستمتع بتحويل الأفكار المعقدة إلى تطبيقات بسيطة وفعالة.</p>
                    
                    <div class="about-stats">
                        <div class="stat-box">
                            <i class="fas fa-briefcase"></i>
                            <span class="number">7+</span>
                            <span class="text">سنوات خبرة</span>
                        </div>
                        <div class="stat-box">
                            <i class="fas fa-project-diagram"></i>
                            <span class="number">120+</span>
                            <span class="text">مشروع مكتمل</span>
                        </div>
                        <div class="stat-box">
                            <i class="fas fa-users"></i>
                            <span class="number">85+</span>
                            <span class="text">عميل راضي</span>
                        </div>
                        <div class="stat-box">
                            <i class="fas fa-award"></i>
                            <span class="number">12</span>
                            <span class="text">جوائز وتكريمات</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم المهارات -->
    <section id="skills" class="skills">
        <div class="container">
            <div class="section-title">
                <h2>مهاراتي</h2>
            </div>
            
            <div class="skills-container">
                <div class="skill-category">
                    <h3><i class="fas fa-laptop-code"></i> تطوير الواجهة الأمامية</h3>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>HTML5 & CSS3</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="95"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>JavaScript</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="90"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>React.js</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>Vue.js</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="80"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-server"></i> تطوير الواجهة الخلفية</h3>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>Node.js</span>
                            <span>88%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="88"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>PHP</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>Python</span>
                            <span>75%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="75"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>MySQL</span>
                            <span>82%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="82"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-mobile-alt"></i> تطوير الجوال والتصميم</h3>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>React Native</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="80"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>UI/UX Design</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="90"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>Figma</span>
                            <span>92%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="92"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-info">
                            <span>Adobe XD</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم الخبرات -->
    <section id="experience" class="experience">
        <div class="container">
            <div class="section-title">
                <h2>خبراتي العملية</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="timeline-date">2021 - الحاضر</span>
                        <h3>مطور ويب رئيسي</h3>
                        <h4>شركة التقنية المتقدمة</h4>
                        <p>قيادة فريق تطوير مكون من 8 أعضاء لإنشاء تطبيقات ويب معقدة للعملاء الدوليين. تطوير معمارية التطبيقات وضمان جودة الكود وأداء التطبيقات.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="timeline-date">2018 - 2021</span>
                        <h3>مطور تطبيقات جوال</h3>
                        <h4>ستارت أب تك</h4>
                        <p>تطوير تطبيقات جوال باستخدام React Native لأنظمة iOS و Android. العمل مع مصممين لتحويل التصاميم إلى تطبيقات وظيفية وسهلة الاستخدام.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="timeline-date">2016 - 2018</span>
                        <h3>مطور واجهات أمامية</h3>
                        <h4>وكالة إبداع ويب</h4>
                        <p>إنشاء واجهات مستخدم تفاعلية باستخدام HTML, CSS و JavaScript. تحسين تجربة المستخدم وأداء المواقع للعملاء في مختلف المجالات.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <span class="timeline-date">2014 - 2016</span>
                        <h3>متدرب تطوير ويب</h3>
                        <h4>مركز التكنولوجيا الحديثة</h4>
                        <p>تدريب مكثف على أساسيات تطوير الويب. المشاركة في مشاريع حقيقية واكتساب الخبرة العملية في بيئة احترافية.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم المشاريع -->
    <section id="projects" class="projects">
        <div class="container">
            <div class="section-title">
                <h2>مشاريعي</h2>
            </div>
            
            <div class="projects-filter">
                <button class="filter-btn active" data-filter="all">الكل</button>
                <button class="filter-btn" data-filter="web">تطبيقات ويب</button>
                <button class="filter-btn" data-filter="mobile">تطبيقات جوال</button>
                <button class="filter-btn" data-filter="design">تصميم</button>
            </div>
            
            <div class="projects-grid">
                <div class="project-card" data-category="web">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80" alt="مشروع نظام إدارة">
                    </div>
                    <div class="project-content">
                        <div class="project-tags">
                            <span class="project-tag">ويب</span>
                            <span class="project-tag">React</span>
                            <span class="project-tag">Node.js</span>
                        </div>
                        <h3>نظام إدارة المشاريع</h3>
                        <p>منصة متكاملة لإدارة المشاريع والمهام، تمكن الفرق من التعاون وتتبع التقدم وتحسين الإنتاجية.</p>
                        <div class="project-links">
                            <a href="#"><i class="fas fa-external-link-alt"></i></a>
                            <a href="#"><i class="fab fa-github"></i></a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card" data-category="mobile">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1581094794329-16b5e1b5c6e1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80" alt="تطبيق اللياقة البدنية">
                    </div>
                    <div class="project-content">
                        <div class="project-tags">
                            <span class="project-tag">جوال</span>
                            <span class="project-tag">React Native</span>
                            <span class="project-tag">Firebase</span>
                        </div>
                        <h3>تطبيق اللياقة البدنية</h3>
                        <p>تطبيق جوال شامل لللياقة البدنية يوفر تمارين مخصصة، تتبع التقدم، وتوصيات غذائية.</p>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-app-store"></i></a>
                            <a href="#"><i class="fab fa-google-play"></i></a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card" data-category="design">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1547658719-da2b51169166?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="تصميم متجر إلكتروني">
                    </div>
                    <div class="project-content">
                        <div class="project-tags">
                            <span class="project-tag">تصميم</span>
                            <span class="project-tag">UI/UX</span>
                            <span class="project-tag">Figma</span>
                        </div>
                        <h3>واجهة متجر إلكتروني</h3>
                        <p>تصميم واجهة مستخدم حديثة وسهلة الاستخدام لمتجر إلكتروني متخصص في المنتجات التقنية.</p>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-figma"></i></a>
                            <a href="#"><i class="fas fa-palette"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم التواصل -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>تواصل معي</h2>
            </div>
            
            <div class="contact-container">
                <div class="contact-info">
                    <h3>معلومات التواصل</h3>
                    
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div class="contact-details">
                            <h4>الموقع</h4>
                            <p>الرياض، المملكة العربية السعودية</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div class="contact-details">
                            <h4>البريد الإلكتروني</h4>
                            <p>ahmed@example.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div class="contact-details">
                            <h4>الهاتف</h4>
                            <p>+966 55 123 4567</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div class="contact-details">
                            <h4>أوقات العمل</h4>
                            <p>الأحد - الخميس: 9 صباحًا - 5 مساءً</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>أرسل لي رسالة</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">الاسم الكامل</label>
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
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn">إرسال الرسالة</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- التذييل -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>أحمد.كوم</h3>
                    <p>أحول الأفكار إلى تطبيقات رقمية مبتكرة مع تجارب مستخدم متميزة.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-behance"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>روابط سريعة</h3>
                    <ul class="footer-links">
                        <li><a href="#home"><i class="fas fa-chevron-left"></i> الرئيسية</a></li>
                        <li><a href="#about"><i class="fas fa-chevron-left"></i> عني</a></li>
                        <li><a href="#skills"><i class="fas fa-chevron-left"></i> المهارات</a></li>
                        <li><a href="#experience"><i class="fas fa-chevron-left"></i> الخبرات</a></li>
                        <li><a href="#projects"><i class="fas fa-chevron-left"></i> المشاريع</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>خدماتي</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-left"></i> تطوير الويب</a></li>
                        <li><a href="#"><i class="fas fa-chevron-left"></i> تطبيقات الجوال</a></li>
                        <li><a href="#"><i class="fas fa-chevron-left"></i> تصميم واجهات المستخدم</a></li>
                        <li><a href="#"><i class="fas fa-chevron-left"></i> استشارات تقنية</a></li>
                        <li><a href="#"><i class="fas fa-chevron-left"></i> تطوير الأعمال</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>جميع الحقوق محفوظة &copy; 2023 أحمد.كوم | تم التصميم والتطوير بواسطة أحمد التميمي</p>
            </div>
        </div>
    </footer>

    <script>
        // تنشيط القائمة المتحركة
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
            const navMenu = document.querySelector('nav ul');
            
            mobileMenuBtn.addEventListener('click', function() {
                navMenu.classList.toggle('active');
                this.querySelector('i').classList.toggle('fa-bars');
                this.querySelector('i').classList.toggle('fa-times');
            });
            
            // إغلاق القائمة عند النقر على رابط
            document.querySelectorAll('nav ul li a').forEach(link => {
                link.addEventListener('click', () => {
                    navMenu.classList.remove('active');
                    mobileMenuBtn.querySelector('i').classList.add('fa-bars');
                    mobileMenuBtn.querySelector('i').classList.remove('fa-times');
                });
            });
            
            // تنشيط شريط التقدم في المهارات
            const skillProgressBars = document.querySelectorAll('.skill-progress');
            
            const animateSkills = () => {
                skillProgressBars.forEach(bar => {
                    const width = bar.getAttribute('data-width');
                    bar.style.width = width + '%';
                });
            };
            
            // تنشيط التأثيرات عند التمرير
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        animateSkills();
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.3 });
            
            document.querySelectorAll('.skills').forEach(section => {
                observer.observe(section);
            });
            
            // فلترة المشاريع
            const filterButtons = document.querySelectorAll('.filter-btn');
            const projectCards = document.querySelectorAll('.project-card');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', () => {
                    // إزالة النشط من جميع الأزرار
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    // إضافة النشط للزر المحدد
                    button.classList.add('active');
                    
                    const filter = button.getAttribute('data-filter');
                    
                    projectCards.forEach(card => {
                        if (filter === 'all' || card.getAttribute('data-category') === filter) {
                            card.style.display = 'block';
                        } else {
                            card.style.display = 'none';
                        }
                    });
                });
            });
            
            // إرسال نموذج التواصل
            const contactForm = document.getElementById('contactForm');
            
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // هنا يمكنك إضافة كود إرسال الرسالة
                alert('تم إرسال رسالتك بنجاح! سأتواصل معك قريبًا.');
                contactForm.reset();
            });
            
            // تأثير الكتابة
            const typedTextSpan = document.querySelector('.typed-text');
            const textArray = ["تطوير تطبيقات الويب المتكاملة", "تصميم واجهات المستخدم", "تطوير تطبيقات الجوال"];
            let textArrayIndex = 0;
            let charIndex = 0;
            
            function type() {
                if (charIndex < textArray[textArrayIndex].length) {
                    typedTextSpan.textContent += textArray[textArrayIndex].charAt(charIndex);
                    charIndex++;
                    setTimeout(type, 100);
                } else {
                    setTimeout(erase, 2000);
                }
            }
            
            function erase() {
                if (charIndex > 0) {
                    typedTextSpan.textContent = textArray[textArrayIndex].substring(0, charIndex - 1);
                    charIndex--;
                    setTimeout(erase, 50);
                } else {
                    textArrayIndex++;
                    if (textArrayIndex >= textArray.length) textArrayIndex = 0;
                    setTimeout(type, 500);
                }
            }
            
            // بدء التأثير عند تحميل الصفحة
            setTimeout(type, 1000);
        });
    </script>
</body>
</html>
