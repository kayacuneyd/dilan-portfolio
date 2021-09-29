<script>
  import { onMount } from "svelte";
  const dataPath = "./assets/js/data.json";
  let data = [];

  onMount(async function () {
    const response = await fetch(dataPath);
    data = await response.json();
  });

  /*   let iconName;
  let iconSize;
  let iconLink = `https://icongr.am/entypo/${iconName}.svg?size=${iconSize}`; */
</script>

<!-- About Section -->
<div class="w3-content w3-justify w3-text-grey w3-padding-32" id="about">
  <h2>About Me</h2>
  <hr class="w3-opacity" />
  <p>
    Some text about me. Some text about me. I am lorem ipsum consectetur
    adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
    aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
    nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
    reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
    pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
    officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed
    do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
    minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex
    ea commodo consequat.
  </p>

  <br />

  <!-- Testimonials -->
  <h2 class="w3-padding-24">My Articles & Projects</h2>

  {#each data as item}
    <img
      alt="icon of {item.iconName}-{item.id}"
      src="https://icongr.am/entypo/{item.iconName}.svg?size={item.iconSize}"
      class="w3-left w3-margin-right"
    />
    <p>
      {item.pubName}
    </p>
    <br />
  {/each}

  <!-- End About Section -->
</div>
