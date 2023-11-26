<script setup>
import { toRefs, computed } from "vue";

const props = defineProps({
    firstName: String,
    lastName: String
});


const { firstName, lastName } = toRefs(props);



const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
})


</script>
<template>
    <p>{{ firstName }}</p>
    <p>{{ lastName }}</p>
    <p>{{ fullName }}</p>
</template>