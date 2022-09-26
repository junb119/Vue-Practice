<template>
  <div 
    class='btn'>
    <slot></slot>
  </div>
  <h1 @dblclick="$emit('heropy',$event)">
    ABC
  </h1>

  <input 
  type="text" 
  v-model="msg" /> <!--1. 양방향 데이터 바인딩을 통해 서로 실시간으로 데이터 갱신 -->
</template>

<script>
export default {
  emits : [ 
    'heropy',
    'changeMsg'
  ],
  data() {
    return{
      msg:''
    }
  },
  // 2. v-model로 인해 data에 실시간 갱신되는 msg 감시 -> (App.vue)
  watch : {
    msg() {
      this.$emit('changeMsg', this.msg)
    }
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