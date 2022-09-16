<template>
  <button @click="add">Add</button>

  <h1>{{reversedMessage}}</h1>
  <h1>{{reversedMessage}}</h1>
  <h1>{{reversedMessage}}</h1>
  <h1>{{reversedMessage}}</h1>

<!-- methods는 반복할 때마다 연산 -->
<!-- computed는 첫 시도만 연산 후 캐싱한 값으로 반복 -->

</template>

<script>
export default {
  data () {
    return {
      msg : 'Hello Computed!'
    }
  },

  methods: {
    add() {
      this.reversedMessage += '?!'
    }
  },

  computed : {
    // computed 는 기본적으로 Getter(읽기전용)이라 업데이트 할 수 없음.
    
    // Getter 
    // reversedMessage() {
    //   return this.msg.split('').reverse().join('')

  // Getter(get()), Setter(set()) 을 통해 설정
    reversedMessage : {

      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value

      }
    }
  }
}
</script>