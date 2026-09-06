<script setup>
import AppPromotion from "~/components/Promotion/AppPromotion.vue";
import { bestSellingProducts, mostPopularProducts } from "~/data/data.js";
</script>
<template>
  <Header />
  <Hero />
  <CategorySection />
  <BrandSection />
  <ProductSection />
  <PromoSection />
  <ProductCarousel
    title="Best selling products"
    :products="bestSellingProducts"
  />
  <Newsletter />
  <ProductCarousel
    title="Most selling products"
    :products="mostPopularProducts"
  />
  <ProductCarousel title="Just Arrived" :products="mostPopularProducts" />
  <BlogSection />
  <AppPromotion />
</template>
