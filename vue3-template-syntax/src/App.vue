<template>
  <div
  class="parent"
  @wheel.passive="handlerA">
    <div
    class="child">
    </div>
  </div>

<!-- @wheel  : 휠을 움직일 때마다 핸들링
passive : 화면과 로직을 따로 처리하여 화면을 최대한 부드럽게 전환하고 로직은 독립적으로 처리
-->
</template>

<script>
export default {
  methods: {
    handlerA (event) {
      for (let i = 0; i<10000; i += 1) {
        console.log(event)
      }
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
    overflow: auto;
    .child {
      width: 100px;
      height: 2000px;
      background-color: orange;

      }
    }

</style>

