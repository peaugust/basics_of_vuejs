<template>
    <div>
      <p>Aqui vai ter um textinho explicando a finalidade desse Projeto e mais botões</p>
      <button @click="go('/example')">Clica em mim</button>
    </div>
</template>

<script>
export default {
  name: 'Home',
  methods: {
    go: function (route) {
      this.$router.push({path: route})
    }
  }
}
</script>

<style scoped>

</style>
