<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rice Ceremony Invitation - Pravisha</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Noto+Serif&display=swap');

    body {
      margin: 0;
      padding: 30px 10px;
      font-family: 'Noto Serif', serif;
      background: linear-gradient(135deg, #fffdf7, #fef6ec);
      display: flex;
      justify-content: center;
      min-height: 100vh;
      overflow-y: auto;
      overflow-x: hidden;
      position: relative;
    }

    /* Background Alpona */
    .alpona-bg {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 500px;
      height: 500px;
      background: url("https://i.ibb.co/Y3gzJ4m/alpona.png") no-repeat center/contain;
      opacity: 0.08;
      animation: spin 60s linear infinite;
      z-index: 0;
    }
    @keyframes spin {
      from { transform: translate(-50%, -50%) rotate(0deg);}
      to { transform: translate(-50%, -50%) rotate(360deg);}
    }

    /* Floating balloons */
    .balloon {
      position: fixed;
      bottom: -150px;
      width: 60px;
      opacity: 0.8;
      animation: fly 15s linear infinite;
      z-index: 0;
    }
    @keyframes fly {
      0% { transform: translateY(0) scale(1);}
      100% { transform: translateY(-120vh) scale(1.1);}
    }
    .balloon:nth-child(2) { left: 10%; animation-delay: 0s; }
    .balloon:nth-child(3) { left: 25%; animation-delay: 4s; width: 70px; }
    .balloon:nth-child(4) { left: 50%; animation-delay: 2s; width: 50px; }
    .balloon:nth-child(5) { left: 70%; animation-delay: 6s; }
    .balloon:nth-child(6) { left: 85%; animation-delay: 3s; width: 75px; }

    /* Invitation card */
    .card {
      position: relative;
      background: #fffefb;
      border-radius: 20px;
      padding: 30px;
      max-width: 620px;
      width: 100%;
      text-align: center;
      box-shadow: 0 8px 25px rgba(0,0,0,0.15);
      animation: fadeIn 1.2s ease-in-out;
      z-index: 2;
      overflow: hidden;
      height: 20%;       
      min-height: unset; 
      /* Bengali Alpana border */
      
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px);}
      to { opacity: 1; transform: translateY(0);}
    }

    h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 2.4em;
      color: #7a5c2e;
      margin: 0 0 12px;
      animation: glow 2s infinite alternate;
    }
    @keyframes glow {
      from { text-shadow: 0 0 6px #f9e6b3; }
      to { text-shadow: 0 0 16px #d4af37; }
    }

    h2, p {
      opacity: 0;
      animation: fadeText 1s forwards;
    }
    h2 { animation-delay: 0.8s; position: relative; z-index: 2; }
    p:nth-of-type(1) { animation-delay: 0.4s; }
    p:nth-of-type(2) { animation-delay: 1.2s; }
    p:nth-of-type(3) { animation-delay: 1.6s; }
    .footer { animation-delay: 2s; }

    @keyframes fadeText {
      from {opacity: 0; transform: translateY(15px);}
      to {opacity: 1; transform: translateY(0);}
    }

    .highlight {
      color: #b8860b;
      font-weight: bold;
    }

    .footer {
      margin-top: 20px;
      font-size: 0.95em;
      color: #555;
      opacity: 0;
      animation: fadeText 1s forwards;
    }

    .icon {
      width: 110px;
      margin: 10px auto 15px;
      display: block;
      animation: float 4s ease-in-out infinite;
      position: relative;
      z-index: 2;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-12px); }
      100% { transform: translateY(0); }
    }

    .btn {
      display: inline-block;
      margin-top: 15px;
      background: #fff;
      color: #7a5c2e;
      border: 2px solid #d4af37;
      padding: 10px 18px;
      border-radius: 8px;
      text-decoration: none;
      font-size: 1em;
      font-weight: bold;
      transition: 0.3s;
      animation: pulse 2s infinite;
      position: relative;
      z-index: 2;
    }
    .btn:hover {
      background: #fceecf;
    }
    @keyframes pulse {
      0% { box-shadow: 0 0 0 0 rgba(212,175,55,0.6);}
      70% { box-shadow: 0 0 0 12px rgba(212,175,55,0);}
      100% { box-shadow: 0 0 0 0 rgba(212,175,55,0);}
    }

    /* Sparkles inside card */
    .sparkle {
      position: absolute;
      width: 8px;
      height: 8px;
      background: gold;
      border-radius: 50%;
      opacity: 0.7;
      animation: sparkleMove 6s linear infinite;
    }
    .sparkle:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
    .sparkle:nth-child(2) { top: 40%; left: 80%; animation-delay: 2s; }
    .sparkle:nth-child(3) { top: 70%; left: 30%; animation-delay: 4s; }
    .sparkle:nth-child(4) { top: 85%; left: 60%; animation-delay: 1s; }

    @keyframes sparkleMove {
      0% { transform: scale(0.5) translateY(0); opacity: 0.7; }
      50% { transform: scale(1.2) translateY(-20px); opacity: 1; }
      100% { transform: scale(0.5) translateY(0); opacity: 0.7; }
    }

    /* Rotating alpona motif behind name */
    .alpona-inside {
      position: absolute;
      top: 55%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 650px;
      height: 650px;
      background: url("https://img.freepik.com/premium-vector/line-art-alpona-mandala-flower-wedding-print-poster-cover-brochure-flyer-banner_622541-15.jpg?w=1060") no-repeat center/contain;
      opacity: 0.1;
      animation: spin 20s linear infinite;
      z-index: 1;
    }

    @media (max-width: 480px) {
      h1 { font-size: 2em; }
      h2 { font-size: 1.3em; }
      p  { font-size: 0.95em; }
      .icon { width: 85px; }
    }
  </style>
</head>
<body>

  <!-- Background Alpona -->
  <div class="alpona-bg"></div>

  <!-- Floating balloons -->
  <img src="https://d1nhio0ox7pgb.cloudfront.net/_img/g_collection_png/standard/512x512/balloon.png" class="balloon" alt="balloon">
  <img src="https://cdn-icons-png.flaticon.com/512/3784/3784476.png" class="balloon" alt="balloon">
  <img src="https://cdn-icons-png.flaticon.com/512/4208/4208599.png" class="balloon" alt="balloon">
  <img src="https://cdn-icons-png.flaticon.com/512/4208/4208599.png" class="balloon" alt="balloon">
  <img src="https://cdn-icons-png.flaticon.com/512/3784/3784476.png" class="balloon" alt="balloon">

  <!-- Invitation card -->
  <div class="card">
    <!-- Sparkles -->
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>

    <!-- Inside rotating alpona motif -->
    <div class="alpona-inside"></div>

    <img src="https://img.freepik.com/free-vector/vector-icon-design-element-logo-ad-banners-kids-menu-icon_134830-1178.jpg" class="icon" alt="Rice Ceremony">

    <h1>Rice Ceremony Invitation</h1>

    <p>With joy in our hearts, we invite you to the<br>
      <span class="highlight">Annaprashan</span> of our beloved daughter</p>

    <h2><img src="https://cdn-icons-png.flaticon.com/512/2792/2792981.png" height="40">Pravisha</h2>

    <p>📅 Date & Time: <span class="highlight">5th Oct, 2025 | 12:00 PM Onwards</span></p>
    <p>📍 Venue: <span class="highlight">Roy Anusthan Bhavan, Kirnahar, Birbhum</span></p>

    <!-- Google Maps Button -->
    <a href="https://maps.app.goo.gl/vuCgGWXbLS2Rn1V98?g_st=aw" target="_blank" class="btn">📍 View on Google Maps</a>

    <p>Your presence will bless this occasion<br> and make it memorable 🙏</p>

    <div class="footer">With love,<br>Payel & Soumesh</div>
  </div>

  <!-- Background Music -->
  <audio id="bg-music" loop autoplay>
    <source src="https://www.bensound.com/bensound-music/bensound-slowmotion.mp3" type="audio/mp3">
  </audio>
</body>
</html>
