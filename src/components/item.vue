<template>
  <div>
    <li v-bind:class="{select: s.selected}">
      <span>
        <input type="checkbox" v-on:change="s.selected = !s.selected">
        <strong>{{ s.service }} ${{ s.price }}</strong>
      </span>
    </li>
  </div>
</template>

<script>
export default {
  props: {
    s: {
      type: Object,
      required: true
    }
  },
}
</script>

<style scoped>
li{
  border: 1px solid #ccc;
  display: flex;
  justify-content: space-between;
  padding: .5rem 2rem;
  margin: 1rem;
  max-width: 200px;
  background: orangered;
}
input{
  margin-right: 1rem;
}

.select{
  background: limegreen;
}
</style>