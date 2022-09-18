<template>
<!-- v-model : 양방향 데이터 바인딩 # 한글은 매끄럽게 적용안됨 -->
  <h1>{{msg}}</h1>
  <input type="text"
  v-model="msg" />

  <h1>{{checkbox}}</h1>
  <input type="checkbox"
  v-model="checkbox" />

<!-- 한글 사용시 양방향 데이터 바인딩 (수동)-->
  <h1>{{kor}}</h1>
  <input type="text"
  :value="kor"  
  @input="kor = $event.target.value"/>

</template>


<script>
export default {
  data () {
    return {
      msg : 'Hello world!',
      checkbox : false,
      kor : '안녕하세요.'
    } 
  }
}
</script>