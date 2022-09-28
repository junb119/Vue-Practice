<template>
  <div>
      Child: {{ msg }}  
  </div>
</template>


<script>
export default {
  // injecet를 통해 데이터를 받음
  inject : ['msg'] //배열
  
}
</script>