<script setup>
import { ref, toRefs, computed, inject, watch } from 'vue';

const props = defineProps({
  firstName: String,
  lastName: String,
});

const { firstName, lastName } = toRefs(props);

const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`;
});
// se inyecta para que pueda ser usado por otros componentes
const username = inject('username');

defineExpose({
  fullName,
});

const btn = ref(null);

console.log(btn.value);

watch(btn, (valor) => {
  console.log('btn valor: ', valor);
});
</script>
<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
  <button ref="btn">Click!</button>
</template>