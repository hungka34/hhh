<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tỏ Tình Cùng Em 💕</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(to bottom, #0c1445, #1a237e, #283593);
            color: white;
            min-height: 100vh;
            overflow: hidden;
            position: relative;
        }

        .city-background {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 40%;
            background: 
                linear-gradient(to top, #0c1445 10%, transparent),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400" fill="%23123777"><rect width="1200" height="400" fill="%230c1445"/><rect x="50" y="150" width="80" height="250" fill="%23123777"/><rect x="70" y="100" width="40" height="50" fill="%23123777"/><rect x="75" y="80" width="30" height="20" fill="%23123777"/><rect x="200" y="180" width="100" height="220" fill="%23123777"/><rect x="230" y="130" width="40" height="50" fill="%23123777"/><rect x="235" y="110" width="30" height="20" fill="%23123777"/><rect x="350" y="200" width="120" height="200" fill="%23123777"/><rect x="390" y="150" width="40" height="50" fill="%23123777"/><rect x="395" y="130" width="30" height="20" fill="%23123777"/><rect x="550" y="170" width="90" height="230" fill="%23123777"/><rect x="580" y="120" width="30" height="50" fill="%23123777"/><rect x="585" y="100" width="20" height="20" fill="%23123777"/><rect x="700" y="190" width="110" height="210" fill="%23123777"/><rect x="740" y="140" width="30" height="50" fill="%23123777"/><rect x="745" y="120" width="20" height="20" fill="%23123777"/><rect x="900" y="160" width="80" height="240" fill="%23123777"/><rect x="930" y="110" width="20" height="50" fill="%23123777"/><rect x="935" y="90" width="10" height="20" fill="%23123777"/><rect x="1050" y="180" width="100" height="220" fill="%23123777"/><rect x="1080" y="130" width="40" height="50" fill="%23123777"/><rect x="1085" y="110" width="30" height="20" fill="%23123777"/></svg>');
            background-size: cover;
            z-index: 1;
        }

        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 60%;
            z-index: 0;
        }

        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            animation: twinkle 4s infinite;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
            text-align: center;
            position: relative;
            z-index: 2;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .title {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            text-shadow: 0 0 10px rgba(255, 105, 180, 0.7);
            animation: pulse 2s infinite;
        }

        .message {
            font-size: 1.5rem;
            margin-bottom: 3rem;
            line-height: 1.6;
            color: #f8c8dc;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            position: relative;
            z-index: 10;
        }

        .btn {
            padding: 1rem 2rem;
            font-size: 1.5rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .yes-btn {
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            color: white;
            transform: scale(1);
        }

        .no-btn {
            background: linear-gradient(45deg, #6b6bff, #8e8eff);
            color: white;
            transform: scale(1);
        }

        .hearts-container {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 5;
        }

        .heart-emoji {
            position: absolute;
            font-size: 2.5rem;
            animation: float 6s infinite ease-in-out;
            opacity: 0.8;
            filter: drop-shadow(0 0 8px rgba(255, 105, 180, 0.6));
        }

        .fireworks {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 100;
            display: none;
        }

        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            animation: explode 1s forwards;
        }

        .heart {
            position: absolute;
            font-size: 2rem;
            animation: floatUp 4s forwards;
            opacity: 0;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        @keyframes float {
            0%, 100% { 
                transform: translateY(0) rotate(0deg) scale(1);
            }
            25% { 
                transform: translateY(-15px) rotate(-5deg) scale(1.1);
            }
            50% { 
                transform: translateY(-25px) rotate(0deg) scale(1);
            }
            75% { 
                transform: translateY(-15px) rotate(5deg) scale(1.1);
            }
        }

        @keyframes explode {
            0% { 
                transform: translate(0, 0) scale(1);
                opacity: 1;
            }
            100% { 
                transform: translate(var(--tx), var(--ty)) scale(0);
                opacity: 0;
            }
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) scale(0);
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) scale(1);
                opacity: 0;
            }
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        .congrats {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 200;
            display: none;
        }

        .congrats h1 {
            font-size: 4rem;
            color: #ff6b6b;
            margin-bottom: 2rem;
            text-align: center;
            animation: pulse 1s infinite;
        }

        .congrats p {
            font-size: 1.8rem;
            color: #f8c8dc;
            text-align: center;
            max-width: 80%;
            animation: heartbeat 1.5s infinite;
        }

        @media (max-width: 768px) {
            .title {
                font-size: 2.2rem;
            }
            
            .message {
                font-size: 1.2rem;
            }
            
            .buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 80%;
                margin-bottom: 1rem;
            }
            
            .heart-emoji {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    <div class="city-background"></div>
    
    <div class="container">
        <h1 class="title">💖 Làm Người Yêu Anh Nhé! 💖</h1>
        <p class="message">Từ lần đầu gặp em, trái tim anh đã thuộc về em. Cùng anh viết nên câu chuyện tình yêu đẹp nhất nhé!</p>
        
        <div class="buttons">
            <button class="btn yes-btn" id="yesBtn">Đồng Ý 💕</button>
            <button class="btn no-btn" id="noBtn">Không Đâu 😢</button>
        </div>
    </div>
    
    <div class="hearts-container" id="heartsContainer"></div>
    <div class="fireworks" id="fireworks"></div>
    
    <div class="congrats" id="congrats">
        <h1>Yay! Anh Biết Mà! 💖</h1>
        <p>Anh yêu em! Anh yêu em! Anh yêu em! ❤️</p>
    </div>

    <script>
        // Tạo sao lấp lánh
        const starsContainer = document.getElementById('stars');
        for (let i = 0; i < 150; i++) {
            const star = document.createElement('div');
            star.classList.add('star');
            star.style.left = `${Math.random() * 100}%`;
            star.style.top = `${Math.random() * 60}%`;
            star.style.width = `${Math.random() * 3 + 1}px`;
            star.style.height = star.style.width;
            star.style.animationDelay = `${Math.random() * 4}s`;
            starsContainer.appendChild(star);
        }

        // Tạo trái tim emoji
        const heartsContainer = document.getElementById('heartsContainer');
        const heartEmojis = ['❤️', '💕', '💖', '💗', '💓', '💘', '💝', '💞', '🧡', '💛', '💚', '💙', '💜'];
        
        function createHeartEmoji() {
            const heart = document.createElement('div');
            heart.classList.add('heart-emoji');
            heart.textContent = heartEmojis[Math.floor(Math.random() * heartEmojis.length)];
            heart.style.left = `${Math.random() * 100}%`;
            heart.style.top = `${Math.random() * 100}%`;
            heart.style.animationDelay = `${Math.random() * 6}s`;
            heart.style.fontSize = `${Math.random() * 2 + 2}rem`;
            heartsContainer.appendChild(heart);
        }
        
        for (let i = 0; i < 15; i++) {
            createHeartEmoji();
        }

        // Xử lý nút "Không"
        const noBtn = document.getElementById('noBtn');
        let noClickCount = 0;
        let yesScale = 1;

        noBtn.addEventListener('click', function() {
            noClickCount++;
            
            // Làm nút "Không" nhỏ dần
            const currentScale = parseFloat(noBtn.style.transform.replace('scale(', '').replace(')', '')) || 1;
            const newScale = Math.max(0.1, currentScale - 0.1);
            noBtn.style.transform = `scale(${newScale})`;
            
            // Làm nút "Đồng Ý" to dần
            yesScale += 0.2;
            yesBtn.style.transform = `scale(${yesScale})`;
            
            // Di chuyển nút "Không" đến vị trí ngẫu nhiên
            const maxX = window.innerWidth - noBtn.offsetWidth;
            const maxY = window.innerHeight - noBtn.offsetHeight;
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;
            
            noBtn.style.position = 'absolute';
            noBtn.style.left = `${randomX}px`;
            noBtn.style.top = `${randomY}px`;
            
            // Thay đổi văn bản nút "Không" sau một số lần nhấp
            const messages = [
                "Chắc chưa? 😢",
                "Thật lòng á? 💔",
                "Suy nghĩ lại đi! 🥺",
                "Anh buồn lắm đó 😭",
                "Lần cuối hỏi nha! 💕"
            ];
            
            if (noClickCount <= messages.length) {
                noBtn.textContent = messages[noClickCount - 1];
            }
            
            // Thêm trái tim emoji buồn
            createSadHearts();
        });

        // Tạo trái tim buồn khi nhấn nút "Không"
        function createSadHearts() {
            const sadHearts = ['💔', '😢', '😭', '🥺'];
            
            for (let i = 0; i < 3; i++) {
                const heart = document.createElement('div');
                heart.classList.add('heart-emoji');
                heart.textContent = sadHearts[Math.floor(Math.random() * sadHearts.length)];
                heart.style.left = `${Math.random() * 100}%`;
                heart.style.top = `${Math.random() * 100}%`;
                heart.style.animation = 'float 4s infinite ease-in-out';
                heart.style.fontSize = `${Math.random() * 1.5 + 1.5}rem`;
                heartsContainer.appendChild(heart);
                
                // Xóa sau 8 giây
                setTimeout(() => {
                    heart.remove();
                }, 8000);
            }
        }

        // Xử lý nút "Đồng Ý"
        const yesBtn = document.getElementById('yesBtn');
        const fireworksContainer = document.getElementById('fireworks');
        const congratsScreen = document.getElementById('congrats');

        yesBtn.addEventListener('click', function() {
            // Hiển thị pháo hoa
            fireworksContainer.style.display = 'block';
            
            // Tạo pháo hoa trái tim
            createHeartFireworks();
            
            // Tạo trái tim vui vẻ
            createHappyHearts();
            
            // Hiển thị màn hình chúc mừng sau 2 giây
            setTimeout(() => {
                congratsScreen.style.display = 'flex';
            }, 2000);
            
            // Ẩn các nút
            document.querySelector('.buttons').style.display = 'none';
        });

        // Tạo trái tim vui vẻ khi đồng ý
        function createHappyHearts() {
            const happyHearts = ['❤️', '💕', '💖', '💗', '💓', '💘', '💝', '💞'];
            
            for (let i = 0; i < 20; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.classList.add('heart-emoji');
                    heart.textContent = happyHearts[Math.floor(Math.random() * happyHearts.length)];
                    heart.style.left = `${Math.random() * 100}%`;
                    heart.style.top = `${Math.random() * 100}%`;
                    heart.style.animation = 'float 3s infinite ease-in-out';
                    heart.style.fontSize = `${Math.random() * 2 + 2}rem`;
                    heart.style.animationDelay = '0s';
                    heartsContainer.appendChild(heart);
                    
                    // Xóa sau 6 giây
                    setTimeout(() => {
                        heart.remove();
                    }, 6000);
                }, i * 150);
            }
        }

        // Tạo pháo hoa trái tim
        function createHeartFireworks() {
            const colors = ['#ff6b6b', '#ff8e8e', '#ff5252', '#ff3838', '#ff9f9f'];
            
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    createFirework(
                        Math.random() * window.innerWidth,
                        Math.random() * window.innerHeight,
                        colors[Math.floor(Math.random() * colors.length)]
                    );
                }, i * 100);
            }
            
            // Tạo trái tim bay lên
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    createHeart();
                }, i * 200);
            }
        }

        function createFirework(x, y, color) {
            const firework = document.createElement('div');
            firework.classList.add('firework');
            firework.style.left = `${x}px`;
            firework.style.top = `${y}px`;
            firework.style.backgroundColor = color;
            
            // Tạo hiệu ứng nổ
            for (let i = 0; i < 30; i++) {
                const particle = document.createElement('div');
                particle.classList.add('firework');
                particle.style.left = `${x}px`;
                particle.style.top = `${y}px`;
                particle.style.backgroundColor = color;
                
                const angle = Math.random() * Math.PI * 2;
                const distance = Math.random() * 100 + 50;
                const tx = Math.cos(angle) * distance;
                const ty = Math.sin(angle) * distance;
                
                particle.style.setProperty('--tx', `${tx}px`);
                particle.style.setProperty('--ty', `${ty}px`);
                
                fireworksContainer.appendChild(particle);
                
                setTimeout(() => {
                    particle.remove();
                }, 1000);
            }
            
            fireworksContainer.appendChild(firework);
            
            setTimeout(() => {
                firework.remove();
            }, 1000);
        }

        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.textContent = '💖';
            heart.style.left = `${Math.random() * 100}%`;
            heart.style.bottom = '0';
            heart.style.animationDelay = `${Math.random() * 2}s`;
            heart.style.fontSize = `${Math.random() * 2 + 1}rem`;
            
            document.body.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 4000);
        }

        // Làm nút "Không" di chuyển khi di chuột vào gần
        document.addEventListener('mousemove', function(e) {
            const noBtnRect = noBtn.getBoundingClientRect();
            const noBtnCenterX = noBtnRect.left + noBtnRect.width / 2;
            const noBtnCenterY = noBtnRect.top + noBtnRect.height / 2;
            
            const distance = Math.sqrt(
                Math.pow(e.clientX - noBtnCenterX, 2) + 
                Math.pow(e.clientY - noBtnCenterY, 2)
            );
            
            if (distance < 150 && noClickCount < 5) {
                const maxX = window.innerWidth - noBtn.offsetWidth;
                const maxY = window.innerHeight - noBtn.offsetHeight;
                const randomX = Math.random() * maxX;
                const randomY = Math.random() * maxY;
                
                noBtn.style.position = 'absolute';
                noBtn.style.left = `${randomX}px`;
                noBtn.style.top = `${randomY}px`;
            }
        });

        // Thêm hiệu ứng nhấp nháy cho các trái tim
        setInterval(() => {
            const hearts = document.querySelectorAll('.heart-emoji');
            hearts.forEach(heart => {
                if (Math.random() > 0.7) {
                    heart.style.transform = 'scale(1.2)';
                    setTimeout(() => {
                        heart.style.transform = 'scale(1)';
                    }, 300);
                }
            });
        }, 1000);
    </script>
</body>
</html>
