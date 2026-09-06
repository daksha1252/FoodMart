<template>
  <div class="header__search-wrapper">
    <div class="header__searchbar">

      <div class="header__category">
        <select>
          <option>All Categories</option>
          <option>Groceries</option>
          <option>Drinks</option>
          <option>Chocolates</option>
        </select>
      </div>

      <input
        type="text"
        placeholder="Search for more than 20,000 products"
      />

      <button
        class="header__search-button"
        type="button"
        aria-label="Search"
      >
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