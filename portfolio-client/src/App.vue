<script setup lang="ts">
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
import SandboxLand from './components/SandboxLand.vue'

const count = ref(10)
function downWeGo() {
  count.value--
}
</script>

<template>
  <header>
    <img alt="oiia" class="logo" src="./assets/oiia.gif" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it! Eat shit!" />
      <HelloWorld tacoprop="taco taco taco taco" />
      <div>
        <button @click="downWeGo">smash that like button: {{ count }}</button>
      </div>
    </div>
  </header>

  <main>
    <SandboxLand />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    flex-direction: column;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
