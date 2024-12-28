<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sovchilar - Yangi Yil</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: url('https://i.postimg.cc/nLDpX6cW/2201-street-snowfall-winter-2160x3840.jpg') center/cover fixed;
            min-height: 80vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
            position: relative;
        }

        .container {
            background: rgba(30,30,30,0.238);
            padding: 2rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            transform-style: preserve-3d;
            perspective: 1000px;
            max-width: 450px;
            width: 100%;
            text-align: center;
            position: relative;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotateX(0); }
            50% { transform: translateY(-20px) rotateX(5deg); }
        }

        .logo {
            width: 150px;
            height: 150px;
            background: rgba(51, 51, 51, 0.9);
            border-radius: 50%;
            margin: 0 auto 30px;
            position: relative;
            transform: translateZ(50px);
            transition: transform 0.3s;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            overflow: hidden;
        }

        .logo:hover {
            transform: translateZ(70px) scale(1.1);
        }


        .title {
            color: white;
            font-size: 2em;
            margin-bottom: 2rem;
            text-shadow: 0 0 10px rgba(255,255,255,0.3);
            transform: translateZ(40px);
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 10px rgba(255,255,255,0.3); }
            to { text-shadow: 0 0 20px rgba(255,255,255,0.5), 0 0 30px rgba(255,255,255,0.3); }
        }

        .btn {
            display: block;
            margin: 1rem 0;
            padding: 1rem;
            border-radius: 10px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            position: relative;
            transition: all 0.3s ease;
            transform-style: preserve-3d;
            transform: translateZ(20px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .btn::before {
            content: '';
            position: absolute;
            inset: 0;
            border-radius: 10px;
            background: rgb(252,22,22);
            transform: translateZ(-26px);
            transition: all 0.3s ease;
        }

        .btn:hover {
            transform: translateZ(30px) scale(1.05);
            box-shadow: 0 10px 25px rgb(255,8,8);
        }

        .btn:active {
            transform: translateZ(10px) scale(0.95);
        }

        .telegram {
            background: linear-gradient(145deg, #0088cc, #25b4fd);
            animation: buttonFloat 3s ease-in-out infinite;
        }

        .chat {
            background: linear-gradient(145deg, #444, #222);
            animation: buttonFloat 3s ease-in-out infinite 0.2s;
        }

        .youtube {
            background: linear-gradient(145deg, #ff0000, #cc0000);
            animation: buttonFloat 3s ease-in-out infinite 0.4s;
        }

        @keyframes buttonFloat {
            0%, 100% { transform: translateZ(100px); }
            50% { transform: translateZ(30px); }
        }

        .snowflake {
            position: absolute;
            width: 10px;
            height: 10px;
            background: white;
            border-radius: 50%;
            filter: blur(2px);
            pointer-events: none;
        }

        @keyframes snowfall {
            0% {
                transform: translateY(-100vh) rotate(0deg);
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
            }
        }

        .snow-container {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1;
        }

        .container {
            z-index: 2;
        }
    </style>
</head>
<body>
    <div class="snow-container" id="snow"></div>
    
    <div class="container">
        <div class="logo">
            <img 
                src="https://i.postimg.cc/6qrpM2b9/Picsart-24-12-02-20-38-34-469.png" 
                alt="Kelinlar Logo"
                style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;"
            />
        </div>
        <h1 class="title">SOVCHILAR</h1>
        
        <a href="https://t.me/+_rFTajPX3_1kMTg6" class="btn telegram">
            <i class="fas fa-paper-plane"></i> Telegram
        </a>
        
        <a href="https://hacer4546zip.github.io/Sovchilar" class="btn chat">
            <i class="fas fa-comments"></i> Online Chat Va Qizlar
        </a>
        
        <a href="https://t.me/+_rFTajPX3_1kMTg6" class="btn telegram">
            <i class="fas fa-paper-plane"></i> Telegram
        </a>
        
        <a href="https://hacer4546zip.github.io/Jonimsankumami/" class="btn chat">
            <i class="fas fa-globe"></i> Boshqa Elonlar Ko'rish
        </a>
        
        <a href="https://youtube.com/channel/UCNXs27Km-C6ROiInCveXazA?si=CD0kTzCvlnOVxZkE" class="btn youtube">
            <i class="fab fa-youtube"></i> YOU TUBE KANAL
        </a>
    </div>

    <script>
        function createSnow() {
            const snowContainer = document.getElementById('snow');
            for(let i = 0; i < 50; i++) {
                const snowflake = document.createElement('div');
                snowflake.className = 'snowflake';
                snowflake.style.left = Math.random() * 100 + '%';
                snowflake.style.opacity = Math.random();
                snowflake.style.animation = `snowfall ${Math.random() * 3 + 2}s linear infinite`;
                snowflake.style.animationDelay = Math.random() * 2 + 's';
                snowContainer.appendChild(snowflake);
            }
        }

        createSnow();
    </script>
</body>
