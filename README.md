<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>นางสาวมนฤทัย บานแย้ม | E-Portfolio</title>
    
    <!-- นำเข้าฟอนต์ Prompt (สำหรับภาษาไทย) และ Font Awesome (สำหรับไอคอน) -->
    <link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- General & Theme Settings --- */
        :root {
            --primary: #1E3A8A; /* น้ำเงินเข้ม */
            --secondary: #3B82F6; /* น้ำเงินสว่าง */
            --accent: #EC4899; /* ชมพูพาสเทล/สีเน้น */
            --bg-light: #F8FAFC; /* พื้นหลังเทา-ฟ้าอ่อน */
            --text-dark: #1E293B; /* ตัวอักษรเข้ม */
            --text-light: #64748B; /* ตัวอักษรจาง */
            --white: #FFFFFF;
            --card-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.05), 0 8px 10px -6px rgba(0, 0, 0, 0.05);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Prompt', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- Navigation Bar --- */
        header {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            transition: var(--transition);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 75px;
        }

        .logo {
            font-weight: 700;
            font-size: 1.3rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 8px;
            text-decoration: none;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 24px;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: var(--transition);
            font-size: 0.95rem;
            padding: 6px 12px;
            border-radius: 8px;
        }

        .nav-links a:hover, .nav-links a.active {
            color: var(--primary);
            background-color: rgba(59, 130, 246, 0.08);
        }

        .btn-github {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--primary);
            color: var(--white) !important;
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 500;
            text-decoration: none;
            transition: var(--transition);
            box-shadow: 0 4px 6px -1px rgba(30, 58, 138, 0.1);
        }

        .btn-github:hover {
            background: var(--secondary);
            transform: translateY(-2px);
        }

        /* Mobile Menu Toggle */
        .menu-btn {
            display: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--primary);
        }

        /* --- Hero/Home Section --- */
        #home {
            padding: 160px 0 100px 0;
            background: radial-gradient(circle at top right, rgba(59, 130, 246, 0.05), transparent 60%);
            min-height: 90vh;
            display: flex;
            align-items: center;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 50px;
            align-items: center;
        }

        .badge {
            display: inline-block;
            background: rgba(236, 72, 153, 0.1);
            color: var(--accent);
            padding: 6px 16px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 20px;
            border: 1px solid rgba(236, 72, 153, 0.2);
        }

        .hero-text h2 {
            font-size: 1.2rem;
            color: var(--secondary);
            font-weight: 500;
            margin-bottom: 10px;
        }

        .hero-text h1 {
            font-size: 3rem;
            color: var(--primary);
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-text .highlight {
            color: var(--accent);
            display: block;
        }

        .hero-text p {
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 30px;
            max-width: 600px;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
        }

        .btn-primary {
            background: var(--primary);
            color: var(--white);
            padding: 14px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            box-shadow: 0 4px 6px -1px rgba(30, 58, 138, 0.2);
        }

        .btn-primary:hover {
            background: var(--secondary);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: var(--white);
            color: var(--primary);
            padding: 14px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            border: 2px solid var(--primary);
        }

        .btn-secondary:hover {
            background: rgba(30, 58, 138, 0.05);
            transform: translateY(-2px);
        }

        /* ภาพหน้าปก หรือตัวแทนกราฟิก */
        .hero-img-container {
            position: relative;
            display: flex;
            justify-content: center;
        }

        .hero-img-bg {
            position: absolute;
            width: 380px;
            height: 380px;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.2), rgba(236, 72, 153, 0.2));
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            animation: morph 8s ease-in-out infinite alternate;
            z-index: 1;
        }

        .hero-img {
            position: relative;
            z-index: 2;
            width: 320px;
            height: 320px;
            background: #E2E8F0;
            border-radius: 50%;
            border: 8px solid var(--white);
            box-shadow: var(--card-shadow);
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero-img i {
            font-size: 8rem;
            color: #94A3B8;
        }

        @keyframes morph {
            0% { border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; }
            100% { border-radius: 70% 30% 30% 70% / 70% 70% 30% 30%; }
        }

        /* --- About Section --- */
        section {
            padding: 90px 0;
            border-bottom: 1px solid rgba(0,0,0,0.03);
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.2rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }

        .section-title p {
            color: var(--text-light);
            margin-top: 10px;
            font-size: 1.05rem;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 50px;
            align-items: start;
        }

        .about-info {
            background: var(--white);
            padding: 30px;
            border-radius: 20px;
            box-shadow: var(--card-shadow);
            border-left: 5px solid var(--primary);
        }

        .info-item {
            margin-bottom: 18px;
        }

        .info-item strong {
            color: var(--primary);
            display: block;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 4px;
        }

        .info-item p {
            font-size: 1.05rem;
        }

        .about-detail h3 {
            color: var(--primary);
            font-size: 1.6rem;
            margin-bottom: 15px;
        }

        .about-detail .desc {
            color: var(--text-light);
            font-size: 1.05rem;
            margin-bottom: 30px;
        }

        .skills h4 {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: var(--text-dark);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .skill-tag {
            background: var(--white);
            padding: 12px 18px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            gap: 12px;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.02);
            border: 1px solid rgba(0,0,0,0.04);
            font-size: 0.95rem;
        }

        .skill-tag i {
            color: var(--secondary);
            font-size: 1.2rem;
        }

        /* --- Portfolio (Works) Section --- */
        .filter-buttons {
            display: flex;
            justify-content: center;
            gap: 12px;
            margin-bottom: 40px;
        }

        .filter-btn {
            background: var(--white);
            color: var(--text-dark);
            border: 1px solid rgba(0,0,0,0.08);
            padding: 10px 24px;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 500;
            font-family: inherit;
            transition: var(--transition);
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--primary);
            color: var(--white);
            border-color: var(--primary);
            box-shadow: 0 4px 12px rgba(30, 58, 138, 0.15);
        }

        .works-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
            gap: 30px;
        }

        .work-card {
            background: var(--white);
            border-radius: 18px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border: 1px solid rgba(0,0,0,0.03);
            display: flex;
            flex-direction: column;
        }

        .work-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.08);
        }

        .work-img {
            height: 200px;
            background: #E2E8F0;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .work-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .work-img-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(30, 58, 138, 0.9), transparent);
            display: flex;
            align-items: flex-end;
            padding: 20px;
            opacity: 0;
            transition: var(--transition);
        }

        .work-card:hover .work-img-overlay {
            opacity: 1;
        }

        .work-category {
            color: var(--white);
            background: var(--accent);
            padding: 4px 12px;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
        }

        .work-content {
            padding: 24px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .work-content h3 {
            font-size: 1.2rem;
            color: var(--primary);
            margin-bottom: 10px;
        }

        .work-content p {
            color: var(--text-light);
            font-size: 0.95rem;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .work-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--secondary);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .work-link:hover {
            color: var(--primary);
        }

        /* --- Activities Section --- */
        .activities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
            gap: 30px;
        }

        .activity-card {
            background: var(--white);
            border-radius: 18px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            border: 1px solid rgba(0,0,0,0.03);
            display: flex;
            flex-direction: column;
        }

        .activity-img {
            height: 220px;
            background: #E2E8F0;
            position: relative;
        }

        .activity-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .activity-date {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--primary);
            color: var(--white);
            padding: 6px 14px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .activity-content {
            padding: 24px;
        }

        .activity-content h3 {
            font-size: 1.15rem;
            color: var(--primary);
            margin-bottom: 10px;
        }

        .activity-content p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* --- Footer Section --- */
        footer {
            background: #0F172A; /* ดาร์กโทน */
            color: #94A3B8;
            padding: 60px 0 30px 0;
            font-size: 0.95rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            color: var(--white);
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 15px;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .footer-logo span {
            color: var(--accent);
        }

        .footer-desc {
            margin-bottom: 20px;
            line-height: 1.7;
        }

        .footer-title {
            color: var(--white);
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 20px;
            position: relative;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: #94A3B8;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--white);
            padding-left: 5px;
        }

        .contact-info li {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 15px;
        }

        .contact-info i {
            color: var(--secondary);
            font-size: 1.1rem;
        }

        .social-icons {
            display: flex;
            gap: 12px;
            margin-top: 15px;
        }

        .social-btn {
            background: rgba(255,255,255,0.05);
            color: var(--white);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: var(--transition);
        }

        .social-btn:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.05);
            padding-top: 30px;
            text-align: center;
            font-size: 0.85rem;
        }

        /* --- Responsive Styles --- */
        @media (max-width: 992px) {
            .hero-grid {
                grid-template-columns: 1fr;
                gap: 40px;
                text-align: center;
            }

            .badge {
                margin: 0 auto 20px auto;
            }

            .hero-text p {
                margin: 0 auto 30px auto;
            }

            .hero-buttons {
                justify-content: center;
            }

            .hero-img-container {
                order: -1;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .menu-btn {
                display: block;
            }

            .nav-links {
                position: fixed;
                top: 75px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 75px);
                background: var(--white);
                flex-direction: column;
                align-items: center;
                padding: 40px 20px;
                gap: 24px;
                transition: var(--transition);
                box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            }

            .nav-links.active {
                left: 0;
            }

            .hero-text h1 {
                font-size: 2.2rem;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- Header & Navigation -->
    <header id="header">
        <div class="container">
            <nav>
                <a href="#home" class="logo">
                    <i class="fa-solid fa-graduation-cap"></i> Monruthai<span>portfolio</span>
                </a>
                <ul class="nav-links" id="nav-menu">
                    <li><a href="#home" class="active">หน้าแรก</a></li>
                    <li><a href="#about">แนะนำตัว</a></li>
                    <li><a href="#works">ผลงาน</a></li>
                    <li><a href="#activities">กิจกรรม</a></li>
                    <li><a href="https://github.com/monruthai-banyam" target="_blank" class="btn-github"><i class="fa-brands fa-github"></i> GitHub</a></li>
                </ul>
                <div class="menu-btn" id="menu-toggle">
                    <i class="fa-solid fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Section: Home -->
    <section id="home">
        <div class="container">
            <div class="hero-grid">
                <div class="hero-text">
                    <span class="badge">E-PORTFOLIO ✦ ยินดีต้อนรับสู่เว็บแฟ้มสะสมงาน</span>
                    <h2>Hello, I'm a Teacher! 👋</h2>
                    <h1>นางสาวมนฤทัย บานแย้ม <span class="highlight">เทคโนโลยีและการเขียนโปรแกรม</span></h1>
                    <p>ครูผู้มุ่งมั่นในการพัฒนาทักษะด้านเทคโนโลยีและโค้ดดิ้งให้กับผู้เรียน เพื่อเตรียมพร้อมสำหรับยุคดิจิทัลอย่างยั่งยืน</p>
                    <div class="hero-buttons">
                        <a href="#works" class="btn-primary">ชมผลงานของฉัน <i class="fa-solid fa-arrow-right"></i></a>
                        <a href="#about" class="btn-secondary">รู้จักกันมากขึ้น</a>
                    </div>
                </div>
                <div class="hero-img-container">
                    <div class="hero-img-bg"></div>
                    <div class="hero-img">
                        <!-- สามารถสลับใส่รูปภาพได้ที่นี่ ตัวอย่างภาพจำลอง -->
                        <i class="fa-solid fa-user-tie"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section: About -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>แนะนำตัวเอง</h2>
                <p>ประวัติการทำงาน การศึกษา และทักษะความสามารถ</p>
            </div>
            <div class="about-grid">
                <div class="about-info">
                    <div class="info-item">
                        <strong>ชื่อ-นามสกุล</strong>
                        <p>นางสาวมนฤทัย บานแย้ม</p>
                    </div>
                    <div class="info-item">
                        <strong>ตำแหน่ง</strong>
                        <p>ครูผู้สอนด้านเทคโนโลยีสารสนเทศ</p>
                    </div>
                    <div class="info-item">
                        <strong>สังกัด</strong>
                        <p>กลุ่มสาระการเรียนรู้วิทยาศาสตร์และเทคโนโลยี</p>
                    </div>
                    <div class="info-item">
                        <strong>การติดต่อ</strong>
                        <p>monruthai.b@school.ac.th</p>
                    </div>
                </div>
                <div class="about-detail">
                    <h3>" มุ่งเน้นสร้างแรงบันดาลใจ ส่งเสริมกระบวนการคิดด้วยโค้ดดิ้ง "</h3>
                    <p class="desc">มีความชื่นชอบและมีประสบการณ์ในการจัดกระบวนการเรียนรู้ด้านการเขียนโปรแกรม (Programming), วิทยาการคำนวณ (Computing Science), และเทคโนโลยีสารสนเทศสมัยใหม่ โดยเน้นการลงมือปฏิบัติจริง (Active Learning) เพื่อให้ผู้เรียนสามารถนำความรู้ไปต่อยอดและประยุกต์ใช้งานในชีวิตจริงได้</p>
                    
                    <div class="skills">
                        <h4>ทักษะและความเชี่ยวชาญ (Skills & Expertise)</h4>
                        <div class="skills-grid">
                            <div class="skill-tag">
                                <i class="fa-solid fa-code"></i> HTML / CSS / JavaScript
                            </div>
                            <div class="skill-tag">
                                <i class="fa-solid fa-robot"></i> Python & Block-based coding
                            </div>
                            <div class="skill-tag">
                                <i class="fa-solid fa-lightbulb"></i> วิทยาการคำนวณ & การแก้ปัญหา
                            </div>
                            <div class="skill-tag">
                                <i class="fa-solid fa-users-gear"></i> การออกแบบสื่อและ Active Learning
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section: Portfolio (Works) -->
    <section id="works">
        <div class="container">
            <div class="section-title">
                <h2>ผลงานที่โดดเด่น</h2>
                <p>รวมระบบ สื่อการเรียนสอน และผลลัพธ์จากความมุ่งมั่นในการเขียนโปรแกรมและพัฒนาผู้เรียน</p>
            </div>

            <!-- Filter Buttons -->
            <div class="filter-buttons">
                <button class="filter-btn active" data-filter="all">ทั้งหมด</button>
                <button class="filter-btn" data-filter="web">เว็บแอปพลิเคชัน</button>
                <button class="filter-btn" data-filter="media">สื่อการสอน</button>
                <button class="filter-btn" data-filter="academic">งานวิชาการ</button>
            </div>

            <div class="works-grid">
                <!-- Card 1 -->
                <div class="work-card" data-category="web">
                    <div class="work-img">
                        <i class="fa-solid fa-laptop-code" style="font-size: 4rem; color: #94A3B8;"></i>
                        <div class="work-img-overlay">
                            <span class="work-category">Web Application</span>
                        </div>
                    </div>
                    <div class="work-content">
                        <h3>ระบบบันทึกคะแนนและประเมินผลออนไลน์</h3>
                        <p>ระบบเว็บช่วยครูในการประเมินและวิเคราะห์คะแนนสอบของนักเรียนแบบเรียลไทม์ พัฒนาด้วย HTML, CSS และ JavaScript</p>
                        <a href="https://github.com/monruthai-banyam/score-grading-system" target="_blank" class="work-link">
                            <i class="fa-brands fa-github"></i> ดูซอร์สโค้ดใน GitHub <i class="fa-solid fa-arrow-up-right-from-square"></i>
                        </a>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="work-card" data-category="media">
                    <div class="work-img">
                        <i class="fa-solid fa-gamepad" style="font-size: 4rem; color: #94A3B8;"></i>
                        <div class="work-img-overlay">
                            <span class="work-category">Teaching Media</span>
                        </div>
                    </div>
                    <div class="work-content">
                        <h3>เกมแนวฝึกคิดแก้ปัญหา (Computational Thinking Game)</h3>
                        <p>สื่อการเรียนรู้แบบ Interactive เพื่อพัฒนาทักษะกระบวนการคิดเชิงคำนวณและพื้นฐาน อัลกอริทึมสำหรับนักเรียนชั้นมัธยมศึกษา</p>
                        <a href="https://github.com/monruthai-banyam/ct-learning-game" target="_blank" class="work-link">
                            <i class="fa-brands fa-github"></i> ดูซอร์สโค้ดใน GitHub <i class="fa-solid fa-arrow-up-right-from-square"></i>
                        </a>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="work-card" data-category="academic">
                    <div class="work-img">
                        <i class="fa-regular fa-file-pdf" style="font-size: 4rem; color: #94A3B8;"></i>
                        <div class="work-img-overlay">
                            <span class="work-category">Academic Work</span>
                        </div>
                    </div>
                    <div class="work-content">
                        <h3>เอกสารประกอบการสอนวิชาการเขียนโปรแกรมเบื้องต้น</h3>
                        <p>คู่มือและแผนการจัดกิจกรรมการเรียนรู้แบบโครงงานเป็นฐาน (Project-Based) เพื่อสนับสนุนและส่งเสริมผู้เรียน</p>
                        <a href="https://github.com/monruthai-banyam/programming-curriculum" target="_blank" class="work-link">
                            <i class="fa-brands fa-github"></i> ดูไฟล์ประกอบใน GitHub <i class="fa-solid fa-arrow-up-right-from-square"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section: Activities -->
    <section id="activities">
        <div class="container">
            <div class="section-title">
                <h2>กิจกรรมและการอบรม</h2>
                <p>ภาพรวมกิจกรรมการมีส่วนร่วมในโรงเรียนและการพัฒนาตนเองในฐานะครู</p>
            </div>
            <div class="activities-grid">
                <!-- Activity 1 -->
                <div class="activity-card">
                    <div class="activity-img">
                        <div class="activity-date">10 พ.ย. 2026</div>
                        <div style="width:100%; height:100%; display:flex; align-items:center; justify-content:center; background:#E2E8F0;">
                            <i class="fa-solid fa-trophy" style="font-size: 4rem; color:#94A3B8;"></i>
                        </div>
                    </div>
                    <div class="activity-content">
                        <h3>งานสัปดาห์วิทยาศาสตร์และเทคโนโลยี</h3>
                        <p>ทำหน้าที่หัวหน้างานและผู้ดูแลบอร์ดนิทรรศการรวมถึงจัดการแข่งขันทักษะคอมพิวเตอร์และการเขียนโปรแกรมระดับโรงเรียน</p>
                    </div>
                </div>

                <!-- Activity 2 -->
                <div class="activity-card">
                    <div class="activity-img">
                        <div class="activity-date">24 ต.ค. 2026</div>
                        <div style="width:100%; height:100%; display:flex; align-items:center; justify-content:center; background:#E2E8F0;">
                            <i class="fa-solid fa-chalkboard-user" style="font-size: 4rem; color:#94A3B8;"></i>
                        </div>
                    </div>
                    <div class="activity-content">
                        <h3>วิทยากรค่ายคอมพิวเตอร์</h3>
                        <p>เป็นผู้บรรยายและจัดกิจกรรมเวิร์กช็อป "การสร้างเว็บเบื้องต้นด้วย HTML/CSS" สำหรับนักเรียนระดับชั้นมัธยมศึกษาตอนปลาย</p>
                    </div>
                </div>

                <!-- Activity 3 -->
                <div class="activity-card">
                    <div class="activity-img">
                        <div class="activity-date">15 ก.ย. 2026</div>
                        <div style="width:100%; height:100%; display:flex; align-items:center; justify-content:center; background:#E2E8F0;">
                            <i class="fa-solid fa-certificate" style="font-size: 4rem; color:#94A3B8;"></i>
                        </div>
                    </div>
                    <div class="activity-content">
                        <h3>การอบรมด้านความปลอดภัยไซเบอร์และวิทยาการคอมพิวเตอร์</h3>
                        <p>เข้าร่วมศึกษาต่อยอดและแบ่งปันความรู้หลักสูตรความมั่นคงปลอดภัยบนเครือข่ายสำหรับครูผู้สอนเพื่อประยุกต์สอนเด็กๆ</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <div>
                    <a href="#" class="footer-logo">
                        <i class="fa-solid fa-graduation-cap"></i> Monruthai<span>portfolio</span>
                    </a>
                    <p class="footer-desc">พื้นที่บันทึกผลงานการสอน พัฒนาสื่อความรู้ เพื่อยกระดับและเปลี่ยนผ่านการศึกษาไทยไปสู่ความรู้ด้านนวัตกรรมและเทคโนโลยีสารสนเทศ</p>
                    <div class="social-icons">
                        <a href="https://github.com/monruthai-banyam" class="social-btn" target="_blank"><i class="fa-brands fa-github"></i></a>
                        <a href="mailto:monruthai.b@school.ac.th" class="social-btn"><i class="fa-solid fa-envelope"></i></a>
                    </div>
                </div>
                <div>
                    <h3 class="footer-title">ลิงก์ภายในเว็บ</h3>
                    <ul class="footer-links">
                        <li><a href="#home">หน้าแรก</a></li>
                        <li><a href="#about">แนะนำตัว</a></li>
                        <li><a href="#works">ผลงาน</a></li>
                        <li><a href="#activities">กิจกรรมและการอบรม</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="footer-title">ติดต่อฉัน</h3>
                    <ul class="contact-info">
                        <li><i class="fa-solid fa-location-dot"></i> <span>โรงเรียนประจำจังหวัด สพม.</span></li>
                        <li><i class="fa-solid fa-envelope"></i> <span>monruthai.b@school.ac.th</span></li>
                        <li><i class="fa-solid fa-phone"></i> <span>08x-xxx-xxxx (ติดต่อเพื่อการศึกษา)</span></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 นางสาวมนฤทัย บานแย้ม. All Rights Reserved. | พัฒนาด้วยความมุ่งมั่น 💻</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // 1. Mobile Menu Toggle
        const menuToggle = document.getElementById('menu-toggle');
        const navMenu = document.getElementById('nav-menu');

        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('active');
            const icon = menuToggle.querySelector('i');
            if(navMenu.classList.contains('active')) {
                icon.className = 'fa-solid fa-xmark';
            } else {
                icon.className = 'fa-solid fa-bars';
            }
        });

        // Close menu when link is clicked (Mobile)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
                menuToggle.querySelector('i').className = 'fa-solid fa-bars';
            });
        });

        // 2. Active Scroll Link Highlighting & Header Scroll Effect
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-links a:not(.btn-github)');
        const header = document.getElementById('header');

        window.addEventListener('scroll', () => {
            // Header height shrinkage on scroll
            if (window.scrollY > 50) {
                header.style.padding = '5px 0';
                header.style.boxShadow = '0 10px 15px -3px rgba(0, 0, 0, 0.05)';
            } else {
                header.style.padding = '0';
                header.style.boxShadow = '0 2px 10px rgba(0,0,0,0.05)';
            }

            // Highlighting active section based on scroll position
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= (sectionTop - 120)) {
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

        // 3. Filtering Works System
        const filterBtns = document.querySelectorAll('.filter-btn');
        const workCards = document.querySelectorAll('.work-card');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Change active button style
                filterBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');

                // Filter cards based on category
                const filterValue = btn.getAttribute('data-filter');
                
                workCards.forEach(card => {
                    if (filterValue === 'all' || card.getAttribute('data-category') === filterValue) {
                        card.style.display = 'flex';
                        // Add fade-in animation
                        card.style.animation = 'fadeIn 0.5s ease forwards';
                    } else {
                        card.style.display = 'none';
                    }
                });
            });
        });

        // Define fadeIn animation on the fly
        const style = document.createElement('style');
        style.innerHTML = `
            @keyframes fadeIn {
                from { opacity: 0; transform: translateY(10px); }
                to { opacity: 1; transform: translateY(0); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
