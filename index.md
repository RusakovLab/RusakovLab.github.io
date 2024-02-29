---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h3>Neuroalgebra is a portal for brain cell computations with stochastic nano-properties and interactive control of 3D environment.</h3>

<!-- Container for all three tools with videos -->
<div class="tools-container">

  <!-- ASTRO -->
  <div class="video-container" onclick="location.href='{% link astro.md %}'">
    <div class="video-text">
      <p><strong><h3>ASTRO</h3></strong> simulates complex realistic astrocytes based on 3D two-photon and EM data</p>
    </div>
    <img class="video-fallback1" src="assets/Astro.png" alt="ASTRO simulation preview">
    <video id="myVideo1" loop autoplay muted playsinline>
      <source src="assets/Astro.mp4" type="video/mp4">
    </video>
  </div>

  <!-- BRAINCELL-1: SPINE -->
  <div class="video-container" onclick="location.href='{% link braincell.md %}'">
    <div class="video-text">
      <p><strong><h3>BRAINCELL</h3></strong> visualizing synaptic activation and 
      electrical dynamics in a CA1 neuron</p>
    </div><br>
    <img class="video-fallback2" src="assets/BrainCellSpine.png" alt="BRAINCELL simulation preview">
    <video id="myVideo2" loop autoplay muted playsinline>
      <source src="assets/BrainCellSpine.mp4" type="video/mp4">
    </video>
    <br>
  </div>

  <!-- BRAINCELL-2: GABA -->
  <div class="video-container" onclick="location.href='{% link braincell.md %}'">
    <div class="video-text">
      <p><strong><h3>BRAINCELL</h3></strong> simulates basket cell axonal release: modeling GABA</p> 
    </div><br>
    <img class="video-fallback3" src="assets/BrainCellGaba.png" alt="BRAINCELL simulation preview">
    <video id="myVideo3" loop autoplay muted playsinline>
      <source src="assets/BrainCellGaba.mp4" type="video/mp4">
    </video>
  </div>

  <!-- ARACHNE -->
  <div class="video-container" onclick="location.href='{% link arachne.md %}'">
    <div class="video-text">
      <p><strong><h3>ARACHNE</h3></strong> shows spiking neuronal networks with volume transmission</p><br>
    </div>
    <img class="video-fallback4" src="assets/Arachne.png" alt="ARACHNE simulation preview">
    <video id="myVideo4" loop autoplay muted playsinline>
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
      const cacheBuster = Date.now();
      fetch(`${mp4Name}?cache=${cacheBuster}`) //to debug without caching videos
//      fetch(`${mp4Name}`)
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
    loadVideo("myVideo1", "video-fallback1", "assets/Astro.mp4");
    loadVideo("myVideo2", "video-fallback2", "assets/BrainCellSpine.mp4");
    loadVideo("myVideo4", "video-fallback4", "assets/Arachne.mp4");
    loadVideo("myVideo3", "video-fallback3", "assets/BrainCellGaba.mp4");

  });

</script>