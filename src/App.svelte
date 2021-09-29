<script>
  import About from "./About.svelte";
  import Contact from "./Contact.svelte";
  import Footer from "./Footer.svelte";
  import Header from "./Header.svelte";
  import Sidebar from "./Sidebar.svelte";
  /*   import Portfolio from "./Portfolio.svelte"; */

  function openNav() {
    if (window.screen.width > 600) {
      // If screen width is 600 or above
      document.getElementById("mySidebar").style.width = "60%";
    } else {
      document.getElementById("mySidebar").style.width = "100%";
    }

    document.getElementById("mySidebar").style.display = "block";
  }
</script>

<Sidebar />

<!-- Page Content -->
<div class="w3-main w3-padding-large" style="margin-left:40%">
  <!-- Menu icon to open sidebar -->
  <span
    class="w3-button w3-top w3-white w3-xxlarge w3-text-grey w3-hover-text-black"
    style="width:auto; right:0;"
    on:click={openNav}><i class="fa fa-bars" /></span
  >

  <Header />

  <!--   <Portfolio /> -->

  <About />

  <Contact />

  <Footer />

  <!-- END PAGE CONTENT -->
</div>
