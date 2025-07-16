<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>GERENTEX</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@500&display=swap" rel="stylesheet">
<style>
  body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #6a11cb, #2575fc);
    color: #fff;
    font-family: 'Cairo', sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    text-align: center;
    padding: 20px;
  }
  #welcome {
    font-size: 1.8em;
    min-height: 3em;
    white-space: pre-wrap;
    word-break: break-word;
    max-width: 90%;
  }
  .links {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-top: 30px;
    opacity: 0;
    transform: translateX(-50px);
    transition: all 0.6s ease;
    width: 100%;
    max-width: 300px;
  }
  .links.show {
    opacity: 1;
    transform: translateX(0);
  }
  .link-btn {
    background: rgba(255,255,255,0.1);
    border: 2px solid #fff;
    padding: 10px 15px;
    border-radius: 15px;
    color: #fff;
    text-decoration: none;
    font-size: 1em;
    display: flex;
    align-items: center;
    gap: 10px;
    transition: all 0.3s ease;
  }
  .link-btn:hover {
    background: rgba(255,255,255,0.2);
    transform: scale(1.05);
  }
  .icon {
    width: 20px;
    height: 20px;
  }
</style>
</head>
<body>
  <div id="welcome"></div>
  <div class="links" id="links">
    <a href="#" class="link-btn">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/discord.svg" alt="Discord" class="icon" style="filter: invert(1);">
      ديسكورد
    </a>
    <a href="#" class="link-btn">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/youtube.svg" alt="YouTube" class="icon" style="filter: invert(1);">
      يوتيوب
    </a>
    <a href="#" class="link-btn">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/tiktok.svg" alt="TikTok" class="icon" style="filter: invert(1);">
      تيك توك
    </a>
  </div>

<script>
const text = "مرحبا بك في GERENTEX (:\nمرحبًا بك مرة أخرى واستمتع بتجربتك معنا!";
let i = 0;
const speed = 80;

function typeWriter() {
  if (i < text.length) {
    document.getElementById("welcome").textContent += text.charAt(i);
    i++;
    setTimeout(typeWriter, speed);
  } else {
    document.getElementById("links").classList.add("show");
  }
}

typeWriter();
</script>
</body>
</html>
