<template>
  <div>
    <strong>Итого: </strong>
    <strong v-for="s in services" :key="s.id">
      {{calculator(s)}}+
    </strong>
    <strong>$</strong>
  </div>
</template>

<script>


export default {
  props: ['services'],
  methods:{
    calculator(s){
      if(s.selected){
        return s.price
      }
      return 0
    }
  }
}
</script>