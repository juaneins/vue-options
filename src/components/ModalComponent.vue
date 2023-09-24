<template>
  <div>
    <button @click="toggle">Modal</button>
    <teleport to="body">
      <div v-show="show" class="modal">
        <h1>Titutlo</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Totam fugiat esse ut quam nisi,
          odit consectetur cumque commodi? Obcaecati reiciendis aperiam corporis ea excepturi optio
          possimus nisi. Commodi, ratione nihil?
        </p>
        <button @click="toggle">Cerrar</button>
      </div>
    </teleport>
  </div>
</template>
<script>
export default {
  data() {
    return {
      show: false
    }
  },
  methods: {
    toggle() {
      this.show = !this.show
    }
  }
}
</script>
