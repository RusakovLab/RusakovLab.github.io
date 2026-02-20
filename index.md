---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h3> Computational portal for modelling brain cells with stochastic nano-properties and interactive 3D environment.</h3>

<!-- Container for all three tools with videos -->
<div class="tools-container">

  <!-- ASTRO -->
  <div class="video-container astro" onclick="location.href='{% link astro.md %}'">
    <div class="video-text">
      <p><strong><h3>ASTRO</h3></strong> simulates complex realistic astrocytes incorporating their stochastic nanoscopic 
      morphology</p>
    </div>
    <br>
    <div class="media-wrapper">
      <img class="video-fallback" src="assets/Astro.png" alt="ASTRO simulation preview">
      <video id="myVideo1" loop muted playsinline>
        <source src="assets/Astro.mp4" type="video/mp4">
      </video>
    </div>
  </div>

  <!-- BRAINCELL -->
  <div class="video-container braincell" onclick="location.href='{% link braincell.md %}'">
    <div class="video-text">
      <p><strong><h3>BRAINCELL</h3></strong> simulates brain cell morphology and physiology
      with their stochastic nano-features, dynamic extracellular environment and inter-cellular </p>
      <p> signalling, on the scale from nanometers to hundreds of microns </p>
    </div>
    <br>
    <div class="braincell-videos">
      <div class="video-subcontainer">
        <div class="media-wrapper">
          <img class="video-fallback" src="assets/BrainCellSpine.png" alt="BRAINCELL simulation preview">
          <video id="myVideo2" loop muted playsinline>
            <source src="assets/BrainCellSpine.mp4" type="video/mp4">
          </video>
        </div>
      </div>
      <div class="separator"></div>
      <div class="video-subcontainer">
        <div class="media-wrapper">
          <img class="video-fallback" src="assets/BrainCellGaba.png" alt="BRAINCELL simulation preview">
          <video id="myVideo3" loop muted playsinline>
            <source src="assets/BrainCellGaba.mp4" type="video/mp4">
          </video>
        </div>
      </div>
    </div>
  </div>

  <!-- ARACHNE -->
  <div class="video-container arachne" onclick="location.href='{% link arachne.md %}'">
    <div class="video-text">
      <p><strong><h3>ARACHNE</h3></strong> simulates multi-cell spiking neuronal networks with astrocytes, excitation-inhibition, volume transmission, and flexible memory rules </p><br>
    </div>
    <div class="media-wrapper">
      <img class="video-fallback" src="assets/Arachne.png" alt="ARACHNE simulation preview">
      <video id="myVideo4" loop muted playsinline>
        <source src="assets/Arachne.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</div>

<style>
  .media-wrapper {
    position: relative;
    width: 100%;
    display: block;
  }

  .media-wrapper .video-fallback {
    display: block;
    width: 100%;
    height: auto;
  }

  .media-wrapper video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    transition: opacity 0.6s ease-in-out;
    object-fit: cover;
  }

  .media-wrapper video.ready {
    opacity: 1;
  }
</style>

<script>
  function loadVideo(videoEl, mp4Name) {
    const nav = navigator.connection;
    const navApiAvailable = (nav !== undefined);
    const isWifiOrEthernet = navApiAvailable && (nav.type === "wifi" || nav.type === "ethernet");
    const downlinkSufficient = navApiAvailable && nav.downlink > 5;
    const grabMP4 = (!navApiAvailable || isWifiOrEthernet || downlinkSufficient);

    if (!grabMP4) return;

    fetch(`${mp4Name}?cache=${Date.now()}`)
      .then(response => {
        if (response.status === 304) return null;
        if (!response.ok) throw new Error(`Error: ${response.status} - ${response.statusText}`);
        return response.blob();
      })
      .then(blob => {
        if (!blob) return;
        videoEl.src = URL.createObjectURL(blob);
        videoEl.addEventListener('canplay', () => {
          videoEl.play();
          // Fade in the video — fallback image stays underneath, no layout jump
          requestAnimationFrame(() => {
            videoEl.classList.add('ready');
          });
        }, { once: true });
      })
      .catch(err => console.warn(`Video load failed for ${mp4Name}:`, err));
  }

  document.addEventListener("DOMContentLoaded", function() {
    loadVideo(document.getElementById("myVideo1"), "assets/Astro.mp4");
    loadVideo(document.getElementById("myVideo2"), "assets/BrainCellSpine.mp4");
    loadVideo(document.getElementById("myVideo3"), "assets/BrainCellGaba.mp4");
    loadVideo(document.getElementById("myVideo4"), "assets/Arachne.mp4");
  });
</script>
