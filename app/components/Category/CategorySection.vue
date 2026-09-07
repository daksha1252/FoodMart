<script setup>
import { ref, computed } from "vue";
import { categories } from "~/data/data.js";

const categoryViewport = ref(null);
const currentIndex = ref(0);

const visibleCards = ref(6);

const maxIndex = computed(() => {
  return Math.max(0, categories.length - visibleCards.value);
});

const next = () => {
  if (currentIndex.value < maxIndex.value) {
    currentIndex.value++;

    categoryViewport.value.scrollBy({
      left: 365,
      behavior: "smooth"
    });
  }
};

const previous = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--;

    categoryViewport.value.scrollBy({
      left: -365,
      behavior: "smooth"
    });
  }
};
</script>

<template>
  <section class="category">

    <CommonSectionHeader
      title="Category"
      :previous-disabled="currentIndex === 0"
      :next-disabled="currentIndex === maxIndex"
      @previous="previous"
      @next="next"
    />

    <div
      ref="categoryViewport"
      class="category__viewport"
    >
      <div class="category__track">
        <CategoryCard
          v-for="category in categories"
          :key="category.id"
          :name="category.name"
          :image="category.image"
        />
      </div>
    </div>

  </section>
</template>