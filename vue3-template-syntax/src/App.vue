<template>
  <!-- 컴포지션 api 구성(반응형 데이터) -->
  <div @click ="increase">
    {{count}}
  </div>
</template>

<script>
import {ref} from 'vue'
export default {
  setup() {
    // 데이터 자체로는 반응성을 가질 수 없으므로 ref를 이용해 반응성 객체 반환
    let count = ref('a')
    function increase() {
      count.value +='bcd' // 객체로 반환되므로 데이터는 .value를 통해 접근 가능
    }

    return {
      count,
      increase
    }
  }
  
}
</script>