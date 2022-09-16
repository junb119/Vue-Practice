<template>
  <button @click="handler">Click me!</button>
  <h1 v-for="{id,name} in newfruits"
  :key="id">
    {{name}}-{{id}}
  </h1>

  
    <!-- 변이 메소드 
    Vue는 감시중인 배열의 변이 메소드를 래핑하여 뷰 갱신을 트리거한다(=반응성)
    push()
    pop()
    shift()
    unshift()
    splice() : index를 이용해 데이터를 넣거나 빼거나 삭제
    sort()
    reverse()
  -->

  <!-- 비변이 메소드(원래 배열을 변경 x) 
    filter()
    concat()
    slice()
  -->
</template>

<script>
import shortid from 'shortid'
export default {
  data () {
    return {
      fruits : ['Apple','Banana','Cherry']
    }
  },

  computed : {
    newfruits () {

      return this.fruits.map( fruit  => ({
        id : shortid.generate(),
        name : fruit
      }))
  }},

  methods: {
    handler () {
      this.fruits.push('orange')
    }
  }
  
}
</script>

