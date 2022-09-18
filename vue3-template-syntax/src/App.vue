<template>
<!-- v-model.lazy : 실시간으로 양방향 바인딩이 되는 것이 아닌 포커스가 해제될 때. -->
  <h1>{{msg}}</h1>
  <input type="text"
  v-model.lazy="msg" />

<!-- @change : v.model.lazy의 수동 버젼 -->
  <h1>{{kor}}</h1>
  <input type="text"
  :value="kor"  
  @change="kor = $event.target.value"/>

<!-- v-model.number : 데이터 바인딩 과정에서 문자로 형변환을 방지하여 숫자로 유지하고자할 때 사용 -->
  <h1>{{num}}</h1>
  <input type="text"
  v-model.number="num" />

<!-- v-model.trim : 양방향에 공백이 입력되면 공백을 지움 -->
  <h1>{{msg}}</h1>
  <input type="text"
  v-model="msg" />
</template>


<script>
export default {
  data () {
    return {
      msg : 'Hello world!',
      checkbox : false,
      kor : '안녕하세요.',
      num : 123
    } 
  },
  watch : {
    num() {
      console.log(typeof this.num)
    },
    msg() {
      console.log(this.msg)
    }
  }
}
</script>