<script>
  //Make background fade in
  import { onMount } from "svelte";
  import "$lib/global.css";
  import { fade, slide } from "svelte/transition";
  const collections = [
    {
      name: "GT Challenge COTA 2023",
      link: "/portfolio/gtchallenge",
    },
    {
      name: "Formula 1 COTA 2023",
      link: "/portfolio/F123",
    },
    {
      name: "KBD Event",
      link: "/portfolio/kbd",
    },
  ];

  function getLastPartOfUrl(url) {
    const parts = url.split("/");
    return parts[parts.length - 1];
  }

  async function fetchFirstImage(link) {
    return null;
    // const portfolioName = getLastPartOfUrl(link);
    // const response = await fetch(
    //   `https://leohanney.com/images/${portfolioName}/image1.avif`,
    // );
    // return response.ok
    //   ? `https://leohanney.com/images/${portfolioName}/image1.avif`
    //   : null;
  }

  let collectionItems = [];

  onMount(async () => {
    collectionItems = await Promise.all(
      collections.map(async (collection) => {
        const thumbnailUrl = await fetchFirstImage(collection.link);
        return { ...collection, thumbnailUrl };
      }),
    );
  });
  const year = new Date().getFullYear();
</script>

<svelte:head>
  <title>Zach Niederstadt - Photographer</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<div class="main">
  <main
    class="bg-cover bg-center content-center h-lvh"
    style="background-image: url('/images/portfoliobg.avif'); "
    transition:fade={{ duration: 300 }}
  >
    <div class="body">
      <nav
        class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center content-center"
      >
        <a class="nav-link mr-5 other" href="/about" style="color: white;"
          >About</a
        >
        <a
          class="navbar-brand text-4xl font-semibold font-orbitron text tracking-wider"
          href="/photography">ZN</a
        >
        <a class="nav-link ml-5 other" href="/portfolio" style="color: white;"
          >Portfolio</a
        >
      </nav>

      <div class="pt-10 pr-5 pl-5 f" transition:fade={{ duration: 300 }}>
        <div class="container mx-auto grid lg:grid-cols-3 gap-4">
          <div class="col-md-4" style="margin-top: 30px;">
            <div
              class="bg-black rounded-lg overflow-hidden shadow-md"
              style="border: 5px solid"
            >
              <img
                src="/images/F1/image-1.avif"
                alt="gtchallenge"
                class="w-full h-64 object-cover"
              />
              <div class="p-4">
                <a
                  href="/portfolio/F123"
                  class="block bg-stone-800 text-white text-center py-2 rounded mt-2 hover:bg-stone-500 transition duration-300 ease-in-out font-orbitron"
                  >F1 Cota 2023</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-4" style="margin-top: 30px;">
            <div
              class="bg-black rounded-lg overflow-hidden shadow-md"
              style="border: 5px solid"
            >
              <img
                src="/images/gtchallenge/image-16.avif"
                alt="gtchallenge"
                class="w-full h-64 object-cover"
              />
              <div class="p-4">
                <a
                  href="/portfolio/gtchallenge"
                  class="block bg-stone-800 text-white text-center py-2 rounded mt-2 hover:bg-stone-500 transition duration-300 ease-in-out font-orbitron"
                  >GT Challenge</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-4 pb-5" style="margin-top: 30px;">
            <div
              class="bg-black rounded-lg overflow-hidden shadow-md"
              style="border: 5px solid"
            >
              <img
                src="/images/kbd/image8.avif"
                alt="gtchallenge"
                class="w-full h-64 object-cover"
              />
              <div class="p-4">
                <a
                  href="/portfolio/kbd"
                  class="block bg-stone-800 text-white text-center py-2 rounded mt-2 hover:bg-stone-500 transition duration-300 ease-in-out font-orbitron"
                  >KBD Drift Event</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="pb-5 pr-5 pl-5" transition:fade={{ duration: 300 }}>
        <div class="container mx-auto gap-4">
          <div class="col-md-4 pb-10" style="margin-top: 30px;">
            <div
              class="bg-black rounded-lg overflow-hidden shadow-md"
              style="border: 5px solid"
            >
              <img
                src="/images/baa.avif"
                alt="gtchallenge"
                class="w-full h-64 object-cover"
              />
              <div class="p-4">
                <a
                  href="/portfolio/baa"
                  class="block bg-stone-800 text-white text-center py-2 rounded mt-2 hover:bg-stone-500 transition duration-300 ease-in-out font-orbitron"
                  >Before and Afters</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>

      <div out:slide>
        <p class="text-white text-center py-3 pt-2" out:fade in:fade>
          &copy; {year} Zach Niederstadt. All rights reserved.
        </p>
      </div>
    </div>
  </main>
</div>

<style>
  .main {
    height: 100vh;
  }
  .body {
    height: 100vh;
    overflow: hidden;
    overflow-y: scroll;
  }
  .background,
  .body {
  }
</style>
