<!-- 
<template>
  일반적으로 html의 요소를 javascript을 통해 찾을 때 아래와 같은 방법을 사용한다
  <h1 id = 'hello'>
    Hello world!
  </h1>

</template>

<script>

export default {
  mounted() {
    const h1El = document.querySelector('#hello')
    console.log(h1El.textContent)
  }

}
</script> 



vue.js에서는 이 방법을 간소화해서 사용가능
-->

<template>
  <h1 ref="hello">
    Hello world!
  </h1>
</template>

<script>
export default {
  created() {
    console.log(this.$refs.hello)
  // created에서는 ref사용 불가
  },
  mounted() {
    console.log(this.$refs.hello.textContent)
  }
}
</script>