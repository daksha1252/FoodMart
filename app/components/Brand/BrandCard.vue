<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },

  title: {
    type: String,
    required: true,
  },

  image: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <article class="brand-card">
    <div class="brand-card__image">
      <img :src="image" :alt="name" />
    </div>

    <div class="brand-card__content">
      <p class="brand-card__name">
        {{ name }}
      </p>

      <h3 class="brand-card__title">
        {{ title }}
      </h3>
    </div>
  </article>
</template>
