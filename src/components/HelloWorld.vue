<script setup>
import { ref } from "vue";
import SelfCounter from "./SelfCounter.vue";
defineProps({
  msg: String,
});
const count = ref(0);
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <!-- <button type="button" @click="count + 2">count is {{ count }}</button> -->
    <SelfCounter :count="count" @click="count++"></SelfCounter>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
