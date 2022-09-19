<template>
<!--컴포넌트 - 속성 : 최상위루트가 하날-->
  <MyBtn 
    class="heropy" 
    style='color:red;'
    title='Hello world!'
    id='1231231'>
    Banana
  </MyBtn>

</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  components : {
    MyBtn
  },

}
</script>