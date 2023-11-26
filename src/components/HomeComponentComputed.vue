<script setup>
import { ref, computed } from "vue";

const firstName = ref("Juan");
const lastName = ref("Perez");

const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
})


</script>
<template>
    <p>{{ firstName }}</p>
    <p>{{ lastName }}</p>
    <p>{{ fullName }}</p>
</template>