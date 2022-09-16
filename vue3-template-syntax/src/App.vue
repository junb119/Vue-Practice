<template>
  <h1
    :style="{
      color,
      fontSize
      }"
      @click="changeStyle">
      Hello?! 
  </h1>

</template>

<script>
export default {
  data () {
    return {
      color : 'orange',
      fontSize: '30px'
    }
  },
  methods : {
    changeStyle() {
      this.color = 'red',
      this.fontSize = '50px'
    }
  }

  
}
</script>

<style scoped>
  .active {
    color: red;
    font-weight: bold ;
  }
</style>