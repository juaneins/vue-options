<script setup></script>
<script>
export default {
  data() {
    return {
      text: 'hello vue!'
    }
  },
  beforeCreate() {
    console.log('beforeCreate', this.$data, this.$el)
  },
  created() {
    console.log('created', this.$data, this.$el)
  },
  mounted() {
    console.log('mounted', this.$data, this.$el)
  }
}
</script>

<template>
  <div>{{ text }}</div>
</template>

<style scoped></style>
