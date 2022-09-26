<template>
  <div 
    class='btn'>
    <!-- Fallback 컨텐츠: 만약 App.vue에 내용이 없으면 default값으로 'Apple' 출력 -->
    <slot>Apple</slot> 
  </div> 
  
</template>

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