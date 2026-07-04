# To-White-Happy-Birthday#

<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>彼，生日快乐！🎉</title>
  <!-- 使用 Google Font 艺术字体 -->
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=ZCOOL+KuaiLe&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #1a1a2e;
      font-family: 'ZCOOL KuaiLe', 'Dancing Script', cursive, sans-serif;
      overflow: hidden;
      width: 100vw;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      color: #fff;
      user-select: none;
    }

    /* 全屏容器 —— 滑动翻页 */
    .fullscreen-carousel {
      position: relative;
      width: 100vw;
      height: 100vh;
      overflow: hidden;
      background: radial-gradient(circle at center, #2d2d44, #12121e);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .slides-wrapper {
      display: flex;
      width: 100%;
      height: 100%;
      transition: transform 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
      will-change: transform;
    }

    .slide {
      flex: 0 0 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 1.5rem 1rem;
      text-align: center;
      position: relative;
      overflow-y: auto;
    }

    /* 标题：照片上方，艺术字体，大，居中 */
    .photo-title {
      font-family: 'Dancing Script', 'ZCOOL KuaiLe', cursive;
      font-size: clamp(2.4rem, 12vw, 4.8rem);
      font-weight: 700;
      color: #ffe9b0;
      text-shadow: 0 0 20px rgba(255, 200, 100, 0.6), 0 4px 10px rgba(0,0,0,0.5);
      letter-spacing: 2px;
      margin-bottom: 0.4rem;
      padding: 0 0.3rem;
      line-height: 1.2;
      word-break: break-word;
      width: 100%;
      max-width: 800px;
    }

    /* 图片容器：自适应尺寸，保持比例 */
    .photo-frame {
      width: 90%;
      max-width: 700px;
      max-height: 70vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 40px 12px 40px 12px;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6), 0 0 0 2px rgba(255, 215, 150, 0.2);
      padding: 0.8rem;
      backdrop-filter: blur(2px);
      transition: all 0.2s;
    }

    .photo-frame img {
      width: 100%;
      height: auto;
      max-height: 65vh;
      object-fit: contain;
      border-radius: 28px 8px 28px 8px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
      display: block;
      transition: transform 0.3s ease;
      background: #2a2a3e;
    }

    /* 最后一页 (第7张) 特殊：全屏祝福 + 烟花背景 */
    .slide:last-child .photo-frame {
      background: transparent;
      box-shadow: none;
      backdrop-filter: none;
      padding: 0;
    }
    .slide:last-child .photo-frame img {
      display: none;
    }

    /* 祝福语 (全屏) */
    .birthday-message {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: radial-gradient(circle at 30% 30%, #2e1b3a, #0b0b16);
      z-index: 10;
      padding: 2rem;
      text-align: center;
      border-radius: 0;
      color: #ffecce;
      text-shadow: 0 0 40px rgba(255, 180, 80, 0.5);
      pointer-events: none;
    }

    .birthday-message h1 {
      font-family: 'Dancing Script', cursive;
      font-size: clamp(3.5rem, 18vw, 7rem);
      margin-bottom: 0.5rem;
      letter-spacing: 6px;
      color: #fddc9b;
      text-shadow: 0 0 30px #f7b32b, 0 0 60px #f7b32b80;
    }

    .birthday-message p {
      font-family: 'ZCOOL KuaiLe', cursive;
      font-size: clamp(1.6rem, 7vw, 3.2rem);
      line-height: 1.6;
      max-width: 800px;
      margin: 0.5rem 0;
      background: rgba(0,0,0,0.2);
      padding: 0.8rem 1.8rem;
      border-radius: 60px;
      backdrop-filter: blur(4px);
      border: 1px solid rgba(255, 215, 150, 0.3);
    }

    /* 导航提示 */
    .nav-hint {
      position: absolute;
      bottom: 2.5rem;
      left: 0;
      width: 100%;
      text-align: center;
      font-size: clamp(1rem, 4vw, 1.8rem);
      color: rgba(255, 240, 200, 0.7);
      letter-spacing: 4px;
      text-shadow: 0 2px 12px #00000055;
      z-index: 20;
      background: linear-gradient(90deg, transparent, rgba(255,215,150,0.1), transparent);
      padding: 0.6rem 0;
      backdrop-filter: blur(2px);
      pointer-events: none;
    }

    .nav-hint i {
      display: inline-block;
      margin: 0 12px;
      font-style: normal;
      background: rgba(0,0,0,0.2);
      padding: 0 16px;
      border-radius: 40px;
      border: 1px solid rgba(255,215,150,0.2);
    }

    /* 左右箭头 (只在非移动端显示) */
    .arrow-nav {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      z-index: 30;
      font-size: 3rem;
      color: rgba(255, 235, 180, 0.6);
      background: rgba(0, 0, 0, 0.2);
      backdrop-filter: blur(6px);
      width: 64px;
      height: 64px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: all 0.2s;
      border: 1px solid rgba(255, 215, 150, 0.2);
      box-shadow: 0 4px 20px rgba(0,0,0,0.3);
      font-weight: bold;
      text-shadow: 0 0 10px #00000088;
      user-select: none;
    }

    .arrow-nav:hover {
      background: rgba(255, 215, 150, 0.25);
      color: #ffe9b0;
      border-color: #ffd58c;
      transform: translateY(-50%) scale(1.06);
    }

    .arrow-left {
      left: 1.5rem;
    }
    .arrow-right {
      right: 1.5rem;
    }

    /* 烟花画布 (最后一页) */
    #fireworks-canvas {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 5;
    }

    /* 移动端适配：触摸友好 */
    @media (max-width: 640px) {
      .photo-title {
        font-size: clamp(1.8rem, 10vw, 3.2rem);
      }
      .photo-frame {
        width: 94%;
        max-height: 60vh;
        padding: 0.5rem;
      }
      .photo-frame img {
        max-height: 50vh;
      }
      .arrow-nav {
        width: 48px;
        height: 48px;
        font-size: 2.2rem;
        opacity: 0.7;
      }
      .arrow-left {
        left: 0.6rem;
      }
      .arrow-right {
        right: 0.6rem;
      }
      .birthday-message p {
        font-size: clamp(1.2rem, 5vw, 2.2rem);
        padding: 0.4rem 1rem;
      }
      .birthday-message h1 {
        font-size: clamp(2.8rem, 14vw, 5rem);
      }
      .nav-hint {
        bottom: 1.2rem;
        font-size: clamp(0.8rem, 3.5vw, 1.2rem);
      }
      .nav-hint i {
        margin: 0 6px;
        padding: 0 10px;
      }
    }

    /* 隐藏滚动条 */
    .slide::-webkit-scrollbar {
      display: none;
    }
    .slide {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }
  </style>
</head>
<body>

<div class="fullscreen-carousel" id="carousel">
  <div class="slides-wrapper" id="slidesWrapper">

    <!-- 1. 花之日 -->
    <div class="slide" data-index="0">
      <div class="photo-title">🌸 花之日</div>
      <div class="photo-frame"><img src="1.JPG" alt="花之日"></div>
    </div>
    <!-- 2. 小王子- B612号小行星 -->
    <div class="slide" data-index="1">
      <div class="photo-title">🌟 小王子 · B612</div>
      <div class="photo-frame"><img src="2.JPG" alt="小王子- B612号小行星"></div>
    </div>
    <!-- 3. 四叶草🍀 -->
    <div class="slide" data-index="2">
      <div class="photo-title">🍀 四叶草</div>
      <div class="photo-frame"><img src="3.JPG" alt="四叶草🍀"></div>
    </div>
    <!-- 4. INFP & ISTJ -->
    <div class="slide" data-index="3">
      <div class="photo-title">💫 INFP & ISTJ</div>
      <div class="photo-frame"><img src="4.JPG" alt="INFP & ISTJ"></div>
    </div>
    <!-- 5. 偷拍 -->
    <div class="slide" data-index="4">
      <div class="photo-title">📸 偷拍</div>
      <div class="photo-frame"><img src="5.JPG" alt="偷拍"></div>
    </div>
    <!-- 6. 睡觉时间到 -->
    <div class="slide" data-index="5">
      <div class="photo-title">😴 睡觉时间到</div>
      <div class="photo-frame"><img src="6.JPG" alt="睡觉时间到"></div>
    </div>
    <!-- 7. 训练程子 + 全屏祝福 + 烟花 -->
    <div class="slide" data-index="6">
      <div class="photo-title">🏋️ 训练程子</div>
      <div class="photo-frame"><img src="7.JPG" alt="训练程子"></div>
      <!-- 全屏祝福层 -->
      <div class="birthday-message">
        <h1>🎂 生日快乐</h1>
        <p>愿你的世界永远有花、有光、<br>有期待新一天到来的理由</p>
      </div>
      <!-- 烟花 canvas -->
      <canvas id="fireworks-canvas"></canvas>
    </div>
  </div>

  <!-- 导航箭头 -->
  <div class="arrow-nav arrow-left" id="prevBtn">‹</div>
  <div class="arrow-nav arrow-right" id="nextBtn">›</div>

  <!-- 底部提示 -->
  <div class="nav-hint">
    <i>⬅️</i> 左右方向键切换 <i>➡️</i>
  </div>
</div>

<!-- 自动播放音乐 (背景) -->
<audio id="bgMusic" autoplay loop preload="auto">
  <source src="music.mp3" type="audio/mpeg">
  您的浏览器不支持音频播放。
</audio>

<script>
  (function(){
    // ---- 配置 ----
    const slidesWrapper = document.getElementById('slidesWrapper');
    const slides = document.querySelectorAll('.slide');
    const totalSlides = slides.length;
    let currentIndex = 0;
    let isTransitioning = false;

    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');

    // 音乐自动播放（部分浏览器需用户交互，但autoplay已写，再加一层保险）
    const music = document.getElementById('bgMusic');
    // 如果自动播放被阻止，点击页面任意处尝试播放
    document.addEventListener('click', function resumeAudio() {
      if (music.paused) {
        music.play().catch(() => {});
      }
    }, { once: false });

    // 更新幻灯片位置
    function goToSlide(index) {
      if (isTransitioning || index === currentIndex) return;
      if (index < 0) index = 0;
      if (index >= totalSlides) index = totalSlides - 1;
      isTransitioning = true;
      currentIndex = index;
      slidesWrapper.style.transform = `translateX(-${currentIndex * 100}%)`;
      // 触发烟花：如果是最后一页 (index === totalSlides-1)
      if (currentIndex === totalSlides - 1) {
        initFireworks();
      } else {
        // 清除烟花 (隐藏canvas)
        const canvas = document.getElementById('fireworks-canvas');
        if (canvas) {
          canvas.style.display = 'none';
          const ctx = canvas.getContext('2d');
          ctx.clearRect(0, 0, canvas.width, canvas.height);
        }
      }
      setTimeout(() => {
        isTransitioning = false;
      }, 520);
    }

    // 上一页 / 下一页
    function prevSlide() {
      if (currentIndex > 0) goToSlide(currentIndex - 1);
    }
    function nextSlide() {
      if (currentIndex < totalSlides - 1) goToSlide(currentIndex + 1);
    }

    // 事件绑定
    prevBtn.addEventListener('click', prevSlide);
    nextBtn.addEventListener('click', nextSlide);

    // 键盘监听 (左右方向键)
    document.addEventListener('keydown', (e) => {
      if (e.key === 'ArrowLeft') {
        e.preventDefault();
        prevSlide();
      } else if (e.key === 'ArrowRight') {
        e.preventDefault();
        nextSlide();
      }
    });

    // 触摸滑动 (简单支持)
    let touchStartX = 0;
    let touchEndX = 0;
    const carousel = document.getElementById('carousel');
    carousel.addEventListener('touchstart', (e) => {
      touchStartX = e.changedTouches[0].screenX;
    }, { passive: true });
    carousel.addEventListener('touchend', (e) => {
      touchEndX = e.changedTouches[0].screenX;
      const diff = touchStartX - touchEndX;
      if (Math.abs(diff) > 40) {
        if (diff > 0) {
          nextSlide();
        } else {
          prevSlide();
        }
      }
    }, { passive: true });

    // ---- 🎆 烟花 (只在最后一页) ----
    function initFireworks() {
      const canvas = document.getElementById('fireworks-canvas');
      if (!canvas) return;
      canvas.style.display = 'block';
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
      const ctx = canvas.getContext('2d');

      // 粒子数组
      let particles = [];
      const colors = ['#ffd700', '#ff6b6b', '#ff9f43', '#f368e0', '#48dbfb', '#1dd1a1', '#feca57', '#ff9ff3'];

      class Particle {
        constructor(x, y, color) {
          this.x = x;
          this.y = y;
          this.color = color || colors[Math.floor(Math.random() * colors.length)];
          this.radius = Math.random() * 4 + 2;
          this.vx = (Math.random() - 0.5) * 10;
          this.vy = (Math.random() - 0.5) * 10 - 4;
          this.alpha = 1;
          this.deceleration = 0.98;
          this.gravity = 0.1;
          this.life = 1;
          this.damping = 0.99;
        }
        update() {
          this.vx *= this.damping;
          this.vy *= this.damping;
          this.vy += this.gravity;
          this.x += this.vx;
          this.y += this.vy;
          this.alpha -= 0.012;
          this.life -= 0.012;
          this.radius *= 0.995;
        }
        draw() {
          ctx.save();
          ctx.globalAlpha = Math.max(this.alpha, 0);
          ctx.beginPath();
          ctx.arc(this.x, this.y, Math.max(this.radius, 0.5), 0, Math.PI * 2);
          ctx.fillStyle = this.color;
          ctx.shadowColor = this.color;
          ctx.shadowBlur = 20;
          ctx.fill();
          ctx.restore();
        }
      }

      // 生成烟花 (多个爆炸)
      function createExplosion(cx, cy) {
        const count = 60 + Math.floor(Math.random() * 40);
        const color = colors[Math.floor(Math.random() * colors.length)];
        for (let i = 0; i < count; i++) {
          const angle = Math.random() * Math.PI * 2;
          const speed = Math.random() * 5 + 2;
          const p = new Particle(cx, cy, color);
          p.vx = Math.cos(angle) * speed;
          p.vy = Math.sin(angle) * speed - 1.5;
          p.radius = Math.random() * 5 + 2;
          particles.push(p);
        }
      }

      // 随机发射烟花 (从底部向上)
      function launchFirework() {
        const x = Math.random() * canvas.width * 0.8 + canvas.width * 0.1;
        const y = canvas.height * 0.2 + Math.random() * canvas.height * 0.4;
        createExplosion(x, y);
      }

      // 动画循环
      let frameId = null;
      function animate() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        // 更新粒子
        for (let i = particles.length - 1; i >= 0; i--) {
          const p = particles[i];
          p.update();
          if (p.alpha <= 0.02 || p.life <= 0) {
            particles.splice(i, 1);
          } else {
            p.draw();
          }
        }
        // 如果粒子太少，补充新烟花
        if (particles.length < 50) {
          launchFirework();
          if (Math.random() < 0.3) launchFirework(); // 偶尔双响
        }
        frameId = requestAnimationFrame(animate);
      }

      // 清除旧动画，开始新动画
      if (frameId) cancelAnimationFrame(frameId);
      particles = [];
      // 初始生成几朵
      for (let i = 0; i < 5; i++) {
        setTimeout(() => {
          launchFirework();
        }, i * 400);
      }
      animate();

      // 窗口尺寸变化重置canvas
      function resizeCanvas() {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      }
      window.addEventListener('resize', resizeCanvas);
      // 存储清理函数 (可选)
      canvas._resizeHandler = resizeCanvas;
    }

    // 如果一开始就是最后一页（比如只有7张，初始第0页，不会触发，但以防万一）
    // 但初始在第一页，所以没问题。 手动检查当前页
    // 在goToSlide 中已处理

    // 额外：初始显示第一页，且确保烟花隐藏
    window.addEventListener('load', function() {
      goToSlide(0);
      // 确保canvas隐藏
      const canvas = document.getElementById('fireworks-canvas');
      if (canvas) {
        canvas.style.display = 'none';
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      }
      // 尝试自动播放音乐
      music.play().catch(() => {});
    });

    // 重绘调整
    window.addEventListener('resize', function() {
      const canvas = document.getElementById('fireworks-canvas');
      if (canvas && canvas.style.display !== 'none') {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      }
    });

  })();
</script>

<!-- 备注：请确保 1.JPG ~ 7.JPG 以及 music.mp3 位于同一目录下 -->
</body>
</html>
