<script setup>
//import HelloWorld from './components/HelloWorld.vue'
import MenuTest from './components/MenuTest.vue'
</script>
<script>
export default {
  data() {
    return {
      show: false
    }
  }
}
</script>

<template>
  <!-- <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main> -->
  <button @click="show = !show">Menu</button>
  <transition name="fade">
    <MenuTest v-show="show" />
  </transition>
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
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

.fade-leave-to,
.fade-enter-from {
  opacity: 0;
}

.fade-leave-active,
.fade-enter-active {
  border: 1px solid turquoise;
  background-color: violet;
  transition: opacity 0.5s ease;
}
</style>
