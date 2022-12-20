<script setup lang="ts">
import Sidebar from "./components/Sidebar.vue";
import Content from "./components/Content.vue";
</script>

<template>
  <div class="app">
    <Sidebar />
    <Content />
  </div>
</template>

<style scoped>
.app {
  display: flex;
}
</style>
