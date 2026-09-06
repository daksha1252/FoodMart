<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },

  image: {
    type: String,
    required: true,
  },

  discount: {
    type: String,
    default: "",
  },

  unit: {
    type: String,
    required: true,
  },

  rating: {
    type: String,
    required: true,
  },

  price: {
    type: String,
    required: true,
  },
});

const quantity = ref(1);

const increaseQuantity = () => {
  quantity.value++;
};

const decreaseQuantity = () => {
  if (quantity.value > 1) {
    quantity.value--;
  }
};

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};
</script>

<template>
  <article class="product-card">
    <!-- Image section -->
    <div class="product-card__image">
      <span v-if="discount" class="product-card__discount">
        {{ discount }}
      </span>

      <button
        type="button"
        class="product-card__wishlist"
        aria-label="Add to wishlist"
        @click="scrollToTop"
      >
        ♡
      </button>

      <img :src="image" :alt="name" />
    </div>

    <!-- Product details -->
    <div class="product-card__content">
      <h3 class="product-card__name">
        {{ name }}
      </h3>

      <div class="product-card__rating">
        <span class="product-card__unit">
          {{ unit }}
        </span>

        <span class="product-card__star"> ★ </span>

        <span class="product-card__rating-value">
          {{ rating }}
        </span>
      </div>

      <p class="product-card__price">
        {{ price }}
      </p>

      <div class="product-card__bottom">
        <div class="product-card__quantity">
          <button
            type="button"
            class="product-card__quantity-minus"
            @click="decreaseQuantity"
          >
            −
          </button>
          <span>{{ quantity }}</span>
          <button
            type="button"
            class="product-card__quantity-plus"
            @click="increaseQuantity"
          >
            +
          </button>
        </div>

        <button type="button" class="product-card__cart">Add to Cart</button>
      </div>
    </div>
  </article>
</template>
