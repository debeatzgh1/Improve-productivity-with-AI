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
  overflow:hidden;
}
.carousel{
  display:flex;
  gap:20px;
  overflow-x:auto;
  scroll-snap-type:x mandatory;
  padding-bottom:10px;
}
.carousel::-webkit-scrollbar{height:8px}
.carousel::-webkit-scrollbar-thumb{
  background:#cbd5e1;
  border-radius:20px;
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
  text-align:center;
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

/* Overlay iframe */
#overlay{
  position:fixed;
  inset:0;
  background:#fff;
  display:none;
  flex-direction:column;
  z-index:99999;
}
#overlay-bar{
  background:#111;
  color:#fff;
  padding:12px;
  display:flex;
  justify-content:flex-end;
}
#close{
  cursor:pointer;
  font-size:18px;
}
#viewer{
  flex:1;
  width:100%;
  border:none;
}
</style>
</head>

<body>

<header>
  <h1>🚀 Digital Apps & Creator Tools</h1>
  <p>A professional portfolio showcasing productivity apps, AI platforms, side-hustle tools, and digital solutions for creators, entrepreneurs, and online builders.</p>
</header>

<section class="carousel-wrap">
  <div class="carousel">

    <!-- Card 1 -->
    <div class="card">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/07/imagine_14268752983581284557979788324544592.jpg">
      <div class="card-content">
        <h3>SocialCreator TechShop</h3>
        <p>Dynamic platform packed with AI tools, productivity ideas, and smart digital solutions for creators and entrepreneurs.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.socialcreator.com/techshop')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.socialcreator.com/techshop')">Install</button>
        </div>
      </div>
    </div>

    <!-- Card 2 -->
    <div class="card">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/12/1763148379311_1619032177476517720.jpg">
      <div class="card-content">
        <h3>Lifestyle & Productivity Hub</h3>
        <p>All-in-one lifestyle and productivity app giving you tools, ideas, and resources you need online in one place.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.appcreator24.com/app3221514-9n1p8c')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.appcreator24.com/app3221514-9n1p8c')">Install</button>
        </div>
      </div>
    </div>

    <!-- Card 3 -->
    <div class="card">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/wp-17550753355015215823208011315422.jpg">
      <div class="card-content">
        <h3>Collaborators Hub</h3>
        <p>A shared workspace for collaboration, project contribution, and community-driven digital creation.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://debeatzgh1.github.io/Debeatzgh-Collaborators-Hub/')">Preview</button>
          <button class="btn install" onclick="openInstall('https://debeatzgh1.github.io/Debeatzgh-Collaborators-Hub/')">Install</button>
        </div>
      </div>
    </div>

    <!-- Card 4 -->
    <div class="card">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/minimalistbusinessiconthemealaptopwithdollarsignsorgrowtharrows4197483127374475983.jpg">
      <div class="card-content">
        <h3>SideHustleGenie</h3>
        <p>Your ultimate hub for AI-powered and traditional income ideas tailored for students, workers, and entrepreneurs.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.socialcreator.com/sidehustle')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.socialcreator.com/sidehustle')">Install</button>
        </div>
      </div>
    </div>

    <!-- Card 5 -->
    <div class="card">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/09/asleekandmoderngoogleclassroombannerfortechaihubfeaturingfuturisticdigitalelements261807892942313727.jpg">
      <div class="card-content">
        <h3>AI Knowledge Hub</h3>
        <p>An accessible guide to AI exploring its benefits, challenges, real-world applications, and impact on daily life.</p>
        <div class="btns">
          <button class="btn preview" onclick="openPreview('https://www.socialcreator.com/digitalstore')">Preview</button>
          <button class="btn install" onclick="openInstall('https://www.socialcreator.com/digitalstore')">Install</button>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- Iframe Overlay -->
<div id="overlay">
  <div id="overlay-bar">
    <span id="close" onclick="closePreview()">✖ Close</span>
  </div>
  <iframe id="viewer"
    sandbox="allow-scripts allow-same-origin allow-forms allow-popups">
  </iframe>
</div>

<script>
function openPreview(url){
  document.getElementById("overlay").style.display="flex";
  document.getElementById("viewer").src=url;
}
function closePreview(){
  document.getElementById("overlay").style.display="none";
  document.getElementById("viewer").src="";
}
function openInstall(url){
  window.open(url,"_blank");
}
</script>

</body>
</html>
