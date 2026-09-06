<script setup>
import { ref, computed } from "vue";

const props = defineProps({
  title: {
    type: String,
    required: true,
  },

  products: {
    type: Array,
    required: true,
  },
});

const currentIndex = ref(0);

const visibleCards = 6;

const maxIndex = computed(() => {
  return Math.max(0, props.products.length - visibleCards);
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
  <section class="product-carousel">
    <CommonSectionHeader
      :title="title"
      :previous-disabled="currentIndex === 0"
      :next-disabled="currentIndex === maxIndex"
      @previous="previous"
      @next="next"
    />

    <div class="product-carousel__viewport">
      <div
        class="product-carousel__track"
        :style="{
          transform: `translateX(-${currentIndex * 292}px)`,
        }"
      >
        <ProductCard
          v-for="product in products"
          :key="product.id"
          :name="product.name"
          :image="product.image"
          :discount="product.discount"
          :unit="product.unit"
          :rating="product.rating"
          :price="product.price"
        />
      </div>
    </div>
  </section>
</template>
