<template>
  <input 
    type="text"
    @keydown.ctrl.shift.a="handler" />
    <!-- keydown : 키를 눌렀을 때 이벤트 실행-->
</template>

<script>
export default {
  methods : {
    handler() {
      console.log('Enter')
    }
  }
  
}
</script>