<template>
  <div 
    class='btn'>
    <slot></slot>
  </div>
  <!-- 상속받을 속성을 지정(각각 지정 가능) -->
  <h1 
    :class="$attrs.class" 
    :style="$attrs.style">
  </h1>
  <!-- 상속받을 속성을 모두 한꺼번에 적용하고싶다면 v-bind 이용 -->
  <h2 v-bind="$attrs">
  </h2>

</template>

<script>
export default {
  inheritAttrs: false, // inheritAttrs : 속성 상속 옵션 지정
  created() {
    console.log(this.$attrs) // 상속받는 속성을 저장
  }
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