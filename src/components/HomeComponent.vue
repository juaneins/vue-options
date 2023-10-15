<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
  <button ref="btn">Click!</button>
</template>

<script>
import { ref, toRefs, computed, inject, watch } from 'vue';

export default {
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props, { expose }) {
    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });
    // se inyecta para que pueda ser usado por otros componentes
    const username = inject('username');

    expose({
      fullName,
    });

    const btn = ref(null);

    console.log(btn.value);

    watch(btn, (valor) => {
      console.log('btn valor: ', valor);
    });

    return {
      fullName,
      username,
      btn,
    };
  },
};
</script>
