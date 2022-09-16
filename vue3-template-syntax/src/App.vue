<template>
  <button @click="handler">Click me!</button>
  <h1 v-show="isShow">
    <!-- v-if    VS    v-show  -->
    <!-- v-show : 
      - <template> 사용불가
      - 항상 렌더링 되어 DOM(HTMl)에 남아있음. 
      - 단순 display속성만 전환함(랜더링은 되어 console에 남음. 보이지만 않음)
      - 초기비용 발생후 전환시 비용이 낮음 -> 자주 전환하면 v-show 아니면 v-if 추천      
       -->
    Hello?!
  </h1>
</template>

<script>
export default {
  data () {
    return {
      isShow : true,
      count : 0
    }
  },
  methods: {
    handler () {
      this.isShow = !this.isShow,
      this.count += 1
    }
  }
}
</script>
