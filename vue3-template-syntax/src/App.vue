<template>
  <!-- provide & inject : 
    1. 매개체를 거치지 않고 후손 컴포넌트에 데이터를 전달할 수 있음
    2. props와 달리 반응성 제공 X. 따로 지정해줘야함. -->
  <button @click="message = 'Good?'">
    <!-- button을 눌러도 App부분만 바뀜.  -->
    Click!
  </button>
  <h1>App: {{message}}</h1>
  <Parent />

</template>

<script>
import Parent from '~/components/Parent'

//반응성 제공
import {computed} from 'vue'
export default {
  components : {
    Parent
  },
  data () {
    return {
      message : 'Hello world'
    }
  },
  provide(){ 
    return {
      // 반응성 제공 computed 사용
      msg: computed(() =>  this.message)
    }
  }

}
</script>