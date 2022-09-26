<template>
  <!-- slot 응용 - 이름을 갖는 슬론(=v-slot, #) -->
  <MyBtn >
    <!-- 1. v-slot에 지정한 이름의 순서대로 보장해줌. v-slot = # -->
    <template v-slot:text><span>Banana</span></template>
    <template v-slot:icon><span>(B) </span></template>

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