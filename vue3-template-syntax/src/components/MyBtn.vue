<template>
  <div 
    class='btn'>
    <slot></slot>
  </div>
  <h1 @dblclick="$emit('heropy',$event)">
    <!-- 3. 트리거가 될 이벤트에 상속받을 emit 지정. -->
    ABC
  </h1>

</template>

<script>
export default {
  emits : [ // 2. emits 에 사용할 이벤트 목록 작성
    'heropy'
  ]
}
</script>


<style scoped lang = 'scss'>
  .btn {
    display: inline-block;
    margin:4px;
    padding: 6px 12px;
    border-radius: 4px;
    background-color: gray;
    color:white;
    cursor:pointer;
    &.large{
    font-size: 20px;
    padding:10px 20px;
    }
  }
</style>