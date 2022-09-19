<template>
<!-- propos 부모 자식간 데이터 통신 -->  
  <MyBtn>Banana</MyBtn>
  <MyBtn 
    :color="color">
    <span style='color:red;'>Banana</span></MyBtn>
  <MyBtn :color="color">
    Apple
  </MyBtn>
  <MyBtn 
    large 
    color='royalblue'>
    Cherry 
  </MyBtn>
    <MyBtn :color="'green'"> <span style='background-color:black;'> Blueberry </span></MyBtn>

</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  components : {
    MyBtn
  },
  data() {
    return {
      color: '#000'
    }
  }

}
</script>