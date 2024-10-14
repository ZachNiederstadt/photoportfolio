<script>
  import { onMount } from "svelte";
  import "$lib/global.css";
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

<main
  class="bg-cover bg-center"
  style="background-image: url('/images/portfoliobg.avif');"
>
  <nav
    class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center"
  >
    <a class="nav-link mr-5" href="/about" style="color: white;">About</a>
    <a
      class="navbar-brand text-2xl font-semibold"
      href="/photography"
      style="color: white;">Zach Niederstadt</a
    >
    <a class="nav-link ml-5" href="/portfolio" style="color: white;"
      >Portfolio</a
    >
  </nav>

  <div
    class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 bg-cover bg-center min-h-screen"
  >
    <div class="col-md-4" style="margin-top: 100px;">
      <div class="bg-white rounded-lg overflow-hidden shadow-md">
        <img
          src="/images/gtchallenge/image-16.avif"
          alt="gtchallenge"
          class="w-full h-64 object-cover"
        />
        <div class="p-4">
          <a
            href="/portfolio/gtchallenge"
            class="block bg-gray-900 text-white text-center py-2 rounded mt-2 hover:bg-gray-700 transition duration-300 ease-in-out"
            >GT Challenge</a
          >
        </div>
      </div>
    </div>
    <div class="col-md-4" style="margin-top: 100px;">
      <div class="bg-white rounded-lg overflow-hidden shadow-md">
        <img
          src="/images/gtchallenge/image-16.avif"
          alt="gtchallenge"
          class="w-full h-64 object-cover"
        />
        <div class="p-4">
          <a
            href="/portfolio/gtchallenge"
            class="block bg-gray-900 text-white text-center py-2 rounded mt-2 hover:bg-gray-700 transition duration-300 ease-in-out"
            >GT Challenge</a
          >
        </div>
      </div>
    </div>
    <div class="col-md-4" style="margin-top: 100px;">
      <div class="bg-white rounded-lg overflow-hidden shadow-md">
        <img
          src="/images/gtchallenge/image-16.avif"
          alt="gtchallenge"
          class="w-full h-64 object-cover"
        />
        <div class="p-4">
          <a
            href="/portfolio/gtchallenge"
            class="block bg-gray-900 text-white text-center py-2 rounded mt-2 hover:bg-gray-700 transition duration-300 ease-in-out"
            >GT Challenge</a
          >
        </div>
      </div>
    </div>
  </div>

  <p class="text-white text-center py-3" style="margin-top:-3rem">
    &copy; {year} Zach Niederstadt. All rights reserved.
  </p>
</main>
