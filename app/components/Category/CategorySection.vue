<script setup>
import { ref, computed } from "vue";
import { categories } from "~/data/data.js";

const currentIndex = ref(0);

const visibleCards = 6;

const maxIndex = computed(() => {
  return categories.length - visibleCards;
});

const next = () => {
  if (currentIndex.value < maxIndex.value) {
    currentIndex.value++;
  }
};

const previous = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--;
  }
};
</script>

<template>
  <section class="category">
    <!-- Section header -->
    <CommonSectionHeader
      title="Category"
      :previous-disabled="currentIndex === 0"
      :next-disabled="currentIndex === maxIndex"
      @previous="previous"
      @next="next"
    />

    <!-- Cards viewport -->
    <div class="category__viewport">
      <div
        class="category__track"
        :style="{
          transform: `translateX(-${currentIndex * 252}px)`,
        }"
      >
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
