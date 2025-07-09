<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your English Mentor (YEM) - Nâng Tầm Tiếng Anh Cùng Chuyên Gia IELTS</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary-color: #00897B; /* Teal - Màu xanh ngọc lam chủ đạo */
            --secondary-color: #FF7043; /* Coral - Màu cam đào, năng động */
            --accent-color: #FFC107; /* Amber/Gold - Vàng hổ phách cho điểm nhấn/CTA */
            --text-dark: #37474F; /* Dark Slate Gray - Màu chữ tối, ấm */
            --text-light: #ECF0F1; /* Light Gray - Màu chữ sáng */
            --bg-light: #F8F9FA; /* Off-white background */
            --bg-medium: #E0F2F1; /* Light Teal for alternating sections */
            --bg-dark: #263238; /* Dark Blue Gray for footer */
            --card-bg: #FFFFFF; /* White for content cards */
            --header-gradient: linear-gradient(135deg, #004D40 0%, #00897B 100%); /* Giữ nguyên xanh ban đầu cho header */
            --sale-gradient: linear-gradient(135deg, #FF5722 0%, #FFAB91 100%); /* Orange Red to Light Orange */
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
            scroll-behavior: smooth;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        /* --- Navigation Bar --- */
        .navbar {
            background-color: white;
            padding: 15px 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8em;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .navbar ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .navbar ul li {
                margin-left: 30px;
        }

        .navbar ul li a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 1.1em;
            transition: color 0.3s ease;
        }

        .navbar ul li a:hover {
            color: var(--primary-color);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            z-index: 1001;
        }

        .menu-toggle span {
            height: 3px;
            width: 25px;
            background-color: var(--text-dark);
            margin-bottom: 4px;
            border-radius: 2px;
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }
            .navbar ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 60px; /* Adjust based on navbar height */
                left: 0;
                width: 100%;
                background-color: white;
                box-shadow: 0 8px 16px rgba(0,0,0,0.1);
                padding: 20px 0;
                border-top: 1px solid #eee;
            }
            .navbar ul.active {
                display: flex;
            }
            .navbar ul li {
                margin: 10px 20px;
                text-align: center;
            }
            .navbar ul li a {
                padding: 10px 0;
                display: block;
            }
        }


        /* --- Header --- */
        header {
            background: var(--header-gradient); /* Giữ nguyên gradient xanh ban đầu */
            color: white;
            padding: 100px 20px 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
            animation: fadeIn 1s ease-out;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        header h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4em;
            margin: 0;
            letter-spacing: 2px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.6em;
            margin-top: 20px;
            font-weight: 300;
            opacity: 0.9;
        }

        .button {
            display: inline-block;
            background: var(--accent-color);
            color: var(--text-dark);
            padding: 15px 35px;
            border-radius: 50px;
            margin-top: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1em;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            border: none;
        }

        .button:hover {
            background: #FFD254; /* Lighter amber on hover */
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }

        /* --- Global Section Styling --- */
        .section {
            padding: 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .section:nth-of-type(odd) { /* Alternating background for sections */
            background-color: var(--bg-light);
        }

        .section:nth-of-type(even) {
            background-color: var(--bg-medium);
        }

        .section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.8em;
            color: var(--primary-color);
            margin-bottom: 40px;
            position: relative;
            padding-bottom: 15px;
        }

        .section h2::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color); /* Coral underline */
            border-radius: 2px;
        }

        /* --- Features Section --- */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .feature {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
            border-bottom: 5px solid var(--primary-color); /* Teal border */
        }

        .feature:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
            border-color: var(--secondary-color); /* Coral on hover */
        }

        .feature h3 {
            color: var(--primary-color);
            font-size: 1.6em;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .feature h3 i {
            margin-right: 10px;
            color: var(--secondary-color); /* Coral icon */
            font-size: 1.5em; /* Larger icon */
            transition: transform 0.3s ease;
        }
        .feature:hover h3 i {
            transform: scale(1.1); /* Slight grow on icon hover */
        }

        .feature p {
            font-size: 1.1em;
            color: var(--text-dark);
        }

        /* --- Mentor Section --- */
        .mentors {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .mentor {
            text-align: center;
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .mentor:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.12);
        }

        .mentor img {
            border-radius: 50%;
            width: 140px;
            height: 140px;
            object-fit: cover;
            border: 4px solid var(--primary-color);
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
            transition: border-color 0.3s ease;
        }
        .mentor:hover img {
            border-color: var(--secondary-color);
        }

        .mentor h4 {
            margin: 15px 0 8px;
            color: var(--text-dark);
            font-size: 1.5em;
            font-family: 'Montserrat', sans-serif;
        }

        .mentor p {
            font-size: 1.1em;
            color: var(--primary-color);
            font-weight: 600;
        }

        /* --- Testimonials Section (New Design) --- */
        #cam-nhan {
            background-color: var(--bg-medium); /* Use alternating background */
            position: relative;
            padding: 100px 20px;
        }

        .testimonials-container {
            display: flex;
            overflow-x: auto; /* Enable horizontal scrolling */
            scroll-snap-type: x mandatory;
            -webkit-overflow-scrolling: touch;
            padding-bottom: 20px; /* Space for scrollbar */
            gap: 30px;
            justify-content: flex-start; /* Align items to start */
        }

        .testimonial-card {
            flex: 0 0 350px; /* Fixed width for cards, adjust as needed */
            background: var(--card-bg);
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
            padding: 30px;
            text-align: left;
            scroll-snap-align: start;
            border-top: 5px solid var(--secondary-color); /* Coral top border */
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.12);
        }

        .testimonial-card .quote-icon {
            font-size: 2.5em;
            color: var(--primary-color);
            margin-bottom: 15px;
            display: block;
        }

        .testimonial-card p {
            font-size: 1.05em;
            color: var(--text-dark);
            margin-bottom: 15px;
            font-style: italic;
        }

        .testimonial-card .author-info {
            display: flex;
            align-items: center;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px dashed #eee;
        }

        .testimonial-card .author-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
            border: 2px solid var(--primary-color);
        }

        .testimonial-card .author-name {
            font-weight: 600;
            color: var(--primary-color);
            font-size: 1.1em;
        }

        .testimonial-card .author-title {
            font-size: 0.9em;
            color: #666;
        }


        /* --- Social Media Section (New Design) --- */
        #mang-xa-hoi {
            background-color: var(--bg-light); /* Use alternating background */
            padding: 80px 20px;
        }

        .social-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .social-item {
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: var(--text-dark);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .social-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }

        .social-item i {
            font-size: 3.5em;
            margin-bottom: 15px;
            color: var(--primary-color);
            transition: color 0.3s ease;
        }

        .social-item:hover i {
            color: var(--secondary-color);
        }

        .social-item span {
            font-weight: 600;
            font-size: 1.2em;
        }
        /* Specific social colors */
        .social-item.facebook i { color: #3b5998; }
        .social-item.facebook:hover i { color: #2d4373; }

        .social-item.tiktok i { color: #000; } /* TikTok's main color is black */
        .social-item.tiktok:hover i { color: #FE2C55; } /* TikTok's brand red */

        .social-item.youtube i { color: #FF0000; }
        .social-item.youtube:hover i { color: #CC0000; }

        .social-item.instagram i {
            background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .social-item.instagram:hover i {
            filter: brightness(1.2);
        }


        /* --- Sale Box --- */
        .sale-box {
            background: none; /* Remove any background color/image */
            padding: 0; /* Remove padding as the image itself will have dimensions */
            border-radius: 20px;
            margin: 60px auto;
            max-width: 900px; /* Controls the max width of the container for the image */
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden; /* Ensures image corners are clipped by border-radius */
            animation: bounceIn 1s ease-out;
            border: none;
            transform: rotateZ(-1deg);
            transition: transform 0.3s ease;
            text-align: center; /* Centers the image */
        }

        .sale-box:hover {
            transform: rotateZ(0deg); /* Straighten on hover */
        }

        /* Style for the image inside the sale-box */
        .sale-box img {
            width: 100%; /* Make the image fill the width of its container (sale-box) */
            height: auto; /* Maintain aspect ratio */
            display: block; /* Remove extra space below image */
            border-radius: 20px; /* Apply border-radius to the image itself */
        }

        /* Remove any pseudo-elements if they were defined for sale-box as they won't apply to the image */
        .sale-box::before, .sale-box::after {
            content: none;
        }

        /* Remove or adjust these if they were meant for text within the box */
        .sale-box h2,
        .sale-box .subtitle,
        .sale-box .gift-text,
        .sale-box .discount-line {
            display: none; /* Hide any previous text elements */
        }

        .sale-box a.button {
             display: none; /* Hide button if image contains CTA */
        }

        /* NEW: Small consultation bar */
        .small-consultation-wrapper {
            text-align: center; /* Đảm bảo thẻ span bên trong được căn giữa */
            margin-top: 40px; /* Khoảng cách từ section phía trên */
            margin-bottom: 20px; /* Thêm khoảng cách dưới cho đẹp mắt */
        }

                .small-consultation-wrapper span {
            background-color: transparent; /* bỏ nền */
            color: var(--primary-color); /* chữ xanh */
            font-size: 0.9em;
            font-weight: 600;
            border: 2px solid var(--primary-color); /* viền xanh */
            border-radius: 50px; /* bo tròn nhiều hơn */
            padding: 6px 16px; /* nút to gọn */
            display: inline-block;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .small-consultation-wrapper span:hover {
            background-color: var(--primary-color);
            color: white;
         }


        /* Responsive cho small-consultation-wrapper */
        @media (max-width: 768px) {
            .small-consultation-wrapper span {
                padding: 3px 7px; /* Giảm padding thêm cho mobile */
                font-size: 0.65em; /* Giảm font-size thêm cho mobile */
                letter-spacing: normal; /* Đặt lại normal cho mobile */
            }
        }


        /* --- Footer --- */
        footer {
            background: var(--bg-dark);
            color: var(--text-light);
            text-align: center;
            padding: 40px 20px;
            font-size: 1em;
            border-top: 5px solid var(--primary-color);
        }

        footer p {
            margin: 8px 0;
        }

        footer a {
            color: var(--accent-color);
            text-decoration: none;
            transition: color 0.3s;
        }

        footer a:hover {
            color: white;
        }

        /* --- Animations --- */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes bounceIn {
            0% { transform: scale(0.8); opacity: 0; }
            50% { transform: scale(1.05); opacity: 1; }
            100% { transform: scale(1); }
        }

        /* --- Responsive Design --- */
        @media (max-width: 768px) {
            header h1 { font-size: 2.8em; }
            header p { font-size: 1.4em; }
            .section h2 { font-size: 2.2em; }
            .features, .mentors {
                grid-template-columns: 1fr;
            }
            .feature, .mentor {
                margin-bottom: 20px;
            }
            .sale-box {
                padding: 30px;
                font-size: 0.9em;
            }
            .sale-box h2 {
                font-size: 2.2em;
            }
            .sale-box .subtitle {
                font-size: 1.4em;
            }
            .testimonials-container {
                flex-wrap: nowrap; /* Keep cards in a single row for horizontal scroll */
                justify-content: flex-start;
            }
            .testimonial-card {
                flex: 0 0 90%; /* Make cards take up more width on small screens */
            }
            .social-grid {
                grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            }
            .social-item i {
                font-size: 3em;
            }
            .social-item span {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <a href="#home" class="logo">YEM</a>
        <div class="menu-toggle" id="mobile-menu">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <ul class="nav-links">
            <li><a href="a.html">HOME</a></li>
            <li><a href="about.html">GIỚI THIỆU</a></li>
            <li><a href="courses.html">KHÓA HỌC</a></li>
        </ul>
    </nav>

    <header id="home">
        <h1>Your English Mentor</h1>
        <p>Nâng tầm tiếng Anh, kiến tạo tương lai cùng IELTS!</p>
    </header>

    <div class="section" id="gioi-thieu">
        <h2>Vì sao hàng ngàn học viên lựa chọn YEM?</h2>
        <div class="features">
            <div class="feature">
                <h3><i class="fas fa-route"></i> Cá nhân hoá lộ trình</h3>
                <p>Thiết kế riêng biệt, phù hợp với mục tiêu và năng lực của từng học viên, tối ưu hóa quá trình học.</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-user-graduate"></i> Đội ngũ Mentor 7.5+</h3>
                <p>Giáo viên IELTS 7.5+ dày dặn kinh nghiệm, tâm huyết, luôn sẵn sàng đồng hành cùng bạn.</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-wallet"></i> Học phí hợp lý</h3>
                <p>Chính sách học phí linh hoạt, phù hợp với ngân sách của sinh viên và mọi đối tượng.</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-lightbulb"></i> Phương pháp hiện đại</h3>
                <p>Áp dụng phương pháp giảng dạy tiên tiến, giúp bạn học nhanh, nhớ lâu và áp dụng hiệu quả.</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-users"></i> Lớp học tinh gọn</h3>
                <p>Chỉ tối đa 5 học viên/lớp, đảm bảo tương tác tối đa, cá nhân hóa cao và hiệu quả vượt trội.</p>
               </div>
        </div>
    </div>

    <div class="section" id="khoa-hoc">
        <h2>Gặp gỡ đội ngũ Mentor xuất sắc của YEM</h2>
        <div class="mentors">
            <div class="mentor">
                <img src="nnk.png" alt="Nguyễn Ngọc Khánh">
                <h4>Nguyễn Ngọc Khánh</h4>
                <p>IELTS 8.0 Overall</p>
            </div>
            <div class="mentor">
                <img src="đpl.png" alt="Đặng Phương Linh">
                <h4>Đặng Phương Linh</h4>
                <p>IELTS 8.0 Overall</p>
            </div>
            <div class="mentor">
                <img src="hpt.png" alt="Hoàng Phương Thảo">
                <h4>Hoàng Phương Thảo</h4>
                <p>IELTS 8.0 Overall</p>
            </div>
        </div>
    </div>

    <div class="section" id="cam-nhan">
        <h2>Học viên nói gì về YEM?</h2>
        <div class="testimonials-container">
            <div class="testimonial-card">
                <i class="fas fa-quote-left quote-icon"></i>
                <p>"YEM là lựa chọn đúng đắn nhất của tôi! Lộ trình cá nhân hóa giúp tôi đạt band điểm mong muốn nhanh hơn dự kiến. Các thầy cô vô cùng nhiệt tình và kiến thức chuyên sâu."</p>
                <div class="author-info">
                    <div>
                        <div class="author-name">Nguyễn Văn A</div>
                        <div class="author-title">IELTS 7.0 Overall</div>
                    </div>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fas fa-quote-left quote-icon"></i>
                <p>"Phương pháp giảng dạy của YEM rất hiện đại, dễ hiểu và thực tế. Các lớp học nhóm nhỏ giúp tôi tương tác nhiều hơn và nhận được sự hỗ trợ sát sao từ mentor."</p>
                <div class="author-info">
                    <div>
                        <div class="author-name">Nguyễn Văn B</div>
                        <div class="author-title">IELTS 7.5 Overall</div>
                    </div>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fas fa-quote-left quote-icon"></i>
                <p>"Học phí rất hợp lý so với chất lượng đào tạo. YEM không chỉ dạy tiếng Anh mà còn truyền cảm hứng, giúp tôi tự tin hơn rất nhiều khi giao tiếp."</p>
                <div class="author-info">
                    <div>
                        <div class="author-name">Nguyễn Văn C</div>
                        <div class="author-title">IELTS 6.5 Overall</div>
                    </div>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fas fa-quote-left quote-icon"></i>
                <p>"Mình rất thích cách YEM thiết kế lộ trình riêng cho từng bạn. Điều đó giúp mình tập trung vào điểm yếu và phát triển đúng hướng. Highly recommend!"</p>
                <div class="author-info">
                    <div>
                        <div class="author-name">Nguyễn Văn D</div>
                        <div class="author-title">IELTS 7.0 Overall</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="section" id="uu-dai">
        <h2>Ưu đãi đặc biệt dành riêng cho bạn!</h2>
        <div class="sale-box">
            <img src="cm1.jpg" alt="Ưu đãi YEM">
        </div>
    </div>
    <<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Ưu đãi Giáng Sinh từ YEM</title>
  <style>
    body {
      background-color: #f9f9f9;
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 30px;
    }
    img {
      width: 80%;
      max-width: 800px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
    }
    h1 {
      color: #b30000;
      margin-bottom: 10px;
    }
    p {
      font-size: 18px;
      color: #333;
      margin-bottom: 30px;
    }
  </style>
</head>
<body>
  <h1>🎄 Mừng Giáng Sinh & Năm Mới 🎁</h1>
  <p>Ưu đãi lớn từ YEM – Tất cả trong mùa lễ hội!</p>
  <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD..." alt="Khuyến mãi từ YEM">
    <div class="section" id="mang-xa-hoi">
        <h2>Kết nối với YEM trên mạng xã hội</h2>
        <div class="social-grid">
            <a href="https://www.facebook.com/people/Your-English-Mentor-YEM/61565666090833/" target="_blank" class="social-item facebook">
                <i class="fab fa-facebook-f"></i>
                <span>Facebook</span>
            </a>
            <a href="https://www.tiktok.com/@yourenglishmentor.yem?" target="_blank" class="social-item tiktok">
                <i class="fab fa-tiktok"></i>
                <span>TikTok</span>
            </a>
            <a href="https://www.youtube.com/@yourenglishmentor-yem" target="_blank" class="social-item youtube">
                <i class="fab fa-youtube"></i>
                <span>YouTube</span>
            </a>
            <a href="https://www.instagram.com/yourenglishmentor.yem" target="_blank" class="social-item instagram">
                <i class="fab fa-instagram"></i>
                <span>Instagram</span>
            </a>
        </div>
    </div>

    <div class="small-consultation-wrapper">
        <span>Đăng ký tư vấn tại đây</span>
    </div>
    <footer>
        <p><strong>Your English Mentor (YEM)</strong> - Nâng tầm tiếng Anh của bạn!</p>
        <p>Liên hệ: <a href="mailto:yourenglishmentor.vn@gmail.com">yourenglishmentor.vn@gmail.com</a> | Hotline: <a href="tel:0822901266">0822 901 266 (Ms Mai Anh)</a></p>
        <p>© 2025 Your English Mentor. All rights reserved.</p>
    </footer>

    <script>
        // JavaScript for mobile menu toggle
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.querySelector('.nav-links');

        mobileMenu.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close menu when a link is clicked (for smooth scroll)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Your English Mentor (YEM) - Nâng Tầm Tiếng Anh</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Montserrat:wght@600;700&display=swap" rel="stylesheet" />
    <style>
        :root {
            --primary-color: #00897B; /* Teal - Màu xanh ngọc lam chủ đạo */
            --secondary-color: #FF7043; /* Coral - Màu cam đào, năng động */
            --accent-color: #FFC107; /* Amber/Gold - Vàng hổ phách cho điểm nhấn/CTA */
            --text-dark: #37474F; /* Dark Slate Gray - Màu chữ tối, ấm */
            --text-light: #ECF0F1; /* Light Gray - Màu chữ sáng */
            --bg-light: #F8F9FA; /* Off-white background */
            --bg-medium: #E0F2F1; /* Light Teal for alternating sections */
            --bg-dark: #263238; /* Dark Blue Gray for footer */
            --card-bg: #FFFFFF; /* White for content cards */
            --header-gradient: linear-gradient(135deg, #004D40 0%, #00897B 100%); /* Giữ nguyên xanh ban đầu cho header */
            --sale-gradient: linear-gradient(135deg, #FF5722 0%, #FFAB91 100%); /* Orange Red to Light Orange */
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
            scroll-behavior: smooth;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }
        
        /* --- Navigation Bar --- */
        .navbar {
            background-color: white;
            padding: 15px 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8em;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .navbar ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .navbar ul li {
                margin-left: 30px;
        }

        .navbar ul li a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 1.1em;
            transition: color 0.3s ease;
        }

        .navbar ul li a:hover {
            color: var(--primary-color);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            z-index: 1001;
        }

        .menu-toggle span {
            height: 3px;
            width: 25px;
            background-color: var(--text-dark);
            margin-bottom: 4px;
            border-radius: 2px;
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }
            .navbar ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 60px; /* Adjust based on navbar height */
                left: 0;
                width: 100%;
                background-color: white;
                box-shadow: 0 8px 16px rgba(0,0,0,0.1);
                padding: 20px 0;
                border-top: 1px solid #eee;
            }
            .navbar ul.active {
                display: flex;
            }
            .navbar ul li {
                margin: 10px 20px;
                text-align: center;
            }
            .navbar ul li a {
                padding: 10px 0;
                display: block;
            }
        }


        /* --- Header --- */
        header {
            background: var(--header-gradient); /* Giữ nguyên gradient xanh ban đầu */
            color: white;
            padding: 100px 20px 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
            animation: fadeIn 1s ease-out;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        header h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4em;
            margin: 0;
            letter-spacing: 2px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.6em;
            margin-top: 20px;
            font-weight: 300;
            opacity: 0.9;
        }

        .button {
            display: inline-block;
            background: var(--accent-color);
            color: var(--text-dark);
            padding: 15px 35px;
            border-radius: 50px;
            margin-top: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1em;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            border: none;
        }

        .button:hover {
            background: #FFD254; /* Lighter amber on hover */
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }
        section {
            padding: 60px 20px;
            max-width: 900px;
            margin: auto;
            text-align: center;
        }
        section:nth-of-type(even) {
            background: var(--bg-alt);
        }
        section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5em; /* TO HƠN */
            color: var(--primary-color);
            margin-bottom: 25px;
        }
        section h3 {
            font-size: 1.5em; /* TO HƠN */
            color: var(--accent-color);
            margin-top: 25px;
        }
        section p, section li {
            font-size: 1.2em; /* TO HƠN */
            max-width: 700px;
            margin: 10px auto;
        }
        section ul {
            list-style: none;
            padding-left: 0;
        }
        section li::before {
            content: "• ";
            color: var(--primary-color);
            font-weight: bold;
        }
        footer {
            background: #263238;
            color: var(--text-light);
            padding: 30px 20px;
            font-size: 1em;
            text-align: center;
        }
        footer a {
            color: var(--accent-color);
            text-decoration: none;
        }
        footer a:hover {
            color: #FFD180;
        }
        @media (max-width: 768px) {
            body {
                font-size: 1.1em;
            }
            header h1 {
                font-size: 2.2em;
            }
            header p {
                font-size: 1.2em;
            }
            section h2 {
                font-size: 2em;
            }
            section h3 {
                font-size: 1.3em;
            }
            section p, section li {
                font-size: 1.1em;
            }
            .menu-toggle {
                display: flex;
            }
            .nav-links {
                display: none;
                flex-direction: column;
                background: var(--bg-light);
                position: absolute;
                top: 70px;
                right: 20px;
                padding: 10px;
                border-radius: 8px;
                box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            }
            .nav-links.active {
                display: flex;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <a href="#home" class="logo">YEM</a>
        <div class="menu-toggle" id="mobile-menu">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <ul class="nav-links">
            <li><a href="a.html">HOME</a></li>
            <li><a href="about.html">GIỚI THIỆU</a></li>
            <li><a href="courses.html">KHÓA HỌC</a></li>
        </ul>
    </nav>

    <header id="home">
        <h1>Your English Mentor</h1>
        <p>Nâng tầm tiếng Anh, kiến tạo tương lai cùng IELTS!</p>
    </header>

    <section>
        <h2>GIỚI THIỆU VỀ YEM</h2>
        <h3>Giải pháp toàn diện cho hành trình học IELTS của bạn</h3>
        <p>Với đội ngũ giáo viên và mentor IELTS từ 7.5 trở lên, giàu kinh nghiệm và nhiệt huyết, YEM cam kết đồng hành cùng bạn xuyên suốt quá trình học, giúp bạn chinh phục IELTS một cách dễ dàng và hiệu quả.</p>
        <p>Chúng tôi áp dụng phương pháp giảng dạy hiện đại như Sơ đồ tư duy, Kỹ thuật Logic, Đọc hiểu nhanh, Liên tưởng hình ảnh và Học siêu tốc để bạn tiếp thu kiến thức tự nhiên, dễ nhớ, dễ ứng dụng vào bài thi thực tế.</p>
        <p>Đặc biệt, bạn sẽ được làm đề test IELTS 4 kỹ năng miễn phí và nhận lộ trình học tập cá nhân hóa, được thiết kế riêng bởi đội ngũ mentor của YEM, đảm bảo phù hợp với mục tiêu và năng lực của bạn.</p>
        <h3>Tầm nhìn của YEM</h3>
        <p>Trở thành nền tảng EdTech đào tạo tiếng Anh hàng đầu cho người Việt, giúp người học nâng cao kỹ năng tiếng Anh học thuật và ứng dụng trong công việc, cuộc sống, chinh phục chứng chỉ quốc tế và vươn xa ra thế giới.</p>
        <h3>Sứ mệnh của YEM</h3>
        <ul>
            <li>Đồng hành cùng người học chinh phục IELTS với lộ trình tối ưu, phương pháp khoa học và chi phí phù hợp.</li>
            <li>Tạo ra cộng đồng học tập tiếng Anh tích cực, hỗ trợ nhau phát triển toàn diện.</li>
            <li>Nâng cao năng lực tiếng Anh cho thế hệ trẻ Việt Nam, mở rộng cơ hội học tập và làm việc toàn cầu.</li>
        </ul>
    </section>

    <footer>
        <p><strong>Your English Mentor (YEM)</strong> - Nâng tầm tiếng Anh của bạn!</p>
        <p>Liên hệ: <a href="mailto:yourenglishmentor.vn@gmail.com">yourenglishmentor.vn@gmail.com</a> | Hotline: <a href="tel:0822901266">0822 901 266 (Ms Mai Anh)</a></p>
        <p>© 2025 Your English Mentor. All rights reserved.</p>
    </footer>

    <script>
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.querySelector('.nav-links');
        mobileMenu.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your English Mentor (YEM) - Nâng Tầm Tiếng Anh Cùng Chuyên Gia IELTS</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Đảm bảo ảnh trong .picture không bị tràn ra ngoài body */
.picture {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    overflow: hidden;
    margin: 0 auto;
    max-width: 100vw;
}
.picture img {
    max-width: 100%;
    height: auto;
    display: block;
    border-radius: 12px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.08);
}

        :root {
            --primary-color: #00897B; /* Teal - Màu xanh ngọc lam chủ đạo */
            --secondary-color: #FF7043; /* Coral - Màu cam đào, năng động */
            --accent-color: #FFC107; /* Amber/Gold - Vàng hổ phách cho điểm nhấn/CTA */
            --text-dark: #37474F; /* Dark Slate Gray - Màu chữ tối, ấm */
            --text-light: #ECF0F1; /* Light Gray - Màu chữ sáng */
            --bg-light: #F8F9FA; /* Off-white background */
            --bg-medium: #E0F2F1; /* Light Teal for alternating sections */
            --bg-dark: #263238; /* Dark Blue Gray for footer */
            --card-bg: #FFFFFF; /* White for content cards */
            --header-gradient: linear-gradient(135deg, #004D40 0%, #00897B 100%); /* Dark Teal to Teal */
            --sale-gradient: linear-gradient(135deg, #FF5722 0%, #FFAB91 100%); /* Orange Red to Light Orange */
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
            scroll-behavior: smooth;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        /* --- Navigation Bar --- */
        .navbar {
            background-color: white;
            padding: 15px 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8em;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .navbar ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .navbar ul li {
            margin-left: 30px;
        }

        .navbar ul li a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 1.1em;
            transition: color 0.3s ease;
        }

        .navbar ul li a:hover {
            color: var(--primary-color);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            z-index: 1001;
        }

        .menu-toggle span {
            height: 3px;
            width: 25px;
            background-color: var(--text-dark);
            margin-bottom: 4px;
            border-radius: 2px;
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }
            .navbar ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 60px; /* Adjust based on navbar height */
                left: 0;
                width: 100%;
                background-color: white;
                box-shadow: 0 8px 16px rgba(0,0,0,0.1);
                padding: 20px 0;
                border-top: 1px solid #eee;
            }
            .navbar ul.active {
                display: flex;
            }
            .navbar ul li {
                margin: 10px 20px;
                text-align: center;
            }
            .navbar ul li a {
                padding: 10px 0;
                display: block;
            }
        }


        /* --- Header --- */
        header {
            background: var(--header-gradient);
            color: white;
            padding: 100px 20px 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
            animation: fadeIn 1s ease-out;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        header h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4em;
            margin: 0;
            letter-spacing: 2px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.6em;
            margin-top: 20px;
            font-weight: 300;
            opacity: 0.9;
        }

        .button {
            display: inline-block;
            background: var(--accent-color);
            color: var(--text-dark);
            padding: 15px 35px;
            border-radius: 50px;
            margin-top: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1em;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            border: none;
        }

        .button:hover {
            background: #FFD254; /* Lighter amber on hover */
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }

        /* --- Global Section Styling --- */
        .section {
            padding: 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .section:nth-of-type(odd) { /* Alternating background for sections */
            background-color: var(--bg-light);
        }

        .section:nth-of-type(even) {
            background-color: var(--bg-medium);
        }

        .section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.8em;
            color: var(--primary-color);
            margin-bottom: 40px;
            position: relative;
            padding-bottom: 15px;
        }

        .section h2::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color); /* Coral underline */
            border-radius: 2px;
        }

        /* --- Features Section --- */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .feature {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
            border-bottom: 5px solid var(--primary-color); /* Teal border */
        }

        .feature:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
            border-color: var(--secondary-color); /* Coral on hover */
        }

        .feature h3 {
            color: var(--primary-color);
            font-size: 1.6em;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .feature h3 i {
            margin-right: 10px;
            color: var(--secondary-color); /* Coral icon */
            font-size: 1.5em; /* Larger icon */
            transition: transform 0.3s ease;
        }
        .feature:hover h3 i {
            transform: scale(1.1); /* Slight grow on icon hover */
        }

        .feature p {
            font-size: 1.1em;
            color: var(--text-dark);
        }

        /* --- Mentor Section --- */
        .mentors {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .mentor {
            text-align: center;
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .mentor:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.12);
        }

        .mentor img {
            border-radius: 50%;
            width: 140px;
            height: 140px;
            object-fit: cover;
            border: 4px solid var(--primary-color);
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
            transition: border-color 0.3s ease;
        }
        .mentor:hover img {
            border-color: var(--secondary-color);
        }

        .mentor h4 {
            margin: 15px 0 8px;
            color: var(--text-dark);
            font-size: 1.5em;
            font-family: 'Montserrat', sans-serif;
        }

        .mentor p {
            font-size: 1.1em;
            color: var(--primary-color);
            font-weight: 600;
        }

        /* --- Testimonials Section (New Design) --- */
        #cam-nhan {
            background-color: var(--bg-medium); /* Use alternating background */
            position: relative;
            padding: 100px 20px;
        }

        .testimonials-container {
            display: flex;
            overflow-x: auto; /* Enable horizontal scrolling */
            scroll-snap-type: x mandatory;
            -webkit-overflow-scrolling: touch;
            padding-bottom: 20px; /* Space for scrollbar */
            gap: 30px;
            justify-content: flex-start; /* Align items to start */
        }

        .testimonial-card {
            flex: 0 0 350px; /* Fixed width for cards, adjust as needed */
            background: var(--card-bg);
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
            padding: 30px;
            text-align: left;
            scroll-snap-align: start;
            border-top: 5px solid var(--secondary-color); /* Coral top border */
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.12);
        }

        .testimonial-card .quote-icon {
            font-size: 2.5em;
            color: var(--primary-color);
            margin-bottom: 15px;
            display: block;
        }

        .testimonial-card p {
            font-size: 1.05em;
            color: var(--text-dark);
            margin-bottom: 15px;
            font-style: italic;
        }

        .testimonial-card .author-info {
            display: flex;
            align-items: center;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px dashed #eee;
        }

        .testimonial-card .author-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
            border: 2px solid var(--primary-color);
        }

        .testimonial-card .author-name {
            font-weight: 600;
            color: var(--primary-color);
            font-size: 1.1em;
        }

        .testimonial-card .author-title {
            font-size: 0.9em;
            color: #666;
        }


        /* --- Social Media Section (New Design) --- */
        #mang-xa-hoi {
            background-color: var(--bg-light); /* Use alternating background */
            padding: 80px 20px;
        }

        .social-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .social-item {
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: var(--text-dark);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .social-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }

        .social-item i {
            font-size: 3.5em;
            margin-bottom: 15px;
            color: var(--primary-color);
            transition: color 0.3s ease;
        }

        .social-item:hover i {
            color: var(--secondary-color);
        }

        .social-item span {
            font-weight: 600;
            font-size: 1.2em;
        }
        /* Specific social colors */
        .social-item.facebook i { color: #3b5998; }
        .social-item.facebook:hover i { color: #2d4373; }

        .social-item.tiktok i { color: #000; } /* TikTok's main color is black */
        .social-item.tiktok:hover i { color: #FE2C55; } /* TikTok's brand red */

        .social-item.youtube i { color: #FF0000; }
        .social-item.youtube:hover i { color: #CC0000; }

        .social-item.instagram i {
            background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .social-item.instagram:hover i {
            filter: brightness(1.2);
        }


        /* --- Sale Box --- */
        .sale-box {
            background: var(--sale-gradient);
            color: white;
            padding: 50px;
            border-radius: 20px;
            margin: 60px auto;
            max-width: 900px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden;
            animation: bounceIn 1s ease-out;
            border: none; /* Remove dashed border */
            transform: rotateZ(-1deg); /* Slight playful tilt */
            transition: transform 0.3s ease;
        }

        .sale-box:hover {
            transform: rotateZ(0deg); /* Straighten on hover */
        }

        .sale-box::before, .sale-box::after {
            content: ''; /* Remove specific emoji content */
            position: absolute;
            opacity: 0.1;
            font-size: 10em;
            color: white;
            z-index: 0;
            pointer-events: none;
        }
        .sale-box::before {
            content: '🌟'; /* Star */
            top: -20px;
            left: -20px;
            transform: rotate(20deg);
        }
        .sale-box::after {
            content: '🎁'; /* Gift */
            bottom: -20px;
            right: -20px;
            transform: rotate(-30deg);
        }


        .sale-box h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 3em;
            color: white;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            z-index: 1; /* Ensure text is above pseudo-elements */
            position: relative;
        }
        .sale-box .subtitle {
            font-size: 1.6em;
            margin-top: -10px;
            margin-bottom: 25px;
            font-weight: 500;
            color: var(--text-light); /* Lighter text for subtitle */
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .sale-box p {
            font-size: 1.5em;
            margin-bottom: 15px;
            font-weight: 400;
            z-index: 1;
            position: relative;
        }

        .sale-box strong {
            color: var(--accent-color);
            font-size: 1.2em;
            font-weight: 700;
        }

        /* --- Footer --- */
        footer {
            background: var(--bg-dark);
            color: var(--text-light);
            text-align: center;
            padding: 40px 20px;
            font-size: 1em;
            border-top: 5px solid var(--primary-color);
        }

        footer p {
            margin: 8px 0;
        }

        footer a {
            color: var(--accent-color);
            text-decoration: none;
            transition: color 0.3s;
        }

        footer a:hover {
            color: white;
        }

        /* --- Animations --- */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes bounceIn {
            0% { transform: scale(0.8); opacity: 0; }
            50% { transform: scale(1.05); opacity: 1; }
            100% { transform: scale(1); }
        }

        /* --- Responsive Design --- */
        @media (max-width: 768px) {
            header h1 { font-size: 2.8em; }
            header p { font-size: 1.4em; }
            .section h2 { font-size: 2.2em; }
            .features, .mentors {
                grid-template-columns: 1fr;
            }
            .feature, .mentor {
                margin-bottom: 20px;
            }
            .sale-box {
                padding: 30px;
                font-size: 0.9em;
            }
            .sale-box h2 {
                font-size: 2.2em;
            }
            .sale-box .subtitle {
                font-size: 1.4em;
            }
            .testimonials-container {
                flex-wrap: nowrap; /* Keep cards in a single row for horizontal scroll */
                justify-content: flex-start;
            }
            .testimonial-card {
                flex: 0 0 90%; /* Make cards take up more width on small screens */
            }
            .social-grid {
                grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            }
            .social-item i {
                font-size: 3em;
            }
            .social-item span {
                font-size: 1em;
            }
        }

    </style>
</head>
<body>
    <nav class="navbar">
        <a href="#home" class="logo">YEM</a>
        <div class="menu-toggle" id="mobile-menu">
            <span></span>   
            <span></span>
            <span></span>
        </div>
        <ul class="nav-links">
            <li><a href="a.html">HOME</a></li>
            <li><a href="about.html">GIỚI THIỆU</a></li>
            <li><a href="courses.html">KHÓA HỌC</a></li>
        </ul>
    </nav>

    <div class="section" id="doi-tuong">
        <h2>Đối tượng </h2>
        <ul>
            <li><strong>Học sinh cấp 3</strong>: Chuẩn bị cho kỳ thi IELTS để du học hoặc xét tuyển đại học.</li>
            <li><strong>Sinh viên đại học</strong>: Nâng cao kỹ năng tiếng Anh để đáp ứng yêu cầu học tập và nghề nghiệp.</li>
            <li><strong>Người đi làm</strong>: Cải thiện khả năng giao tiếp tiếng Anh trong công việc và thăng tiến sự nghiệp.</li>
            <li><strong>Người mới bắt đầu</strong>: Xây dựng nền tảng tiếng Anh vững chắc từ cơ bản đến nâng cao.</li>
        </ul>
    </div>
    <div class="section" id="gioi-thieu">
        <h2>Các khóa học</h2>
        <div class="features">
            <div class="feature">
                <h3><i class="fas fa-route"></i>Khóa 0.0 - 3.0</h3>
                <p>24 Buổi</p>
                <p>(1.5h/buổi)</p>
                <p>Học phí: 4.500.000đ</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-user-graduate"></i>Khóa 3.0 - 5.0</h3>
                <p>24 Buổi</p>
                <p>(1.5h/buổi)</p>
                <p>Học phí: 4.500.000đ</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-wallet"></i>Khóa 5.0-6.5</h3>
                <p>24 Buổi</p>
                <p>(1.5h/buổi)</p>
                <p>Học phí: 4.875.000đ</p>
            </div>
            <div class="feature">
                <h3><i class="fas fa-lightbulb"></i> Khóa 7.0+</h3>
                <p>24 Buổi</p>
                <p>(1.5h/buổi)</p>
                <p>Học phí: 6.000.000đ</p>
            </div>
        </div>
    </div>

    <div class="section" id="luu-y">
        <h2>Lưu ý</h2>
        <p>Các khóa đều có bài kiểm tra giữa khóa và cuối khóa để đánh giá tiến độ học và đảm bảo đầu ra của Học viên</p>
        <p>Thời gian học tập được điều chỉnh cá nhân hoá để tối ưu nhất với trình độ của từng học viên.</p>
    </div>

    <div class="section" id="live-stream">
        <div class="picture">
            <img src="https://scontent.fhan15-2.fna.fbcdn.net/v/t39.30808-6/458270115_122093363240522203_4234998061404100579_n.png?stp=dst-jpg_tt6&_nc_cat=103&ccb=1-7&_nc_sid=86c6b0&_nc_ohc=6U2BVUJFn3oQ7kNvwGDGZEe&_nc_oc=Adlpe-swDfoauadHwQgzmpfAM7fDnPE7RcjxFYds7BR7YRxAzlniHXuWAMMsj2psrJd0r5gfOwP0dyEh7FBYYLko&_nc_zt=23&_nc_ht=scontent.fhan15-2.fna&_nc_gid=VmqmFCLupZoojqOsEQ4VFA&oh=00_AfQKylHpx_CIoubo2-5as3IwpnEgJ8YgyWD3rYoUkFLX3w&oe=686F09C1" alt="picture">
        </div>
    </div>

    <div class="section" id="mang-xa-hoi">
        <h2>Kết nối với YEM trên mạng xã hội</h2>        
        <div class="social-grid">
            <a href="https://www.facebook.com/profile.php?id=61565666090833" target="_blank" class="social-item facebook">
                <i class="fab fa-facebook-f"></i>
                <span>Facebook</span>
            </a>
            <a href="https://www.tiktok.com/@yourenglishmentor.yem?is_from_webapp=1&sender_device=pc" target="_blank" class="social-item tiktok">
                <i class="fab fa-tiktok"></i>
                <span>TikTok</span>
            </a>
            <a href="https://www.youtube.com/@yourenglishmentor-YEM" target="_blank" class="social-item youtube">
                <i class="fab fa-youtube"></i>
                <span>YouTube</span>
            </a>
            <a href="https://www.instagram.com/yourenglishmentor.yem/" target="_blank" class="social-item instagram">
                <i class="fab fa-instagram"></i>
                <span>Instagram</span>
            </a>
        </div>
    </div>

    
    <footer>
        <p><strong>Your English Mentor (YEM)</strong> - Nâng tầm tiếng Anh của bạn!</p>
        <p>Liên hệ: <a href="mailto:yourenglishmentor.vn@gmail.com ">yourenglishmentor.vn@gmail.com </a> | Hotline: <a href="tel:0822901266">0822 901 266 (Ms Mai Anh)</a></p>
    </footer>

   
</body>
</html>
