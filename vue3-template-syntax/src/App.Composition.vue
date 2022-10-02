<template>
  <!-- 컴포지션 api로 작성  -->
  <h1 @click="increase">
    {{count}} / {{doubleCount}}
  </h1>

  <h1 @click="changeMessage">
    {{message}} / {{reversedMessage}}
  </h1>
</template>

<script>
import {ref, computed,watch, onMounted} from 'vue'
export default {
  setup() {
    // created 라이프 사이클은 따로 존재하지 않고
    // setup 내 = created라 생각하면된다.
    const count = ref(0)
    const doubleCount =computed(() => {
      return count.value*2
    })
    function increase() {
      count.value +=1
    }
    
    const message = ref('Hello world')
    const reversedMessage = computed(()=>{
      return message.value.split('').reverse().join('')
    })
    watch(message, newValue => {
      console.log(newValue)
    })
    function changeMessage() {
      message.value = 'Good?!'
    }
    console.log(message.value)// (= created)
    onMounted(()=> {
      console.log(count.value)
    })
    return {
      count,
      doubleCount,
      increase,
      message,
      reversedMessage,
      changeMessage,
      
    }
  }
  
}
</script>