<template>
  <MyBtn @heropy="log" @change-msg='logMsg'>  
    <!--3. emit을 통해 받은 changeMsg의 logMsg 메소드 실행(= 실시간 변경되는 내용을 콘솔에 출력) -->
    Banana
  </MyBtn>

</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  components : {
    MyBtn
  },
  methods : {
    log(event) {
      console.log('Click')
      console.log(event)
    },
    logMsg(msg){
      console.log(msg)
    }

  }

}
</script>