<script setup>
import { products } from "~/data/data.js";
</script>

<template>
  <section class="product">
    <div class="product__header">
      <h3 class="product__heading">Trending Products</h3>

      <div class="product__tabs">
        <button type="button" class="product__tab product__tab--active">
          ALL
        </button>

        <button type="button" class="product__tab">FRUITS & VEGES</button>

        <button type="button" class="product__tab">JUICES</button>
      </div>
    </div>

    <div class="product__grid">
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
  </section>
</template>
