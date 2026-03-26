<template>
  <div>
    <button @click="add">Adicionar produto</button>
    <p>Total: {{ total }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    total() {
      return this.$store.getters.cartItemCount
    }
  },
  methods: {
    add() {
      this.$store.dispatch('addToCart', { nome: 'Produto' })
    }
  }
}
</script>
