<script setup>
import { ref, reactive } from "vue";

let counter = ref(0);
let obj = reactive({ counter2: 0 });

setInterval(() => {
    counter.value++;
    obj.counter2++;
}, 1500);

</script>
<template>
    <p>{{ counter }}</p>
    <p>{{ obj }}</p>
</template>