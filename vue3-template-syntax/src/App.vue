<template>
  <a href="https://naver.com"
  target="_brank"
  @click.prevent.once="handler">
  <!--once: handler를 한번만 실행시킴
      prevent: html의 기본동작을 막음 (= event.preventDefault() ) -->
  NAVER
  </a>
</template>

<script>
export default {
  methods: {
    handler (event) {
      // event.preventDefault()
      console.log('ABC')
    }
  }
}
</script>

