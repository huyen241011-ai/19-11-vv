<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gửi phtiendat ❤️</title>
    <style>
        /* Thiết lập nền chung */
        body {
            margin: 0;
            padding: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            /* Thay background thành bầu trời hoa hồng lãng mạn */
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), 
                        url('https://unsplash.com') no-repeat center center/cover;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
        }

        /* Hiệu ứng hoa hồng/tim rơi ở nền */
        .rose-bg {
            position: absolute;
            color: rgba(255, 105, 180, 0.4);
            font-size: 20px;
            animation: fall linear infinite;
            z-index: 1;
            user-select: none;
        }
        @keyframes fall {
            0% { transform: translateY(-10vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(110vh) rotate(360deg); opacity: 0; }
        }

        /* Khung chứa thiệp lật nằm chính giữa màn hình */
        .card-container {
            position: relative;
            width: 360px;
            height: 480px;
            perspective: 1000px;
            z-index: 2;
            cursor: pointer;
        }

        .card {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transition: transform 1.2s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 20px 50px rgba(0,0,0,0.6);
            border-radius: 20px;
        }

        /* Khi rê chuột hoặc chạm vào thì lật mở thiệp */
        .card-container:hover .card {
            transform: rotateY(-180deg);
        }

        .card-front, .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 30px;
            box-sizing: border-box;
        }

        /* TRANG ĐẦU (MẶT TRƯỚC THIỆP) */
        .card-front {
            background: linear-gradient(135deg, #ff5e62, #ff9966);
            color: white;
            text-align: center;
            border: 4px solid #fff;
        }

        .card-front h1 {
            font-size: 1.6rem;
            line-height: 1.5;
            margin: 15px 0;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .main-heart {
            font-size: 70px;
            animation: beat 1.2s infinite;
        }

        @keyframes beat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }

        /* TRANG TRONG (MẶT SAU KHI MỞ RA) */
        .card-back {
            /* Mặt sau có cùng background bầu trời hoa hồng đồng bộ với nền */
            background: linear-gradient(rgba(255, 255, 255, 0.85), rgba(255, 255, 255, 0.85)), 
                        url('https://unsplash.com') no-repeat center center/cover;
            color: #333333;
            transform: rotateY(180deg);
            justify-content: flex-start;
            border: 4px solid #ff5e62;
            padding-top: 40px;
        }

        .card-back h2 {
            color: #d63031;
            font-size: 1.3rem;
            margin-bottom: 20px;
            border-bottom: 2px dashed #ff5e62;
            padding-bottom: 5px;
            width: 100%;
            text-align: center;
        }

        /* Từng dòng lời chúc */
        .letter-content {
            font-size: 1.05rem;
            line-height: 1.8;
            text-align: justify;
            font-weight: 500;
        }

        .letter-content p {
            margin: 12px 0;
        }

        .signature {
            text-align: right;
            width: 100%;
            margin-top: 25px;
            font-size: 1.2rem;
            font-weight: bold;
            color: #d63031;
            font-style: italic;
        }

        /* Gợi ý mở thiệp */
        .hint {
            position: absolute;
            bottom: 20px;
            font-size: 0.85rem;
            opacity: 0.8;
            animation: fade 1s infinite alternate;
        }
        @keyframes fade { 0% { opacity: 0.4; } 100% { opacity: 1; } }
    </style>
</head>
<body>

    <!-- Khung chứa thiệp -->
    <div class="card-container">
        <div class="card">
            
            <!-- TRANG ĐẦU CỦA BỨC THƯ -->
            <div class="card-front">
                <div class="main-heart">🌹</div>
                <h1>Chúc phtiendat,<br>ny em 19/11 vui vẻ!</h1>
                <div class="hint">Chạm hoặc di chuột để mở thư nhé... ✨</div>
            </div>
            
            <!-- TRANG Ở GIỮA KHI MỞ BỨC THƯ RA -->
            <div class="card-back">
                <h2>Gửi anh... 🤍</h2>
                <div class="letter-content">
                    <p>Nay là 19/11, em mong anh sẽ luôn mạnh khỏe, nghe lời bố mẹ, bớt game lo học và luôn quan tâm tới em.</p>
                    <p>Em biết anh kcon tcam với em nữa nhưng em mong anh vẫn có thể cố gắng bước tiếp với em.</p>
                </div>
                <div class="signature">Yêu anh! 🌹</div>
            </div>

        </div>
    </div>

    <!-- Hiệu ứng cánh hoa bay ngẫu nhiên phía nền -->
    <script>
        function createRose() {
            const rose = document.createElement('div');
            rose.classList.add('rose-bg');
            // Random ngẫu nhiên giữa hoa hồng và trái tim nhỏ
            const icons = ['🌹', '🌸', '❤️', '💕'];
            rose.innerHTML = icons[Math.floor(Math.random() * icons.length)];
            
            rose.style.left = Math.random() * 100 + 'vw';
            rose.style.animationDuration = Math.random() * 3 + 4 + 's'; // từ 4-7 giây
            rose.style.fontSize = Math.random() * 12 + 12 + 'px'; // từ 12-24px
            document.body.appendChild(rose);
            
            setTimeout(() => {
                rose.remove();
            }, 7000);
        }
        // Tạo cánh hoa liên tục mỗi 400ms
        setInterval(createRose, 400);
    </script>

</body>
</html>
