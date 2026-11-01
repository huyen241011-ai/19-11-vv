<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gửi Người Đàn Ông Của Em | 19.11</title>
    <style>
        /* Phong cách lãng mạn hiện đại */
        body {
            margin: 0;
            padding: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #1f1c2c, #928dab);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
        }

        /* Hiệu ứng tim rơi phía nền */
        .heart-bg {
            position: absolute;
            color: rgba(255, 75, 75, 0.3);
            font-size: 20px;
            animation: fall linear infinite;
            z-index: 1;
        }
        @keyframes fall {
            0% { transform: translateY(-10vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(110vh) rotate(360deg); opacity: 0; }
        }

        /* Hộp thiệp 3D */
        .card-container {
            position: relative;
            width: 380px;
            height: 500px;
            perspective: 1000px;
            z-index: 2;
            cursor: pointer;
        }

        .card {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transition: transform 1s ease-in-out;
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
            border-radius: 15px;
        }

        /* Hiệu ứng lật mở khi rê chuột hoặc click */
        .card-container:hover .card {
            transform: rotateY(-180deg);
        }

        .card-front, .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 30px;
            box-sizing: border-box;
        }

        /* Mặt trước của thiệp */
        .card-front {
            background: linear-gradient(to bottom, #ff416c, #ff4b2b);
            color: white;
            text-align: center;
        }

        .card-front h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .card-front p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .main-heart {
            font-size: 80px;
            color: white;
            animation: beat 1.2s infinite;
            margin: 20px 0;
        }

        @keyframes beat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }

        /* Mặt sau chứa thư tình ngọt ngào */
        .card-back {
            background: #ffffff;
            color: #333333;
            transform: rotateY(180deg);
            justify-content: flex-start;
            overflow-y: auto;
            border: 5px solid #ff4b2b;
        }

        .card-back h2 {
            color: #ff416c;
            margin-top: 10px;
            font-size: 1.5rem;
            border-bottom: 2px dashed #ff4b2b;
            padding-bottom: 5px;
            width: 100%;
            text-align: center;
        }

        /* Nội dung bức thư */
        .letter-content {
            font-size: 1.05rem;
            line-height: 1.6;
            text-align: justify;
            font-style: italic;
            color: #444;
        }

        .signature {
            text-align: right;
            width: 100%;
            margin-top: 15px;
            font-weight: bold;
            color: #ff416c;
        }

        /* Gợi ý tương tác nhỏ */
        .hint {
            position: absolute;
            bottom: 15px;
            font-size: 0.85rem;
            opacity: 0.7;
            animation: fade 1.5s infinite alternate;
        }
        @keyframes fade { 0% { opacity: 0.3; } 100% { opacity: 0.9; } }
    </style>
</head>
<body>

    <!-- Khung chứa thiệp lật -->
    <div class="card-container">
        <div class="card">
            
            <!-- MẶT TRƯỚC THIỆP -->
            <div class="card-front">
                <p>Thế giới có 8 tỷ người...</p>
                <div class="main-heart">❤️</div>
                <h1>HAPPY MEN'S DAY</h1>
                <p>Ngày 19 tháng 11 đặc biệt</p>
                <div class="hint">Chạm hoặc rê chuột để mở thư nhé... ✨</div>
            </div>
            
            <!-- MẶT SAU THIỆP (NỘI DUNG THƯ) -->
            <div class="card-back">
                <h2>Gửi Anh - Người Đàn Ông Của Em!</h2>
                <div class="letter-content">
                    <p><br>
                        Hôm nay là 19/11, ngày để cả thế giới tôn vinh những người đàn ông tuyệt vời, và với em, anh chính là người tuyệt vời nhất! 
                    </p>
                    <p>
                        Cảm ơn anh vì đã luôn là bờ vai vững chãi, luôn kiên nhẫn yêu thương, che chở và bao dung cho những hờn dỗi vu vơ của em. Ở bên anh, em luôn có cảm giác bình yên đến lạ kỳ.
                    </p>
                    <p>
                        Chúc người yêu của em ngày một trưởng thành, luôn vững vàng với những đam mê và gặt hái được mọi thành công mà anh mong muốn. Cho dù áp lực cuộc sống ngoài kia có lớn thế nào, hãy nhớ rằng luôn có em ở phía sau ủng hộ và yêu thương anh vô điều kiện.
                    </p>
                    <p>
                        Hôm nay anh chỉ việc mỉm cười và hạnh phúc thôi, cả thế giới này cứ để em lo (hoặc ít nhất là lo cho anh)! Moahhh ~ 💋
                    </p>
                </div>
                <div class="signature">Yêu anh rất nhiều! 💕</div>
            </div>

        </div>
    </div>

    <!-- Đoạn code JS tạo hiệu ứng tim bay ngẫu nhiên ở nền -->
    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart-bg');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 3 + 's';
            heart.style.fontSize = Math.random() * 15 + 15 + 'px';
            document.body.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 6000);
        }
        setInterval(createHeart, 300);
    </script>

</body>
</html>
