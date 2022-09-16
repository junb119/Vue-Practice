<template>
  <h1 @click="changeMessage">{{msg}}</h1>
  <h1>{{reversedMessage}}</h1>

</template>

<script>
// import Fruits from './components/Fruits'
export default {
  data () {
    return {
      msg : 'Hello?'
    }
  },
  computed : {
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    }
  },

  watch : { // 데이터들의 변경사항을 감시하는 옵션
    msg(newValue) {
      console.log('msg :', newValue)
    },

    reversedMessage(newValue) {
      console.log('reversedMessage :', newValue)
    }
  },

  methods : {
    changeMessage() {
      this.msg = 'Good!'
    }
  }  
}
</script>

<style scoped>

</style>