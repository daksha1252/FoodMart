<script setup>
import { blogs } from "~/data/data.js";

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};
</script>

<template>
  <section class="blog">
    <div class="blog__header">
      <h2 class="blog__heading">Our Recent Blog</h2>

      <NuxtLink to="/" class="blog__view-all" @click="scrollToTop">
        Read All Articles →
      </NuxtLink>
    </div>

    <div class="blog__grid">
      <BlogCard
        v-for="blog in blogs"
        :key="blog.id"
        :date="blog.date"
        :category="blog.category"
        :image="blog.image"
        :title="blog.title"
        :description="blog.description"
      />
    </div>
  </section>
</template>
