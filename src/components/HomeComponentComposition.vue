<script setup>
import { ref, reactive, watch } from "vue";

let counter = ref(0);
let obj = reactive({ counter2: 0 });

setInterval(() => {
    counter.value++;
    obj.counter2++;
}, 1500);

// watch a una variable
watch(counter, (nuevo, viejo) => {
    console.log(nuevo, viejo);
});


// watch a un objeto
watch(() => obj.counter2, (valor, old) => {
    console.log(valor, old);
});


</script>
<template>
    <p>{{ counter }}</p>
    <p>{{ obj }}</p>
</template>