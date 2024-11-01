<script>
    import "$lib/global.css";
    import { onMount } from "svelte";
    import { fade, slide, fly } from "svelte/transition";
    //import { Fullscreen } from "$lib/cmp/fullscreen";
    let collections = [
        {
            name: "F1 2023",
            images: [
                "/images/F1/image-1.avif",
                "/images/F1/image-4.avif",
                "/images/F1/image-2.avif",
                "/images/F1/image-3.avif",
                "/images/F1/image-6.avif",
                "/images/F1/image-9.avif",
                "/images/F1/image-8.avif",
                "/images/F1/image-5.avif",
                "/images/F1/image-7.avif",
                "/images/F1/image-10.avif",
                "/images/F1/image-15.avif",
                "/images/F1/image-11.avif",
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
    <title>F1 COTA 2023 - Zach Niederstadt</title>
    <meta
        property="og:title"
        content="Twilight Toboganning - Zach Niederstadt"
    />
    <meta
        property="og:description"
        content="Shoot for Mendip Activity Centers Twilight Toboganning"
    />
    <meta property="og:image" content="/images/_DSC2618.avif" />
</svelte:head>

<div out:fade>
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

    <section id="portfolio" class="py-5">
        <div class="container mx-auto mt-20 text-center">
            <h1
                class="text-5xl font-bold text-white mb-4 font-orbitron tracking-wider"
                transition:fly={{ x: -50, duration: 700 }}
            >
                F1 COTA 2023
            </h1>
            <p class="text-md font-semibold text-white mb-8 pl-2 pr-2">
                My view from the Legendary Cota S section
            </p>
            <div
                class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-2"
            >
                {#each collections[0].images as image, index}
                    <div class="content-center">
                        <img
                            src={image}
                            alt={`Image ${index + 1}`}
                            class="w-full h-auto cursor-pointer shadow-sm"
                            on:click={() => toggleFullScreen(image)}
                        />
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <footer class="text-white text-center py-3">
        &copy; {year} Zach Niederstadt. All rights reserved.
    </footer>
</div>

<style>
</style>
