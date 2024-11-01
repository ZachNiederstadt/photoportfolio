<script>
  import "$lib/global.css";
  import { onMount } from "svelte";
  import { fade, slide, fly } from "svelte/transition";

  let collections = [
    {
      name: "STL Midnight Event",
      images: [
        "/images/stl/main.avif",
        "/images/stl/image-02.avif",
        "/images/stl/image-03.avif",
        "/images/stl/image-04.avif",
        "/images/stl/image-05.avif",
        "/images/stl/image-06.avif",
        "/images/stl/image-07.avif",
        "/images/stl/image-08.avif",
        "/images/stl/image-09.avif",
        "/images/stl/image-10.avif",
        "/images/stl/image-11.avif",
        "/images/stl/image-12.avif",
        "/images/stl/image-17.avif",
        "/images/stl/image-14.avif",
        "/images/stl/image-15.avif",
        "/images/stl/image-16.avif",
      ],
    },
  ];
  let backgroundImage = "";
  let fullscreen = false;
  let imgElement;
  let fullscreenContainer;

  onMount(() => {
    const randomIndex = Math.floor(
      Math.random() * collections[0].images.length,
    );
    backgroundImage = `url('${collections[0].images[randomIndex]}')`;

    document.body.style.backgroundImage = backgroundImage;
    document.body.style.backgroundSize = "cover";
    document.body.style.backgroundRepeat = "no-repeat";
  });

  const year = new Date().getFullYear();
  function toggleFullScreen(imageUrl) {
    if (!fullscreen) {
      // Create a container for the fullscreen image
      fullscreenContainer = document.createElement("div");
      fullscreenContainer.style.position = "fixed";
      fullscreenContainer.style.top = "0";
      fullscreenContainer.style.left = "0";
      fullscreenContainer.style.width = "100%";
      fullscreenContainer.style.height = "100%";
      fullscreenContainer.style.backgroundColor = "rgba(0,0,0,0.9)";
      fullscreenContainer.style.display = "flex";
      fullscreenContainer.style.justifyContent = "center";
      fullscreenContainer.style.alignItems = "center";
      fullscreenContainer.style.zIndex = "9999";

      // Create the image element
      imgElement = document.createElement("img");
      imgElement.src = imageUrl;
      imgElement.style.maxWidth = "100%";
      imgElement.style.maxHeight = "100%";
      imgElement.style.objectFit = "contain";
      imgElement.style.cursor = "zoom-out";

      // Add click event to exit fullscreen
      fullscreenContainer.addEventListener("click", exitFullScreen);

      // Append image to container and container to body
      fullscreenContainer.appendChild(imgElement);
      document.body.appendChild(fullscreenContainer);

      fullscreen = true;
    } else {
      exitFullScreen();
    }
  }

  function exitFullScreen() {
    if (fullscreenContainer && fullscreenContainer.parentNode) {
      fullscreenContainer.parentNode.removeChild(fullscreenContainer);
      fullscreen = false;
    }
  }
</script>

<svelte:head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>STL Midnight Drift Event 2024 - Zach Niederstadt</title>
  <meta property="og:title" content="KBD Drift Event 2024 - Zach Niederstadt" />
  <meta
    property="og:description"
    content="Photos from an amazing KBD Event at Cams Acres"
  />
  <meta property="og:image" content="" />
</svelte:head>

<div in:fade out:fade>
  <nav
    class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center content-center"
  >
    <a class="nav-link mr-5 other" href="/about" style="color: white;">About</a>
    <a
      class="navbar-brand text-4xl font-semibold font-orbitron text tracking-wider"
      href="/photography">ZN</a
    >
    <a class="nav-link ml-5 other" href="/portfolio" style="color: white;"
      >Portfolio</a
    >
  </nav>

  <section id="portfolio" class="py-5">
    <div class="container mx-auto mt-20 text-center">
      <h1
        class="text-5xl font-bold text-white mb-4 pl-2 pr-2 tracking-wider font-orbitron"
        transition:fly={{ x: -50, duration: 700 }}
      >
        STL Midnight Madness Drifting
      </h1>
      <p class="text-sm font-semibold text-white mb-8 pl-2 pr-2">
        Fun event I made it to where I got to practice low light action shots
      </p>
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-2"
      >
        {#each collections[0].images as image, index}
          <div class="content-center" in:slide out:fade>
            <img
              src={image}
              alt={`Image ${index + 1}`}
              class="w-full h-auto cursor-pointer shadow-lg"
              on:click={() => toggleFullScreen(image)}
            />
          </div>
        {/each}
      </div>
    </div>
  </section>

  <footer class="flex items-end text-white ml-10 mb-5">
    &copy; {year} Zach Niederstadt. All rights reserved.
  </footer>
</div>
