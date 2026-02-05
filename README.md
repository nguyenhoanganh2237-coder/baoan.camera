[baoan.html](https://github.com/user-attachments/files/25113930/baoan.html)
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bảo An Camera | Định Nghĩa Lại An Ninh Số</title>
    
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap" rel="stylesheet">

    <style>
        :root {
            --primary: #00f2fe;
            --secondary: #4facfe;
            --bg: #050505;
            --card-bg: rgba(255, 255, 255, 0.05);
            --text: #ffffff;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Plus Jakarta Sans', sans-serif; 
            background: var(--bg); 
            color: var(--text); 
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Nền hiệu ứng hạt lấp lánh nhẹ */
        body::before {
            content: ""; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #1a1a2e 0%, #050505 100%);
            z-index: -1;
        }

        /* Navigation */
        nav {
            padding: 20px 8%; display: flex; justify-content: space-between; align-items: center;
            position: fixed; width: 100%; top: 0; z-index: 1000;
            background: rgba(5, 5, 5, 0.8); backdrop-filter: blur(15px);
        }
        .logo { font-size: 1.5rem; font-weight: 800; background: linear-gradient(to right, var(--primary), var(--secondary)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .nav-links a { color: white; text-decoration: none; margin-left: 30px; font-weight: 500; font-size: 0.9rem; transition: 0.3s; opacity: 0.8; }
        .nav-links a:hover { opacity: 1; color: var(--primary); }

        /* Hero Section */
        .hero {
            height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            text-align: center; padding: 0 10%; position: relative;
        }
        .hero-badge { background: rgba(255,255,255,0.1); padding: 8px 20px; border-radius: 50px; font-size: 0.8rem; margin-bottom: 20px; border: 1px solid rgba(255,255,255,0.2); }
        .hero h1 { font-size: clamp(2.5rem, 8vw, 5rem); font-weight: 800; line-height: 1.1; margin-bottom: 25px; }
        .hero span { background: linear-gradient(45deg, var(--primary), var(--secondary)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .hero p { max-width: 600px; font-size: 1.1rem; opacity: 0.7; margin-bottom: 40px; }

        /* Buttons */
        .btn-grad {
            padding: 15px 40px; background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: #000; text-decoration: none; border-radius: 12px; font-weight: 700;
            transition: 0.4s; box-shadow: 0 0 20px rgba(0, 242, 254, 0.4);
        }
        .btn-grad:hover { transform: translateY(-5px); box-shadow: 0 0 40px rgba(0, 242, 254, 0.6); }

        /* Section Styling */
        section { padding: 100px 8%; }
        .section-title { font-size: 2.5rem; margin-bottom: 50px; text-align: center; }

        /* Product Cards - Glassmorphism */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .glass-card {
            background: var(--card-bg); border: 1px solid rgba(255,255,255,0.1);
            border-radius: 30px; padding: 30px; backdrop-filter: blur(10px);
            transition: 0.4s; position: relative; overflow: hidden;
        }
        .glass-card:hover { border-color: var(--primary); transform: scale(1.02); background: rgba(255,255,255,0.08); }
        .glass-card img { width: 100%; border-radius: 20px; margin-bottom: 20px; filter: grayscale(20%); transition: 0.5s; }
        .glass-card:hover img { filter: grayscale(0%); transform: scale(1.05); }
        .price { font-size: 1.8rem; font-weight: 800; color: var(--primary); display: block; margin: 15px 0; }

        /* Info Section */
        .info-box { display: flex; flex-wrap: wrap; gap: 50px; align-items: center; background: rgba(0, 242, 254, 0.03); border-radius: 40px; padding: 60px; }
        .stat-item h2 { font-size: 3rem; color: var(--primary); }

        /* Form */
        .contact-form {
            background: var(--card-bg); padding: 50px; border-radius: 30px; border: 1px solid rgba(255,255,255,0.1);
            max-width: 800px; margin: 0 auto;
        }
        input, select, textarea {
            width: 100%; padding: 15px; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);
            border-radius: 12px; color: white; margin-bottom: 20px; outline: none;
        }
        input:focus { border-color: var(--primary); }

        /* Floating Contact */
        .zalo-float {
            position: fixed; bottom: 30px; right: 30px; width: 60px; height: 60px;
            background: #0068ff; border-radius: 50%; display: flex; align-items: center;
            justify-content: center; font-size: 24px; color: white; text-decoration: none;
            box-shadow: 0 10px 30px rgba(0, 104, 255, 0.4); z-index: 1000;
        }

        footer { text-align: center; padding: 50px; opacity: 0.5; font-size: 0.8rem; border-top: 1px solid rgba(255,255,255,0.05); }

    </style>
</head>
<body>

    <nav>
        <div class="logo">BẢO AN </div>
        <div class="nav-links">
            <a href="#san-pham">SẢN PHẨM</a>
            <a href="#gioi-thieu">TẦM NHÌN</a>
            <a href="#lien-he">LIÊN HỆ</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-badge" data-aos="fade-down">CÔNG NGHỆ GIÁM SÁT 2026</div>
        <h1 data-aos="zoom-in">Mắt Thần <span>Bảo An</span><br>Kiến Tạo An Ninh</h1>
        <p data-aos="fade-up" data-aos-delay="200">Hệ sinh thái Camera AI thông minh vượt thời đại. Bảo vệ tuyệt đối, cảnh báo tức thì, hình ảnh cực đại.</p>
        <a href="#san-pham" class="btn-grad" data-aos="fade-up" data-aos-delay="400">KHÁM PHÁ NGAY</a>
    </section>

    <section id="san-pham">
        <h2 class="section-title" data-aos="fade-up">Thiết Bị Đẳng Cấp</h2>
        <div class="grid">
            <div class="glass-card" data-aos="fade-up">
                <img src="https://images.unsplash.com/photo-1557597774-9d273605dfa9?auto=format&fit=crop&w=500&q=80" alt="Camera">
                <h3>Bảo An Ultra 4K</h3>
                <span class="price">1.200.000đ</span>
                <p>Mắt đọc Sony, nhìn xuyên đêm có màu 100m.</p>
                <a href="#" class="btn-grad" style="padding: 10px 20px; font-size: 0.8rem;">CHI TIẾT</a>
            </div>
            <div class="glass-card" data-aos="fade-up" data-aos-delay="200">
                <img src="data:image/jpeg;base64,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" alt="Camera">
                <h3>Bảo An 360 AI</h3>
                <span class="price">1.850.000đ</span>
                <p>Xoay không góc chết, nhận diện khuôn mặt người quen.</p>
                <a href="#" class="btn-grad" style="padding: 10px 20px; font-size: 0.8rem;">CHI TIẾT</a>
            </div>
            <div class="glass-card" data-aos="fade-up" data-aos-delay="400">
                <img src="https://images.unsplash.com/photo-1516733725897-1aa73b87c8e8?auto=format&fit=crop&w=500&q=80" alt="Camera">
                <h3>Hệ Thống Enterprise</h3>
                <span class="price">9.900.000đ</span>
                <p>Giải pháp tổng thể cho tòa nhà và chuỗi cửa hàng.</p>
                <a href="#" class="btn-grad" style="padding: 10px 20px; font-size: 0.8rem;">CHI TIẾT</a>
            </div>
        </div>
    </section>

    <section id="gioi-thieu">
        <div class="info-box" data-aos="fade-right">
            <div style="flex: 1; min-width: 300px;">
                <h2 style="font-size: 2.5rem; margin-bottom: 20px;">Chúng tôi là <span style="color: var(--primary);">Bảo An</span></h2>
                <p style="opacity: 0.7; font-size: 1.1rem;">Không dừng lại ở việc quan sát, chúng tôi mang trí tuệ nhân tạo vào từng điểm ảnh để đảm bảo an toàn tuyệt đối cho bạn và tài sản.</p>
                <div style="display: flex; gap: 40px; margin-top: 40px;">
                    <div class="stat-item"><h2>15k</h2><p>Dự án</p></div>
                    <div class="stat-item"><h2>99%</h2><p>Hài lòng</p></div>
                </div>
            </div>
            <div style="flex: 1; min-width: 300px;">
                <img src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=800&q=80" style="width: 100%; border-radius: 30px;" alt="Tech">
            </div>
        </div>
    </section>

    <section id="lien-he">
        <h2 class="section-title">Khởi Tạo Kết Nối</h2>
        <div class="contact-form" data-aos="zoom-in">
            <form>
                <input type="text" placeholder="Tên của bạn" required>
                <input type="tel" placeholder="Số điện thoại" required>
                <select>
                    <option>Chọn dịch vụ tư vấn</option>
                    <option>Lắp đặt tại nhà</option>
                    <option>Dự án doanh nghiệp</option>
                </select>
                <textarea rows="5" placeholder="Bạn cần chúng tôi giúp gì?"></textarea>
                <button type="submit" class="btn-grad" style="width: 100%; border: none; cursor: pointer;">GỬI THÔNG ĐIỆP</button>
            </form>
        </div>
    </section>

    <footer>
        &copy; BẢO AN CAMERA - THE FUTURE OF SECURITY. DESIGNED BY GEMINI.
    </footer>

    <a href="https://www.facebook.com/cp.tienphu.2024" class="zalo-float">
        <i class="fab fa-facebook-messenger"></i>
    </a>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init({ duration: 1000, once: true });
    </script>
</body>
</html>
