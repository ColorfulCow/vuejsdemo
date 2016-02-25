<template>
  <div>
    <span>{{ myMessage }}</span>
    <input v-model="query">
    <ul>
      <li v-for="item in list | filterBy query" transition="staggered">
        {{ item.msg }}
      </li>
    </ul> 
  </div>
</template>

<script>
export default {
  data () {
    return {
      query: '',
      list: [
        { msg: 'Bruce Lee' },
        { msg: 'Jackie Chan' },
        { msg: 'Chuck Norris' },
        { msg: 'Jet Li' },
        { msg: 'Kung Fury' }
      ]
    }
  },
  props: ['myMessage']
}
</script>

<style>
  ul {
    padding-left: 0;
    font-family: Helvetica, Arial, sans-serif;
  }
  .staggered-transition {
      transition: all .5s ease;
      overflow: hidden;
      margin: 0;
      height: 20px;
  }
  .staggered-enter, .staggered-leave {
      opacity: 0;
      height: 0;
  }
</style>