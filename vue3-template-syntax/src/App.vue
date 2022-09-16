<template>
  <div
  class="parent"
  @click.capture="handlerA">
    <div
    class="child"
    @click="handlerB">
      <div
      class="child2"
      @click.stop="handlerC">

      </div>
    </div>
  </div>

  <!-- 이벤트 버블링 : 자식 요소 클릭시 자식요소 핸들러, 부모요소 핸들러 순으로 실행됨  -->
  <!-- stop : 이벤트 버블링 방지 (= event.stopPropagation() )-->

  <!-- 이벤트 캡쳐링 : 자식 요소 클릭시 부요요소 -> 자식요소 순으로 실행됨-->

</template>

<script>
export default {
  methods: {
    handlerA () {
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

