
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Digital Portfolio – SocialCreator Apps</title>

<style>
:root{
  --primary:#16a34a;
  --dark:#0f172a;
  --light:#f8fafc;
  --badge:#f59e0b;
}
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:system-ui,-apple-system,Segoe UI,Roboto,sans-serif;
  background:var(--light);
  color:#1e293b;
}
header{
  padding:40px 16px;
  text-align:center;
}
header h1{
  font-size:clamp(24px,5vw,38px);
  margin-bottom:10px;
}
header p{
  max-width:720px;
  margin:auto;
  opacity:.85;
}
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
.carousel::-webkit-scrollbar{height:8px}
.carousel::-webkit-scrollbar-thumb{
  background:#cbd5e1;
  border-radius:20px;
}
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
  position:relative;
}
.badge{
  position:absolute;
  top:14px;
  left:14px;
  background:var(--badge);
  color:#fff;
  font-size:11px;
  font-weight:700;
  padding:6px 12px;
  border-radius:999px;
  z-index:2;
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
.preview{background:var(--dark);color:#fff}
.install{background:var(--primary);color:#fff}
#overlay{
  position:fixed;
  inset:0;
  background:#fff;
  display:none;
  z-index:99999;
}
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
#viewer{
  width:100%;
  height:100%;
  border:none;
}
</style>
</head>

<body>

<header>
  <h1>🚀 SocialCreator Apps Hub</h1>
  <p>Explore popular AI tools, digital products, side-hustle platforms, and creator resources.</p>
</header>

<section class="carousel-wrap">
  <div class="carousel">

    <!-- TechShop -->
    <div class="card">
      <span class="badge">POPULAR</span>
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/07/imagine_14268752983581284557979788324544592.jpg">
      <div class="card-content">
        <h3>TechShop</h3>
        <p>AI tools, productivity resources, and smart digital solutions for creators.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.socialcreator.com/techshop')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.socialcreator.com/techshop')">Open</button>
        </div>
      </div>
    </div>

    <!-- SideHustle Hub -->
    <div class="card">
      <span class="badge">POPULAR</span>
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/minimalistbusinessiconthemealaptopwithdollarsignsorgrowtharrows4197483127374475983.jpg">
      <div class="card-content">
        <h3>SideHustle Hub</h3>
        <p>Proven income ideas, online business tools, and AI-powered monetization.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.socialcreator.com/sidehustle')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.socialcreator.com/sidehustle')">Open</button>
        </div>
      </div>
    </div>

    <!-- Debeatzgh Smart Links -->
    <div class="card">
      <span class="badge">CREATOR HUB</span>
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/wp-17550753355015215823208011315422.jpg">
      <div class="card-content">
        <h3>Debeatzgh Smart Links</h3>
        <p>All-in-one creator bio link featuring apps, projects, social profiles, and offers.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://msha.ke/debeatzgh')">Preview</button>
          <button class="btn install" onclick="openInstall('[https://debeatzgh1.github.io/Home-/](https://debeatzgh1.github.io/Home-/')">Open</button>
        </div>
      </div>
    </div>

    <!-- MB Online -->
    <div class="card">
      <span class="badge">POPULAR</span>
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/09/asleekandmoderngoogleclassroombannerfortechaihubfeaturingfuturisticdigitalelements261807892942313727.jpg">
      <div class="card-content">
        <h3>MB Online Store</h3>
        <p>Digital products, affiliate tools, online income resources, and creator deals.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://debeatzgh1.github.io/MB--online-/')">Preview</button>
          <button class="btn install" onclick="openInstall('https://debeatzgh1.github.io/MB--online-/')">Open</button>
        </div>
      </div>
    </div>

  </div>
</section>

<div id="overlay">
  <div class="overlay-controls">
    <button class="ctrl-btn" onclick="closePreview()">✖ Close</button>
    <button class="ctrl-btn" onclick="toggleFullscreen()">⛶ Fullscreen</button>
  </div>
  <iframe id="viewer" sandbox="allow-scripts allow-same-origin allow-forms allow-popups"></iframe>
</div>

<script>
const STORAGE_KEY = "lastOpenedSocialCreatorApp";

function openPreview(url){
  viewer.src = url;
  overlay.style.display = "block";
  localStorage.setItem(STORAGE_KEY, url);
}
function closePreview(){
  viewer.src = "";
  overlay.style.display = "none";
  localStorage.removeItem(STORAGE_KEY);
}
function toggleFullscreen(){
  if (!document.fullscreenElement) {
    viewer.requestFullscreen().catch(()=>{});
  } else {
    document.exitFullscreen();
  }
}
function openInstall(url){
  window.open(url, "_blank");
}
window.addEventListener("load", () => {
  const last = localStorage.getItem(STORAGE_KEY);
  if (last) openPreview(last);
});
</script>

</body>
</html>
