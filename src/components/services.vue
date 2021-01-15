<template>
  <div>
    <ul>
      <item v-for="s in services" :key="s.id"
            v-bind:s="s"/>
    </ul>
  </div>
</template>

<script>
import item from '@/components/item';

export default {
  props: ['services'],
  components:{
    item
  }
}

</script>

<style scoped>
ul{
  list-style: none;
  padding: 0;
  margin-left: 550px;
}
</style>