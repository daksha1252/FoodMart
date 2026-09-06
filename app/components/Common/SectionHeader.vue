<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },

  previousDisabled: {
    type: Boolean,
    default: false,
  },

  nextDisabled: {
    type: Boolean,
    default: false,
  },
});

const emit = defineEmits(["previous", "next"]);
</script>

<template>
  <div class="section-header">
    <h2 class="section-header__title">
      {{ title }}
    </h2>

    <div class="section-header__actions">
      <NuxtLink to="/categories" class="section-header__view-all">
        View All Categories →
      </NuxtLink>

      <button
        type="button"
        class="section-header__arrow"
        :disabled="previousDisabled"
        @click="emit('previous')"
      >
        ‹
      </button>

      <button
        type="button"
        class="section-header__arrow"
        :disabled="nextDisabled"
        @click="emit('next')"
      >
        ›
      </button>
    </div>
  </div>
</template>
