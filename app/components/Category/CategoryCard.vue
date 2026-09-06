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
});
</script>

<template>
  <article class="category-card">
    <div class="category-card__image">
      <img :src="image" :alt="name" />
    </div>
    <h3 class="category-card-title">{{ name }}</h3>
  </article>
</template>
