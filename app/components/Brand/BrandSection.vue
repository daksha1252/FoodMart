<script setup>
import { ref, computed } from "vue";
import { brands } from "~/data/data.js";

const brandViewport = ref(null);
const currentIndex = ref(0);

const visibleCards = ref(3);

const maxIndex = computed(() => {
  return Math.max(0, brands.length - visibleCards.value);
});

const next = () => {
  if (currentIndex.value < maxIndex.value) {
    currentIndex.value++;

    brandViewport.value.scrollBy({
      left: 481,
      behavior: "smooth"
    });
  }
};

const previous = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--;

    brandViewport.value.scrollBy({
      left: -481,
      behavior: "smooth"
    });
  }
};
</script>

<template>
  <section class="brand">
    <CommonSectionHeader
      title="Newly Arrived Brands"
      :previous-disabled="currentIndex === 0"
      :next-disabled="currentIndex === maxIndex"
      @previous="previous"
      @next="next"
    />

    <div ref="brandViewport" class="brand__viewport">
      <div class="brand__track">
        <BrandCard
          v-for="brand in brands"
          :key="brand.id"
          :name="brand.name"
          :title="brand.title"
          :image="brand.image"
        />
      </div>
    </div>
  </section>
</template>
