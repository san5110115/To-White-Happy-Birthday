# To-White-Happy-Birthday
{\rtf1\ansi\ansicpg1252\cocoartf2870
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 <!DOCTYPE html>\
<html lang="zh-CN">\
<head>\
  <meta charset="UTF-8">\
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">\
  <title>\uc0\u24444 \u65292 \u29983 \u26085 \u24555 \u20048 \u65281 \u55356 \u57225 </title>\
  <!-- \uc0\u20351 \u29992  Google Font \u33402 \u26415 \u23383 \u20307  -->\
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=ZCOOL+KuaiLe&display=swap" rel="stylesheet">\
  <style>\
    * \{\
      margin: 0;\
      padding: 0;\
      box-sizing: border-box;\
    \}\
\
    body \{\
      background: #1a1a2e;\
      font-family: 'ZCOOL KuaiLe', 'Dancing Script', cursive, sans-serif;\
      overflow: hidden;\
      width: 100vw;\
      height: 100vh;\
      display: flex;\
      justify-content: center;\
      align-items: center;\
      position: relative;\
      color: #fff;\
      user-select: none;\
    \}\
\
    /* \uc0\u20840 \u23631 \u23481 \u22120  \'97\'97 \u28369 \u21160 \u32763 \u39029  */\
    .fullscreen-carousel \{\
      position: relative;\
      width: 100vw;\
      height: 100vh;\
      overflow: hidden;\
      background: radial-gradient(circle at center, #2d2d44, #12121e);\
      display: flex;\
      align-items: center;\
      justify-content: center;\
    \}\
\
    .slides-wrapper \{\
      display: flex;\
      width: 100%;\
      height: 100%;\
      transition: transform 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);\
      will-change: transform;\
    \}\
\
    .slide \{\
      flex: 0 0 100%;\
      height: 100%;\
      display: flex;\
      flex-direction: column;\
      justify-content: center;\
      align-items: center;\
      padding: 1.5rem 1rem;\
      text-align: center;\
      position: relative;\
      overflow-y: auto;\
    \}\
\
    /* \uc0\u26631 \u39064 \u65306 \u29031 \u29255 \u19978 \u26041 \u65292 \u33402 \u26415 \u23383 \u20307 \u65292 \u22823 \u65292 \u23621 \u20013  */\
    .photo-title \{\
      font-family: 'Dancing Script', 'ZCOOL KuaiLe', cursive;\
      font-size: clamp(2.4rem, 12vw, 4.8rem);\
      font-weight: 700;\
      color: #ffe9b0;\
      text-shadow: 0 0 20px rgba(255, 200, 100, 0.6), 0 4px 10px rgba(0,0,0,0.5);\
      letter-spacing: 2px;\
      margin-bottom: 0.4rem;\
      padding: 0 0.3rem;\
      line-height: 1.2;\
      word-break: break-word;\
      width: 100%;\
      max-width: 800px;\
    \}\
\
    /* \uc0\u22270 \u29255 \u23481 \u22120 \u65306 \u33258 \u36866 \u24212 \u23610 \u23544 \u65292 \u20445 \u25345 \u27604 \u20363  */\
    .photo-frame \{\
      width: 90%;\
      max-width: 700px;\
      max-height: 70vh;\
      display: flex;\
      justify-content: center;\
      align-items: center;\
      background: rgba(255, 255, 255, 0.08);\
      border-radius: 40px 12px 40px 12px;\
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6), 0 0 0 2px rgba(255, 215, 150, 0.2);\
      padding: 0.8rem;\
      backdrop-filter: blur(2px);\
      transition: all 0.2s;\
    \}\
\
    .photo-frame img \{\
      width: 100%;\
      height: auto;\
      max-height: 65vh;\
      object-fit: contain;\
      border-radius: 28px 8px 28px 8px;\
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);\
      display: block;\
      transition: transform 0.3s ease;\
      background: #2a2a3e;\
    \}\
\
    /* \uc0\u26368 \u21518 \u19968 \u39029  (\u31532 7\u24352 ) \u29305 \u27530 \u65306 \u20840 \u23631 \u31069 \u31119  + \u28895 \u33457 \u32972 \u26223  */\
    .slide:last-child .photo-frame \{\
      background: transparent;\
      box-shadow: none;\
      backdrop-filter: none;\
      padding: 0;\
    \}\
    .slide:last-child .photo-frame img \{\
      display: none;\
    \}\
\
    /* \uc0\u31069 \u31119 \u35821  (\u20840 \u23631 ) */\
    .birthday-message \{\
      position: absolute;\
      top: 0;\
      left: 0;\
      width: 100%;\
      height: 100%;\
      display: flex;\
      flex-direction: column;\
      justify-content: center;\
      align-items: center;\
      background: radial-gradient(circle at 30% 30%, #2e1b3a, #0b0b16);\
      z-index: 10;\
      padding: 2rem;\
      text-align: center;\
      border-radius: 0;\
      color: #ffecce;\
      text-shadow: 0 0 40px rgba(255, 180, 80, 0.5);\
      pointer-events: none;\
    \}\
\
    .birthday-message h1 \{\
      font-family: 'Dancing Script', cursive;\
      font-size: clamp(3.5rem, 18vw, 7rem);\
      margin-bottom: 0.5rem;\
      letter-spacing: 6px;\
      color: #fddc9b;\
      text-shadow: 0 0 30px #f7b32b, 0 0 60px #f7b32b80;\
    \}\
\
    .birthday-message p \{\
      font-family: 'ZCOOL KuaiLe', cursive;\
      font-size: clamp(1.6rem, 7vw, 3.2rem);\
      line-height: 1.6;\
      max-width: 800px;\
      margin: 0.5rem 0;\
      background: rgba(0,0,0,0.2);\
      padding: 0.8rem 1.8rem;\
      border-radius: 60px;\
      backdrop-filter: blur(4px);\
      border: 1px solid rgba(255, 215, 150, 0.3);\
    \}\
\
    /* \uc0\u23548 \u33322 \u25552 \u31034  */\
    .nav-hint \{\
      position: absolute;\
      bottom: 2.5rem;\
      left: 0;\
      width: 100%;\
      text-align: center;\
      font-size: clamp(1rem, 4vw, 1.8rem);\
      color: rgba(255, 240, 200, 0.7);\
      letter-spacing: 4px;\
      text-shadow: 0 2px 12px #00000055;\
      z-index: 20;\
      background: linear-gradient(90deg, transparent, rgba(255,215,150,0.1), transparent);\
      padding: 0.6rem 0;\
      backdrop-filter: blur(2px);\
      pointer-events: none;\
    \}\
\
    .nav-hint i \{\
      display: inline-block;\
      margin: 0 12px;\
      font-style: normal;\
      background: rgba(0,0,0,0.2);\
      padding: 0 16px;\
      border-radius: 40px;\
      border: 1px solid rgba(255,215,150,0.2);\
    \}\
\
    /* \uc0\u24038 \u21491 \u31661 \u22836  (\u21482 \u22312 \u38750 \u31227 \u21160 \u31471 \u26174 \u31034 ) */\
    .arrow-nav \{\
      position: absolute;\
      top: 50%;\
      transform: translateY(-50%);\
      z-index: 30;\
      font-size: 3rem;\
      color: rgba(255, 235, 180, 0.6);\
      background: rgba(0, 0, 0, 0.2);\
      backdrop-filter: blur(6px);\
      width: 64px;\
      height: 64px;\
      border-radius: 50%;\
      display: flex;\
      align-items: center;\
      justify-content: center;\
      cursor: pointer;\
      transition: all 0.2s;\
      border: 1px solid rgba(255, 215, 150, 0.2);\
      box-shadow: 0 4px 20px rgba(0,0,0,0.3);\
      font-weight: bold;\
      text-shadow: 0 0 10px #00000088;\
      user-select: none;\
    \}\
\
    .arrow-nav:hover \{\
      background: rgba(255, 215, 150, 0.25);\
      color: #ffe9b0;\
      border-color: #ffd58c;\
      transform: translateY(-50%) scale(1.06);\
    \}\
\
    .arrow-left \{\
      left: 1.5rem;\
    \}\
    .arrow-right \{\
      right: 1.5rem;\
    \}\
\
    /* \uc0\u28895 \u33457 \u30011 \u24067  (\u26368 \u21518 \u19968 \u39029 ) */\
    #fireworks-canvas \{\
      position: absolute;\
      top: 0;\
      left: 0;\
      width: 100%;\
      height: 100%;\
      pointer-events: none;\
      z-index: 5;\
    \}\
\
    /* \uc0\u31227 \u21160 \u31471 \u36866 \u37197 \u65306 \u35302 \u25720 \u21451 \u22909  */\
    @media (max-width: 640px) \{\
      .photo-title \{\
        font-size: clamp(1.8rem, 10vw, 3.2rem);\
      \}\
      .photo-frame \{\
        width: 94%;\
        max-height: 60vh;\
        padding: 0.5rem;\
      \}\
      .photo-frame img \{\
        max-height: 50vh;\
      \}\
      .arrow-nav \{\
        width: 48px;\
        height: 48px;\
        font-size: 2.2rem;\
        opacity: 0.7;\
      \}\
      .arrow-left \{\
        left: 0.6rem;\
      \}\
      .arrow-right \{\
        right: 0.6rem;\
      \}\
      .birthday-message p \{\
        font-size: clamp(1.2rem, 5vw, 2.2rem);\
        padding: 0.4rem 1rem;\
      \}\
      .birthday-message h1 \{\
        font-size: clamp(2.8rem, 14vw, 5rem);\
      \}\
      .nav-hint \{\
        bottom: 1.2rem;\
        font-size: clamp(0.8rem, 3.5vw, 1.2rem);\
      \}\
      .nav-hint i \{\
        margin: 0 6px;\
        padding: 0 10px;\
      \}\
    \}\
\
    /* \uc0\u38544 \u34255 \u28378 \u21160 \u26465  */\
    .slide::-webkit-scrollbar \{\
      display: none;\
    \}\
    .slide \{\
      -ms-overflow-style: none;\
      scrollbar-width: none;\
    \}\
  </style>\
</head>\
<body>\
\
<div class="fullscreen-carousel" id="carousel">\
  <div class="slides-wrapper" id="slidesWrapper">\
\
    <!-- 1. \uc0\u33457 \u20043 \u26085  -->\
    <div class="slide" data-index="0">\
      <div class="photo-title">\uc0\u55356 \u57144  \u33457 \u20043 \u26085 </div>\
      <div class="photo-frame"><img src="1.JPG" alt="\uc0\u33457 \u20043 \u26085 "></div>\
    </div>\
    <!-- 2. \uc0\u23567 \u29579 \u23376 - B612\u21495 \u23567 \u34892 \u26143  -->\
    <div class="slide" data-index="1">\
      <div class="photo-title">\uc0\u55356 \u57119  \u23567 \u29579 \u23376  \'b7 B612</div>\
      <div class="photo-frame"><img src="2.JPG" alt="\uc0\u23567 \u29579 \u23376 - B612\u21495 \u23567 \u34892 \u26143 "></div>\
    </div>\
    <!-- 3. \uc0\u22235 \u21494 \u33609 \u55356 \u57152  -->\
    <div class="slide" data-index="2">\
      <div class="photo-title">\uc0\u55356 \u57152  \u22235 \u21494 \u33609 </div>\
      <div class="photo-frame"><img src="3.JPG" alt="\uc0\u22235 \u21494 \u33609 \u55356 \u57152 "></div>\
    </div>\
    <!-- 4. INFP & ISTJ -->\
    <div class="slide" data-index="3">\
      <div class="photo-title">\uc0\u55357 \u56491  INFP & ISTJ</div>\
      <div class="photo-frame"><img src="4.JPG" alt="INFP & ISTJ"></div>\
    </div>\
    <!-- 5. \uc0\u20599 \u25293  -->\
    <div class="slide" data-index="4">\
      <div class="photo-title">\uc0\u55357 \u56568  \u20599 \u25293 </div>\
      <div class="photo-frame"><img src="5.JPG" alt="\uc0\u20599 \u25293 "></div>\
    </div>\
    <!-- 6. \uc0\u30561 \u35273 \u26102 \u38388 \u21040  -->\
    <div class="slide" data-index="5">\
      <div class="photo-title">\uc0\u55357 \u56884  \u30561 \u35273 \u26102 \u38388 \u21040 </div>\
      <div class="photo-frame"><img src="6.JPG" alt="\uc0\u30561 \u35273 \u26102 \u38388 \u21040 "></div>\
    </div>\
    <!-- 7. \uc0\u35757 \u32451 \u31243 \u23376  + \u20840 \u23631 \u31069 \u31119  + \u28895 \u33457  -->\
    <div class="slide" data-index="6">\
      <div class="photo-title">\uc0\u55356 \u57291 \u65039  \u35757 \u32451 \u31243 \u23376 </div>\
      <div class="photo-frame"><img src="7.JPG" alt="\uc0\u35757 \u32451 \u31243 \u23376 "></div>\
      <!-- \uc0\u20840 \u23631 \u31069 \u31119 \u23618  -->\
      <div class="birthday-message">\
        <h1>\uc0\u55356 \u57218  \u29983 \u26085 \u24555 \u20048 </h1>\
        <p>\uc0\u24895 \u20320 \u30340 \u19990 \u30028 \u27704 \u36828 \u26377 \u33457 \u12289 \u26377 \u20809 \u12289 <br>\u26377 \u26399 \u24453 \u26032 \u19968 \u22825 \u21040 \u26469 \u30340 \u29702 \u30001 </p>\
      </div>\
      <!-- \uc0\u28895 \u33457  canvas -->\
      <canvas id="fireworks-canvas"></canvas>\
    </div>\
  </div>\
\
  <!-- \uc0\u23548 \u33322 \u31661 \u22836  -->\
  <div class="arrow-nav arrow-left" id="prevBtn">\'8b</div>\
  <div class="arrow-nav arrow-right" id="nextBtn">\'9b</div>\
\
  <!-- \uc0\u24213 \u37096 \u25552 \u31034  -->\
  <div class="nav-hint">\
    <i>\uc0\u11013 \u65039 </i> \u24038 \u21491 \u26041 \u21521 \u38190 \u20999 \u25442  <i>\u10145 \u65039 </i>\
  </div>\
</div>\
\
<!-- \uc0\u33258 \u21160 \u25773 \u25918 \u38899 \u20048  (\u32972 \u26223 ) -->\
<audio id="bgMusic" autoplay loop preload="auto">\
  <source src="music.mp3" type="audio/mpeg">\
  \uc0\u24744 \u30340 \u27983 \u35272 \u22120 \u19981 \u25903 \u25345 \u38899 \u39057 \u25773 \u25918 \u12290 \
</audio>\
\
<script>\
  (function()\{\
    // ---- \uc0\u37197 \u32622  ----\
    const slidesWrapper = document.getElementById('slidesWrapper');\
    const slides = document.querySelectorAll('.slide');\
    const totalSlides = slides.length;\
    let currentIndex = 0;\
    let isTransitioning = false;\
\
    const prevBtn = document.getElementById('prevBtn');\
    const nextBtn = document.getElementById('nextBtn');\
\
    // \uc0\u38899 \u20048 \u33258 \u21160 \u25773 \u25918 \u65288 \u37096 \u20998 \u27983 \u35272 \u22120 \u38656 \u29992 \u25143 \u20132 \u20114 \u65292 \u20294 autoplay\u24050 \u20889 \u65292 \u20877 \u21152 \u19968 \u23618 \u20445 \u38505 \u65289 \
    const music = document.getElementById('bgMusic');\
    // \uc0\u22914 \u26524 \u33258 \u21160 \u25773 \u25918 \u34987 \u38459 \u27490 \u65292 \u28857 \u20987 \u39029 \u38754 \u20219 \u24847 \u22788 \u23581 \u35797 \u25773 \u25918 \
    document.addEventListener('click', function resumeAudio() \{\
      if (music.paused) \{\
        music.play().catch(() => \{\});\
      \}\
    \}, \{ once: false \});\
\
    // \uc0\u26356 \u26032 \u24187 \u28783 \u29255 \u20301 \u32622 \
    function goToSlide(index) \{\
      if (isTransitioning || index === currentIndex) return;\
      if (index < 0) index = 0;\
      if (index >= totalSlides) index = totalSlides - 1;\
      isTransitioning = true;\
      currentIndex = index;\
      slidesWrapper.style.transform = `translateX(-$\{currentIndex * 100\}%)`;\
      // \uc0\u35302 \u21457 \u28895 \u33457 \u65306 \u22914 \u26524 \u26159 \u26368 \u21518 \u19968 \u39029  (index === totalSlides-1)\
      if (currentIndex === totalSlides - 1) \{\
        initFireworks();\
      \} else \{\
        // \uc0\u28165 \u38500 \u28895 \u33457  (\u38544 \u34255 canvas)\
        const canvas = document.getElementById('fireworks-canvas');\
        if (canvas) \{\
          canvas.style.display = 'none';\
          const ctx = canvas.getContext('2d');\
          ctx.clearRect(0, 0, canvas.width, canvas.height);\
        \}\
      \}\
      setTimeout(() => \{\
        isTransitioning = false;\
      \}, 520);\
    \}\
\
    // \uc0\u19978 \u19968 \u39029  / \u19979 \u19968 \u39029 \
    function prevSlide() \{\
      if (currentIndex > 0) goToSlide(currentIndex - 1);\
    \}\
    function nextSlide() \{\
      if (currentIndex < totalSlides - 1) goToSlide(currentIndex + 1);\
    \}\
\
    // \uc0\u20107 \u20214 \u32465 \u23450 \
    prevBtn.addEventListener('click', prevSlide);\
    nextBtn.addEventListener('click', nextSlide);\
\
    // \uc0\u38190 \u30424 \u30417 \u21548  (\u24038 \u21491 \u26041 \u21521 \u38190 )\
    document.addEventListener('keydown', (e) => \{\
      if (e.key === 'ArrowLeft') \{\
        e.preventDefault();\
        prevSlide();\
      \} else if (e.key === 'ArrowRight') \{\
        e.preventDefault();\
        nextSlide();\
      \}\
    \});\
\
    // \uc0\u35302 \u25720 \u28369 \u21160  (\u31616 \u21333 \u25903 \u25345 )\
    let touchStartX = 0;\
    let touchEndX = 0;\
    const carousel = document.getElementById('carousel');\
    carousel.addEventListener('touchstart', (e) => \{\
      touchStartX = e.changedTouches[0].screenX;\
    \}, \{ passive: true \});\
    carousel.addEventListener('touchend', (e) => \{\
      touchEndX = e.changedTouches[0].screenX;\
      const diff = touchStartX - touchEndX;\
      if (Math.abs(diff) > 40) \{\
        if (diff > 0) \{\
          nextSlide();\
        \} else \{\
          prevSlide();\
        \}\
      \}\
    \}, \{ passive: true \});\
\
    // ---- \uc0\u55356 \u57222  \u28895 \u33457  (\u21482 \u22312 \u26368 \u21518 \u19968 \u39029 ) ----\
    function initFireworks() \{\
      const canvas = document.getElementById('fireworks-canvas');\
      if (!canvas) return;\
      canvas.style.display = 'block';\
      canvas.width = window.innerWidth;\
      canvas.height = window.innerHeight;\
      const ctx = canvas.getContext('2d');\
\
      // \uc0\u31890 \u23376 \u25968 \u32452 \
      let particles = [];\
      const colors = ['#ffd700', '#ff6b6b', '#ff9f43', '#f368e0', '#48dbfb', '#1dd1a1', '#feca57', '#ff9ff3'];\
\
      class Particle \{\
        constructor(x, y, color) \{\
          this.x = x;\
          this.y = y;\
          this.color = color || colors[Math.floor(Math.random() * colors.length)];\
          this.radius = Math.random() * 4 + 2;\
          this.vx = (Math.random() - 0.5) * 10;\
          this.vy = (Math.random() - 0.5) * 10 - 4;\
          this.alpha = 1;\
          this.deceleration = 0.98;\
          this.gravity = 0.1;\
          this.life = 1;\
          this.damping = 0.99;\
        \}\
        update() \{\
          this.vx *= this.damping;\
          this.vy *= this.damping;\
          this.vy += this.gravity;\
          this.x += this.vx;\
          this.y += this.vy;\
          this.alpha -= 0.012;\
          this.life -= 0.012;\
          this.radius *= 0.995;\
        \}\
        draw() \{\
          ctx.save();\
          ctx.globalAlpha = Math.max(this.alpha, 0);\
          ctx.beginPath();\
          ctx.arc(this.x, this.y, Math.max(this.radius, 0.5), 0, Math.PI * 2);\
          ctx.fillStyle = this.color;\
          ctx.shadowColor = this.color;\
          ctx.shadowBlur = 20;\
          ctx.fill();\
          ctx.restore();\
        \}\
      \}\
\
      // \uc0\u29983 \u25104 \u28895 \u33457  (\u22810 \u20010 \u29190 \u28856 )\
      function createExplosion(cx, cy) \{\
        const count = 60 + Math.floor(Math.random() * 40);\
        const color = colors[Math.floor(Math.random() * colors.length)];\
        for (let i = 0; i < count; i++) \{\
          const angle = Math.random() * Math.PI * 2;\
          const speed = Math.random() * 5 + 2;\
          const p = new Particle(cx, cy, color);\
          p.vx = Math.cos(angle) * speed;\
          p.vy = Math.sin(angle) * speed - 1.5;\
          p.radius = Math.random() * 5 + 2;\
          particles.push(p);\
        \}\
      \}\
\
      // \uc0\u38543 \u26426 \u21457 \u23556 \u28895 \u33457  (\u20174 \u24213 \u37096 \u21521 \u19978 )\
      function launchFirework() \{\
        const x = Math.random() * canvas.width * 0.8 + canvas.width * 0.1;\
        const y = canvas.height * 0.2 + Math.random() * canvas.height * 0.4;\
        createExplosion(x, y);\
      \}\
\
      // \uc0\u21160 \u30011 \u24490 \u29615 \
      let frameId = null;\
      function animate() \{\
        ctx.clearRect(0, 0, canvas.width, canvas.height);\
        // \uc0\u26356 \u26032 \u31890 \u23376 \
        for (let i = particles.length - 1; i >= 0; i--) \{\
          const p = particles[i];\
          p.update();\
          if (p.alpha <= 0.02 || p.life <= 0) \{\
            particles.splice(i, 1);\
          \} else \{\
            p.draw();\
          \}\
        \}\
        // \uc0\u22914 \u26524 \u31890 \u23376 \u22826 \u23569 \u65292 \u34917 \u20805 \u26032 \u28895 \u33457 \
        if (particles.length < 50) \{\
          launchFirework();\
          if (Math.random() < 0.3) launchFirework(); // \uc0\u20598 \u23572 \u21452 \u21709 \
        \}\
        frameId = requestAnimationFrame(animate);\
      \}\
\
      // \uc0\u28165 \u38500 \u26087 \u21160 \u30011 \u65292 \u24320 \u22987 \u26032 \u21160 \u30011 \
      if (frameId) cancelAnimationFrame(frameId);\
      particles = [];\
      // \uc0\u21021 \u22987 \u29983 \u25104 \u20960 \u26421 \
      for (let i = 0; i < 5; i++) \{\
        setTimeout(() => \{\
          launchFirework();\
        \}, i * 400);\
      \}\
      animate();\
\
      // \uc0\u31383 \u21475 \u23610 \u23544 \u21464 \u21270 \u37325 \u32622 canvas\
      function resizeCanvas() \{\
        canvas.width = window.innerWidth;\
        canvas.height = window.innerHeight;\
      \}\
      window.addEventListener('resize', resizeCanvas);\
      // \uc0\u23384 \u20648 \u28165 \u29702 \u20989 \u25968  (\u21487 \u36873 )\
      canvas._resizeHandler = resizeCanvas;\
    \}\
\
    // \uc0\u22914 \u26524 \u19968 \u24320 \u22987 \u23601 \u26159 \u26368 \u21518 \u19968 \u39029 \u65288 \u27604 \u22914 \u21482 \u26377 7\u24352 \u65292 \u21021 \u22987 \u31532 0\u39029 \u65292 \u19981 \u20250 \u35302 \u21457 \u65292 \u20294 \u20197 \u38450 \u19975 \u19968 \u65289 \
    // \uc0\u20294 \u21021 \u22987 \u22312 \u31532 \u19968 \u39029 \u65292 \u25152 \u20197 \u27809 \u38382 \u39064 \u12290  \u25163 \u21160 \u26816 \u26597 \u24403 \u21069 \u39029 \
    // \uc0\u22312 goToSlide \u20013 \u24050 \u22788 \u29702 \
\
    // \uc0\u39069 \u22806 \u65306 \u21021 \u22987 \u26174 \u31034 \u31532 \u19968 \u39029 \u65292 \u19988 \u30830 \u20445 \u28895 \u33457 \u38544 \u34255 \
    window.addEventListener('load', function() \{\
      goToSlide(0);\
      // \uc0\u30830 \u20445 canvas\u38544 \u34255 \
      const canvas = document.getElementById('fireworks-canvas');\
      if (canvas) \{\
        canvas.style.display = 'none';\
        canvas.width = window.innerWidth;\
        canvas.height = window.innerHeight;\
      \}\
      // \uc0\u23581 \u35797 \u33258 \u21160 \u25773 \u25918 \u38899 \u20048 \
      music.play().catch(() => \{\});\
    \});\
\
    // \uc0\u37325 \u32472 \u35843 \u25972 \
    window.addEventListener('resize', function() \{\
      const canvas = document.getElementById('fireworks-canvas');\
      if (canvas && canvas.style.display !== 'none') \{\
        canvas.width = window.innerWidth;\
        canvas.height = window.innerHeight;\
      \}\
    \});\
\
  \})();\
</script>\
\
<!-- \uc0\u22791 \u27880 \u65306 \u35831 \u30830 \u20445  1.JPG ~ 7.JPG \u20197 \u21450  music.mp3 \u20301 \u20110 \u21516 \u19968 \u30446 \u24405 \u19979  -->\
</body>\
</html>}
