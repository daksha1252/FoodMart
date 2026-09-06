<script setup>
import { ref } from 'vue'

const isPagesOpen = ref(false)
const isNavOpen = ref(false)

const togglePages = () => {
  isPagesOpen.value = !isPagesOpen.value
}

const closePages = () => {
  isPagesOpen.value = false
}

const openNav = () => {
  isNavOpen.value = true
}

const closeNav = () => {
  isNavOpen.value = false
  isPagesOpen.value = false
}
</script>

<template>
  <div class="header__nav-container">
    <div class="header__nav-row">
      <div class="header__nav-wrapper">

        <!-- Hamburger — hidden on desktop, shown on tablet/mobile -->
        <button
          type="button"
          class="header__nav-toggle"
          aria-label="Open menu"
          @click="openNav"
        >
          <svg width="20" height="20" viewBox="0 0 24 24" aria-hidden="true">
            <path fill="currentColor" d="M3 6h18v2H3zm0 5h18v2H3zm0 5h18v2H3z" />
          </svg>
        </button>

        <!-- Backdrop — only present while the offcanvas nav is open -->
        <div
          v-if="isNavOpen"
          class="header__nav-backdrop"
          @click="closeNav"
        ></div>

        <nav
          class="header__main-menu"
          :class="{ 'header__main-menu--open': isNavOpen }"
        >

          <!-- Close button — hidden on desktop, shown on tablet/mobile -->
          <button
            type="button"
            class="header__nav-close"
            aria-label="Close menu"
            @click="closeNav"
          >
            <svg width="16" height="16" viewBox="0 0 24 24" aria-hidden="true">
              <path
                fill="currentColor"
                d="M18.3 5.71L12 12l6.29 6.29-1.41 1.41L10.59 13.41 4.29 19.71 2.88 18.29 9.17 12 2.88 5.71 4.29 4.29l6.3 6.3 6.29-6.3z"
              />
            </svg>
          </button>

          <select class="header__departments">
            <option>Shop by Departments</option>
            <option>Groceries</option>
            <option>Drinks</option>
            <option>Chocolates</option>
          </select>


          <ul class="header__menu-list">

            <li class="header__nav-item">
              <a href="#women" class="header__nav-link">
                Women
              </a>
            </li>

            <li class="header__nav-item">
              <a href="#men" class="header__nav-link">
                Men
              </a>
            </li>

            <li class="header__nav-item">
              <a href="#kids" class="header__nav-link">
                Kids
              </a>
            </li>

            <li class="header__nav-item">
              <a href="#accessories" class="header__nav-link">
                Accessories
              </a>
            </li>

            <!-- Pages -->
            <li class="header__nav-item header__nav-item--dropdown">

              <button
                type="button"
                class="header__nav-link header__pages-toggle"
                @click="togglePages"
              >
                Pages

                <svg
                  width="12"
                  height="12"
                  viewBox="0 0 24 24"
                  aria-hidden="true"
                >
                  <path
                    d="M6 9l6 6 6-6"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
              </button>

              <ul
                v-if="isPagesOpen"
                class="header__dropdown-menu"
              >
                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    About Us
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Shop
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Single Product
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Cart
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    CheckOut
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Blog
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Single Post
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Styles
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Contact
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    Thank You
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    My Account
                  </a>
                </li>

                <li>
                  <a href="#" class="header__dropdown-item" @click="closePages">
                    404 Error
                  </a>
                </li>
              </ul>

            </li>

            <li class="header__nav-item">
              <a href="#brand" class="header__nav-link" @click="closeNav">
                Brand
              </a>
            </li>

            <li class="header__nav-item">
              <a href="#sale" class="header__nav-link" @click="closeNav">
                Sale
              </a>
            </li>

            <li class="header__nav-item">
              <a href="#blog" class="header__nav-link" @click="closeNav">
                Blog
              </a>
            </li>

          </ul>

        </nav>

      </div>
    </div>
  </div>
</template>