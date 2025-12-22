<!-- Floating Launcher -->
<div id="floating-launcher">Web</div>

<!-- Overlay -->
<div id="launcher-overlay">
  <div id="launcher-top">
    <span id="launcher-close">✖ Close</span>
  </div>
  <iframe
    id="launcher-frame"
    sandbox="allow-scripts allow-same-origin allow-forms allow-popups"
  ></iframe>
</div>
<style>
/* Floating Button */
#floating-launcher{
  position:fixed;
  bottom:22px;
  left:20px;
  background:#16a34a;
  color:#fff;
  padding:10px 18px;
  font-size:14px;
  font-weight:600;
  border-radius:22px;
  box-shadow:0 6px 18px rgba(0,0,0,.25);
  cursor:pointer;
  z-index:99999;
  transition:.2s ease;
}
#floating-launcher:hover{
  transform:scale(1.05);
  opacity:.95;
}

/* Overlay */
#launcher-overlay{
  position:fixed;
  inset:0;
  background:#fff;
  display:none;
  flex-direction:column;
  z-index:100000;
}

/* Top bar */
#launcher-top{
  background:#0f172a;
  color:#fff;
  padding:12px;
  display:flex;
  justify-content:flex-end;
}
#launcher-close{
  cursor:pointer;
  font-size:16px;
  padding:4px 12px;
}

/* Iframe */
#launcher-frame{
  flex:1;
  width:100%;
  border:none;
}
</style>
<script>
(function(){

  var launcher = document.getElementById("floating-launcher");
  var overlay  = document.getElementById("launcher-overlay");
  var frame    = document.getElementById("launcher-frame");
  var closeBtn = document.getElementById("launcher-close");

  /* Portfolio / Homepage URL */
  var PORTFOLIO_URL = "https://www.socialcreator.com/techshop";

  launcher.onclick = function(){
    overlay.style.display = "flex";
    frame.src = PORTFOLIO_URL;
  };

  closeBtn.onclick = function(){
    overlay.style.display = "none";
    frame.src = "";
  };

})();
</script>
