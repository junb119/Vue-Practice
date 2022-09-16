<template>
  <button @click="handler('hi', $event)"> {{msg}} </button>
  <!-- 인수가 따로 있을 때 이벤트 객체를 받으려면 인수로 $event -->
</template>

<script>
export default {
  data () {
    return {
    msg : 'Click'
  }},
  methods: {
    handler (string, event) {
      console.log(string),
      console.log(event),
      this.msg = 'Hello~!'
    }
  }
}
</script>

