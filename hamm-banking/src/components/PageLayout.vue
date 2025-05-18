<script setup lang="js">
    import { defineProps } from 'vue';

    defineProps({
        title: {
            type: String,
        }
    });
</script>

<template>
  <section class="mainPages">
    <h1 class="page-title">{{ title }}</h1>
    <div class="page-content">
      <slot />
    </div>
  </section>
</template>

<style scoped>

.page-title {
    font-family: 'Inter', sans-serif;
    font-weight: bold;
    font-size: 2.6rem;
    margin-bottom: 1.5rem;
    width: 85%;
    position: fixed;
    background: white;
    padding: 1rem 2rem;
    z-index: 10;
    box-sizing: border-box;
    top: 0;
    right: 0;
    color: #000000;
    border-bottom: 0.1rem solid #e2cbcb;
}
.page-content {
    width: 100%;
    margin-top: 6.1rem;
    color: #000000;
}
</style>