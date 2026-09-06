<script setup>
defineProps({
  date: {
    type: String,
    required: true,
  },

  category: {
    type: String,
    required: true,
  },

  image: {
    type: String,
    required: true,
  },

  title: {
    type: String,
    required: true,
  },

  description: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <article class="blog-card">
    <div class="blog-card__image">
      <img :src="image" :alt="title" />
    </div>

    <div class="blog-card__content">
      <div class="blog-card__meta">
        <span class="blog-card__date">
          <span class="blog-card__icon">▣</span>
          {{ date }}
        </span>

        <span class="blog-card__category">
          <span class="blog-card__icon">□</span>
          {{ category }}
        </span>
      </div>

      <h3 class="blog-card__title">
        {{ title }}
      </h3>

      <p class="blog-card__description">
        {{ description }}
      </p>
    </div>
  </article>
</template>
