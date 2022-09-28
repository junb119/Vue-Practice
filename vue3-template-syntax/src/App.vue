<template>
  <Hello ref='hello'/>
</template>

<script>
import Hello from '~/components/Hello'

export default {
  components :{
    Hello
  },
  created() {
    console.log(this.$refs.hello)
  // created에서는 ref사용 불가
  },
  mounted() {
    // Hello.vue 의 요소 출력(최상위 요소가 하나일 때 가능)
    // console.log(this.$refs.hello.$el)

    // 최상위 루트에 2개 이상의 요소가 있다면
    // 출력하려는 ref를 지정해서 사용 가능(Hello.vue => h1 ref="good")
    console.log(this.$refs.hello.$refs.good)

}
}
</script>