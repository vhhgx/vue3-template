<template>
  <div class="vh-homes gap-8">
    <div class="flex gap-12">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
      <img src="../assets/vue.svg" class="logo vue" alt="Vue logo" />
    </div>

    <h1>{{ msg }}</h1>

    <div>{{ msg }}</div>

    <div class="selector">
      <input type="checkbox" name="darken" id="" v-model="darken" />
      <label for="darken">暗黑模式</label>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'
const props = defineProps({})

const msg = ref('Hello, Vite + Vue')

let darken = ref(false)
</script>

<style lang="scss" scoped>
.vh-homes {
  height: 150vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  .logo {
    height: 96px;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.vue:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
  }

  .selector {
    // background: var(--primary);

    background: $secondary;
  }
}
</style>
