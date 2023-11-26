<script>
import { toRefs, computed } from "vue";

export default {
    props: {
        firstName: String,
        lastName: String
    },
    setup(props, context) {
        console.log("context:", context);
        const { firstName, lastName } = toRefs(props);

        const fullName = computed(() => {
            return `${firstName.value} ${lastName.value}`;
        });

        return {
            fullName
        };
    }
};
</script>
<template>
    <p>{{ firstName }}</p>
    <p>{{ lastName }}</p>
    <p>{{ fullName }}</p>
</template>