<template>
  <!-- provide & inject : 
    1. 매개체를 거치지 않고 후손 컴포넌트에 데이터를 전달할 수 있음
    2. props와 달리 반응성 제공 X. 따로 지정해줘야함. -->

  <h1>App: {{message}}</h1>
  <Parent />

</template>

<script>
import Parent from '~/components/Parent'

export default {
  components : {
    Parent
  },
  data () {
    return {
      message : 'Hello world'
    }
  },
  // 1. provide를 사용해 데이터를 내보내고 (=>Child.vue)
  provide(){ 
    return {
      msg: this.message
    }
  }

}
</script>