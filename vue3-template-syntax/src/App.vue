<template>
<!-- idActive가 true이면 class = active -->
  <h1 
  :class = "{active: isActive}" 
  @click="activate">
  Hello?({{isActive}})
  </h1>

</template>

<script>
export default {
  data () {
    return {
      isActive : false
      }
  },
  
  methods : {
    activate() {
      this.isActive = true
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