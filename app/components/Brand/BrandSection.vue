<script setup>
import { ref, computed } from "vue";
import { brands } from "~/data/data.js";

const currentIndex = ref(0);

const visibleCards = 4;

const maxIndex = computed(() => {
  return brands.length - visibleCards;
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
  <section class="brand">
    <CommonSectionHeader
      title="Newly Arrived Brands"
      :previous-disabled="currentIndex === 0"
      :next-disabled="currentIndex === maxIndex"
      @previous="previous"
      @next="next"
    />

    <div class="brand__viewport">
      <div
        class="brand__track"
        :style="{
          transform: `translateX(-${currentIndex * 374}px)`,
        }"
      >
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
