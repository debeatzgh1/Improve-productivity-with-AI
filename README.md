
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Debeatzgh – AI Productivity Hub</title>

<style>
/* ===== BASE ===== */
body{
  margin:0;
  font-family:system-ui,-apple-system,BlinkMacSystemFont;
  background:#f3f4f6;
  color:#111827;
}

/* ===== HERO ===== */
.hero{
  padding:60px 20px;
  text-align:center;
  background:linear-gradient(135deg,#0f172a,#1e293b);
  color:#fff;
}
.hero h1{
  font-size:2rem;
  margin-bottom:12px;
}
.hero p{
  max-width:680px;
  margin:auto;
  font-size:1rem;
  opacity:.9;
}

/* ===== CONTENT ===== */
.section{
  max-width:1100px;
  margin:50px auto;
  padding:0 16px;
}
.card{
  background:#fff;
  border-radius:20px;
  box-shadow:0 12px 30px rgba(0,0,0,.15);
  padding:30px;
  text-align:center;
}
.card h2{
  margin-bottom:10px;
}
.card p{
  font-size:15px;
  color:#555;
}

/* ===== FLOATING BUTTON ===== */
#floating-launcher{
  position:fixed;
  bottom:22px;
  left:20px;
  background:#16a34a;
  color:#fff;
  padding:12px 20px;
  font-size:14px;
  font-weight:600;
  border-radius:24px;
  box-shadow:0 6px 18px rgba(0,0,0,.25);
  cursor:pointer;
  z-index:99999;
  transition:.2s ease;
}
#floating-launcher:hover{
  transform:scale(1.05);
  opacity:.95;
}

/* ===== OVERLAY ===== */
#launcher-overlay{
  position:fixed;
  inset:0;
  background:#fff;
  display:none;
  flex-direction:column;
  z-index:100000;
}

/* ===== TOP BAR ===== */
#launcher-top{
  position:relative;
  background:#0f172a;
  height:48px;
}

/* CLOSE BUTTON (TOP LEFT) */
#launcher-close{
  position:absolute;
  top:10px;
  left:12px;
  cursor:pointer;
  font-size:18px;
  color:#fff;
  background:rgba(0,0,0,.35);
  padding:4px 10px;
  border-radius:10px;
}

/* ===== IFRAME ===== */
#launcher-frame{
  flex:1;
  width:100%;
  border:none;
}
</style>
</head>

<body>

<!-- HERO -->
<section class="hero">
  <h1>AI Productivity Web App</h1>
  <p>
    A smart digital workspace for creators, entrepreneurs, and hustlers to
    improve productivity using AI-powered tools and ideas.
  </p>
</section>

<!-- CONTENT -->
<section class="section">
  <div class="card">
    <h2>Improve Productivity with AI</h2>
    <p>
      Launch the full web application instantly using the floating button.
      You can close it anytime and your last open state will be remembered.
    </p>
  </div>
</section>

<!-- FLOATING LAUNCHER -->
<div id="floating-launcher">Web</div>

<!-- FULLSCREEN OVERLAY -->
<div id="launcher-overlay">
  <div id="launcher-top">
    <span id="launcher-close">✖</span>
  </div>
  <iframe
    id="launcher-frame"
    sandbox="allow-scripts allow-same-origin allow-forms allow-popups"
  ></iframe>
</div>

<!-- SCRIPT -->
<script>
(function(){

  var launcher = document.getElementById("floating-launcher");
  var overlay  = document.getElementById("launcher-overlay");
  var frame    = document.getElementById("launcher-frame");
  var closeBtn = document.getElementById("launcher-close");

  var APP_URL = "https://debeatzgh1.github.io/Improve-productivity-with-AI-Web-App-project-/";
  var STORAGE_KEY = "ai_productivity_launcher_open";

  function openLauncher(){
    overlay.style.display = "flex";
    frame.src = APP_URL;
    localStorage.setItem(STORAGE_KEY,"open");
  }

  function closeLauncher(){
    overlay.style.display = "none";
    frame.src = "";
    localStorage.removeItem(STORAGE_KEY);
  }

  launcher.addEventListener("click", openLauncher);
  closeBtn.addEventListener("click", closeLauncher);

  /* Restore last state */
  window.addEventListener("load", function(){
    if(localStorage.getItem(STORAGE_KEY)==="open"){
      openLauncher();
    }
  });

})();
</script>

</body>
</html>
