<script setup>
import HomeComponentInject from '@/components/HomeComponentInject.vue';
import { provide } from "vue";

provide("username", "skynet")

</script>
<template>
  <HomeComponentInject first-name="Pedro" last-name="Rodriguez" otro="otroValor"></HomeComponentInject>
</template>




<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
