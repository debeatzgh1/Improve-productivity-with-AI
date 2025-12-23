<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Digital Portfolio – Apps & Tools</title>

<style>
:root{
  --primary:#16a34a;
  --dark:#0f172a;
  --light:#f8fafc;
}

*{box-sizing:border-box;margin:0;padding:0}

body{
  font-family:system-ui,-apple-system,Segoe UI,Roboto,sans-serif;
  background:var(--light);
  color:#1e293b;
}

/* Header */
header{
  padding:40px 16px;
  text-align:center;
}
header h1{
  font-size:clamp(24px,5vw,38px);
  margin-bottom:10px;
}
header p{
  max-width:700px;
  margin:auto;
  opacity:.85;
}

/* Carousel */
.carousel-wrap{
  max-width:1200px;
  margin:auto;
  padding:20px 16px 60px;
}
.carousel{
  display:flex;
  gap:20px;
  overflow-x:auto;
  scroll-snap-type:x mandatory;
}

/* Card */
.card{
  min-width:280px;
  max-width:320px;
  background:#fff;
  border-radius:20px;
  box-shadow:0 10px 25px rgba(0,0,0,.08);
  overflow:hidden;
  scroll-snap-align:start;
  display:flex;
  flex-direction:column;
}
.card img{
  width:100%;
  height:180px;
  object-fit:cover;
}
.card-content{
  padding:18px;
  display:flex;
  flex-direction:column;
  flex:1;
}
.card h3{
  font-size:18px;
  margin-bottom:8px;
}
.card p{
  font-size:14px;
  opacity:.85;
  flex:1;
}

/* Buttons */
.btns{
  display:flex;
  gap:10px;
  margin-top:14px;
}
.btn{
  flex:1;
  padding:10px;
  border-radius:20px;
  font-size:13px;
  font-weight:600;
  cursor:pointer;
  border:none;
}
.preview{
  background:var(--dark);
  color:#fff;
}
.install{
  background:var(--primary);
  color:#fff;
}

/* Overlay */
#overlay{
  position:fixed;
  inset:0;
  background:#fff;
  display:none;
  z-index:99999;
}

/* Top Controls */
.overlay-controls{
  position:fixed;
  top:12px;
  left:12px;
  display:flex;
  gap:10px;
  z-index:100000;
}

.ctrl-btn{
  background:#111;
  color:#fff;
  padding:8px 14px;
  border-radius:999px;
  font-size:13px;
  cursor:pointer;
  border:none;
}

/* Iframe */
#viewer{
  width:100%;
  height:100%;
  border:none;
}
</style>
</head>

<body>

<header>
  <h1>🚀 Digital Apps & Creator Tools</h1>
  <p>Productivity apps, AI platforms, and digital solutions for creators and entrepreneurs.</p>
</header>

<section class="carousel-wrap">
  <div class="carousel">

    <div class="card">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/07/imagine_14268752983581284557979788324544592.jpg">
      <div class="card-content">
        <h3>SocialCreator TechShop</h3>
        <p>AI tools, productivity ideas, and smart digital solutions.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.socialcreator.com/techshop')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.socialcreator.com/techshop')">Install</button>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- Overlay -->
<div id="overlay">
  <div class="overlay-controls">
    <button class="ctrl-btn" onclick="closePreview()">✖ Close</button>
    <button class="ctrl-btn" onclick="toggleFullscreen()">⛶ Fullscreen</button>
  </div>

  <iframe id="viewer"
    sandbox="allow-scripts allow-same-origin allow-forms allow-popups">
  </iframe>
</div>

<script>
const STORAGE_KEY = "lastOpenedApp";

/* Open Preview */
function openPreview(url){
  const overlay = document.getElementById("overlay");
  const viewer = document.getElementById("viewer");

  viewer.src = url;
  overlay.style.display = "block";

  localStorage.setItem(STORAGE_KEY, url);
}

/* Close Preview */
function closePreview(){
  const overlay = document.getElementById("overlay");
  const viewer = document.getElementById("viewer");

  viewer.src = "";
  overlay.style.display = "none";

  localStorage.removeItem(STORAGE_KEY);
}

/* Fullscreen Toggle */
function toggleFullscreen(){
  const iframe = document.getElementById("viewer");

  if (!document.fullscreenElement) {
    iframe.requestFullscreen().catch(err => console.log(err));
  } else {
    document.exitFullscreen();
  }
}

/* Install */
function openInstall(url){
  window.open(url, "_blank");
}

/* Restore Last Opened */
window.addEventListener("load", () => {
  const lastApp = localStorage.getItem(STORAGE_KEY);
  if (lastApp) {
    openPreview(lastApp);
  }
});
</script>

</body>
</html>
