<template>
  <div>
    <h1>Básico de Vue.js</h1>
    <p>Aperta o F12 aí mano!</p>
    <button @click="counter++">ADD 1</button>
    <button @click="counter--">REMOVE 1</button>
    <button @click="secondCounter++">ADD 1(2nd counter)</button>

    <p>{{ counter }} | {{ secondCounter }} </p>
    <p>{{ result() }} | {{ output }}</p>
    <div>
      <ul style="list-style-type:none">
        <li>el: </li>
        <li>data:</li>
        <li>methods: </li>
        <li>computed: </li>
        <li>watch: </li>
        <li>beforeUpdate: </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function () {
    return {
      counter: 0,
      secondCounter: 0
    }
  },
  computed: {
    output: function () {
      console.log('Olá Dev eu sou um função do tipo: Computed')
      return this.counter > 5 ? 'Greater 5' : 'Smaller than 5'
    }
  },
  methods: {
    result: function () {
      console.log('Olá Dev eu sou um função do tipo: Method')
      return this.counter > 5 ? 'Greater 5' : 'Smaller than 5'
    }
  },
  watch: {
    counter: function (value) {
      var vm = this
      console.log(this)
      setTimeout(function () {
        console.log('Olá Dev eu sou um função do tipo: Watch')
        vm.counter = 0
      }, 2000)
    }
  },
  beforeUpdate: function () {
    return console.log('Olá Dev eu sou um função do tipo: beforeUpdate')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
