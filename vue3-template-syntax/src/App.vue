<template>
  <div
  class="parent"
  @click.self="handlerA">
    <div
    class="child">
    </div>
  </div>

<!-- self : 가려지지 않은 자기 영역만 핸들링 (= ( event.target == event.currenTarget )  )-->

</template>

<script>
export default {
  methods: {
    handlerA (event) {
      console.log('Target: ', event.target)
      console.log('currenTarget :', event.currentTarget)
      console.log('A')
    },
    handlerB () {
      // event.stopPropagation() 
      // 이벤트 전파방지 = 이벤트 버블링 방지

      console.log('B')
    },
    handlerC () {
      console.log('c')
    }

  }
}
</script>

<style scoped lang ='scss'>
  .parent {
    width: 200px;
    height: 100px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    .child {
      width: 100px;
      height: 100px;
      /* margin:20px;
      padding:20px; */
      background-color: orange;
      .child2 {
        width: 50px;
        height: 50px;
        background-color: #fff;
      }
    }
  }

</style>

