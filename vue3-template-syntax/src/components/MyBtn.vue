<template>
  <div 
    class='btn'>
    <!-- 2. name으로 지정한 순서를 지킴 -->
    <slot name="icon"></slot>
    <slot name="text"></slot>

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