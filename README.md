happy birthday lhh
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>生日祝福</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/fullPage.js/3.1.2/fullpage.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Zhi+Mang+Xing&display=swap'); /* 引入行楷字体 */
        
        :root {
            --heart-top: 50%; /* 控制爱心的垂直位置 */
            --heart-left: 50%; /* 控制爱心的水平位置 */
        }

        body {
            font-family: 'Zhi Mang Xing', cursive; /* 使用行楷字体 */
            background-color: #9370DB; /* 深紫色背景 */
            color: #fff;
            text-align: center;
            overflow: hidden; /* 禁止滚动条 */
        }
        .section {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .heart {
            position: absolute;
            top: var(--heart-top);
            left: var(--heart-left);
            width: 300px;
            height: 300px;
            background-color: #ff0000; /* 红色背景 */
            transform: translate(-50%, -50%) rotate(-45deg);
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .heart:before,
        .heart:after {
            content: "";
            position: absolute;
            width: 300px;
            height: 300px;
            background-color: #ff0000; /* 红色背景 */
            border-radius: 50%;
        }
        .heart:before {
            top: -150px;
            left: 0;
        }
        .heart:after {
            left: 150px;
            top: 0;
        }
        .heart-content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(45deg);
            background: linear-gradient(45deg, red, orange, yellow, green, blue, indigo, violet);
            -webkit-background-clip: text;
            color: transparent;
            text-align: center;
            width: 80%;
            z-index: 10; /* 确保文字在最上方 */
        }
        .heart-content h1 {
            font-size: 2.5em; /* 调整字体大小 */
            margin: 0.5em 0;
        }
        .heart-content p {
            font-size: 1.2em; /* 调整字体大小 */
            margin: 0.5em 0;
        }
        .meteor {
            position: absolute;
            width: 2px;
            height: 100px;
            background: linear-gradient(45deg, white, rgba(255, 255, 255, 0));
            animation: meteor 2s linear infinite;
        }
        @keyframes meteor {
            0% {
                transform: translateY(-100vh) translateX(0);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) translateX(100vw);
                opacity: 0;
            }
        }
        .music-player {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background: rgba(0, 0, 0, 0.5);
            padding: 10px;
            border-radius: 5px;
            display: flex;
            align-items: center;
            z-index: 100;
        }
        .music-player button {
            background: none;
            border: none;
            color: white;
            font-size: 1.5em;
            cursor: pointer;
            margin-right: 10px;
        }
        .music-player input[type="range"] {
            width: 100px;
            margin-right: 10px;
        }
        .music-player select {
            margin-right: 10px;
        }
        .music-player .time {
            color: white;
            font-size: 1em;
        }

        /* 气球样式 */
        .balloon {
            position: absolute;
            bottom: -100px;
            width: 60px;
            height: 80px;
            background-color: red;
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            box-shadow: inset -5px -10px rgba(0, 0, 0, 0.2);
            animation: float 10s ease-in infinite, disappear 10s ease-in infinite;
        }

        .balloon:before {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            width: 2px;
            height: 20px;
            background-color: #555;
        }

        @keyframes float {
            0% {
                transform: translateY(0);
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh);
                opacity: 1;
            }
        }

        @keyframes disappear {
            0%, 90% {
                opacity: 1;
            }
            100% {
                opacity: 0;
            }
        }

        /* 烟花样式 */
        .firework {
            position: absolute;
            width: 3px;
            height: 3px;
            background: white;
            border-radius: 50%;
            animation: explode 1s ease-out forwards;
        }

        @keyframes explode {
            0% {
                transform: scale(1);
                opacity: 1;
            }
            100% {
                transform: scale(3);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
<div id="fullpage">
    <div class="section">
        <div class="heart">
            <div class="heart-content">
                <h1>生日快乐！</h1>
                <p>亲爱的：李欢欢</p>
                <p>祝你生日快乐！愿你在新的一年里，健康快乐，心想事成！</p>
            </div>
        </div>
    </div>
    <div class="section">
        <div class="heart">
            <div class="heart-content">
                <h1>美好回忆</h1>
                <p>2024-10-05</p>
                <p>这是我们第一次见面的日子。</p>
            </div>
        </div>
    </div>
    <div class="section">
        <div class="heart">
            <div class="heart-content">
                <h1>难忘瞬间</h1>
                <p>2025-01-01</p>
                <p>这是我们一起度过的美好时光。</p>
            </div>
        </div>
    </div>
    <div class="section">
        <div class="heart">
            <div class="heart-content">
                <h1>未来可期</h1>
                <p>愿我们的未来充满更多美好的回忆。</p>
            </div>
        </div>
    </div>
</div>

<div id="balloon-container"></div>
<div id="firework-container"></div>

<audio id="background-music" src="C:/Users/yunch/Desktop/生日祝福/happy.mp3" autoplay loop>
    Your browser does not support the audio element.
</audio>

<div class="music-player">
    <button id="play-pause-btn">▶</button>
    <input type="range" id="progress-bar" value="0" max="100">
    <span class="time" id="current-time">00:00</span> / <span class="time" id="duration">00:00</span>
    <input type="range" id="volume-control" min="0" max="1" step="0.01" value="1">
    <select id="playback-rate">
        <option value="0.5">0.5x</option>
        <option value="1" selected>1x</option>
        <option value="1.5">1.5x</option>
        <option value="2">2x</option>
    </select>
    <audio id="background-music" src="path/to/your/music.mp3" loop></audio>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/fullPage.js/3.1.2/fullpage.min.js"></script>
<script>
    new fullpage('#fullpage', {
        autoScrolling: true,
        navigation: true,
        navigationPosition: 'right',
        navigationTooltips: ['首页', '美好回忆', '难忘瞬间', '未来可期'],
        showActiveTooltip: true,
        anchors: ['home', 'memories', 'moments', 'future']
    });

    // 创建流星效果
    function createMeteor() {
        const meteor = document.createElement('div');
        meteor.classList.add('meteor');
        meteor.style.left = `${Math.random() * 100}vw`;
        document.body.appendChild(meteor);
        setTimeout(() => {
            meteor.remove();
        }, 2000);
    }

    setInterval(createMeteor, 500);

    // 创建气球效果
    function createBalloon() {
        const balloon = document.createElement('div');
        balloon.classList.add('balloon');
        balloon.style.left = `${Math.random() * 1000}vw`;
        balloon.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 50%)`;
        document.getElementById('balloon-container').appendChild(balloon);
        setTimeout(() => {
            balloon.remove();
        }, 10000); // 与动画持续时间匹配
    }

    setInterval(createBalloon, 500); // 调整生成频率为每500毫秒生成一个气球

    // 创建烟花效果
    function createFirework() {
        const fireworkContainer = document.getElementById('firework-container');
        const fireworkCount = 20;
        for (let i = 0; i < fireworkCount; i++) {
            const firework = document.createElement('div');
            firework.classList.add('firework');
            firework.style.left = `${Math.random() * 100}vw`;
            firework.style.top = `${Math.random() * 100}vh`;
            fireworkContainer.appendChild(firework);
            setTimeout(() => {
                firework.remove();
            }, 1000); // 与动画持续时间匹配
        }
    }

    setInterval(createFirework, 2000); // 每2秒生成一次烟花

    const playPauseBtn = document.getElementById('play-pause-btn');
    const backgroundMusic = document.getElementById('background-music');
    const progressBar = document.getElementById('progress-bar');
    const currentTimeElem = document.getElementById('current-time');
    const durationElem = document.getElementById('duration');
    const volumeControl = document.getElementById('volume-control');
    const playbackRate = document.getElementById('playback-rate');

    playPauseBtn.addEventListener('click', () => {
        if (backgroundMusic.paused) {
            backgroundMusic.play();
            playPauseBtn.textContent = '❚❚';
        } else {
            backgroundMusic.pause();
            playPauseBtn.textContent = '▶';
        }
    });

    backgroundMusic.addEventListener('timeupdate', () => {
        const progress = (backgroundMusic.currentTime / backgroundMusic.duration) * 100;
        progressBar.value = progress;
        currentTimeElem.textContent = formatTime(backgroundMusic.currentTime);
        durationElem.textContent = formatTime(backgroundMusic.duration);
    });

    progressBar.addEventListener('input', () => {
        const seekTime = (progressBar.value / 100) * backgroundMusic.duration;
        backgroundMusic.currentTime = seekTime;
    });

    volumeControl.addEventListener('input', () => {
        backgroundMusic.volume = volumeControl.value;
    });

    playbackRate.addEventListener('change', () => {
        backgroundMusic.playbackRate = playbackRate.value;
    });

    function formatTime(seconds) {
        const minutes = Math.floor(seconds / 60);
        seconds = Math.floor(seconds % 60);
        return `${minutes}:${seconds < 10 ? '0' : ''}${seconds}`;
    }

    // 页面加载完成后自动播放背景音乐
    window.addEventListener('load', () => {
        backgroundMusic.play().catch(error => {
            console.log('自动播放被阻止:', error);
        });
    });
</script>
</body>
</html>
