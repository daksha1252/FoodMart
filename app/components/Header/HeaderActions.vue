<template>
  <div class="header__actions">

    <div class="header__support">
      <span>For Support?</span>
      <h5>+980-34984089</h5>
    </div>

    <!-- User + Wishlist -->
    <ul class="header__icons">
      <li>
        <a href="#">
          <svg width="20" height="20" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M15.71 12.71a6 6 0 1 0-7.42 0a10 10 0 0 0-6.22 8.18a1 1 0 0 0 2 .22a8 8 0 0 1 15.9 0a1 1 0 0 0 1 .89h.11a1 1 0 0 0 .88-1.1a10 10 0 0 0-6.25-8.19ZM12 12a4 4 0 1 1 4-4a4 4 0 0 1-4 4Z"
            />
          </svg>
        </a>
      </li>

      <li>
        <a href="#">
          <svg width="20" height="20" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M20.16 4.61A6.27 6.27 0 0 0 12 4a6.27 6.27 0 0 0-8.16 9.48l7.45 7.45a1 1 0 0 0 1.42 0l7.45-7.45a6.27 6.27 0 0 0 0-8.87Zm-1.41 7.46L12 18.81l-6.75-6.74a4.28 4.28 0 0 1 3-7.3a4.25 4.25 0 0 1 3 1.25a1 1 0 0 0 1.42 0a4.27 4.27 0 0 1 6 6.05Z"
            />
          </svg>
        </a>
      </li>
    </ul>

    <!-- Cart -->
    <div class="header__cart">
      <button type="button">
        <!-- Icon only shown on tablet/mobile, hidden on desktop via CSS -->
        <svg
          class="header__cart-icon"
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          viewBox="0 0 24 24"
        >
          <path
            fill="currentColor"
            d="M7 18a2 2 0 1 0 2 2a2 2 0 0 0-2-2ZM1 2v2h2l3.6 7.59l-1.35 2.45A2 2 0 0 0 7 17h12v-2H7l1.1-2h7.45a2 2 0 0 0 1.75-1.03l3.58-6.49A1 1 0 0 0 20 4H5.21l-.94-2Zm16 16a2 2 0 1 0 2 2a2 2 0 0 0-2-2Z"
          />
        </svg>
        <span>Your Cart &#9662;</span>
        <strong>$1290.00</strong>
      </button>
    </div>

    <!-- Search icon — only shown on tablet/mobile, replaces the search bar -->
    <div class="header__mobile-search">
      <button type="button" aria-label="Search">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          viewBox="0 0 24 24"
        >
          <path
            fill="currentColor"
            d="M21.71 20.29L18 16.61A9 9 0 1 0 16.61 18l3.68 3.68a1 1 0 0 0 1.42 0a1 1 0 0 0 0-1.39ZM11 18a7 7 0 1 1 7-7a7 7 0 0 1-7 7Z"
          />
        </svg>
      </button>
    </div>

  </div>
</template>