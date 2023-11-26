<template>
  <HomeComponent first-name="Miguel" last-name="Torres" otro="algo"></HomeComponent>
  <p>{{ texto }}</p>
</template>

<script>
import HomeComponent from '@/components/HomeComponent.vue';
import base from '@/mixins/base.js';
import { provide } from 'vue';

export default {
  name: 'App',
  mixins: [base],
  components: {
    HomeComponent,
  },
  setup() {
    provide('username', 'juaneins');
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
