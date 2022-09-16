<template>
  <h1
    :style="
      [fontstyle,
      backgroundColor]
      "
      @click="changeStyle">
      Hello?! 
  </h1>

</template>

<script>
export default {
  data () {
    return {
      fontstyle : {
        color : 'orange',
        fontSize: '30px'
      },
      backgroundColor : {
        'background-color' : 'black'
      }
    }
  },
  methods : {
    changeStyle() {
      this.fontstyle.color = 'red',
      this.fontstyle.fontSize = '50px',
      this.backgroundColor.backgroundColor = 'orange'
    }
  }

  
}
</script>
