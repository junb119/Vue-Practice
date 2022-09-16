<template>
  <button @click="handler">Click me!</button>
  <template v-if="isShow">    <!-- <template>를 사용하면 console창에 불필요한 태그 표시 안됨 -->
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </template>
</template>

<script>
export default {
  data () {
    return {
      isShow : true,
      count : 0
    }
  },
  methods: {
    handler () {
      this.isShow = !this.isShow,
      this.count += 1
    }
  }
}
</script>
