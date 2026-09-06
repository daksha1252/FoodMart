<template>
  <section
    class="hero"
    style="background-image: url(&quot;/images/background-pattern.jpg&quot;)"
  >
    <div class="hero__container">
      <div class="hero__grid">
        <!-- Large left banner -->
        <div class="hero__banner hero__banner--large">
          <div class="hero__banner-content">
            <div class="hero__content">
              <div class="hero__category">100% Natural</div>

              <h2>
                Fresh Smoothie<br />
                & Summer Juice
              </h2>

              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing<br />
                elit. Dignissim massa diam elementum.
              </p>

              <NuxtLink to="/shop" class="hero__button"> Shop Now </NuxtLink>
            </div>

            <div class="hero__image">
              <img
                src="/images/product-thumb-1.png"
                alt="Fresh Smoothie and Summer Juice"
              />
            </div>
          </div>

          <!-- Slider dots -->
          <div class="hero__pagination">
            <span
              class="hero__pagination-dot hero__pagination-dot--active"
            ></span>
            <span class="hero__pagination-dot"></span>
            <span class="hero__pagination-dot"></span>
          </div>
        </div>

        <!-- Right side -->
        <div class="hero__side">
          <!-- Top right banner -->
          <div class="hero__banner hero__banner--top">
            <div class="hero__banner-content">
              <div class="hero__content">
                <div class="hero__category hero__category--sale">20% Off</div>

                <div class="hero__sale">
                  <span class="hero__sale-line"></span>
                  <span class="hero__sale-text">SALE</span>
                </div>

                <h3>
                  Fruits &<br />
                  Vegetables
                </h3>

                <NuxtLink to="/shop" class="hero__link">
                  Shop Collection

                  <svg
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    aria-hidden="true"
                  >
                    <path
                      fill="currentColor"
                      d="M17.92 11.62a1 1 0 0 0-.21-.33l-5-5a1 1 0 0 0-1.42 1.42l3.3 3.29H7a1 1 0 0 0 0 2h7.59l-3.3 3.29a1 1 0 0 0 0 1.42a1 1 0 0 0 1.42 0l5-5a1 1 0 0 0 .21-.33a1 1 0 0 0 0-.76Z"
                    />
                  </svg>
                </NuxtLink>
              </div>

              <!-- <div class="hero__image">
                <img src="/images/ad-image-1.png" alt="Fruits and vegetables" />
              </div> -->
            </div>
          </div>

          <!-- Bottom right banner -->
          <div class="hero__banner hero__banner--bottom">
            <div class="hero__banner-content">
              <div class="hero__content">
                <div class="hero__category hero__category--sale">15% Off</div>

                <div class="hero__sale">
                  <span class="hero__sale-line"></span>
                  <span class="hero__sale-text">SALE</span>
                </div>

                <h3>Baked Products</h3>

                <NuxtLink to="/shop" class="hero__link">
                  Shop Collection

                  <svg
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    aria-hidden="true"
                  >
                    <path
                      fill="currentColor"
                      d="M17.92 11.62a1 1 0 0 0-.21-.33l-5-5a1 1 0 0 0-1.42 1.42l3.3 3.29H7a1 1 0 0 0 0 2h7.59l-3.3 3.29a1 1 0 0 0 0 1.42l5-5a1 1 0 0 0 .21-.33a1 1 0 0 0-.76Z"
                    />
                  </svg>
                </NuxtLink>
              </div>

              <!-- <div class="hero__image">
                <img src="/images/ad-image-2.png" alt="Baked products" />
              </div> -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
