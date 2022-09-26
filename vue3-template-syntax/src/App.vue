<template>
<!-- emit : 속성이 아닌 이벤트를 상속받음 -->
  <MyBtn @heropy="log">   <!--1. 이벤트 지정. 임의로 지정해도 됨   -->
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
    }
  }

}
</script>