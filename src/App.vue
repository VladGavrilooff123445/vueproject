<template>
  <div id="app">
    <h1>Услуги</h1>
    <services
        v-bind:services="services"
    />
    <Result
        v-bind:services="services"
    />
  </div>
</template>

<script>


import Services from "@/components/services";
import Result from "@/components/result";


export default {
  name: 'App',
  data() {
    return {
      services: [
        {id: 1, service: 'Веб разработка', price: 300.00, selected: false},
        {id: 2, service: 'Дизайн', price: 400.00, selected: false},
        {id: 3, service: 'Интеграция', price: 250.00, selected: false},
        {id: 4, service: 'Обучение', price: 220.00, selected: false}
      ]
    }
  },
  components: {
    Result,
    Services
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
