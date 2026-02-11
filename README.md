# buat-my-princessss-cacakk
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Untuk My Princess 💖</title>
    <style>
        /* Dasar & Background Animasi */
        body {
            background: linear-gradient(135deg, #ffc0cb 0%, #ffe4e1 100%);
            font-family: 'Poppins', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            overflow: hidden;
            position: relative;
        }

        /* Container Lebih Lebar & Mewah */
        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 30px;
            box-shadow: 0 15px 35px rgba(255, 20, 147, 0.2);
            text-align: center;
            max-width: 800px; /* Diperlebar */
            width: 85%;
            border: 5px solid #fff;
            position: relative;
            z-index: 10;
            animation: bounceIn 1.5s ease;
        }

        h1 {
            color: #ff1493;
            font-size: 2.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px #ffb6c1;
        }

        .message {
            color: #444;
            line-height: 1.8;
            font-size: 1.1rem;
            text-align: center;
            margin-bottom: 30px;
            background: rgba(255, 182, 193, 0.1);
            padding: 25px;
            border-radius: 20px;
            border-left: 5px solid #ff69b4;
        }

        /* Tombol yang Lebih Menarik */
        .buttons {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 40px;
            margin-top: 20px;
            min-height: 60px;
        }

        button {
            padding: 15px 40px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        #btnYa {
            background: linear-gradient(45deg, #ff69b4, #ff1493);
            color: white;
        }

        #btnYa:hover {
            transform: scale(1.2);
            box-shadow: 0 8px 20px rgba(255, 20, 147, 0.4);
        }

        #btnTidak {
            background-color: #fbced7;
            color: #ff1493;
            position: absolute;
        }

        /* Animasi Hati Berjatuhan */
        .heart {
            position: absolute;
            color: #ff69b4;
            font-size: 20px;
            top: -20px;
            user-select: none;
            z-index: 1;
            animation: fall linear forwards;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh) rotate(360deg);
            }
        }

        @keyframes bounceIn {
            0% { opacity: 0; transform: scale(0.3); }
            50% { opacity: 1; transform: scale(1.05); }
            70% { transform: scale(0.9); }
            100% { transform: scale(1); }
        }

        .emoji-header {
            font-size: 50px;
            margin-bottom: 10px;
            display: block;
        }

        /* Responsif Mobile */
        @media (max-width: 600px) {
            h1 { font-size: 1.8rem; }
            .message { font-size: 0.95rem; }
            .container { width: 90%; padding: 20px; }
        }
    </style>
</head>
<body>

<div class="container">
    <span class="emoji-header">🥺🌸💖✨</span>
    <h1>Maafin Aku Ya Sayang?</h1>
    
    <div class="message">
        <strong>Sayangku, my princess, my bini, my sawit, my everyting</strong><br><br>
        Aku tahu kamu lagi marah sama aku sekarang, dan aku nggak nyalahin kamu sama sekali. Mungkin aku emang sering bikin kamu kecewa tanpa sadar, entah karena aku kurang perhatian atau kata-kataku yang kadang nggak pas. Aku minta maaf banget dari hati yang paling dalam.<br><br>
        Kamu adalah orang yang paling berharga buat aku, dan liat kamu sedih atau marah gara-gara aku bikin hatiku ikut sakit. Aku janji deh, mulai sekarang aku bakal lebih peka lagi sama perasaanmu. Kita kan <strong>pasangan plenger</strong>, saling jaga dan saling lengkapin.<br><br>
        Tolong maafin aku ya, cintaku? Besok pagi aku jemput dan kita makan-makan favoritmu, gimana? Aku sayang kamu lebih dari apa pun. 
        <br><strong>Peluk erat dari jauh! ❤️</strong>
    </div>

    <div class="buttons">
        <button id="btnYa" onclick="berhasil()">Ya, Maafin!</button>
        <button id="btnTidak" onmouseover="lari()" onclick="lari()">Nggak!</button>
    </div>
</div>

<script>
    // Efek Hati Berjatuhan otomatis
    function createHeart() {
        const heart = document.createElement('div');
        heart.classList.add('heart');
        heart.innerHTML = '❤️';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = Math.random() * 2 + 3 + 's';
        heart.style.opacity = Math.random();
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 5000);
    }

    setInterval(createHeart, 300);

    // Fungsi Tombol Kabur
    function lari() {
        const btnTidak = document.getElementById('btnTidak');
        // Area lari tetap di sekitar layar tapi tidak keluar batas
        const x = Math.random() * (window.innerWidth - btnTidak.offsetWidth);
        const y = Math.random() * (window.innerHeight - btnTidak.offsetHeight);
        
        btnTidak.style.position = 'fixed';
        btnTidak.style.left = x + 'px';
        btnTidak.style.top = y + 'px';
    }

    // Fungsi Klik Ya
    function berhasil() {
        // Efek kembang api sederhana dengan alert
        document.querySelector('.container').innerHTML = `
            <span style="font-size: 60px;">🥰</span>
            <h1 style="color: #ff1493;">Yeeayy! Makasih Sayang!</h1>
            <p style="font-size: 1.2rem; color: #555;">Janji besok pagi aku jemput tepat waktu!<br>I Love You So Much, My Everything! ❤️❤️❤️</p>
            <button onclick="location.reload()" style="background: #ff69b4; color: white; margin-top: 20px;">Klik untuk peluk!</button>
        `;
        
        // Membuat hujan hati lebih banyak saat dimaafkan
        setInterval(createHeart, 50);
    }
</script>

</body>
</html>
