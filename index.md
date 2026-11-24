---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h3> Computational portal for modelling brain cells with stochastic nano-properties and interactive 3D environment.</h3>

<!-- Container for all four tools with videos -->
<div class="tools-container">

  <!-- ASTRO -->
  <div class="video-container astro" onclick="location.href='{% link astro.md %}'">
    <div class="video-text">
      <p><strong><h3>ASTRO</h3></strong> simulates complex realistic astrocytes incorporating their stochastic nanoscopic 
      morphology</p>
    </div>
    <br>
    <img class="video-fallback-astro" src="assets/Astro.png" alt="ASTRO simulation preview">
    <video id="vidAstro" loop autoplay muted playsinline>
      <source src="assets/Astro.mp4" type="video/mp4">
    </video>
  </div>

  <!-- BRAINCELL -->
  <div class="video-container braincell" onclick="location.href='{% link braincell.md %}'">
    <div class="video-text">
      <p><strong><h3>BRAINCELL</h3></strong> simulates brain cell morphology and physiology
      with their stochastic nano-features, dynamic extracellular environment and inter-cellular </p>
      <p> signalling, on the scale from nanometers to hundreds of microns </p>
    </div>
    <br>
    <img class="video-fallback-braincell" src="assets/BrainCellGaba.png" alt="BRAINCELL simulation preview">
    <video id="vidBraincell" loop autoplay muted playsinline>
      <source src="assets/BrainCellGaba.mp4" type="video/mp4">
    </video>
  </div>

  <!-- STOCHASTIC SYNAPSE -->
  <div class="video-container stochastic" onclick="location.href='{% link stochsyn.md %}'">
    <div class="video-text">
      <p><strong><h3>STOCHASTIC SYNAPSE</h3></strong> simulates release, Brownian diffusion and uptake of neurotransmitter among nanoscopic obstacles, and computes activation of synaptic and extrasynaptic receptors</p>
    </div>
    <br>
    <img class="video-fallback-stochastic" src="assets/StochasticSynapse.png" alt="STOCHASTIC SYNAPSE simulation preview">
    <video id="vidStochastic" loop autoplay muted playsinline>
      <source src="assets/stochasticSynapse.mp4" type="video/mp4">
    </video>
  </div>

  <!-- ARACHNE -->
  <div class="video-container arachne" onclick="location.href='{% link arachne.md %}'">
    <div class="video-text">
      <p><strong><h3>ARACHNE</h3></strong> simulates multi-cell spiking neuronal networks with astrocytes, excitation-inhibition, volume transmission, and flexible memory rules </p><br>
    </div>
    <img class="video-fallback-arachne" src="assets/Arachne.png" alt="ARACHNE simulation preview">
    <video id="vidArachne" loop autoplay muted playsinline>
      <source src="assets/Arachne.mp4" type="video/mp4">
    </video>
  </div>
</div>

<script>
  function loadVideo(videoID, fallbackID, mp4Name) {
    const video = document.getElementById(videoID);
    video.style.display = "none";

    const nav = navigator.connection;
    const navApiAvailable = (nav !== undefined);
    const isWifiOrEthernet = navApiAvailable && (nav.type === "wifi" || nav.type === "ethernet" );
    const downlinkSufficient = navApiAvailable && nav.downlink > 5;
    const grabMP4 = (!navApiAvailable || isWifiOrEthernet || downlinkSufficient);

    if (grabMP4) {
      fetch(mp4Name)   // let the browser/CDN cache the video across visits
        .then(response => {
            if (response.status === 304) { // Resource not modified, use the cached version
                return null;
            } else if (!response.ok) {
                throw new Error(`Error: ${response.status} - ${response.statusText}`);
            }
            return response.blob();
        })
        .then(blob => {
           if (blob !== null) {
             video.src = URL.createObjectURL(blob);
             video.addEventListener('loadeddata', () => {
               // Video has loaded successfully, remove fallback PNG
               const fallbackElement = document.querySelector(`.${fallbackID}`);
               if (fallbackElement) { fallbackElement.remove(); }  //to avoid removing twice
               video.style.display = "block";
               video.play();
             });
           }
        })
    }
  }

  document.addEventListener("DOMContentLoaded", function() {
    // Call the function for each video
    loadVideo("vidAstro",      "video-fallback-astro",      "assets/Astro.mp4");
    loadVideo("vidBraincell",  "video-fallback-braincell",  "assets/BrainCellGaba.mp4");
    loadVideo("vidStochastic", "video-fallback-stochastic", "assets/stochasticSynapse.mp4");
    loadVideo("vidArachne",    "video-fallback-arachne",    "assets/Arachne.mp4");

    // Keyboard / screen-reader accessibility for the clickable tiles
    // (behaves like a link; no visual change).
    document.querySelectorAll(".video-container").forEach(function(tile) {
      tile.setAttribute("role", "link");
      tile.setAttribute("tabindex", "0");
      var h = tile.querySelector("h3");
      if (h) { tile.setAttribute("aria-label", "Open the " + h.textContent.trim() + " page"); }
      tile.addEventListener("keydown", function(e) {
        if (e.key === "Enter" || e.key === " ") { e.preventDefault(); tile.click(); }
      });
    });

  });

</script>
