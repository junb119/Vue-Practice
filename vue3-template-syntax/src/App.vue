<template>
  <h1 v-bind:class="msg"> 
    {{msg}}
    </h1>
</template>

<script>
export default {
  data() {
    return {
      msg : 'active' 
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