<template>
  <h1 :[attr]="'active'"       
  @[event]='add'>    <!-- v-on, 동적인자전달 -->
    {{msg}}
    </h1>
</template>

<script>
export default {
  data() {
    return {
      msg : 'active' ,
      
      attr : 'class',
      event: 'click',
    }
  },
  methods : {
    add() {
    this.msg += '!'
    }
  }
}
</script>

<style scoped>
  .active {
    color : royalblue;
    font-size: 100px;
  }
</style>