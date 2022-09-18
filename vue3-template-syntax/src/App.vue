<template>
  <input 
    type="text"
    @keydown="handler" />
    <!-- keydown : 키를 눌렀을 때 이벤트 실행-->
</template>

<script>
export default {
  methods : {
    handler(event) {
      if (event.key === 'Enter') {
        console.log('Enter')
      }
    }
  }
  
}
</script>