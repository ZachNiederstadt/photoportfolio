<head>
  <meta charset="utf-8" />
  <meta name="description" content="" />
  <link rel="icon" href="./favicon.png" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shopping Cart</title>
  <link
    rel="stylesheet"
    href="/_app/assets/pages/__layout.svelte-719c01e0.css"
  />
  <link
    rel="stylesheet"
    href="/_app/assets/pages/components/Cart.svelte-892715a1.css"
  />
  <link
    rel="stylesheet"
    href="/_app/assets/pages/components/CartNotification.svelte-d46cf0c7.css"
  />
  <link rel="stylesheet" href="/_app/assets/pages/index.svelte-3ecdf366.css" />
  <link
    rel="stylesheet"
    href="/_app/assets/pages/ProductImages.svelte-8c533a46.css"
  />
  <link
    rel="stylesheet"
    href="/_app/assets/pages/components/QuantityInput.svelte-ce9dd641.css"
  />
  <link rel="modulepreload" href="/_app/start-909050a4.js" />
  <link rel="modulepreload" href="/_app/chunks/index-36c70804.js" />
  <link rel="modulepreload" href="/_app/chunks/index-9126f338.js" />
  <link rel="modulepreload" href="/_app/pages/__layout.svelte-e79ece89.js" />
  <link
    rel="modulepreload"
    href="/_app/pages/components/Navbar.svelte-2632f3ba.js"
  />
  <link
    rel="modulepreload"
    href="/_app/pages/components/CloseButton.svelte-5d2ba839.js"
  />
  <link
    rel="modulepreload"
    href="/_app/pages/components/Cart.svelte-cbbc9396.js"
  />
  <link rel="modulepreload" href="/_app/chunks/cart.store-bfe5c33e.js" />
  <link
    rel="modulepreload"
    href="/_app/pages/components/CartNotification.svelte-1ddc6a97.js"
  />
  <link rel="modulepreload" href="/_app/pages/index.svelte-c6c9e94c.js" />
  <link
    rel="modulepreload"
    href="/_app/pages/ProductImages.svelte-6953f981.js"
  />
  <link
    rel="modulepreload"
    href="/_app/pages/components/QuantityInput.svelte-37e99f28.js"
  />
  <link
    rel="modulepreload"
    as="script"
    crossorigin=""
    href="/_app/error.svelte-89ffeb09.js"
  /></head
>
<body data-new-gr-c-s-check-loaded="8.912.0" data-gr-ext-installed="">
  <div>
    <header class="header" id="header">
      <nav class="nav">
        <button
          name="toggle-menu"
          type="button"
          class="icon-button nav__toggle"
          id="nav-toggle"><img src="images/icon-menu.svg" alt="" /></button
        > <img src="images/logo.svg" class="nav__logo" alt="logo" />
        <div class="nav__menu_container">
          <div class="nav__menu" id="nav-menu">
            <button class="icon-button nav__close"
              ><img src="images/icon-close.svg" alt="close" /></button
            >
            <ul class="nav__list">
              <li class="nav__item">
                <a class="nav__item-text" href="/">Collections</a>
              </li>
              <li class="nav__item">
                <a class="nav__item-text" href="/">Men</a>
              </li>
              <li class="nav__item">
                <a class="nav__item-text" href="/">Women</a>
              </li>
              <li class="nav__item">
                <a class="nav__item-text" href="/">About</a>
              </li>
              <li class="nav__item">
                <a class="nav__item-text" href="/">Contact</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="nav__user">
          <button class="cart__notification svelte-p570iy"
            ><img src="images/icon-cart.svg" alt="shopping cart" />
          </button>
          <img
            class="user-thumbnail"
            src="images/image-avatar.png"
            alt="user"
          />
        </div>
      </nav>
    </header>
    <main class="main">
      <section class="section product">
        <div class="product-images svelte-1yum1o3">
          <div class="slider-container svelte-1yum1o3">
            <div
              class="swiper swiper-initialized swiper-horizontal swiper-pointer-events item__swiper swiper-backface-hidden"
            >
              <div
                class="swiper-wrapper"
                style="transform: translate3d(-400px, 0px, 0px); transition-duration: 0ms;"
              >
                <div
                  class="swiper-slide swiper-slide-duplicate swiper-slide-prev"
                  data-swiper-slide-index="3"
                  style="width: 400px;"
                >
                  <img
                    src="images/image-product-4.jpg"
                    class="item__image svelte-1yum1o3"
                    alt="product"
                  />
                </div>
                <div
                  class="swiper-slide swiper-slide-active"
                  data-swiper-slide-index="0"
                  style="width: 400px;"
                >
                  <img
                    src="images/image-product-1.jpg"
                    class="item__image svelte-1yum1o3"
                    alt="product"
                  />
                </div>
                <div
                  class="swiper-slide swiper-slide-next"
                  data-swiper-slide-index="1"
                  style="width: 400px;"
                >
                  <img
                    src="images/image-product-2.jpg"
                    class="item__image svelte-1yum1o3"
                    alt="product"
                  />
                </div>
                <div
                  class="swiper-slide"
                  data-swiper-slide-index="2"
                  style="width: 400px;"
                >
                  <img
                    src="images/image-product-3.jpg"
                    class="item__image svelte-1yum1o3"
                    alt="product"
                  />
                </div>
                <div
                  class="swiper-slide swiper-slide-duplicate-prev"
                  data-swiper-slide-index="3"
                  style="width: 400px;"
                >
                  <img
                    src="images/image-product-4.jpg"
                    class="item__image svelte-1yum1o3"
                    alt="product"
                  />
                </div>
                <div
                  class="swiper-slide swiper-slide-duplicate swiper-slide-duplicate-active"
                  data-swiper-slide-index="0"
                  style="width: 400px;"
                >
                  <img
                    src="images/image-product-1.jpg"
                    class="item__image svelte-1yum1o3"
                    alt="product"
                  />
                </div>
              </div>
            </div>
            <div class="swiper__control svelte-1yum1o3 showControls">
              <button class="swiper__button swiper-button-prev svelte-1yum1o3"
                ><img
                  src="images/icon-previous.svg"
                  alt="arrow left"
                  class="svelte-1yum1o3"
                /></button
              >
              <button class="swiper__button swiper-button-next svelte-1yum1o3"
                ><img
                  src="images/icon-next.svg"
                  alt="arrow right"
                  class="svelte-1yum1o3"
                /></button
              >
            </div>
          </div>
          <div class="swiper__thumbnails svelte-1yum1o3">
            <div class="swiper__thumbnail svelte-1yum1o3 active">
              <img
                class="swiper__thumbnail-img svelte-1yum1o3"
                src="images/image-product-1-thumbnail.jpg"
                alt="product"
              />
            </div>
            <div class="swiper__thumbnail svelte-1yum1o3">
              <img
                class="swiper__thumbnail-img svelte-1yum1o3"
                src="images/image-product-2-thumbnail.jpg"
                alt="product"
              />
            </div>
            <div class="swiper__thumbnail svelte-1yum1o3">
              <img
                class="swiper__thumbnail-img svelte-1yum1o3"
                src="images/image-product-3-thumbnail.jpg"
                alt="product"
              />
            </div>
            <div class="swiper__thumbnail svelte-1yum1o3">
              <img
                class="swiper__thumbnail-img svelte-1yum1o3"
                src="images/image-product-4-thumbnail.jpg"
                alt="product"
              />
            </div>
          </div>
        </div>
        <div class="information svelte-1mso0bt">
          <h2 class="information__company-name svelte-1mso0bt">
            SNEAKER COMPANY
          </h2>
          <h1 class="information__product-name svelte-1mso0bt">
            Fall Limited Edition Sneakers
          </h1>
          <p class="information__product-description svelte-1mso0bt">
            These low-profile sneakers are your perfect casual wear companion.
            Featuring a durable rubber outer sole, they’ll withstand everything
            the weather can offer.
          </p>
          <div class="information__price-container svelte-1mso0bt">
            <span class="information__price-value svelte-1mso0bt">$125.00</span>
            <span class="information__price-discount svelte-1mso0bt">50%</span>
            <del class="information__price-old svelte-1mso0bt">$250.00</del>
          </div>
          <div class="purchase svelte-1mso0bt">
            <div class="quantity svelte-12h66vn">
              <button class="quantity__minus svelte-12h66vn"
                ><img src="images/icon-minus.svg" alt="decrese" /></button
              >
              <input
                type="number"
                class="quantity__input svelte-12h66vn"
                min="0"
                max="10"
              />
              <button class="quantity__plus svelte-12h66vn"
                ><img src="images/icon-plus.svg" alt="increment" /></button
              >
            </div>
            <button class="purchase__button svelte-1mso0bt"
              ><img
                src="images/icon-cart.svg"
                alt="cart"
                class="purchase__button-icon svelte-1mso0bt"
              />
              <span class="purchase__button-text svelte-1mso0bt"
                >Add to cart</span
              ></button
            >
          </div>
        </div>
      </section>
    </main>
    <div
      id="svelte-announcer"
      aria-live="assertive"
      aria-atomic="true"
      style="position: absolute; left: 0px; top: 0px; clip: rect(0px, 0px, 0px, 0px); clip-path: inset(50%); overflow: hidden; white-space: nowrap; width: 1px; height: 1px;"
    ></div>
  </div>
</body><grammarly-desktop-integration data-grammarly-shadow-root="true"
></grammarly-desktop-integration>
