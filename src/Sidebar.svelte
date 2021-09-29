<script>
  import SocialIcon from "./SocialIcon.svelte";

  export function closeNav() {
    document.getElementById("mySidebar").style.display = "none";
  }
</script>

<!-- Sidebar with image -->
<nav class="w3-sidebar w3-hide-medium w3-hide-small" style="width:40%">
  <div class="bgimg" />
</nav>

<!-- Hidden Sidebar (reveals when clicked on menu icon)-->
<nav
  class="w3-sidebar w3-black w3-animate-right w3-xxlarge"
  style="display:none;padding-top:150px;right:0;z-index:2"
  id="mySidebar"
>
  <button
    on:click={closeNav}
    class="w3-button w3-black w3-xxxlarge w3-display-topright"
    style="padding:0 12px;"
  >
    <i class="fa fa-remove" />
  </button>
  <div class="w3-bar-block w3-center">
    <a
      href="#home"
      class="w3-bar-item w3-button w3-text-grey w3-hover-black"
      on:click={closeNav}>Home</a
    >
    <!-- <a
      href="#portfolio"
      class="w3-bar-item w3-button w3-text-grey w3-hover-black"
      on:click={closeNav}>Portfolio</a
    > -->
    <a
      href="#about"
      class="w3-bar-item w3-button w3-text-grey w3-hover-black"
      on:click={closeNav}>About</a
    >
    <a
      href="#contact"
      class="w3-bar-item w3-button w3-text-grey w3-hover-black"
      on:click={closeNav}>Contact</a
    >
  </div>
  <div class="w3-bar-block w3-center">
    <SocialIcon />
  </div>
</nav>
